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
ms.openlocfilehash: 1890ff127f60188deae8fdad251e44b3edb614f7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748781"
---
# <a name="componentinfo-object"></a>Objeto ComponentInfo

O objeto ComponentInfo representa detalhes adicionais sobre um componente que pode ser obtido por meio de uma chamada de MsiGetComponentPathEx.

**[Windows Installer 4,5 ou anterior](not-supported-in-windows-installer-4-5.md):** Sem suporte. Esse objeto está disponível a partir do Windows Installer 5,0.

## <a name="members"></a>Membros

O objeto **ComponentInfo** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

O objeto **ComponentInfo** tem essas propriedades.



| Propriedade                                                        | Descrição                                                 |
|:----------------------------------------------------------------|:------------------------------------------------------------|
| [**ComponentCode**](componentinfo-componentcode.md)<br/> | O código do componente em questão.<br/> |
| [**Caminho**](componentinfo-componentcode.md)<br/>          | O caminho do componente.<br/>                       |
| [**Status**](componentinfo-state.md)<br/>                 | O estado do componente.<br/>                      |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 ou posterior.<br/>                                         |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl> |
| IID<br/>     | IID \_ IComponentInfo é definido como 000C1099-0000-0000-C000-000000000046<br/>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Usando a interface de automação](using-the-automation-interface.md)
</dt> <dt>

[Exemplos de script de Windows Installer](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




