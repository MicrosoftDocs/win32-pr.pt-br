---
title: Função RtmBlockDeleteRoutes (Rtm.h)
description: A função RtmBlockDeleteRoutes exclui todas as rotas no subconjunto especificado de rotas na tabela.
ms.assetid: d191883d-da3d-4a91-92e6-4979db96f4a4
keywords:
- Função RAS RtmBlockDeleteRoutes
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
ms.openlocfilehash: f830603bba4bcdf07bd7bc8c631ac17028301a795fc14ebbce6483ef72f81361
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073876"
---
# <a name="rtmblockdeleteroutes-function"></a>Função RtmBlockDeleteRoutes

\[Essa API foi superada pela API do Gerenciador de Tabelas de Roteamento versão [2](about-routing-table-manager-version-2.md) e não estará disponível além do Windows Server 2003. Os aplicativos devem usar a API do Gerenciador de Tabelas de Roteamento versão 2.\]

A **função RtmBlockDeleteRoutes** exclui todas as rotas no subconjunto especificado de rotas na tabela.

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

*ClientHandle* \[ Em\]
</dt> <dd>

Identificador que identifica o cliente e, portanto, o protocolo de roteamento das rotas a serem excluídas.

</dd> <dt>

*EnumerationFlags* \[ Em\]
</dt> <dd>

Especifica quais rotas devem ser enumeradas. Esse parâmetro limita o conjunto de rotas excluídas a um subconjunto definido pelos sinalizadores a seguir e aos valores nos membros correspondentes da estrutura apontada pelo parâmetro *CriteriaRoute.* Os sinalizadores são os mesmos usados em [**RtmCreateEnumerationHandle,**](rtmcreateenumerationhandle.md) exceto pelo fato de que AS ROTAS MELHORES SOMENTE RTM são redundantes para \_ \_ \_ **RtmBlockDeleteRoutes**. A melhor designação de rota é ajustada à medida que as rotas são excluídas, portanto, a função eventualmente exclui todas as rotas no subconjunto.

</dd> <dt>

*CriteriaRoute* \[ Em\]
</dt> <dd>

Ponteiro para uma estrutura de rota específica da família de protocolos ( [**RTM \_ IP \_ ROUTE**](rtm-ip-route.md) ou [**RTM \_ IPX \_ ROUTE**](rtm-ipx-route.md)). Os valores de membro nessa estrutura correspondem aos sinalizadores especificados pelo *parâmetro EnumerationFlags.*

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, o valor de retorno será NENHUM \_ ERRO.

Se a função falhar, o valor de retorno será um dos códigos de erro a seguir.



| Valor                                                                                                       | Descrição                                                                                                |
|-------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ERRO \_ SEM \_ ROTAS**</dt> </dl>            | Não há rotas que tenham os critérios especificados.<br/>                                           |
| <dl> <dt>**ERROR \_ INVALID \_ HANDLE**</dt> </dl>       | O *parâmetro ClientHandle* não é válido.<br/>                                                      |
| <dl> <dt>**ERRO \_ PARÂMETRO \_ INVÁLIDO**</dt> </dl>    | Um ou mais dos parâmetros de entrada são inválidos, por exemplo, os sinalizadores de enumeração são inválidos.<br/> |
| <dl> <dt>**ERRO \_ NENHUM RECURSO DO \_ \_ SISTEMA**</dt> </dl> | Não há recursos suficientes para executar a operação.<br/>                                    |
| <dl> <dt>**ERRO \_ SEM \_ MEMÓRIA \_ SUFICIENTE**</dt> </dl>   | Não há memória suficiente para executar a operação.<br/>                                        |



 

## <a name="remarks"></a>Comentários

A função gera mensagens de notificação apropriadas para todos os clientes registrados, incluindo o chamador.

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

[**RtmCreateEnumerationHandle**](rtmcreateenumerationhandle.md)
</dt> <dt>

[**RtmRegisterClient**](rtmregisterclient.md)
</dt> </dl>

 

 





