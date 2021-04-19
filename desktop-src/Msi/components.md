---
description: O objeto de componente representa uma instância exclusiva de um componente que está disponível para enumeração.
ms.assetid: cdc99bc3-9e2a-49db-8c01-b9634aefac38
title: Objeto de componente
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Component
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 5e31d6a7c3d2422111d0d8c3247e022fa35bdc43
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748989"
---
# <a name="component-object"></a>Objeto de componente

O objeto de componente representa uma instância exclusiva de um componente que está disponível para enumeração.

**[Windows Installer 4,5 ou anterior](not-supported-in-windows-installer-4-5.md):** Sem suporte. Esse objeto está disponível a partir do Windows Installer 5,0.

## <a name="members"></a>Membros

O objeto de **componente** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

O objeto de **componente** tem essas propriedades.



| Propriedade                                                    | Descrição                                                                               |
|:------------------------------------------------------------|:------------------------------------------------------------------------------------------|
| [**ComponentCode**](component-componentcode.md)<br/> | O código do componente em questão.<br/>                               |
| [**Contexto**](component-context.md)<br/>             | O contexto que foi determinado para ser aplicável ao componente em questão.<br/> |
| [**UserSID**](component-usersid.md)<br/>             | O SID do usuário para o componente enumerado.<br/>                                     |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 ou posterior.<br/>                                         |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl> |
| IID<br/>     | IID \_ IComponent é definido como 000C1097-0000-0000-C000-000000000046<br/>      |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Usando a interface de automação](using-the-automation-interface.md)
</dt> <dt>

[Exemplos de script de Windows Installer](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




