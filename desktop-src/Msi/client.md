---
description: O objeto Client representa uma relação entre um componente e um produto cliente.
ms.assetid: ac1fbd74-fbc4-4f76-8e14-af48443a8528
title: Objeto de cliente
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Client
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 4308084bb1e5e081668bbe85dfb458f747fe34b25be0dd1858b5a7b7fae8a269
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119328376"
---
# <a name="client-object"></a>Objeto de cliente

O objeto Client representa uma relação entre um componente e um produto cliente.

**[Windows Instalador 4.5 ou anterior:](not-supported-in-windows-installer-4-5.md)** Sem suporte. Este objeto está disponível a partir do Windows Installer 5.0.

## <a name="members"></a>Membros

O **objeto** Client tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

O **objeto Client** tem essas propriedades.



| Propriedade                                                 | Descrição                                                 |
|:---------------------------------------------------------|:------------------------------------------------------------|
| [**ComponentCode**](client-componentcode.md)<br/> | O código do componente em questão.<br/> |
| [**Contexto**](client-context.md)<br/>             | O contexto do produto.<br/>                      |
| [**ProductCode**](client-productcode.md)<br/>     | O produto cliente do componente em questão.<br/> |
| [**UserSID**](client-usersid.md)<br/>             | O SID do usuário para o componente.<br/>                  |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Instalador 5.0 ou posterior.<br/>                                         |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl> |
| IID<br/>     | IID IClient é definido como \_ 000C1098-0000-0000-C000-000000000046<br/>         |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Usando a interface de automação](using-the-automation-interface.md)
</dt> <dt>

[Windows Exemplos de script do instalador](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




