---
description: A propriedade de manifesto é usada para definir ou obter o contexto de ativação ativa.
ms.assetid: 5ad16c7b-3d66-4083-bc0f-f8294757764f
title: Propriedade ActCtx. manifest
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
ms.openlocfilehash: 2ebc671bbfcdfc951343e7f92cc0385ace43997e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920830"
---
# <a name="actctxmanifest-property"></a>Propriedade ActCtx. manifest

A propriedade de **manifesto** é usada para definir ou obter o contexto de ativação ativa.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```JScript
propVal = ActCtx.Manifest
```



## <a name="property-value"></a>Valor da propriedade

## <a name="remarks"></a>Comentários

Se um contexto de ativação puder ser criado com o arquivo de manifesto fornecido, o script a seguir definirá a propriedade de manifesto e ativará a constante de ativação especificada pelo manifesto. Se um contexto de ativação não puder ser criado a partir do manifesto, o contexto de ativação permanecerá definido como o contexto de ativação ativo no momento.

ActCtxObj. manifest = "<*nome do arquivo de manifesto*>";

Se um contexto de ativação tiver sido criado ou ativado anteriormente, o script a seguir definirá a propriedade de **manifesto** como o contexto de ativação atual. Se um contexto de ativação não tiver sido criado ou ativado anteriormente, isso definirá a propriedade de **manifesto** como uma cadeia de caracteres vazia.

"BSTR bstrManifest = ActCtxObj. manifest"

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Sxsoa.dll</dt> </dl> |
| IID<br/>                      | IID \_ IActCtx é definido como 8FA7728F-B69B-4EE5-99F2-E2AA021BEF28<br/>           |



 

 




