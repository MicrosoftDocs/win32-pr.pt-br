---
title: Exibir. tamanho
description: O método de tamanho redimensiona a exibição em uma borda especificada.
ms.assetid: c15a33b2-3618-41a7-bff1-9d48a566ed4f
keywords:
- Windows Media Player de exibição. tamanho
topic_type:
- apiref
api_name:
- VIEW.size
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e0d9bd583b280f39bee38f0e109e6bb2bba6ce08ec0e7cea4c082b4a6db55739
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119615306"
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

 

 





