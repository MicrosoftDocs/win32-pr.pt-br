---
title: Evento Player. KeyDown
description: O evento KeyDown ocorre quando uma tecla é pressionada. | Evento Player. KeyDown
ms.assetid: a34dafca-5db2-4065-bcfe-d66e633b26fb
keywords:
- Evento KeyDown Windows Media Player
- Evento KeyDown Windows Media Player, classe Player
- Classe Player Windows Media Player, evento KeyDown
topic_type:
- apiref
api_name:
- Player.KeyDown
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 226430421977a58eca02b7a42cf0349f2a5ff520
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105811093"
---
# <a name="playerkeydown-event"></a>Evento Player. KeyDown

O evento **KeyDown** ocorre quando uma tecla é pressionada.

## <a name="syntax"></a>Sintaxe


```JScript
Player.KeyDown(
  nKeyCode,
  nShiftState
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*nKeyCode* 
</dt> <dd>

**Número** (**int**) que especifica qual chave física é pressionada. Para obter os valores possíveis, consulte a seção comentários.

</dd> <dt>

*nShiftState* 
</dt> <dd>

**Número** (**int**) especificando um campo de bits com os menos significativos que correspondem à tecla Shift (bit 0), a tecla Ctrl (bit 1) e a tecla Alt (bit 2). Esses bits correspondem aos valores 1, 2 e 4, respectivamente. O argumento Shift indica o estado dessas chaves. Alguns, todos ou nenhum dos bits podem ser definidos, indicando que algumas, todas ou nenhuma das chaves são pressionadas.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse evento não retorna um valor.

## <a name="remarks"></a>Comentários

O argumento *nKeyCode* especifica uma chave física. As tabelas a seguir mostram os valores possíveis para as chaves principais em um teclado padrão.

Valores para as chaves principais.



| Chave                     | Valor   |
|-------------------------|---------|
| A-Z                     | 65-90   |
| 0-9                     | 48-56   |
| F1-F12                  | 112-123 |
| ESC                     | 27      |
| TAB                     | 9       |
| CAPS LOCK               | 20      |
| SHIFT (esquerda ou direita)   | 16      |
| CTRL (esquerda ou direita)    | 17      |
| ALT (esquerda ou direita)     | 18      |
| SPACE                   | 32      |
| BACKSPACE               | 8       |
| Enter                   | 13      |
| Tecla com o logotipo do Windows, esquerda  | 91      |
| Tecla com o logotipo do Windows, direita | 92      |
| Chave do aplicativo         | 93      |



 

Valores para as chaves do teclado numérico.



| Chave               | Valor  |
|-------------------|--------|
| 0-9               | 96-105 |
| NUM LOCK          | 144    |
| DIVIDIR (/)        | 111    |
| MULTIPLICAr ( \* )     | 106    |
| Subtrair (-)      | 109    |
| ADICIONAR (+)           | 107    |
| Separador (Enter) | 108    |
| DECIMAL (.)       | 110    |



 

Valores para as chaves de navegação.



| Chave         | Valor |
|-------------|-------|
| INSERT      | 45    |
| Delete (excluir)      | 46    |
| HOME        | 36    |
| END         | 35    |
| PAGE UP     | 33    |
| PAGE DOWN   | 34    |
| SETA PARA CIMA    | 38    |
| SETA PARA BAIXO  | 40    |
| SETA PARA A ESQUERDA  | 37    |
| SETA PARA A DIREITA | 39    |



 

O valor dos parâmetros de evento é especificado pelo Windows Media Player e pode ser acessado ou transmitido para um método em um arquivo JScript importado usando o nome de parâmetro fornecido. Esse nome de parâmetro deve ser digitado exatamente como mostrado, incluindo a capitalização.

**Windows Media Player 10 Mobile:** Não há suporte para esse evento.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player 9 Series ou posterior.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto de jogador**](player-object.md)
</dt> </dl>

 

 





