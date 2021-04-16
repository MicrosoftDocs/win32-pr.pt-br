---
title: Método WebViewFolderContents. SelectItem (shldisp. h)
description: Define o estado de seleção de um item na exibição.
ms.assetid: c0e163ee-1951-476c-807a-781e26766d99
keywords:
- Recursos do ambiente Windows herdado do método SelectItem
- Método SelectItem recursos de ambiente herdados do Windows, objeto WebViewFolderContents
- Recursos do ambiente Windows herdado do objeto WebViewFolderContents, método SelectItem
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
ms.openlocfilehash: e491fb27db2d6e1e9b449be4aa2924684021539a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105765362"
---
# <a name="webviewfoldercontentsselectitem-method"></a>Método WebViewFolderContents. SelectItem

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

*vItem* \[ no\]
</dt> <dd>

Tipo: **Variant \** _

O objeto [_ *FolderItem* *](../shell/folderitem.md) para o qual o estado de seleção será definido.

</dd> <dt>

*dwFlags* \[ no\]
</dt> <dd>

Tipo: **inteiro**

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

Anular seleção de todos, exceto o item especificado.

</dd> <dt>



 (8)


</dt> <dd>

Verifique se o item é exibido na exibição.

</dd> <dt>



 (16)


</dt> <dd>

Dê o foco ao item.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="examples"></a>Exemplos

O exemplo a seguir mostra o uso correto desse método para JScript Embedded em HTML.


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
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]<br/>                                         |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                           |
| Cabeçalho<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                           |
| INSERI<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versão 4,71 ou posterior)</dt> </dl> |



 

