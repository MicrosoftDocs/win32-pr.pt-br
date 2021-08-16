---
title: Parâmetros de controle comuns
description: O exemplo a seguir descreve a sintaxe geral para uma instrução control resource-definition.
ms.assetid: e7a49a9f-93b5-4221-8006-3d1864b7a6a1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abbdbf707e1ee72f62c7c08cb7065f4d1a4b8f2f4c000d52f3a28c9806a21a0f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117870557"
---
# <a name="common-control-parameters"></a>Parâmetros de controle comuns

O exemplo a seguir descreve a sintaxe geral para uma instrução control resource-definition. O significado de cada parâmetro é dado abaixo. Ocasionalmente, uma instrução usará um parâmetro de forma diferente ou poderá ignorar um parâmetro. A variação específica da instrução é descrita na documentação da instrução .

``` syntax
control [[text,]] id, x, y, width, height[[, style[[, extended-style]]]][, helpId]
[{ data-element-1 [, data-element-2 [,  . . . ]]}]
```

<dl> <dt>

<span id="text"></span><span id="TEXT"></span>*Texto*
</dt> <dd>

Texto que deve ser exibido com o controle . O texto é posicionado dentro do controle ou adjacente ao controle .

Esse parâmetro deve conter zero ou mais caracteres entre aspas duplas ("). As cadeias de caracteres são terminadas em nulo automaticamente e convertidas em Unicode no arquivo de recurso resultante.

Por padrão, os caracteres listados entre aspas duplas são caracteres ANSI e sequências de escape são interpretadas como sequências de escape de byte. Se a cadeia de caracteres for precedida pelo prefixo "L", a cadeia de caracteres será uma cadeia de caracteres largos e as sequências de escape serão interpretadas como sequências de escape de 2 byte que especificam caracteres Unicode. Se uma aspas duplas for necessária no texto, você deverá incluir aspas duplas duas vezes.

Um caractere de & (e ampersand) no texto indica que o caractere a seguir é usado como um caractere mnemônico para o controle . Quando o controle é exibido, o e ampersand não é mostrado, mas o caractere mnemônico é sublinhado. O usuário pode escolher o controle pressionando a tecla correspondente ao caractere mnemônico sublinhado. Para usar o e comercial como um caractere em uma cadeia de caracteres, insira dois e comercial (&&).

</dd> <dt>

<span id="id"></span><span id="ID"></span>*Id*
</dt> <dd>

Identificador do controle. Esse valor deve ser um inteiro sem sinal de 16 bits no intervalo de 0 a 65.535 ou uma expressão aritmética simples que seja avaliada como um valor nesse intervalo.

</dd> <dt>

<span id="x"></span><span id="X"></span>*X*
</dt> <dd>

Coordenada X do lado esquerdo do controle em relação ao lado esquerdo da caixa de diálogo. Esse valor deve ser um inteiro sem sinal de 16 bits no intervalo de 0 a 65.535. A coordenada está em unidades de diálogo e é relativa à origem da caixa de diálogo, janela ou controle que contém o controle especificado.

</dd> <dt>

<span id="y"></span><span id="Y"></span>*Y*
</dt> <dd>

Coordenada Y do lado superior do controle em relação à parte superior da caixa de diálogo. Esse valor deve ser um inteiro sem sinal de 16 bits no intervalo de 0 a 65.535. A coordenada está em unidades de diálogo relativas à origem da caixa de diálogo, da janela ou do controle que contém o controle especificado.

</dd> <dt>

<span id="width"></span><span id="WIDTH"></span>*Largura*
</dt> <dd>

Largura do controle. Esse valor deve ser um inteiro sem sinal de 16 bits no intervalo de 1 a 65.535. A largura está em unidades de 1/4 caracteres.

</dd> <dt>

<span id="height"></span><span id="HEIGHT"></span>*Altura*
</dt> <dd>

Altura do controle. Esse valor deve ser um inteiro sem sinal de 16 bits no intervalo de 1 a 65.535. A altura está em unidades de 1/8 caracteres.

</dd> <dt>

<span id="style"></span><span id="STYLE"></span>*Estilo*
</dt> <dd>

Estilos de controle. Use o operador OR ( ) bit a \| bit para combinar estilos. Para obter mais informações, consulte [Estilos de janela](../winmsg/window-styles.md).

</dd> <dt>

<span id="extended-style"></span><span id="EXTENDED-STYLE"></span>*estilo estendido*
</dt> <dd>

Estilos de janela estendidos. Você deve especificar *o estilo* para especificar o *estilo estendido.* Para obter mais informações, consulte [**EXSTYLE**](exstyle-statement.md).

</dd> <dt>

<span id="helpId"></span><span id="helpid"></span><span id="HELPID"></span>*helpId*
</dt> <dd>

Expressão numérica que indica a ID usada para identificar o controle durante o processamento [**\_ da AJUDA do WM.**](../shell/wm-help.md)

</dd> <dt>

<span id="controlData"></span><span id="controldata"></span><span id="CONTROLDATA"></span>*Controldata*
</dt> <dd>

Dados específicos de controle para o controle. Quando uma caixa de diálogo é criada e um controle nessa caixa de diálogo que tem dados específicos do controle é criado, um ponteiro para esses dados é passado para o procedimento de janela do controle por meio do *lParam* da mensagem [**WM \_ CREATE**](../winmsg/wm-create.md) para esse controle.

</dd> </dl>

## <a name="remarks"></a>Comentários

As unidades de caixa de diálogo horizontais são 1/4 da unidade de largura base do diálogo. As unidades verticais são 1/8 da unidade de altura base da caixa de diálogo. As unidades base da caixa de diálogo atual são computadas da altura e da largura da fonte do sistema atual. A [**função GetDialogBaseUnits**](/windows/win32/api/winuser/nf-winuser-getdialogbaseunits) retorna as unidades base da caixa de diálogo em pixels. As coordenadas são relativas à origem da caixa de diálogo.

 

 