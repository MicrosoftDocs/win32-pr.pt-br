---
description: A propriedade Item é uma propriedade somente leitura que retorna um registro em uma coleção de Objetos RecordList.
ms.assetid: 59646aa8-811c-4658-8b47-42f70abfdfdb
title: Propriedade RecordList.Item
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RecordList.Item
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 7df19a26fd4e8464963f09ffdf227ac88f4376624a88df84d6245efa3c5fd927
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120041806"
---
# <a name="recordlistitem-property"></a>Propriedade RecordList.Item

A **propriedade Item** é uma propriedade somente leitura que retorna um registro em uma coleção de Objetos [**RecordList.**](recordlist-object.md)

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```JScript
propVal = RecordList.Item
```



## <a name="property-value"></a>Valor da propriedade

Número de índice do item com a coleção de cadeias de caracteres. O índice é necessário.

## <a name="remarks"></a>Comentários

O cliente deve verificar se o [**objeto RecordList**](recordlist-object.md) existe e não está vazio antes de referenciar a propriedade Item.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Instalador 5.0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Instalador 4.0 ou Windows Instalador 4.5 no Windows Server 2008 ou Windows Vista. Windows Instalador no Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID IRecordList é definido como \_ 000C1096-0000-0000-C000-000000000046<br/>                                                                                                                                                                          |



 

 




