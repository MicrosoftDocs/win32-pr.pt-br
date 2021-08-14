---
description: O objeto UIPreview é usado para exibir caixas de diálogo e painéis da interface do usuário durante a complicação. Esse objeto é criado pelo método EnableUIPreview do objeto Database.
ms.assetid: 5df2a4f3-6352-4575-b822-1811150a86be
title: Objeto UIPreview
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UIPreview
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 82436f21cc3920c2e1f635f8d1612118831e7d29f3fb1202105511f2e61f7a3d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118623495"
---
# <a name="uipreview-object"></a>Objeto UIPreview

O **objeto UIPreview** é usado para exibir caixas de diálogo e painéis da interface do usuário durante a complicação. Esse objeto é criado pelo método [**EnableUIPreview**](database-enableuipreview.md) do [**objeto Database.**](database-object.md)

## <a name="members"></a>Membros

O **objeto UIPreview** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

O **objeto UIPreview** tem esses métodos.



| Método                                           | Descrição                                                                                             |
|:-------------------------------------------------|:--------------------------------------------------------------------------------------------------------|
| [**ViewBillboard**](uipreview-viewbillboard.md) | Exibe um cartaz autoral usando o controle de host na caixa de diálogo exibida no momento.<br/> |
| [**ViewDialog**](uipreview-viewdialog.md)       | Exibe uma caixa de diálogo de interface do usuário autorada armazenada no banco de dados atual.<br/>                           |



 

### <a name="properties"></a>Propriedades

O **objeto UIPreview** tem essas propriedades.



| Propriedade                                          | Tipo de acesso           | Descrição                                                                                                                                                                       |
|:--------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Propriedade**](uipreview-property.md)<br/> | Leitura/gravação<br/> | Representa o valor de cadeia de caracteres de uma propriedade do instalador nomeado ou, se prefixado com um sinal de porcentagem (%), o valor de uma variável de ambiente do sistema para o processo atual.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Instalador 5.0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Instalador 4.0 ou Windows Instalador 4.5 no Windows Server 2008 ou Windows Vista. Windows Instalador no Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID IUIPreview é definido como \_ 000C109A-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Windows Exemplos de script do instalador](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




