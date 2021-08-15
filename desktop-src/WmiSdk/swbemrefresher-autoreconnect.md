---
description: A propriedade AutoReconnect do objeto SWbemRefresher é um valor booliano que indica se o atualizador se reconecta automaticamente a um provedor remoto se a conexão for interrompida.
ms.assetid: 3be24128-8a35-44b0-befd-8b8937eff1b7
ms.tgt_platform: multiple
title: Propriedade SWbemRefresher.AutoReconnect (Wbemdisp.h)
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
ms.openlocfilehash: b1ad11c4362276d5714e54ef3196b246a40de1e26bf8f311f41fb5b5834bab0b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118312808"
---
# <a name="swbemrefresherautoreconnect-property"></a>Propriedade SWbemRefresher.AutoReconnect

A **propriedade AutoReconnect** do objeto [**SWbemRefresher**](swbemrefresher.md) é um valor booliano que indica se o atualizador se reconecta automaticamente a um provedor remoto se a conexão for interrompida.

Para uma explicação dessa sintaxe, consulte [Convenções de documento para a API de Script](document-conventions-for-the-scripting-api.md).

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```VB
SWbemRefresher.AutoReconnect As Boolean
```



## <a name="property-value"></a>Valor da propriedade

## <a name="remarks"></a>Comentários

Modificar essa propriedade afeta apenas objetos no atualizador que são apoiados por um provedor de alto desempenho. Se o provedor não for um provedor de alto desempenho, definir a propriedade **AutoReconnect** como **TRUE** não terá efeito porque o objeto [**SWbemRefresher**](swbemrefresher.md) nunca se reconecta.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Cabeçalho<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemRefresher<br/>                                                        |
| IID<br/>                      | IID \_ ISWbemRefresher<br/>                                                         |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SWbemRefresher**](swbemrefresher.md)
</dt> </dl>

 

 




