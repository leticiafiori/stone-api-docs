---
title: "O  Objeto Pagamento"
slug: "o-objeto-pagamento"
hidden: false
createdAt: "2019-06-04T19:16:40.905Z"
updatedAt: "2020-04-28T15:16:04.117Z"
weight: 2
---

| Chave                     |    Descrição                                                  |  Tipo       |
| ------------------------- | ------------------------------------------------------------- |-------------|
| account_id                | Identificador da conta.                                       | _String_
| amount                    | Valor da transação, em centavos de reais.                     | _Integer_
| approval_expired_at       | Horário em que a transação expirou, em formato ISO8601. Retorna null caso a transação estaja aguardando aprovação ou já tenha sido aprovada em algum momento. |  _String_
| approved_at               | Horário em que a transação foi aprovada, em formato ISO8601. Retorna null caso a transação não tenha sido aprovada em nenhum momento. |  _String_
| approved_by               | Identificador único da usuária que aprovou a transação, no formato user:UUID4. Retorna null caso não tenha sido aprovada em nenhum momento. | _String_
| barcode                   | Código de barras.                                             | _String_
| cancelled_at              | Horário em que um pagamento agendado foi cancelado, em formato ISO8601. Retorna null caso não haja cancelamento.  |  _String_
| created_at                | Horário em que a transação foi criada, em formato ISO8601. Nesse caso nunca será null. | _String_
| created_by  Identificador único da usuária que criou a transação, no formato user:UUID4. Neste caso nunca irá retornar null. | _String_
| details                   | Detalhes da transferência como nome da instituição, nome do destinatário, documento do beneficiário e nome do beneficiário. Retorna null caso ainda não tenhamos essa informação. Uma outra forma de obter essa informação é realizar uma simulação.  | _Objeto_
| failed_at                 | Horário em que a transação falhou, em formato ISO8601. Retorna null caso a transação nunca tenha falhado.  | _String_
| failure_reason_code       | Código do motivo da falha. | _String_
| failure_reason_description | Descrição do motivo da falha. |  _String_
| fee Taxa da transação, em centavos de reais.    Integer
| finished_at               | Horário em que a transação foi finalizada, em formato ISO8601. Retorna null caso a transação não tenha sido finalizada. | _String_
| id                        | Identificador único da transação, no formato UUID4. | _String_
| refunded_at               | Horário em que a transação foi extornada em caso de falha, em formato ISO8601. Retorna null caso a transação não tenha sido extornada. | _String_
| rejected_at               | Horário em que a transação foi rejeitada, em formato ISO8601. Retorna null caso a transação não tenha sido rejeitada em nenhum momento. | _String_
| rejected_by               | Identificador único da usuária que rejeitou a transação, no formato user:UUID4. Retorna null caso não tenha sido rejeitada em nenhum momento. |  _String_
| scheduled_to              | Data do agendamento. Caso não tenha sido agendado retornará null. |  _String_
| status                    | Status atual do pagamento, podendo ser um dentre os status à seguir: CREATED, REJECTED, EXPIRED, APPROVED, SCHEDULED, FAILED, FINISHED, CANCELLED. | _String_
| writable_line             | Código numérico que acompanha o código de barras. | _String_