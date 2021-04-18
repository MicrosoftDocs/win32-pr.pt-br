---
title: Propriedade Command. KeyTip
description: Representa o KeyTip de um controle.
ms.assetid: 214f69ae-dd35-4abf-b294-d898d7802aa6
keywords:
- Faixa de das propriedades do Windows de Propriedade Command. KeyTip
topic_type:
- apiref
api_name:
- Command.Keytip
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ab16b9b8e52094d6cdc85890dfc1cf8af63942c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105788978"
---
# <a name="commandkeytip-property"></a>Propriedade Command. KeyTip

Representa o KeyTip de um controle.

## <a name="usage"></a>Uso

``` syntax
<Command.Keytip>
  child elements
</Command.Keytip>
```

## <a name="attributes"></a>Atributos

Não há atributos.

## <a name="child-elements"></a>Elementos filho



| Elemento                                                   | Descrição                                   |
|-----------------------------------------------------------|-----------------------------------------------|
| [**Strings**](windowsribbon-element-string.md)<br/> | Pode ocorrer no máximo uma vez<br/> <br/> |



## <a name="parent-elements"></a>Elementos pai



| Elemento                                                     |
|-------------------------------------------------------------|
| [**Comando**](windowsribbon-element-command.md)<br/> |



## <a name="remarks"></a>Comentários

Opcional.

Pode ocorrer no máximo uma vez para cada elemento de [**comando**](windowsribbon-element-command.md) .

**Command. KeyTip** pode conter um valor do tipo *xs: String* restrito a qualquer sequência de caracteres Unicode, incluindo o espaço em branco.

Um **comando. KeyTip** pode começar com um número somente quando associado a um controle dentro de uma [guia](windowsribbon-controls-tab.md) ou na [barra de ferramentas de acesso rápido](windowsribbon-controls-quickaccesstoolbar.md).

Para exibir as dicas de tecla que são válidas para o estado atual da faixa de faixas, pressione e segure a chave ALT. A captura de tela a seguir mostra o inicial, ou primeiro nível, dicas de teclado que são exibidas no Microsoft Paint para Windows 7. Após a seleção de um KeyTip de primeiro nível, somente as keytips de nível de segundo são exibidas.

![Dicas de primeiro nível no Microsoft Paint para Windows 7](images/properties/ui-pkey-label-keytips.png)

O **comando. KeyTip** atua como o acelerador de teclado para um comando, a menos que esse comando seja exposto por meio de um item de menu. Nesse caso, a estrutura ignora o valor de **Command. KeyTip** e, em vez disso, usa um caractere precedido por um e comercial como especificado por [**Command. LabelTitle**](windowsribbon-element-command-labeltitle.md) ou o [ \_ \_ rótulo PKEY da interface do usuário](windowsribbon-reference-properties-uipkey-label.md). Se nenhum e comercial for especificado pelo **comando Command. LabelTitle** ou UI \_ PKEY \_ , nenhum KeyTip ou acelerador de teclado será exposto.

Se nenhum valor for fornecido para **Command. KeyTip**, o elemento filho da [**cadeia de caracteres**](windowsribbon-element-string.md) será necessário.

> [!Note]  
> Se **Command. KeyTip** contiver um valor e um elemento filho de [**cadeia**](windowsribbon-element-string.md) de caracteres, a **cadeia de caracteres** terá precedência.

 

Por padrão, as seguintes letras são usadas pela estrutura para gerar automaticamente dicas de Key:

-   O **F** é atribuído ao [menu do aplicativo](windowsribbon-controls-applicationmenu.md).
-   **Y** é atribuído a qualquer comando que não tenha um KeyTip especificado pelo aplicativo.
-   **Z** é atribuído a cada controle de [grupo](windowsribbon-controls-group.md) e não pode ser personalizado. Um KeyTip de grupo é exibido somente quando o [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) do controle Especifica uma opção de tamanho de **pop-up** . Para obter mais informações, consulte [Personalizando uma faixa de guia por meio de definições de tamanho e políticas de dimensionamento](windowsribbon-templates.md).

> [!Note]  
> Nenhuma dessas letras é reservada pela estrutura. Cada um pode ser atribuído a um ou mais comandos, conforme necessário.

 

A estrutura resolve conflitos de KeyTip das seguintes maneiras:

-   Se um ou mais controles [guia](windowsribbon-controls-tab.md) estiverem associados ao mesmo KeyTip, um número será acrescentado a cada KeyTip, começando em 1 e aumentando sequencialmente (2, 3,...) para cada controle na ordem de declaração. Se qualquer controle de guia for atribuído à letra F como um KeyTip, o [menu do aplicativo](windowsribbon-controls-applicationmenu.md) será atribuído F1 com as dicas de tecla restantes ajustadas conforme descrito.
-   Quando associado a um único controle dentro de uma [guia](windowsribbon-controls-tab.md), o KeyTip F é válido para o controle e o [menu do aplicativo](windowsribbon-controls-applicationmenu.md). O menu do aplicativo padrão KeyTip não é alterado, mas a precedência é dada ao controle na guia ativa.
-   Se um ou mais controles dentro de uma guia estiverem associados ao mesmo KeyTip, a estrutura refatorar automaticamente as dicas de [tecla](windowsribbon-controls-tab.md) desses controles, conforme descrito anteriormente.

> [!Note]  
> Uma pequena variação na cor do texto é usada para realçar as dicas de atalho Refatorada em uma implementação de faixa de medida padrão. Para uma implementação de faixa de faixas não padrão em que a cor da faixa de medida foi personalizada, esse comportamento de estrutura é substituído e todas as keytips são exibidas com a mesma cor do texto. Para obter mais informações, consulte [Personalizando as cores da faixa](ribbon-color.md)de forma.

 

O comprimento máximo é não associado.

## <a name="examples"></a>Exemplos

O exemplo a seguir demonstra a marcação para um elemento [**Command**](windowsribbon-element-command.md) com uma declaração **Command. KeyTip** .


```XML
<Command>
  <Command.Name>cmdSave</Command.Name>
  <Command.Symbol>ID_FILE_SAVE</Command.Symbol>
  <Command.Comment>Save</Command.Comment>
  <Command.Id>25003</Command.Id>
  <Command.LabelTitle>
    <String>
      <String.Content>Label for Save</String.Content>
      <String.Id>59999</String.Id>
      <String.Symbol>strSave</String.Symbol>
    </String>
  </Command.LabelTitle>
  <Command.TooltipTitle>Tooltip title with &amp;&amp; for Save Command</Command.TooltipTitle>
  <Command.TooltipDescription>Tooltip description for Save Command.</Command.TooltipDescription>
  <Command.Keytip>s1</Command.Keytip>
</Command>
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>              |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[\_KeyTip PKEY \_ UI](windowsribbon-reference-properties-uipkey-keytip.md)
</dt> </dl>

 

 





