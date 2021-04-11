---
title: Parâmetros de controle comuns
description: O seguinte descreve a sintaxe geral para uma instrução Control Resource-Definition.
ms.assetid: e7a49a9f-93b5-4221-8006-3d1864b7a6a1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 261c71163276ed39841d6f6d7e125d4eb5420072
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104293986"
---
# <a name="common-control-parameters"></a>Parâmetros de controle comuns

O seguinte descreve a sintaxe geral para uma instrução Control Resource-Definition. O significado de cada parâmetro é fornecido abaixo. Ocasionalmente, uma instrução usará um parâmetro de forma diferente ou poderá ignorar um parâmetro. A variação específica da instrução é descrita na documentação da instrução.

``` syntax
control [[text,]] id, x, y, width, height[[, style[[, extended-style]]]][, helpId]
[{ data-element-1 [, data-element-2 [,  . . . ]]}]
```

<dl> <dt>

<span id="text"></span><span id="TEXT"></span>*texto*
</dt> <dd>

Texto a ser exibido com o controle. O texto é posicionado dentro do controle ou adjacente ao controle.

Esse parâmetro deve conter zero ou mais caracteres entre aspas duplas ("). As cadeias de caracteres são automaticamente terminadas em nulo e convertidas em Unicode no arquivo de recurso resultante.

Por padrão, os caracteres listados entre aspas duplas são caracteres ANSI e as sequências de escape são interpretadas como sequências de escape de byte. Se a cadeia de caracteres for precedida pelo prefixo "L", a cadeia de caracteres será uma cadeia de caracteres largos e as sequências de escape serão interpretadas como sequências de escape de 2 bytes que especificam caracteres Unicode. Se uma aspa dupla for necessária no texto, você deverá incluir duas aspas duas vezes.

Um caractere de e comercial (&) no texto indica que o caractere a seguir é usado como um caractere mnemônico para o controle. Quando o controle é exibido, o e comercial não é mostrado, mas o caractere mnemônico é sublinhado. O usuário pode escolher o controle pressionando a tecla correspondente ao caractere mnemônico sublinhado. Para usar o e comercial como um caractere em uma cadeia de caracteres, insira dois e comercial (&&).

</dd> <dt>

<span id="id"></span><span id="ID"></span>*sessão*
</dt> <dd>

Identificador do controle. Esse valor deve ser um inteiro sem sinal de 16 bits no intervalo de 0 a 65.535 ou uma expressão aritmética simples que é avaliada como um valor nesse intervalo.

</dd> <dt>

<span id="x"></span><span id="X"></span>*w.x.y.*
</dt> <dd>

Coordenada X do lado esquerdo do controle em relação ao lado esquerdo da caixa de diálogo. Esse valor deve ser um inteiro sem sinal de 16 bits no intervalo de 0 a 65.535. A coordenada está em unidades de caixa de diálogo e é relativa à origem da caixa de diálogo, janela ou controle que contém o controle especificado.

</dd> <dt>

<span id="y"></span><span id="Y"></span>*Iar*
</dt> <dd>

Coordenada Y do lado superior do controle em relação à parte superior da caixa de diálogo. Esse valor deve ser um inteiro sem sinal de 16 bits no intervalo de 0 a 65.535. A coordenada está em unidades de caixa de diálogo relativas à origem da caixa de diálogo, janela ou controle que contém o controle especificado.

</dd> <dt>

<span id="width"></span><span id="WIDTH"></span>*Largura*
</dt> <dd>

Largura do controle. Esse valor deve ser um inteiro sem sinal de 16 bits no intervalo de 1 a 65.535. A largura está em unidades de 1/4 caracteres.

</dd> <dt>

<span id="height"></span><span id="HEIGHT"></span>*tamanho*
</dt> <dd>

Altura do controle. Esse valor deve ser um inteiro sem sinal de 16 bits no intervalo de 1 a 65.535. A altura está em unidades de 1/8 caracteres.

</dd> <dt>

<span id="style"></span><span id="STYLE"></span>*estilo*
</dt> <dd>

Estilos de controle. Use o operador OR () de or ( \| ) para combinar estilos. Para obter mais informações, consulte [estilos de janela](../winmsg/window-styles.md).

</dd> <dt>

<span id="extended-style"></span><span id="EXTENDED-STYLE"></span>*estilo estendido*
</dt> <dd>

Estilos de janela estendidos. Você deve especificar o *estilo* para especificar o *estilo estendido*. Para obter mais informações, consulte [**comstyle**](exstyle-statement.md).

</dd> <dt>

<span id="helpId"></span><span id="helpid"></span><span id="HELPID"></span>*HelpID*
</dt> <dd>

Expressão numérica que indica a ID usada para identificar o controle durante o processamento da [**\_ ajuda do WM**](../shell/wm-help.md) .

</dd> <dt>

<span id="controlData"></span><span id="controldata"></span><span id="CONTROLDATA"></span>*controlData*
</dt> <dd>

Dados específicos de controle para o controle. Quando uma caixa de diálogo é criada e um controle nessa caixa de diálogo que tem dados específicos de controle é criado, um ponteiro para esses dados é passado para o procedimento de janela do controle por meio do *lParam* da mensagem de [**\_ criação do WM**](../winmsg/wm-create.md) para esse controle.

</dd> </dl>

## <a name="remarks"></a>Comentários

As unidades de caixa de diálogo horizontais são 1/4 da unidade de largura base da caixa de diálogo. As unidades verticais são 1/8 da unidade de altura base da caixa de diálogo. As unidades base da caixa de diálogo atual são computadas a partir da altura e da largura da fonte atual do sistema. A função [**GetDialogBaseUnits**](/windows/win32/api/winuser/nf-winuser-getdialogbaseunits) retorna as unidades base da caixa de diálogo em pixels. As coordenadas são relativas à origem da caixa de diálogo.

 

 