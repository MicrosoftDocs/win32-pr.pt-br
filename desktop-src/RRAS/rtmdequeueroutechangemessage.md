---
title: Função RtmDequeueRouteChangeMessage (RTM. h)
description: A função RtmDequeueRouteChangeMessage retorna a próxima mensagem de alteração de rota na fila associada ao cliente especificado.
ms.assetid: 44f2116a-3c8d-4ac6-896e-b12930b218a5
keywords:
- Função RtmDequeueRouteChangeMessage RAS
topic_type:
- apiref
api_name:
- RtmDequeueRouteChangeMessage
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 448df230742b03f82294de102bf14b50fefa035c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085792"
---
# <a name="rtmdequeueroutechangemessage-function"></a>Função RtmDequeueRouteChangeMessage

\[Essa API foi substituída pela API do [Gerenciador de tabela de roteamento versão 2](about-routing-table-manager-version-2.md) e não estará disponível além do Windows Server 2003. Os aplicativos devem usar a API da versão 2 do Gerenciador de tabela de roteamento.\]

A função **RtmDequeueRouteChangeMessage** retorna a próxima mensagem de alteração de rota na fila associada ao cliente especificado.

## <a name="syntax"></a>Sintaxe


```C++
DWORD RtmDequeueRouteChangeMessage(
  _In_  HANDLE ClientHandle,
  _Out_ DWORD  Flags,
  _Out_ PVOID  CurBestRoute,
  _Out_ PVOID  PrevBestRoute
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ClientHandle* \[ no\]
</dt> <dd>

Identificador que identifica o cliente para o qual a operação é executada. Obtenha esse identificador chamando [**RtmRegisterClient**](rtmregisterclient.md).

</dd> <dt>

*Sinalizadores* \[ de fora\]
</dt> <dd>

Ponteiro para uma variável **DWORD** . O valor dessa variável é definido pelo Gerenciador de tabela de roteamento. O valor especifica o tipo da mensagem de alteração e quais informações foram retornadas nos buffers fornecidos. Esse parâmetro é um dos seguintes.



| Flags                                                                                                                                                                      | Significado                                                                                                                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RTM_ROUTE_ADDED"></span><span id="rtm_route_added"></span><dl> <dt>**\_rota RTM \_ adicionada**</dt> </dl>       | A primeira rota foi adicionada para uma rede de destino específica. O parâmetro *CurBestRoute* aponta para as informações da rota adicionada.<br/>                                                                                                                                                            |
| <span id="RTM_ROUTE_DELETED"></span><span id="rtm_route_deleted"></span><dl> <dt>**\_rota RTM \_ excluída**</dt> </dl> | A única rota disponível para uma rede de destino específica foi excluída. O parâmetro *PrevBestRoute* aponta para as informações da rota excluída.<br/>                                                                                                                                              |
| <span id="RTM_ROUTE_CHANGED"></span><span id="rtm_route_changed"></span><dl> <dt>**\_rota RTM \_ alterada**</dt> </dl> | Pelo menos um dos parâmetros significativos foi alterado para uma rota melhor para uma rede de destino específica. Os parâmetros significativos são: <br/> Identificador de protocolo<br/> Índice de interface<br/> Endereço do próximo salto<br/> Protocolo-dados específicos da família (incluindo métricas de rota)<br/> |



 

O parâmetro *PrevBestRoute* aponta para as informações de rota como estavam antes da alteração. O parâmetro *CurBestRoute* aponta para as informações de rota atuais (ou seja, após a alteração).

</dd> <dt>

*CurBestRoute* \[ fora\]
</dt> <dd>

Ponteiro para uma estrutura que recebe as informações atuais de melhor rota (se houver). O tipo da estrutura é específico para a família de protocolos, por exemplo, IP ou IPX.

Esse parâmetro é opcional. Se o chamador especificar **NULL** para esse parâmetro, as informações de melhor rota atuais não serão retornadas.

</dd> <dt>

*PrevBestRoute* \[ fora\]
</dt> <dd>

Ponteiro para uma estrutura que recebe as informações de melhor rota anteriores, se houver. O tipo da estrutura é específico para a família de protocolos, por exemplo, IP ou IPX.

Esse parâmetro é opcional. Se o chamador especificar **NULL** para esse parâmetro, as informações de melhor rota anteriores não serão retornadas.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor de retorno é um dos códigos a seguir.



| Valor                                                                                                       | Descrição                                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**SEM \_ erros**</dt> </dl>                    | Esta mensagem foi a última mensagem na fila do cliente. O objeto de evento é redefinido.<br/>                                                                                                                                               |
| <dl> <dt>**\_identificador inválido do erro \_**</dt> </dl>       | O parâmetro *ClientHandle* não é um identificador válido ou, no registro, o cliente não forneceu um objeto de evento para notificação de mensagem de alteração (consulte [**RtmRegisterClient**](rtmregisterclient.md)).<br/>                           |
| <dl> <dt>**ERRO de \_ mais \_ mensagens**</dt> </dl>        | A fila do cliente contém mensagens adicionais. O cliente deve chamar **RtmDequeueRouteChangeMessage** novamente assim que possível para permitir que o Gerenciador de tabela de roteamento libere os recursos associados às mensagens pendentes.<br/> |
| <dl> <dt>**ERRO \_ sem \_ mensagens**</dt> </dl>          | A fila do cliente não contém mensagens; a chamada não foi solicitada. O evento é redefinido.<br/>                                                                                                                                            |
| <dl> <dt>**ERRO \_ sem \_ recursos do sistema \_**</dt> </dl> | Não há recursos suficientes para realizar a operação.<br/>                                                                                                                                                                      |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                               |
| Fim do suporte do servidor<br/>    | Windows Server 2003<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>RTM. h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>RTM. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Rtm.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Referência da versão 1 do Gerenciador de tabela de roteamento](routing-table-manager-version-1-reference.md)
</dt> <dt>

[Funções da versão 1 do Gerenciador de tabela de roteamento](routing-table-manager-version-1-functions.md)
</dt> <dt>

[**RtmRegisterClient**](rtmregisterclient.md)
</dt> </dl>

 

 





