---
title: Evento Player. KeyDown
description: O evento KeyDown ocorre quando uma tecla é pressionada. | Evento Player. KeyDown
ms.assetid: a34dafca-5db2-4065-bcfe-d66e633b26fb
keywords:
- Windows Media Player de evento KeyDown
- Windows Media Player de evento KeyDown, classe Player
- Windows Media Player de classe do Player, evento KeyDown
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
ms.openlocfilehash: a067e0125bea6bcabec591d6c1f3ec6fc5a2ee1b0d649a02009690c89d68952e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134769"
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

## <a name="return-value"></a>Valor retornado

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
| Windows tecla de logotipo, esquerda  | 91      |
| tecla de logotipo Windows, direita | 92      |
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
| DELETE      | 46    |
| HOME        | 36    |
| END         | 35    |
| PAGE UP     | 33    |
| PAGE DOWN   | 34    |
| SETA PARA CIMA    | 38    |
| SETA PARA BAIXO  | 40    |
| SETA PARA A ESQUERDA  | 37    |
| SETA PARA A DIREITA | 39    |



 

o valor dos parâmetros de evento é especificado por Windows Media Player e pode ser acessado ou passado para um método em um arquivo de JScript importado usando o nome de parâmetro fornecido. Esse nome de parâmetro deve ser digitado exatamente como mostrado, incluindo a capitalização.

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

 

 





