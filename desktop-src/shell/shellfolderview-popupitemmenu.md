---
description: Método ShellFolderView.PopupItemMenu – cria um menu de atalho para o item especificado e retorna a cadeia de caracteres de comando selecionada.
title: Método ShellFolderView.PopupItemMenu (Shldisp.h)
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
ms.openlocfilehash: cf538a468e9664810e4a6869e47629adc585bea8ce81431cf3c0de3c583f5285
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968435"
---
# <a name="shellfolderviewpopupitemmenu-method"></a>Método ShellFolderView.PopupItemMenu

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

*vItem* \[ Em\]
</dt> <dd>

Tipo: **Variante**

O [**objeto FolderItem**](folderitem.md) para o qual o menu de atalho será criado.

</dd> <dt>

*vx* \[ in, opcional\]
</dt> <dd>

Tipo: **Variante**

A posição horizontal do menu, em coordenadas de tela.

</dd> <dt>

*vy* \[ in, opcional\]
</dt> <dd>

Tipo: **Variante**

A posição vertical do menu, em coordenadas de tela.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)\***

A **Cadeia de caracteres** que recebe a cadeia de caracteres de comando.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, Windows aplicativos da área de \[ trabalho XP\]<br/>                                         |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                           |
| Cabeçalho<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                           |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versão 4.71 ou posterior)</dt> </dl> |



 

 
