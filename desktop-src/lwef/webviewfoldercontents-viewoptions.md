---
title: Propriedade WebViewFolderContents. ViewOptions (shldisp. h)
description: Obtém um conjunto de sinalizadores ShellFolderViewOptions que indicam as opções atuais da exibição.
ms.assetid: 96edb144-e532-4ab5-99ae-d945e211d744
keywords:
- Recursos de ambiente herdado do Windows da propriedade ViewOptions
- Propriedade ViewOptions recursos de ambiente herdados do Windows, objeto WebViewFolderContents
- Recursos do ambiente Windows herdado do objeto WebViewFolderContents, Propriedade ViewOptions
topic_type:
- apiref
api_name:
- WebViewFolderContents.ViewOptions
api_location:
- Shell32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 737ec5cb22fdc5c0002006898b837b557b5f6089
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008954"
---
# <a name="webviewfoldercontentsviewoptions-property"></a>Propriedade WebViewFolderContents. ViewOptions

Obtém um conjunto de sinalizadores [**ShellFolderViewOptions**](/windows/desktop/api/shldisp/ne-shldisp-shellfolderviewoptions) que indicam as opções atuais da exibição.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```JScript
objViewOptions = WebViewFolderContents.ViewOptions
```



## <a name="property-value"></a>Valor da propriedade

Uma variável do tipo [IDispatch](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) que recebe o objeto de opções de exibição.

## <a name="examples"></a>Exemplos

O exemplo a seguir mostra o uso apropriado dessa propriedade no JScript inserido em HTML.


```HTML
<html>
<head>

...

<script language="JavaScript">
    function fnWebViewFolderContentsViewOptionsJ()
    {
        var nViewOptions;

        nViewOptions = FileList.ViewOptions;
        if (nViewOptions != "")
        {
            alert(nViewOptions);
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



 

