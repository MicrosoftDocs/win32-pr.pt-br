---
description: O objeto cliente representa uma relação entre um componente e um produto cliente.
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
ms.openlocfilehash: 75cb21a4149d8e6758ab24796949777b8052b120
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105780523"
---
# <a name="client-object"></a>Objeto de cliente

O objeto cliente representa uma relação entre um componente e um produto cliente.

**[Windows Installer 4,5 ou anterior](not-supported-in-windows-installer-4-5.md):** Sem suporte. Esse objeto está disponível a partir do Windows Installer 5,0.

## <a name="members"></a>Membros

O objeto de **cliente** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

O objeto de **cliente** tem essas propriedades.



| Propriedade                                                 | Descrição                                                 |
|:---------------------------------------------------------|:------------------------------------------------------------|
| [**ComponentCode**](client-componentcode.md)<br/> | O código do componente em questão.<br/> |
| [**Contexto**](client-context.md)<br/>             | O contexto do produto.<br/>                      |
| [**ProductCode**](client-productcode.md)<br/>     | O produto cliente do componente em questão.<br/> |
| [**UserSID**](client-usersid.md)<br/>             | O SID do usuário para o componente.<br/>                  |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 ou posterior.<br/>                                         |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl> |
| IID<br/>     | IID \_ IClient é definido como 000C1098-0000-0000-C000-000000000046<br/>         |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Usando a interface de automação](using-the-automation-interface.md)
</dt> <dt>

[Exemplos de script de Windows Installer](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




