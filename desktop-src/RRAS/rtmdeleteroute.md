---
title: Função RtmDeleteRoute (RTM. h)
description: A função RtmDeleteRoute exclui uma entrada de rota.
ms.assetid: a98026e9-40f5-42e9-943c-dfc561feef6d
keywords:
- Função RtmDeleteRoute RAS
topic_type:
- apiref
api_name:
- RtmDeleteRoute
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0efe2e34345cc335b8214b781da4dce608dddcc4c2f77e80d8c86f76007c2855
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073846"
---
# <a name="rtmdeleteroute-function"></a>Função RtmDeleteRoute

\[esta api foi substituída pela api do [gerenciador de tabela de roteamento versão 2](about-routing-table-manager-version-2.md) e não estará disponível além do Windows Server 2003. Os aplicativos devem usar a API da versão 2 do Gerenciador de tabela de roteamento.\]

A função **RtmDeleteRoute** exclui uma entrada de rota.

## <a name="syntax"></a>Sintaxe


```C++
DWORD RtmDeleteRoute(
  _In_  HANDLE ClientHandle,
  _In_  PVOID  Route,
  _Out_ DWORD  Flags,
  _Out_ PVOID  CurBestRoute
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ClientHandle* \[ no\]
</dt> <dd>

Identificador que identifica o cliente e, portanto, o protocolo de roteamento da rota adicionada ou atualizada. Obtenha esse identificador chamando [**RtmRegisterClient**](rtmregisterclient.md).

</dd> <dt>

*Rota* \[ no\]
</dt> <dd>

Ponteiro para uma estrutura específica de família de protocolos que especifica a rota nova ou atualizada. Os campos a seguir são usados pelo Gerenciador de tabela de roteamento para atualizar a tabela de roteamento:



| Valor                                                                                                                                                                                                         | Significado                                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| <span id="RR_Network"></span><span id="rr_network"></span><span id="RR_NETWORK"></span><dl> <dt>**\_Rede RR**</dt> </dl>                             | Especifica o número de rede de destino. <br/>                                 |
| <span id="RR_InterfaceID"></span><span id="rr_interfaceid"></span><span id="RR_INTERFACEID"></span><dl> <dt>**Tipo de registro de recurso \_**</dt> </dl>             | Especifica o índice da interface por meio da qual a rota foi recebida.<br/> |
| <span id="RR_NextHopAddress"></span><span id="rr_nexthopaddress"></span><span id="RR_NEXTHOPADDRESS"></span><dl> <dt>**\_NEXTHOPADDRESS RR**</dt> </dl> | Especifica o endereço de rede do roteador do próximo salto.<br/>                      |



 

</dd> <dt>

*Sinalizadores* \[ de fora\]
</dt> <dd>

Ponteiro para um conjunto de sinalizadores que indicam o tipo da mensagem de alteração e quais informações foram colocadas nos buffers fornecidos. Esse parâmetro é um dos valores a seguir.



| Flags                                                                                                                                                                      | Significado                                                                                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RTM_NO_CHANGE"></span><span id="rtm_no_change"></span><dl> <dt>**\_sem alteração no RTM \_**</dt> </dl>             | A exclusão da rota não afetou a melhor rota para qualquer rede de destino. Em outras palavras, outra entrada representa uma rota para a mesma rede de destino e tem uma métrica mais baixa.<br/> |
| <span id="RTM_ROUTE_DELETED"></span><span id="rtm_route_deleted"></span><dl> <dt>**\_rota RTM \_ excluída**</dt> </dl> | A rota excluída foi a única rota disponível para uma rede de destino específica.<br/>                                                                                                  |
| <span id="RTM_ROUTE_CHANGED"></span><span id="rtm_route_changed"></span><dl> <dt>**\_rota RTM \_ alterada**</dt> </dl> | Depois que essa rota foi excluída, outra rota se tornou a melhor rota para uma rede de destino específica. *CurBestRoute* aponta para as informações para a nova rota recomendada.<br/>               |



 

</dd> <dt>

*CurBestRoute* \[ fora\]
</dt> <dd>

Ponteiro para uma estrutura que recebe as informações atuais de melhor rota, se houver. O tipo da estrutura é específico para a família de protocolos, por exemplo, IP ou IPX.

Esse parâmetro é opcional. Se o chamador especificar **NULL** para esse parâmetro, as informações de melhor rota atuais não serão retornadas.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for realizada com sucesso, o valor de retorno **não será um \_ erro**.

Se a função falhar, o valor de retorno será um dos códigos de erro a seguir.



| Valor                                                                                                       | Descrição                                                                                            |
|-------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_identificador inválido do erro \_**</dt> </dl>       | O parâmetro identificador do cliente não é um identificador válido.<br/>                                          |
| <dl> <dt>**\_parâmetro inválido de erro \_**</dt> </dl>    | A estrutura de rota apontada pelo parâmetro de *rota* contém um valor de membro.<br/>            |
| <dl> <dt>**ERRO \_ sem \_ \_ rota**</dt> </dl>       | Não há entradas na tabela de roteamento que correspondam aos parâmetros da rota especificada.<br/> |
| <dl> <dt>**ERRO \_ sem \_ recursos do sistema \_**</dt> </dl> | Não há recursos suficientes para executar a operação. <br/>                                 |



 

## <a name="remarks"></a>Comentários

A função gera uma mensagem de alteração de rota se a melhor rota para uma rede de destino foi alterada como resultado da exclusão. No entanto, a mensagem de alteração de rota não é enviada ao cliente que faz essa chamada. Em vez disso, as informações relevantes são retornadas por essa função diretamente para esse cliente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                               |
| Fim do suporte do servidor<br/>    | Windows Server 2003<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>RTM. h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>RTM. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Rtm.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Referência da versão 1 do Gerenciador de tabela de roteamento](routing-table-manager-version-1-reference.md)
</dt> <dt>

[Funções da versão 1 do Gerenciador de tabela de roteamento](routing-table-manager-version-1-functions.md)
</dt> <dt>

[**RtmAddRoute**](rtmaddroute.md)
</dt> <dt>

[**RtmDequeueRouteChangeMessage**](rtmdequeueroutechangemessage.md)
</dt> </dl>

 

 





