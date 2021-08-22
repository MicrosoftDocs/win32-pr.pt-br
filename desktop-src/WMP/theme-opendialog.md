---
title: THEME. openDialog
description: O método openDialog abre uma caixa de diálogo de arquivo.
ms.assetid: d7f4549c-a5c3-4902-b13b-51f3d4444ea9
keywords:
- Windows Media Player THEME. openDialog
topic_type:
- apiref
api_name:
- THEME.openDialog
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3d57218105aa081ddebcb98fadbdb40b4bbd42511de9df94e204320ce78cf03c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134549"
---
# <a name="themeopendialog"></a>THEME. openDialog

O método **openDialog** abre uma caixa de diálogo de arquivo.

``` syntax
        theme.openDialog(dialogType, parameters)
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="dialogType"></span><span id="dialogtype"></span><span id="DIALOGTYPE"></span>*caixa de diálogo*
</dt> <dd>

Uma **cadeia de caracteres** que especifica o tipo de caixa de diálogo. Deve ser definido como "arquivo \_ aberto".

</dd> <dt>

<span id="parameters"></span><span id="PARAMETERS"></span>*parâmetro*
</dt> <dd>

Uma **cadeia de caracteres** que pode ser usada para obter informações adicionais. Deve ser definido como "arquivos de \_ mídia".

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Esse método retorna uma **cadeia de caracteres** que contém a URL do arquivo selecionado ou "" (cadeia de caracteres vazia) se o usuário clicar em cancelar.

## <a name="remarks"></a>Comentários

Esse método pode ser usado para arquivos nos discos rígidos locais ou em unidades de rede.

## <a name="examples"></a>Exemplos


```JScript
<THEME>
  <VIEW id="View1" 
    backgroundImage="greenstone.bmp" 
    width=500 height=300 author="Microsoft Corp.">
    <BUTTON 
      id="Open" 
      image="Open.png" 
      onclick="jscript:
        player.URL = theme.openDialog('FILE_OPEN','FILES_ALLMEDIA')">
    </BUTTON>
  </VIEW>
</THEME>
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento THEME**](theme-element.md)
</dt> </dl>

 

 





