---
title: Função RtmGetNextRoute (RTM. h)
description: A função RtmGetNextRoute retorna a próxima rota do subconjunto especificado de rotas na tabela.
ms.assetid: 0f413276-2ace-4216-a1a0-1b3061bacc4a
keywords:
- Função RtmGetNextRoute RAS
topic_type:
- apiref
api_name:
- RtmGetNextRoute
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da8592855e0c30cef2ed43b7818badd336bc2ab6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499478"
---
# <a name="rtmgetnextroute-function"></a>Função RtmGetNextRoute

\[Essa API foi substituída pela API do [Gerenciador de tabela de roteamento versão 2](about-routing-table-manager-version-2.md) e não estará disponível além do Windows Server 2003. Os aplicativos devem usar a API da versão 2 do Gerenciador de tabela de roteamento.\]

A função **RtmGetNextRoute** retorna a próxima rota do subconjunto especificado de rotas na tabela.

## <a name="syntax"></a>Sintaxe


```C++
DWORD RtmGetNextRoute(
  _In_    DWORD ProtocolFamily,
  _In_    DWORD EnumerationFlags,
  _Inout_ PVOID Route
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ProtocolFamily* \[ no\]
</dt> <dd>

Especifica a família de protocolos de rotas a recuperar, por exemplo, IP ou IPX.

</dd> <dt>

*EnumerationFlags* \[ no\]
</dt> <dd>

Especifica quais rotas devem ser enumeradas. Esse parâmetro limita o conjunto de rotas excluídas a um subconjunto definido pelos seguintes sinalizadores e os valores nos membros correspondentes da estrutura apontada pelo parâmetro *CriteriaRoute* . Os sinalizadores são os mesmos usados em [**RtmCreateEnumerationHandle**](rtmcreateenumerationhandle.md).

</dd> <dt>

*Rota* \[ entrada, saída\]
</dt> <dd>

Na entrada, a *rota* aponta para uma estrutura específica da família de protocolos [**( \_ \_ rota IP RTM**](rtm-ip-route.md) ou [**\_ \_ rota IPX RTM**](rtm-ipx-route.md)).

A função de chamada fornece valores de membro para esta estrutura. Esses valores, em conjunto com o parâmetro *EnumerationFlags* , especificam o conjunto a partir do qual as rotas são retornadas.

Na saída, a *rota* aponta para uma estrutura que recebe a primeira rota correspondente aos critérios especificados.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for realizada com sucesso, o valor de retorno **não será um \_ erro**.

Se a função falhar, o valor de retorno será um dos códigos de erro a seguir.



| Valor                                                                                                       | Descrição                                                             |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <dt>**\_parâmetro inválido de erro \_**</dt> </dl>    | Um dos parâmetros é inválido.<br/>                            |
| <dl> <dt>**ERRO \_ sem \_ rotas**</dt> </dl>            | Não há rotas que correspondam aos critérios especificados.<br/>       |
| <dl> <dt>**ERRO \_ sem \_ recursos do sistema \_**</dt> </dl> | Não há recursos suficientes para realizar a operação.<br/> |



 

## <a name="remarks"></a>Comentários

As rotas são retornadas na seguinte ordem:

1.  Número de rede
2.  Protocolo de roteamento
3.  Identificador de interface
4.  Endereço do próximo salto

Essa função é menos eficiente do que as funções de identificador de enumeração correspondentes.

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

[**RtmCloseEnumerationHandle**](rtmcloseenumerationhandle.md)
</dt> <dt>

[**RtmCreateEnumerationHandle**](rtmcreateenumerationhandle.md)
</dt> <dt>

[**RtmEnumerateGetNextRoute**](rtmenumerategetnextroute.md)
</dt> <dt>

[**RtmGetFirstRoute**](rtmgetfirstroute.md)
</dt> </dl>

 

 





