---
title: Função RtmAddRoute (RTM. h)
description: A função RtmAddRoute adiciona uma entrada de rota ou atualiza uma entrada de rota existente.
ms.assetid: 09a9b57d-f10b-40b7-a3c1-2e0613f29431
keywords:
- Função RtmAddRoute RAS
topic_type:
- apiref
api_name:
- RtmAddRoute
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0c3ee68c9b026fc37457819777e69d2be7984e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105770127"
---
# <a name="rtmaddroute-function"></a>Função RtmAddRoute

\[Essa API foi substituída pela API do [Gerenciador de tabela de roteamento versão 2](about-routing-table-manager-version-2.md) e não estará disponível além do Windows Server 2003. Os aplicativos devem usar a API da versão 2 do Gerenciador de tabela de roteamento.\]

A função **RtmAddRoute** adiciona uma entrada de rota ou atualiza uma entrada de rota existente.

## <a name="syntax"></a>Sintaxe


```C++
DWORD RtmAddRoute(
  _In_  HANDLE ClientHandle,
  _In_  PVOID  Route,
  _In_  DWORD  TimeToLive,
  _Out_ DWORD  Flags,
  _Out_ PVOID  CurBestRoute,
  _Out_ PVOID  PrevBestRoute
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ClientHandle* \[ no\]
</dt> <dd>

Identificador que identifica o cliente e, portanto, o protocolo de roteamento, que adicionou ou atualizou a rota. Obtenha esse identificador chamando [**RtmRegisterClient**](rtmregisterclient.md).

</dd> <dt>

*Rota* \[ no\]
</dt> <dd>

Ponteiro para uma estrutura específica de família de protocolos que especifica a rota nova ou atualizada. Os campos a seguir são usados pelo Gerenciador de tabela de roteamento para atualizar a tabela de roteamento:



| Valor                                                                                                                                                                                                                                 | Significado                                                                                                                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RR_Network"></span><span id="rr_network"></span><span id="RR_NETWORK"></span><dl> <dt>**\_Rede RR**</dt> </dl>                                                     | Especifica o número de rede de destino.<br/>                                                                                                                                                                                                                                                                                                                                                      |
| <span id="RR_InterfaceID"></span><span id="rr_interfaceid"></span><span id="RR_INTERFACEID"></span><dl> <dt>**Tipo de registro de recurso \_**</dt> </dl>                                     | Especifica o índice da interface por meio da qual a rota foi recebida.<br/>                                                                                                                                                                                                                                                                                                                     |
| <span id="RR_NextHopAddress"></span><span id="rr_nexthopaddress"></span><span id="RR_NEXTHOPADDRESS"></span><dl> <dt>**\_NEXTHOPADDRESS RR**</dt> </dl>                         | Especifica o endereço do roteador do próximo salto.<br/>                                                                                                                                                                                                                                                                                                                                                  |
| <span id="RR_FamilySpecificData"></span><span id="rr_familyspecificdata"></span><span id="RR_FAMILYSPECIFICDATA"></span><dl> <dt>**\_FAMILYSPECIFICDATA RR**</dt> </dl>         | Especifica os dados que são específicos para a família de protocolos. Embora os dados sejam transparentes para o Gerenciador de tabela de roteamento, eles são considerados durante a comparação de rotas para determinar se as informações de rota foram alteradas. Os dados também são usados para definir valores de métrica que são independentes do protocolo de roteamento. Consequentemente, esses dados são usados para determinar a melhor rota para a rede de destino.<br/> |
| <span id="RR_ProtocolSpecificData"></span><span id="rr_protocolspecificdata"></span><span id="RR_PROTOCOLSPECIFICDATA"></span><dl> <dt>**\_PROTOCOLSPECIFICDATA RR**</dt> </dl> | Especifica os dados que são específicos para o protocolo de roteamento que forneceu a rota.<br/>                                                                                                                                                                                                                                                                                                              |
| <span id="RR_TimeStamp"></span><span id="rr_timestamp"></span><span id="RR_TIMESTAMP"></span><dl> <dt>**\_Carimbo de data/hora RR**</dt> </dl>                                             | Especifica a hora atual do sistema. Esse campo é definido pelo Gerenciador de tabela de roteamento.<br/>                                                                                                                                                                                                                                                                                                             |



 

</dd> <dt>

*TimeToLive* \[ no\]
</dt> <dd>

Especifica o número de segundos que a rota especificada deve ser mantida na tabela de roteamento. Se esse parâmetro for definido como infinito, a rota será mantida até ser explicitamente excluída. O limite atual para *TimeToLive* é 2147483 s (mais de 24 dias).

</dd> <dt>

*Sinalizadores* \[ de fora\]
</dt> <dd>

Ponteiro para uma variável **DWORD** . O valor dessa variável é definido pelo Gerenciador de tabela de roteamento. O valor indica o tipo da alteração e quais informações foram retornadas nos buffers fornecidos. Esse parâmetro é um dos seguintes.



| Flags                                                                                                                                                                      | Significado                                                                                                                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RTM_NO_CHANGE"></span><span id="rtm_no_change"></span><dl> <dt>**\_sem alteração no RTM \_**</dt> </dl>             | A adição ou atualização não alterou nenhum dos parâmetros de rota significativos ou a entrada de rota afetada não é a melhor rota entre as entradas da rede de destino.<br/>                                                                                                          |
| <span id="RTM_ROUTE_ADDED"></span><span id="rtm_route_added"></span><dl> <dt>**\_rota RTM \_ adicionada**</dt> </dl>       | A rota foi adicionada para a rede de destino. O parâmetro *CurBestRoute* aponta para as informações da rota adicionada.<br/>                                                                                                                                                                    |
| <span id="RTM_ROUTE_CHANGED"></span><span id="rtm_route_changed"></span><dl> <dt>**\_rota RTM \_ alterada**</dt> </dl> | Pelo menos um dos parâmetros significativos foi alterado para a melhor rota para a rede de destino. Os parâmetros significativos são: <br/> Identificador de protocolo<br/> Índice de interface<br/> Endereço do próximo salto<br/> Protocolo-dados específicos da família (incluindo métricas de rota)<br/> |



 

O parâmetro *PrevBestRoute* aponta para as informações de rota como estavam antes da alteração. O parâmetro *CurBestRoute* aponta para as informações de rota atuais (ou seja, após a alteração).

</dd> <dt>

*CurBestRoute* \[ fora\]
</dt> <dd>

Ponteiro para uma estrutura que recebe as informações atuais de melhor rota, se houver. O tipo da estrutura é específico para a família de protocolos, por exemplo, IP ou IPX.

Esse parâmetro é opcional. Se o chamador especificar **NULL** para esse parâmetro, as informações de melhor rota atuais não serão retornadas.

</dd> <dt>

*PrevBestRoute* \[ fora\]
</dt> <dd>

Ponteiro para uma estrutura que recebe as informações de melhor rota anteriores, se houver. O tipo da estrutura é específico para a família de protocolos, por exemplo, IP ou IPX.

Esse parâmetro é opcional. Se o chamador especificar **NULL** para esse parâmetro, as informações de melhor rota anteriores não serão retornadas.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor de retorno é um dos códigos a seguir.



| Valor                                                                                                       | Descrição                                                             |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <dt>**SEM \_ erros**</dt> </dl>                    | A rota foi adicionada ou atualizada com êxito.<br/>                 |
| <dl> <dt>**\_identificador inválido do erro \_**</dt> </dl>       | O parâmetro identificador do cliente não é um identificador válido.<br/>           |
| <dl> <dt>**\_parâmetro inválido de erro \_**</dt> </dl>    | A estrutura de rota contém um parâmetro inválido.<br/>           |
| <dl> <dt>**ERRO \_ sem \_ recursos do sistema \_**</dt> </dl> | Não há recursos suficientes para realizar a operação.<br/> |
| <dl> <dt>**ERRO \_ de \_ memória insuficiente \_**</dt> </dl>   | Memória insuficiente para alocar a entrada de rota.<br/>    |



 

## <a name="remarks"></a>Comentários

A função gera uma mensagem de alteração de rota se a melhor rota para uma rede de destino foi alterada como resultado dessa operação. No entanto, a mensagem de alteração de rota não é enviada ao cliente que faz essa chamada. Em vez disso, as informações relevantes são retornadas por essa função diretamente para esse cliente por meio dos parâmetros *flags*, *CurBestRoute* e *PrevBestRoute* .

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

[**RtmDeleteRoute**](rtmdeleteroute.md)
</dt> <dt>

[**RtmDequeueRouteChangeMessage**](rtmdequeueroutechangemessage.md)
</dt> </dl>

 

 





