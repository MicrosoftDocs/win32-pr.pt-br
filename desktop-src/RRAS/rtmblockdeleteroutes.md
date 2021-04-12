---
title: Função RtmBlockDeleteRoutes (RTM. h)
description: A função RtmBlockDeleteRoutes exclui todas as rotas no subconjunto especificado de rotas na tabela.
ms.assetid: d191883d-da3d-4a91-92e6-4979db96f4a4
keywords:
- Função RtmBlockDeleteRoutes RAS
topic_type:
- apiref
api_name:
- RtmBlockDeleteRoutes
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a71090371fe8a84698b84b84391e5a782fdc636f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455411"
---
# <a name="rtmblockdeleteroutes-function"></a>Função RtmBlockDeleteRoutes

\[Essa API foi substituída pela API do [Gerenciador de tabela de roteamento versão 2](about-routing-table-manager-version-2.md) e não estará disponível além do Windows Server 2003. Os aplicativos devem usar a API da versão 2 do Gerenciador de tabela de roteamento.\]

A função **RtmBlockDeleteRoutes** exclui todas as rotas no subconjunto especificado de rotas na tabela.

## <a name="syntax"></a>Sintaxe


```C++
HANDLE RtmBlockDeleteRoutes(
  _In_ HANDLE ClientHandle,
  _In_ DWORD  EnumerationFlags,
  _In_ PVOID  CriteriaRoute
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ClientHandle* \[ no\]
</dt> <dd>

Identificador que identifica o cliente e, portanto, o protocolo de roteamento, das rotas a serem excluídas.

</dd> <dt>

*EnumerationFlags* \[ no\]
</dt> <dd>

Especifica quais rotas devem ser enumeradas. Esse parâmetro limita o conjunto de rotas excluídas a um subconjunto definido pelos seguintes sinalizadores e os valores nos membros correspondentes da estrutura apontada pelo parâmetro *CriteriaRoute* . Os sinalizadores são os mesmos usados em [**RtmCreateEnumerationHandle**](rtmcreateenumerationhandle.md) , exceto que o RTM \_ apenas \_ as melhores \_ rotas é redundante para **RtmBlockDeleteRoutes**. A designação de melhor rota é ajustada conforme as rotas são excluídas, portanto, a função eventualmente exclui todas as rotas no subconjunto.

</dd> <dt>

*CriteriaRoute* \[ no\]
</dt> <dd>

Ponteiro para uma estrutura de rota específica da família de protocolos [**( \_ \_ rota de IP RTM**](rtm-ip-route.md) ou [**\_ \_ rota IPX RTM**](rtm-ipx-route.md)). Os valores de membro nessa estrutura correspondem aos sinalizadores especificados pelo parâmetro *EnumerationFlags* .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for realizada com sucesso, o valor de retorno não será um \_ erro.

Se a função falhar, o valor de retorno será um dos códigos de erro a seguir.



| Valor                                                                                                       | Descrição                                                                                                |
|-------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ERRO \_ sem \_ rotas**</dt> </dl>            | Não há rotas com os critérios especificados.<br/>                                           |
| <dl> <dt>**\_identificador inválido do erro \_**</dt> </dl>       | O parâmetro *ClientHandle* não é válido.<br/>                                                      |
| <dl> <dt>**\_parâmetro inválido de erro \_**</dt> </dl>    | Um ou mais dos parâmetros de entrada são inválidos, por exemplo, os sinalizadores de enumeração são inválidos.<br/> |
| <dl> <dt>**ERRO \_ sem \_ recursos do sistema \_**</dt> </dl> | Não há recursos suficientes para realizar a operação.<br/>                                    |
| <dl> <dt>**ERRO \_ de \_ memória insuficiente \_**</dt> </dl>   | Memória insuficiente para realizar a operação.<br/>                                        |



 

## <a name="remarks"></a>Comentários

A função gera mensagens de notificação apropriadas para todos os clientes registrados, incluindo o chamador.

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

[**RtmCreateEnumerationHandle**](rtmcreateenumerationhandle.md)
</dt> <dt>

[**RtmRegisterClient**](rtmregisterclient.md)
</dt> </dl>

 

 





