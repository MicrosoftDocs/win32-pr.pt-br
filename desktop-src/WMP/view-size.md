---
title: Exibir. tamanho
description: O método de tamanho redimensiona a exibição em uma borda especificada.
ms.assetid: c15a33b2-3618-41a7-bff1-9d48a566ed4f
keywords:
- Exibir. dimensionar o Windows Media Player
topic_type:
- apiref
api_name:
- VIEW.size
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: def9b416dfe5eda052ef430b587fa1c6017b4e5f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105813732"
---
# <a name="viewsize"></a>Exibir. tamanho

O método de **tamanho** redimensiona a **exibição** em uma borda especificada.

``` syntax
        elementID.size(handle)
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="handle"></span><span id="HANDLE"></span>*processamento*
</dt> <dd>

Cadeia de caracteres que especifica a borda ou o canto a ser movido ao Dimensionar. Essa cadeia de caracteres deve ter um dos oito valores a seguir.



| Edge   | Canto      |
|--------|-------------|
| top    | canto superior    |
| direita  | bottomright |
| parte inferior | bottomleft  |
| esquerda   | topleft     |



 

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Esse método é normalmente chamado de dentro de um manipulador de **OnMouseDown** . Ele cuida do redimensionamento enquanto o mouse é arrastado e para o redimensionamento quando o botão do mouse é liberado. Se o tamanho da **exibição** for restrito, você não poderá arrastar o mouse para redimensionar a **exibição** além dos limites restritos.

## <a name="examples"></a>Exemplos


```JScript
<THEME>
  <VIEW id="View1" backgroundImage="greenstone.bmp">
    <BUTTON id="sizer" horizontalAlignment="right" 
        verticalAlignment="bottom" image="Open.png" 
        onmousedown="jscript:View1.size('bottomright')">
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

[**Elemento VIEW**](view-element.md)
</dt> </dl>

 

 





