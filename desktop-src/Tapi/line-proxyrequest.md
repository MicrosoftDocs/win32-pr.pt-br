---
description: A mensagem TAPI LINE \_ PROXYREQUEST entrega uma solicitação a um manipulador de funções proxy registrado.
ms.assetid: 7f33de55-2482-4558-bd86-ee2ac1e31269
title: LINE_PROXYREQUEST mensagem (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31986420cd21178cca8e6f0a1006e743c3250e726b4a1bf79513f6d57e380a01
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119003154"
---
# <a name="line_proxyrequest-message"></a>Mensagem \_ LINE PROXYREQUEST

A mensagem TAPI **LINE \_ PROXYREQUEST** entrega uma solicitação a um manipulador de funções proxy registrado.


```C++
            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hDevice* 
</dt> <dd>

O handle do aplicativo para o dispositivo de linha no qual o status do agente foi alterado.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

A instância de retorno de chamada fornecida ao abrir a linha da chamada.

</dd> <dt>

*Dwparam1* 
</dt> <dd>

Ponteiro para uma [**estrutura LINEPROXYREQUEST**](/windows/desktop/api/Tapi/ns-tapi-lineproxyrequest) que contém a solicitação a ser processada pelo aplicativo de manipulador de proxy.

</dd> <dt>

*Dwparam2* 
</dt> <dd>

Reservado.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Reservado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Sem valor de retorno.

## <a name="remarks"></a>Comentários

A **mensagem \_ LINE PROXYREQUEST** é enviada somente para o primeiro aplicativo registrado para lidar com solicitações de proxy do tipo que está sendo entregue.

O aplicativo deve processar a solicitação contida no buffer de proxy e chamar [**lineProxyResponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse) para retornar dados ou entregar resultados. O processamento da solicitação deve ser feito dentro do contexto da função de retorno de chamada TAPI do aplicativo somente se ela puder ser executada imediatamente, sem aguardar a resposta de qualquer outra entidade. Se o aplicativo precisar se comunicar com outras entidades (por exemplo, um provedor de serviços para manipular a ACD baseada em PBX ou qualquer outro serviço do sistema que possa resultar em bloqueio), a solicitação deverá ser enxida dentro do aplicativo e a função de retorno de chamada será finalada para evitar o atraso no recebimento de mensagens TAPI pelo aplicativo.

No momento em que **LINE \_ PROXYREQUEST** é entregue ao manipulador de proxy, a TAPI já retornou um resultado positivo da função *dwRequestID* para o aplicativo original e desbloqueou o thread de chamada para continuar a execução. O aplicativo está aguardando uma [**mensagem \_ LINE REPLY,**](line-reply.md) que é gerada automaticamente quando o aplicativo de manipulador de proxy chama [**lineProxyResponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse).

O aplicativo não deve liberar a memória apontada por *lpProxyRequest.* A TAPI libera a memória durante a execução de [**lineProxyResponse.**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse) O aplicativo pode chamar [**lineProxyResponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse) exatamente uma vez para cada **mensagem LINE \_ PROXYREQUEST.**

Se o aplicativo receber uma mensagem [**LINE \_ CLOSE**](line-close.md) enquanto tiver solicitações de proxy pendentes, ele deverá chamar [**lineProxyResponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse) para cada solicitação pendente, passando um valor *dwResult* apropriado (como LINEERR \_ OPERATIONFAILED).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão do TAPI<br/> | Requer TAPI 2.0 ou posterior<br/>                                             |
| Cabeçalho<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**LINE \_ CLOSE**](line-close.md)
</dt> <dt>

[**RESPOSTA DE \_ LINHA**](line-reply.md)
</dt> <dt>

[**LINEPROXYREQUEST**](/windows/desktop/api/Tapi/ns-tapi-lineproxyrequest)
</dt> <dt>

[**lineProxyResponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse)
</dt> </dl>

 

 




