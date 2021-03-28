---
description: Cria um menu de atalho para o item especificado e retorna a cadeia de caracteres de comando selecionada.
title: Método ShellFolderView. PopupItemMenu (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderView.PopupItemMenu
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 1610d91e-87c3-4ba5-9147-1595eddb2c3a
ms.openlocfilehash: 513f654442361da840cb02089810c814275c5867
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171180"
---
# <a name="shellfolderviewpopupitemmenu-method"></a>Método ShellFolderView. PopupItemMenu

Cria um menu de atalho para o item especificado e retorna a cadeia de caracteres de comando selecionada.

## <a name="syntax"></a>Sintaxe


```JScript
retVal = ShellFolderView.PopupItemMenu(
  vItem,
  [ vx ],
  [ vy ]
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*vItem* \[ no\]
</dt> <dd>

Tipo: **variante**

O objeto [**FolderItem**](folderitem.md) para o qual o menu de atalho será criado.

</dd> <dt>

*VX* \[ em, opcional\]
</dt> <dd>

Tipo: **variante**

A posição horizontal do menu, em coordenadas da tela.

</dd> <dt>

*Vy* \[ em, opcional\]
</dt> <dd>

Tipo: **variante**

A posição vertical do menu, em coordenadas da tela.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr) \** _

A *cadeia de caracteres* _ * que recebe a cadeia de caracteres de comando.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]<br/>                                         |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                           |
| Cabeçalho<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                           |
| INSERI<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versão 4,71 ou posterior)</dt> </dl> |



 

 
