---
title: Método WebViewFolderContents.SelectItem (Shldisp.h)
description: Método WebViewFolderContents.SelectItem – define o estado de seleção de um item na exibição.
ms.assetid: c0e163ee-1951-476c-807a-781e26766d99
keywords:
- Método SelectItem Herdado Windows Recursos de Ambiente
- Método SelectItem Legacy Windows Environment Features , WebViewFolderContents object
- Objeto WebViewFolderContents Legacy Windows Environment Features , método SelectItem
topic_type:
- apiref
api_name:
- WebViewFolderContents.SelectItem
api_location:
- Shell32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d144801e62962f4071b6c8e60147326908a9b4f7787e0d4ac549be9c51fa3c97
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119960616"
---
# <a name="webviewfoldercontentsselectitem-method"></a>Método WebViewFolderContents.SelectItem

Define o estado de seleção de um item na exibição.

## <a name="syntax"></a>Sintaxe


```JScript
WebViewFolderContents.SelectItem(
  vItem,
  dwFlags
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*vItem* \[ Em\]
</dt> <dd>

Tipo: **\* Variante**

O [**objeto FolderItem**](../shell/folderitem.md) para o qual o estado de seleção será definido.

</dd> <dt>

*dwFlags* \[ Em\]
</dt> <dd>

Tipo: **Inteiro**

Um conjunto de sinalizadores que indicam o novo estado de seleção. Pode ser um ou mais dos valores a seguir.

<dt>



  acima (0)


</dt> <dd>

Desmarque o item.

</dd> <dt>



 (1)


</dt> <dd>

Selecione o item.

</dd> <dt>



 (3)


</dt> <dd>

Coloque o item no modo de edição.

</dd> <dt>



 (4)


</dt> <dd>

Desmarque todos, menos o item especificado.

</dd> <dt>



 (8)


</dt> <dd>

Verifique se o item é exibido na exibição.

</dd> <dt>



 (16)


</dt> <dd>

Dê ao item o foco.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="examples"></a>Exemplos

O exemplo a seguir mostra o uso adequado desse método para JScript inserido em HTML.


```HTML
<html>
<head>

...

<script language="JavaScript">
    function fnWebViewFolderContentsSelectItemJ()
    {
        var objFolderItem;

        objFolderItem = FileList.FocusedItem;
        if (objFolderItem != null)
        {
            FileList.SelectItem(objFolderItem, 1);
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



 

