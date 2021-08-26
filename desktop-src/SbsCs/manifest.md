---
description: A propriedade Manifest é usada para definir ou obter o contexto de ativação ativa.
ms.assetid: 5ad16c7b-3d66-4083-bc0f-f8294757764f
title: Propriedade ActCtx.Manifest
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ActCtx.Manifest
api_type:
- COM
api_location:
- Sxsoa.dll
ms.openlocfilehash: 77d45bd0dc97ed99ee976da4e262ed3d4819b0ec4c744a4e0a8d76b98f5bacd7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119977226"
---
# <a name="actctxmanifest-property"></a>Propriedade ActCtx.Manifest

A **propriedade Manifest** é usada para definir ou obter o contexto de ativação ativa.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```JScript
propVal = ActCtx.Manifest
```



## <a name="property-value"></a>Valor da propriedade

## <a name="remarks"></a>Comentários

Se um contexto de ativação puder ser criado com o arquivo de manifesto fornecido, o script a seguir define a propriedade Manifesto e ativa a constante de ativação especificada pelo manifesto. Se um contexto de ativação não puder ser criado a partir do manifesto, o contexto de ativação permanecerá definido como o contexto de ativação ativo no momento.

ActCtxObj.Manifest = "<*nome* do arquivo de manifesto>";

Se um contexto de ativação tiver sido criado ou ativado anteriormente, o script a seguir define a propriedade **Manifesto** para o contexto de ativação atual. Se um contexto de ativação não tiver sido criado ou ativado anteriormente, isso define a propriedade **Manifest** como uma cadeia de caracteres vazia.

"BSTR bstrManifest = ActCtxObj.Manifest"

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Sxsoa.dll</dt> </dl> |
| IID<br/>                      | IID IActCtx é definido como \_ 8FA7728F-B69B-4EE5-99F2-E2AA021BEF28<br/>           |



 

 




