---
title: Propriedade Command. LabelTitle
description: Representa um título de rótulo.
ms.assetid: 97378ec3-7988-4e39-9cf5-c382b246c5c9
keywords:
- propriedade Command. LabelTitle da faixa de Windows
topic_type:
- apiref
api_name:
- Command.LabelTitle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c44995d3f17b165c38f9fe7490a33e5d140c8d2b375d5d6b625bb00e3228b21e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119810786"
---
# <a name="commandlabeltitle-property"></a>Propriedade Command. LabelTitle

Representa um título de rótulo.

## <a name="usage"></a>Uso

``` syntax
<Command.LabelTitle>
  child elements
</Command.LabelTitle>
```

## <a name="attributes"></a>Atributos

Não há atributos.

## <a name="child-elements"></a>Elementos filho



| Elemento                                                   | Descrição                                   |
|-----------------------------------------------------------|-----------------------------------------------|
| [**String**](windowsribbon-element-string.md)<br/> | Pode ocorrer no máximo uma vez<br/> <br/> |



## <a name="parent-elements"></a>Elementos pai



| Elemento                                                     |
|-------------------------------------------------------------|
| [**Comando**](windowsribbon-element-command.md)<br/> |



## <a name="remarks"></a>Comentários

Opcional.

Pode ocorrer no máximo uma vez para cada [**comando**](windowsribbon-element-command.md).

**Command. LabelTitle** pode conter um valor do tipo *xs: String* restrito a qualquer sequência de caracteres, incluindo espaços em branco e caracteres de quebra de linha.

> [!Note]  
> Use a referência de caractere XML UCS (conjunto de caracteres universal) `&#xA;` para especificar uma quebra de linha.

 

O comprimento máximo é não associado.

Se nenhum valor for fornecido para **Command. LabelTitle**, o elemento filho da [**cadeia de caracteres**](windowsribbon-element-string.md) será necessário.

> [!Note]  
> Se **Command. LabelTitle** contiver um valor e um elemento filho de [**cadeia**](windowsribbon-element-string.md) de caracteres, a **cadeia de caracteres** terá precedência.

 

O **comando. LabelTitle** só dá suporte ao alinhamento à esquerda.

Se um comando for exposto por meio de um item de menu e o valor do rótulo **Command. LabelTitle** ou [UI \_ PKEY \_](windowsribbon-reference-properties-uipkey-label.md) contiver uma letra precedida por um e comercial, conforme mostrado no exemplo a seguir, essa letra será tratada como um KeyTip e um acelerador de teclado para esse comando pela estrutura da faixa de opções.


```XML
<Command Name="cmdNew"
         Symbol="ID_FILE_NEW"
         Comment="New"
         Id="25001"
         LabelTitle="&amp;New"/>
```



Para exibir um e comercial em um rótulo, escape a designação de caractere especial com um e comercial duplo ( `&&` ), conforme mostrado no exemplo a seguir.


```XML
<Command Name="cmdOpen"
         Symbol="ID_FILE_OPEN"
         Comment="Open"
         Id="25002"
         LabelTitle="&amp;&amp;Open"/>
```



## <a name="examples"></a>Exemplos

O exemplo a seguir demonstra a marcação para um elemento [**Command**](windowsribbon-element-command.md) com uma declaração **Command. LabelTitle** .


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
| Cliente mínimo com suporte<br/> | \[somente aplicativos de área de trabalho Windows 7\]<br/>              |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do Server 2008 R2\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[\_Rótulo de PKEY da interface do usuário \_](windowsribbon-reference-properties-uipkey-label.md)
</dt> </dl>

 

 





