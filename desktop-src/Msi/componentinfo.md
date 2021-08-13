---
description: O objeto ComponentInfo representa detalhes adicionais sobre um componente que pode ser obtido por meio de uma chamada de MsiGetComponentPathEx.
ms.assetid: 9b0ad0a1-c49f-4b14-817b-0cfc9b228d77
title: Objeto ComponentInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ComponentInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: a59aa1d9f7bdc5babc29461ca90c01b6fe604482cb78ba6549e782b1e34d54b5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119251996"
---
# <a name="componentinfo-object"></a>Objeto ComponentInfo

O objeto ComponentInfo representa detalhes adicionais sobre um componente que pode ser obtido por meio de uma chamada de MsiGetComponentPathEx.

**[Windows Instalador 4.5 ou anterior:](not-supported-in-windows-installer-4-5.md)** Sem suporte. Este objeto está disponível a partir do Windows Installer 5.0.

## <a name="members"></a>Membros

O **objeto ComponentInfo** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

O **objeto ComponentInfo** tem essas propriedades.



| Propriedade                                                        | Descrição                                                 |
|:----------------------------------------------------------------|:------------------------------------------------------------|
| [**ComponentCode**](componentinfo-componentcode.md)<br/> | O código do componente em questão.<br/> |
| [**Caminho**](componentinfo-componentcode.md)<br/>          | O caminho do componente.<br/>                       |
| [**Estado**](componentinfo-state.md)<br/>                 | O estado do componente.<br/>                      |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Instalador 5.0 ou posterior.<br/>                                         |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl> |
| IID<br/>     | IID IComponentInfo é definido como \_ 000C1099-0000-0000-C000-000000000046<br/>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Usando a interface de automação](using-the-automation-interface.md)
</dt> <dt>

[Windows Exemplos de script do instalador](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




