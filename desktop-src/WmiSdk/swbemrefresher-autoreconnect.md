---
description: A propriedade falha do objeto SWbemRefresher é um valor booliano que indica se o atualizador se reconectará automaticamente a um provedor remoto se a conexão for interrompida.
ms.assetid: 3be24128-8a35-44b0-befd-8b8937eff1b7
ms.tgt_platform: multiple
title: Propriedade SWbemRefresher. falha (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefresher.AutoReconnect
- ISWbemRefresher.AutoReconnect
- ISWbemRefresher.get_AutoReconnect
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 4faa02a4a77409bb8b1813ee433c326d1c45d1bd
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104297913"
---
# <a name="swbemrefresherautoreconnect-property"></a>Propriedade SWbemRefresher. falha

A propriedade **falha** do objeto [**SWbemRefresher**](swbemrefresher.md) é um valor booliano que indica se o atualizador se reconectará automaticamente a um provedor remoto se a conexão for interrompida.

Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```VB
SWbemRefresher.AutoReconnect As Boolean
```



## <a name="property-value"></a>Valor da propriedade

## <a name="remarks"></a>Comentários

Modificar essa propriedade afeta apenas os objetos no atualizador que são apoiados por um provedor de alto desempenho. Se o provedor não for um provedor de alto desempenho, a definição da propriedade **falha** como **true** não terá efeito porque o objeto [**SWbemRefresher**](swbemrefresher.md) nunca se reconectará.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_SWBEMREFRESHER CLSID<br/>                                                        |
| IID<br/>                      | ISWbemRefresher de IID \_<br/>                                                         |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SWbemRefresher**](swbemrefresher.md)
</dt> </dl>

 

 




