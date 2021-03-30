---
title: Método WebViewFolderContents. PopupItemMenu (shldisp. h)
description: Cria um menu de atalho para o item especificado e retorna a cadeia de caracteres de comando selecionada.
ms.assetid: 3c07500c-2fe9-4976-a1a8-b128e75f9325
keywords:
- Recursos do ambiente Windows herdado do método PopupItemMenu
- Método PopupItemMenu recursos de ambiente herdados do Windows, objeto WebViewFolderContents
- Recursos do ambiente Windows herdado do objeto WebViewFolderContents, método PopupItemMenu
topic_type:
- apiref
api_name:
- WebViewFolderContents.PopupItemMenu
api_location:
- Shell32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41753814f103998185acc798a37447f22356d2aa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644306"
---
# <a name="webviewfoldercontentspopupitemmenu-method"></a>Método WebViewFolderContents. PopupItemMenu

Cria um menu de atalho para o item especificado e retorna a cadeia de caracteres de comando selecionada.

## <a name="syntax"></a>Sintaxe


```JScript
retVal = WebViewFolderContents.PopupItemMenu(
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

O objeto [**FolderItem**](../shell/folderitem.md) para o qual o menu de atalho será criado.

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

Tipo: **[BSTR](/previous-versions/windows/desktop/automat/bstr) \** _

Quando esse método retorna, contém a cadeia de caracteres de comando.

## <a name="examples"></a>Exemplos

O exemplo a seguir mostra o uso apropriado de _ *PopupItemMenu** para JScript Embedded em HTML.


```HTML
<html>
<head>

...

<script language="JavaScript">
    function fnWebViewFolderContentsPopupItemMenuJ()
    {
        var objFolderItem;

        objFolderItem = FileList.FocusedItem;
        if (objFolderItem != null)
        {
            var szCommand;

            szCommand = FileList.PopupItemMenu(objFolderItem);
        }
    }
</script>

</head>
<body>

...

<object id=FileList classid="clsid:1820FED0-473E-11D0-A96C-00C04FD705A2" tabIndex=1>
</body>
</html>
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]<br/>                                         |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                           |
| Cabeçalho<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                           |
| INSERI<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versão 4,71 ou posterior)</dt> </dl> |



 

