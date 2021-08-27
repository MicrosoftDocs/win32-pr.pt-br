---
title: Função RtmDequeueRouteChangeMessage (Rtm.h)
description: A função RtmDequeueRouteChangeMessage retorna a próxima mensagem de alteração de rota na fila associada ao cliente especificado.
ms.assetid: 44f2116a-3c8d-4ac6-896e-b12930b218a5
keywords:
- Função RAS RtmDequeueRouteChangeMessage
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
ms.openlocfilehash: 5ad69b711568fd8233a60e829da8fb6fd6ce5f74d3556afa82c721a835b98e60
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120035876"
---
# <a name="rtmdequeueroutechangemessage-function"></a>Função RtmDequeueRouteChangeMessage

\[Essa API foi superada pela API do Gerenciador de Tabelas de Roteamento versão [2](about-routing-table-manager-version-2.md) e não estará disponível além do Windows Server 2003. Os aplicativos devem usar a API do Gerenciador de Tabelas de Roteamento versão 2.\]

A **função RtmDequeueRouteChangeMessage** retorna a próxima mensagem de alteração de rota na fila associada ao cliente especificado.

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

*ClientHandle* \[ Em\]
</dt> <dd>

Identificador que identifica o cliente para o qual a operação é executada. Obtenha esse handle chamando [**RtmRegisterClient.**](rtmregisterclient.md)

</dd> <dt>

*Sinalizadores* \[ out\]
</dt> <dd>

Ponteiro para uma **variável DWORD.** O valor dessa variável é definido pelo gerenciador de tabela de roteamento. O valor especifica o tipo da mensagem de alteração e quais informações foram retornadas nos buffers fornecidos. Esse parâmetro é um dos seguintes.



| Flags                                                                                                                                                                      | Significado                                                                                                                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RTM_ROUTE_ADDED"></span><span id="rtm_route_added"></span><dl> <dt>**RTM \_ ROUTE \_ ADDED**</dt> </dl>       | A primeira rota foi adicionada para uma rede de destino específica. O *parâmetro CurIjRoute* aponta para as informações da rota adicionada.<br/>                                                                                                                                                            |
| <span id="RTM_ROUTE_DELETED"></span><span id="rtm_route_deleted"></span><dl> <dt>**ROTA RTM \_ \_ EXCLUÍDA**</dt> </dl> | A única rota disponível para uma rede de destino específica foi excluída. O *parâmetro Prev MeioRoute* aponta para as informações da rota excluída.<br/>                                                                                                                                              |
| <span id="RTM_ROUTE_CHANGED"></span><span id="rtm_route_changed"></span><dl> <dt>**ROTA RTM \_ \_ ALTERADA**</dt> </dl> | Pelo menos um dos parâmetros significativos foi alterado para uma melhor rota para uma rede de destino específica. Os parâmetros significativos são: <br/> Identificador de protocolo<br/> Índice de interface<br/> Endereço do próximo salto<br/> Dados específicos da família de protocolos (incluindo métricas de rota)<br/> |



 

O *parâmetro Prev MeioRoute* aponta para as informações de rota como antes da alteração. O *parâmetro CurIjRoute* aponta para as informações de rota atuais (ou seja, após a alteração).

</dd> <dt>

*CurIjRoute* \[ out\]
</dt> <dd>

Ponteiro para uma estrutura que recebe as informações atuais de melhor rota (se alguma). O tipo da estrutura é específico para a família de protocolos, por exemplo, IP ou IPX.

Esse parâmetro é opcional. Se o chamador especificar **NULL** para esse parâmetro, as informações de melhor rota atuais não são retornadas.

</dd> <dt>

*PrevBestRoute* \[ out\]
</dt> <dd>

Ponteiro para uma estrutura que recebe as informações de melhor rota anteriores, se alguma. O tipo da estrutura é específico para a família de protocolos, por exemplo, IP ou IPX.

Esse parâmetro é opcional. Se o chamador especificar **NULL** para esse parâmetro, as informações de melhor rota anteriores não são retornadas.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno é um dos códigos a seguir.



| Valor                                                                                                       | Descrição                                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NENHUM \_ ERRO**</dt> </dl>                    | Essa mensagem foi a última mensagem na fila do cliente. O objeto de evento é redefinido.<br/>                                                                                                                                               |
| <dl> <dt>**ERROR \_ INVALID \_ HANDLE**</dt> </dl>       | O *parâmetro ClientHandle* não é um identificador válido ou, no registro, o cliente não forneceu um objeto de evento para notificação de mensagem de alteração (consulte [**RtmRegisterClient**](rtmregisterclient.md)).<br/>                           |
| <dl> <dt>**ERRO \_ MAIS \_ MENSAGENS**</dt> </dl>        | A fila do cliente contém mensagens adicionais. O cliente deve chamar **RtmDequeueRouteChangeMessage** novamente assim que possível para permitir que o gerenciador de tabela de roteamento livre os recursos associados às mensagens pendentes.<br/> |
| <dl> <dt>**ERRO \_ SEM \_ MENSAGENS**</dt> </dl>          | A fila do cliente não contém mensagens; a chamada não foi solicitada. O evento é redefinido.<br/>                                                                                                                                            |
| <dl> <dt>**ERRO \_ NENHUM RECURSO DO \_ \_ SISTEMA**</dt> </dl> | Não há recursos suficientes para executar a operação.<br/>                                                                                                                                                                      |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                               |
| Fim do suporte ao servidor<br/>    | Windows Server 2003<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Rtm.h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Rtm.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Rtm.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Referência do Gerenciador de Tabelas de Roteamento versão 1](routing-table-manager-version-1-reference.md)
</dt> <dt>

[Funções do Gerenciador de Tabelas de Roteamento versão 1](routing-table-manager-version-1-functions.md)
</dt> <dt>

[**RtmRegisterClient**](rtmregisterclient.md)
</dt> </dl>

 

 





