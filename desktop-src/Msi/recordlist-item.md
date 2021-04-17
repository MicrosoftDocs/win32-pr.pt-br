---
description: A propriedade item é uma propriedade somente leitura que retorna um registro em uma coleção de objetos Recordlist.
ms.assetid: 59646aa8-811c-4658-8b47-42f70abfdfdb
title: Propriedade recordlist. Item
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
ms.openlocfilehash: 4c7b9332393c4055cb8052b2b759b93781c0fd73
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105780506"
---
# <a name="recordlistitem-property"></a>Propriedade recordlist. Item

A propriedade **Item** é uma propriedade somente leitura que retorna um registro em uma coleção de objetos [**recordlist**](recordlist-object.md) .

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```JScript
propVal = RecordList.Item
```



## <a name="property-value"></a>Valor da propriedade

Número de índice do item com a coleção de cadeias de caracteres. O índice é obrigatório.

## <a name="remarks"></a>Comentários

O cliente deve verificar se o objeto [**recordlist**](recordlist-object.md) existe e não está vazio antes de fazer referência à propriedade item.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IRecordList é definido como 000C1096-0000-0000-C000-000000000046<br/>                                                                                                                                                                          |



 

 




