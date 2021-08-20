---
description: A propriedade Item é uma propriedade somente leitura que retorna uma cadeia de caracteres na coleção StringList Object.
ms.assetid: 5c654927-41cf-4e47-9d4f-76524f8bbc97
title: Propriedade StringList.Item
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StringList.Item
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 85962aac5e841c929518a7a37fdada647ce4c74baa69be23048f26f5470c91fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118142014"
---
# <a name="stringlistitem-property"></a>Propriedade StringList.Item

A **propriedade Item** é uma propriedade somente leitura que retorna uma cadeia de caracteres na coleção [**StringList Object.**](stringlist-object.md)

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```JScript
propVal = StringList.Item
```



## <a name="property-value"></a>Valor da propriedade

Número de índice do item com a coleção de cadeias de caracteres. Este parâmetro é necessário.

## <a name="remarks"></a>Comentários

O cliente deve verificar se o [**Objeto StringList**](stringlist-object.md) existe e não está vazio antes de referenciar a **propriedade Item.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Instalador 5.0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Instalador 4.0 ou Windows Instalador 4.5 no Windows Server 2008 ou Windows Vista. Windows Instalador no Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID IStringList é definido como \_ 000C1095-0000-0000-C000-000000000046<br/>                                                                                                                                                                          |



 

 




