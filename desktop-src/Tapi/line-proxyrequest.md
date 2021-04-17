---
description: A mensagem de PROXYREQUEST de linha TAPI \_ entrega uma solicitação para um manipulador de função proxy registrado.
ms.assetid: 7f33de55-2482-4558-bd86-ee2ac1e31269
title: Mensagem de LINE_PROXYREQUEST (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d536e85a9c773626bb5aacc4745d9d82817fe3c0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105761957"
---
# <a name="line_proxyrequest-message"></a>Mensagem de PROXYREQUEST de linha \_

A mensagem **de \_ PROXYREQUEST de linha** TAPI entrega uma solicitação para um manipulador de função proxy registrado.


```C++
            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hDevice* 
</dt> <dd>

O identificador do aplicativo para o dispositivo de linha no qual o status do agente foi alterado.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

A instância de retorno de chamada fornecida ao abrir a linha do telefonema.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Ponteiro para uma estrutura [**LINEPROXYREQUEST**](/windows/desktop/api/Tapi/ns-tapi-lineproxyrequest) que contém a solicitação a ser processada pelo aplicativo de manipulador de proxy.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Reservado.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Reservado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Sem valor de retorno.

## <a name="remarks"></a>Comentários

A mensagem de **linha \_ PROXYREQUEST** é enviada somente para o primeiro aplicativo registrado para lidar com solicitações de proxy do tipo que está sendo entregue.

O aplicativo deve processar a solicitação contida no buffer de proxy e chamar [**lineProxyResponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse) para retornar dados ou fornecer resultados. O processamento da solicitação deve ser feito dentro do contexto da função de retorno de chamada TAPI do aplicativo somente se puder ser executado imediatamente, sem aguardar a resposta de qualquer outra entidade. Se o aplicativo precisar se comunicar com outras entidades (por exemplo, um provedor de serviços para lidar com AD baseados em PBX ou qualquer outro serviço do sistema que possa resultar em bloqueio), a solicitação deverá ser enfileirada no aplicativo e a função de retorno de chamada será encerrada para evitar atrasar o recebimento de mensagens TAPI adicionais pelo aplicativo.

No momento em que a **linha \_ PROXYREQUEST** é entregue ao manipulador de proxy, a TAPI já retornou um resultado de função *dwRequestID* positivo para o aplicativo original e desbloqueou o thread de chamada para continuar a execução. O aplicativo está aguardando uma mensagem de [**\_ resposta de linha**](line-reply.md) , que é gerada automaticamente quando o aplicativo do manipulador de proxy chama [**lineProxyResponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse).

O aplicativo não deve liberar a memória apontada por *lpProxyRequest*. A TAPI libera a memória durante a execução de [**lineProxyResponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse). O aplicativo pode chamar [**lineProxyResponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse) exatamente uma vez para cada **linha \_ PROXYREQUEST** Message.

Se o aplicativo receber uma mensagem de [**\_ fechamento de linha**](line-close.md) enquanto tem solicitações de proxy pendentes, ele deverá chamar [**lineProxyResponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse) para cada solicitação pendente, passando um valor *dwResult* apropriado (como LINEERR \_ OPERATIONFAILED).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 2,0 ou posterior<br/>                                             |
| parâmetro<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**fechamento de linha \_**](line-close.md)
</dt> <dt>

[**resposta de linha \_**](line-reply.md)
</dt> <dt>

[**LINEPROXYREQUEST**](/windows/desktop/api/Tapi/ns-tapi-lineproxyrequest)
</dt> <dt>

[**lineProxyResponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse)
</dt> </dl>

 

 




