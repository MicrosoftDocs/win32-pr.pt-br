---
title: Propriedade WebViewFolderContents.ViewOptions (Shldisp.h)
description: Obtém um conjunto de sinalizadores ShellFolderViewOptions que indicam as opções atuais da exibição.
ms.assetid: 96edb144-e532-4ab5-99ae-d945e211d744
keywords:
- Propriedade ViewOptions Herdado Windows Recursos de Ambiente
- Propriedade ViewOptions Legacy Windows Environment Features , objeto WebViewFolderContents
- Objeto WebViewFolderContents Legacy Windows Environment Features , propriedade ViewOptions
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
ms.openlocfilehash: 95c897c75eab32962a18981c605c8465630aaf7b0c6b7d3e3f9a4fbe8e3d75d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119607736"
---
# <a name="webviewfoldercontentsviewoptions-property"></a>Propriedade WebViewFolderContents.ViewOptions

Obtém um conjunto [**de sinalizadores ShellFolderViewOptions**](/windows/desktop/api/shldisp/ne-shldisp-shellfolderviewoptions) que indicam as opções atuais da exibição.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```JScript
objViewOptions = WebViewFolderContents.ViewOptions
```



## <a name="property-value"></a>Valor da propriedade

Uma variável do tipo [IDispatch](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) que recebe o objeto de opções de exibição.

## <a name="examples"></a>Exemplos

O exemplo a seguir mostra o uso adequado dessa propriedade no JScript inserido em HTML.


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
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, Windows aplicativos da área de \[ trabalho XP\]<br/>                                         |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                           |
| Cabeçalho<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                           |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versão 4.71 ou posterior)</dt> </dl> |



 

