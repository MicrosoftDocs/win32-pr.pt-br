---
description: O objeto Recordlist é uma coleção de objetos Record. Você deve verificar se o objeto Recordlist existe e não está vazio antes de fazer referência a suas propriedades.
ms.assetid: 7f5ac153-8da1-4dc8-9bb7-defd4e821142
title: Objeto recordlist
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RecordList
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 4528b80b13fbf2667c33d9588dff2ce745d24f8575aa726ea67dc256fdebfd1b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118626804"
---
# <a name="recordlist-object"></a>Objeto recordlist

O objeto **recordlist** é uma coleção de objetos [**Record**](record-object.md) . Você deve verificar se o objeto **recordlist** existe e não está vazio antes de fazer referência a suas propriedades.

## <a name="members"></a>Membros

O objeto **recordlist** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

O objeto **recordlist** tem essas propriedades.



| Propriedade                                     | Descrição                                                          |
|:---------------------------------------------|:---------------------------------------------------------------------|
| [**Count**](recordlist-count.md)<br/> | Retorna o número de itens no objeto **recordlist** .<br/> |
| [**Item**](recordlist-item.md)<br/>   | Retorna um registro em uma coleção de objetos **recordlist** .<br/>   |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows instalador 5,0 em Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou Windows Vista. Windows instalador no Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IRecordList é definido como 000C1096-0000-0000-C000-000000000046<br/>                                                                                                                                                                          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Record**](record-object.md)
</dt> <dt>

[Windows Exemplos de script do instalador](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




