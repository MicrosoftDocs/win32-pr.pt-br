---
title: Recurso DIALOGEX
description: Define uma caixa de diálogo. | Recurso DIALOGEX
ms.assetid: 3ff28b68-e8b4-444d-8e26-5119ed30e44e
keywords:
- Menus de recursos do DIALOGEX e outros recursos
topic_type:
- apiref
api_name:
- DIALOGEX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbd55bfb06b678742aa5e356c9e62b14229aa8d3
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104172798"
---
# <a name="dialogex-resource"></a>Recurso DIALOGEX

Define uma caixa de diálogo. A instrução define a posição e as dimensões da caixa de diálogo na tela, bem como o estilo da caixa de diálogo. Ele também define o seguinte:

-   IDs de ajuda na caixa de diálogo em si, bem como nos controles dentro dela.
-   Uso da instrução [**filestyle**](exstyle-statement.md) para a própria caixa de diálogo, bem como de controles dentro da caixa de diálogo.
-   Espessura da fonte e configurações em itálico para a fonte a ser usada na caixa de diálogo.
-   Dados específicos de controle para controles dentro da caixa de diálogo.
-   Uso dos nomes de classe de sistema predefinidos **BEDIT**, **IEDIT** e **HEDIT** .

``` syntax
nameID DIALOGEX x, y, width, height [ , helpID] [optional-statements]  {control-statements}
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*
</dt> <dd>

Nome exclusivo ou um valor inteiro de 16 bits sem sinal exclusivo que identifica a caixa de diálogo.

</dd> <dt>

<span id="x"></span><span id="X"></span>*w.x.y.*
</dt> <dd>

Local na tela do lado esquerdo da caixa de diálogo, em unidades de diálogo.

</dd> <dt>

<span id="y"></span><span id="Y"></span>*Iar*
</dt> <dd>

Local na tela da parte superior da caixa de diálogo, em unidades de diálogo.

</dd> <dt>

<span id="width"></span><span id="WIDTH"></span>*Largura*
</dt> <dd>

Largura da caixa de diálogo, em unidades de diálogo.

</dd> <dt>

<span id="height"></span><span id="HEIGHT"></span>*tamanho*
</dt> <dd>

Altura da caixa de diálogo, em unidades de diálogo.

</dd> <dt>

<span id="helpID"></span><span id="helpid"></span><span id="HELPID"></span>*HelpID*
</dt> <dd>

Expressão numérica que indica a ID usada para identificar a caixa de diálogo durante o processamento da [**\_ ajuda do WM**](../shell/wm-help.md) .

</dd> <dt>

<span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*instruções opcionais*
</dt> <dd>

Opções para a caixa de diálogo. Isso pode ser zero ou mais das instruções a seguir.



| Instrução                                                         | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Legenda** "*texto*"                                              | Legenda da caixa de diálogo se ela tiver uma barra de título. Para obter mais informações, consulte a [**instrução Caption**](caption-statement.md).                                                                                                                                                                                                                                                                                                                                                            |
| **Características** *DWORD*                                       | Valor **DWORD** definido pelo usuário para uso pelas ferramentas de recurso. Esse valor não é usado pelo sistema. Para obter mais informações, consulte [**declaração de características**](characteristics-statement.md).                                                                                                                                                                                                                                                                                               |
| _Classe_ de classe                                                  | Um inteiro não assinado de 16 bits ou uma cadeia de caracteres entre aspas duplas ("), que identifica a classe da caixa de diálogo. Para obter mais informações, consulte [**declaração de classe**](class-statement.md).                                                                                                                                                                                                                                                                                     |
| **COMstyle** =  *estilos estendidos*                                    | Estilo de janela estendida da caixa de diálogo. Para obter mais informações, consulte [**instrução de filestyle**](exstyle-statement.md).                                                                                                                                                                                                                                                                                                                                                                    |
|  *Pontos* de fonte, "*tipo de letra*", *peso*, *itálico*, conjunto de *caracteres* | Tamanho do ponto e tipo da fonte. Para *peso*, use os **FW \_ \** _ valores definidos em WinGDI. h. Para _italic *, especifique TRUE para usar uma fonte em itálico; caso contrário, FALSE. Para *charset*, use o valor definido no membro **LfCharSet** da estrutura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) . Para obter a fonte definitiva para uma caixa de diálogo, um aplicativo deve especificar *charset* juntamente com outras propriedades Font. Para obter mais informações, consulte [**instrução Font**](font-statement.md). |
|  *Idioma* do idioma, *subidioma*                            | Idioma da caixa de diálogo. Para obter mais informações, consulte a [**instrução de linguagem**](language-statement.md).                                                                                                                                                                                                                                                                                                                                                                               |
|  *Menuname* do menu                                               | Menu a ser usado. Esse valor é o nome do menu ou seu identificador de inteiro. Para obter mais informações, consulte a [**instrução de menu**](menu-statement.md).                                                                                                                                                                                                                                                                                                                             |
|  *Estilos* de estilo                                                | Estilos da caixa de diálogo. Para obter mais informações, consulte [**instrução de estilo**](style-statement.md).                                                                                                                                                                                                                                                                                                                                                                                       |
|  *DWORD* da versão                                               | Valor **DWORD** definido pelo usuário. Essa instrução destina-se ao uso por ferramentas de recursos adicionais e não é usada pelo sistema. Para obter mais informações, consulte a [**instrução de versão**](version-statement.md).                                                                                                                                                                                                                                                                                |



 

</dd> <dt>

<span id="control-statements"></span><span id="CONTROL-STATEMENTS"></span>*instruções de controle*
</dt> <dd>

O corpo do recurso **DIALOGEX** é composto de qualquer número de instruções de controle. Há quatro famílias de instruções de controle: genérico, estático, botão e editar. Para obter mais informações, consulte Comentários.

</dd> </dl>

Alguns atributos também têm suporte para compatibilidade com versões anteriores. Para obter mais informações, consulte [atributos de recursos comuns](common-resource-attributes.md).

## <a name="remarks"></a>Comentários

As operações válidas que podem estar contidas em qualquer uma das expressões numéricas nas instruções de **DIALOGEX** são as seguintes:

-   Adicionar (' + ')
-   Subtrair ('-')
-   Menos unário ('-')
-   Não unário (' ~ ')
-   E (' & ')
-   OU (' \| ')

O corpo do recurso é composto de instruções genéricas, estáticas, de botão e de controle de edição. Embora cada uma dessas famílias de instruções use uma sintaxe diferente para definir recursos específicos de seus controles, todas elas compartilham uma sintaxe comum para definir a posição, o tamanho, os estilos estendidos, o número de identificação da ajuda e os dados específicos do controle. Para obter mais informações, consulte [parâmetros de controle comuns](common-control-parameters.md).

### <a name="generic-control-statements"></a>Instruções de controle genérico

``` syntax
CONTROL controlText, id, className, style
```

<dl> <dt>

<span id="controlText"></span><span id="controltext"></span><span id="CONTROLTEXT"></span>*controlText*
</dt> <dd>

Texto da janela para o controle. Para obter mais informações, consulte [parâmetros de controle comuns](common-control-parameters.md).

</dd> <dt>

<span id="id"></span><span id="ID"></span>*sessão*
</dt> <dd>

Identificador do controle. Para obter mais informações, consulte [parâmetros de controle comuns](common-control-parameters.md).

</dd> <dt>

<span id="className"></span><span id="classname"></span><span id="CLASSNAME"></span>*className*
</dt> <dd>

Nome da classe. Pode ser uma cadeia de caracteres entre aspas duplas (") ou uma das seguintes classes de sistema predefinidas: **botão**, **estático**, **Editar**, **ListBox**, **ScrollBar** ou **ComboBox**.

</dd> <dt>

<span id="style"></span><span id="STYLE"></span>*estilo*
</dt> <dd>

Estilos de janela (os valores explícitos **WS \_ \* *_, _* BS \_ \* *_, _* SS \_ \* *_, _* es \_ \* *_, _* lbs \_ \* *_, _* SBS \_ \* *_ e _* CBS \_ \*** Style definidos em winuser. H podem ser usados pela adição de um include ao arquivo. rc: `#include "winuser.h"` ). Para obter mais informações, consulte [estilos de janela](/windows/desktop/winmsg/window-styles).

</dd> </dl>

### <a name="static-control-statements"></a>Instruções de controle estático

``` syntax
staticClass controlText, id
```

<dl> <dt>

<span id="staticClass"></span><span id="staticclass"></span><span id="STATICCLASS"></span>*staticClass*
</dt> <dd>

**LTEXT**, **RTEXT** ou **CTEXT**.

</dd> <dt>

<span id="controlText"></span><span id="controltext"></span><span id="CONTROLTEXT"></span>*controlText*
</dt> <dd>

Texto da janela para o controle. Para obter mais informações, consulte [parâmetros de controle comuns](common-control-parameters.md).

</dd> <dt>

<span id="id"></span><span id="ID"></span>*sessão*
</dt> <dd>

Identificador do controle. Para obter mais informações, consulte [parâmetros de controle comuns](common-control-parameters.md).

</dd> </dl>

### <a name="button-control-statements"></a>Instruções de controle de botão

``` syntax
buttonClass controlText, id
```

<dl> <dt>

<span id="buttonClass"></span><span id="buttonclass"></span><span id="BUTTONCLASS"></span>*buttonClass*
</dt> <dd>

**AUTO3STATE**, **autocaixa de seleção**, **AUTORADIOBUTTON**, **CheckBox**, **PUSHBOX**, botão de **pressão**, **RadioButton**, **STATE3** ou **UserButton**.

</dd> <dt>

<span id="controlText"></span><span id="controltext"></span><span id="CONTROLTEXT"></span>*controlText*
</dt> <dd>

Texto da janela para o controle. Para obter mais informações, consulte [parâmetros de controle comuns](common-control-parameters.md).

</dd> <dt>

<span id="id"></span><span id="ID"></span>*sessão*
</dt> <dd>

Identificador do controle. Para obter mais informações, consulte [parâmetros de controle comuns](common-control-parameters.md).

</dd> </dl>

### <a name="edit-control-statements"></a>Editar instruções de controle

``` syntax
editClass id
```

<dl> <dt>

<span id="editClass"></span><span id="editclass"></span><span id="EDITCLASS"></span>*editClass*
</dt> <dd>

**EDITTEXT**, **BEDIT**, **HEDIT** ou **IEDIT**.

</dd> <dt>

<span id="id"></span><span id="ID"></span>*sessão*
</dt> <dd>

Identificador do controle. Para obter mais informações, consulte [parâmetros de controle comuns](common-control-parameters.md).

</dd> </dl>

## <a name="see-also"></a>Confira também

<dl> <dt>

[Usando caixas de diálogo](../dlgbox/using-dialog-boxes.md)
</dt> <dt>

[**ACELERADORES**](accelerators-resource.md)
</dt> <dt>

[**CARACTERÍSTICAS**](characteristics-statement.md)
</dt> <dt>

[**CONTROL**](control-control.md)
</dt> <dt>

[**CreateDialog**](/windows/win32/api/winuser/nf-winuser-createdialoga)
</dt> <dt>

[**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa)
</dt> <dt>

[**Caixa**](/windows/win32/api/winuser/nf-winuser-dialogboxa)
</dt> <dt>

[**GetDialogBaseUnits**](/windows/win32/api/winuser/nf-winuser-getdialogbaseunits)
</dt> <dt>

[**LANGUAGE**](language-statement.md)
</dt> <dt>

[**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta)
</dt> <dt>

[ADICIONARMENU](menu-resource.md)
</dt> <dt>

[**RCDATA**](rcdata-resource.md)
</dt> <dt>

[**STRINGTABLE**](stringtable-resource.md)
</dt> <dt>

[**VERSION**](version-statement.md)
</dt> </dl>

 

 
