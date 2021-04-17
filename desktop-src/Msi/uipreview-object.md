---
description: O objeto UIPreview é usado para exibir caixas de diálogo de interface do usuário e murals durante a criação. Esse objeto é criado pelo método EnableUIPreview do objeto Database.
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
ms.openlocfilehash: 6650dc9bcc66a24d0e8a9d7f0d971884a2379f60
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754339"
---
# <a name="uipreview-object"></a>Objeto UIPreview

O objeto **UIPreview** é usado para exibir caixas de diálogo de interface do usuário e murals durante a criação. Esse objeto é criado pelo método [**EnableUIPreview**](database-enableuipreview.md) do objeto [**Database**](database-object.md) .

## <a name="members"></a>Membros

O objeto **UIPreview** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

O objeto **UIPreview** tem esses métodos.



| Método                                           | Descrição                                                                                             |
|:-------------------------------------------------|:--------------------------------------------------------------------------------------------------------|
| [**ViewBillboard**](uipreview-viewbillboard.md) | Exibe um mural criado usando o controle de host na caixa de diálogo exibida no momento.<br/> |
| [**ViewDialog**](uipreview-viewdialog.md)       | Exibe uma caixa de diálogo de IU criada armazenada no banco de dados atual.<br/>                           |



 

### <a name="properties"></a>Propriedades

O objeto **UIPreview** tem essas propriedades.



| Propriedade                                          | Tipo de acesso           | Descrição                                                                                                                                                                       |
|:--------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Propriedade**](uipreview-property.md)<br/> | Leitura/gravação<br/> | Representa o valor da cadeia de caracteres de uma propriedade nomeada do instalador ou, se prefixado com um sinal de porcentagem (%), o valor de uma variável de ambiente do sistema para o processo atual.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IUIPreview é definido como 000C109A-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Exemplos de script de Windows Installer](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




