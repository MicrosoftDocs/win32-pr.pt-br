---
description: A propriedade item é uma propriedade somente leitura que retorna uma cadeia de caracteres na coleção de objetos StringList.
ms.assetid: 5c654927-41cf-4e47-9d4f-76524f8bbc97
title: Propriedade StringList. Item
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
ms.openlocfilehash: ebd32af433fd932cb05d062fbc515a3245113343
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749983"
---
# <a name="stringlistitem-property"></a>Propriedade StringList. Item

A propriedade **Item** é uma propriedade somente leitura que retorna uma cadeia de caracteres na coleção de [**objetos StringList**](stringlist-object.md) .

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```JScript
propVal = StringList.Item
```



## <a name="property-value"></a>Valor da propriedade

Número de índice do item com a coleção de cadeias de caracteres. Este parâmetro é necessário.

## <a name="remarks"></a>Comentários

O cliente deve verificar se o [**objeto StringList**](stringlist-object.md) existe e não está vazio antes de fazer referência à propriedade **Item** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ isastringlist é definida como 000C1095-0000-0000-C000-000000000046<br/>                                                                                                                                                                          |



 

 




