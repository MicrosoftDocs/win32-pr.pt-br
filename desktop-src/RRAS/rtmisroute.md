---
title: Função RtmIsRoute (RTM. h)
description: A função RtmIsRoute determina se existe uma ou mais rotas para uma rede de destino especificada. Nesse caso, a função retorna informações para a melhor rota para essa rede.
ms.assetid: f9939790-d0a6-487e-9674-a01d436dc962
keywords:
- Função RtmIsRoute RAS
topic_type:
- apiref
api_name:
- RtmIsRoute
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e64621732f2f7a35223421e5f0fc86a309d332c1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455648"
---
# <a name="rtmisroute-function"></a>Função RtmIsRoute

\[Essa API foi substituída pela API do [Gerenciador de tabela de roteamento versão 2](about-routing-table-manager-version-2.md) e não estará disponível além do Windows Server 2003. Os aplicativos devem usar a API da versão 2 do Gerenciador de tabela de roteamento.\]

A função **RtmIsRoute** determina se existe uma ou mais rotas para uma rede de destino especificada. Nesse caso, a função retorna informações para a melhor rota para essa rede.

## <a name="syntax"></a>Sintaxe


```C++
BOOL RtmIsRoute(
  _In_  DWORD ProtocolFamily,
  _In_  PVOID Network,
  _Out_ PVOID BestRoute
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ProtocolFamily* \[ no\]
</dt> <dd>

Especifica o tipo de estrutura de dados apontado pelo parâmetro de *rede* , por exemplo [**, \_ rede IP**](ip-network.md), [**\_ rede IPX**](ipx-network.md).

</dd> <dt>

*Rede* \[ no\]
</dt> <dd>

Ponteiro para uma estrutura que especifica dados de número de rede específicos da família de protocolos. Esses dados identificam a rede para a qual o chamador busca informações de rota.

</dd> <dt>

*BestRoute* \[ fora\]
</dt> <dd>

Ponteiro para uma estrutura específica de família de protocolos que recebe as melhores informações de rota atuais, se houver.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor de retorno é um dos códigos a seguir.



| Valor                                                                                                       | Descrição                                                                                                                                              |
|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**TRUE**</dt> </dl>                         | Existe pelo menos uma rota para a rede especificada. A melhor rota é retornada na estrutura apontada pelo parâmetro *BestRoute* .<br/>      |
| <dl> <dt>**FOR**</dt> </dl>                        | Não há rota para a rede especificada ou a operação falhou. Chame [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) para obter mais informações:<br/> |
| <dl> <dt>**SEM \_ erros**</dt> </dl>                    | A operação foi bem-sucedida, mas não há rota para a rede especificada.<br/>                                                                      |
| <dl> <dt>**\_parâmetro inválido de erro \_**</dt> </dl>    | O valor do parâmetro *ProtocolFamily* não corresponde a nenhuma família de protocolos instalada.<br/>                                             |
| <dl> <dt>**ERRO \_ sem \_ recursos do sistema \_**</dt> </dl> | Não há recursos suficientes para realizar a operação.<br/>                                                                                  |



 

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

[**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)
</dt> <dt>

[**\_rede IP**](ip-network.md)
</dt> <dt>

[**\_rede IPX**](ipx-network.md)
</dt> <dt>

[Identificadores da família de protocolos RTMv1](routing-table-manager-version-1-protocol-family-identifiers.md)
</dt> </dl>

 

