---
title: Propriedade Command. SmallImages
description: Representa um contêiner de imagens; Nesse caso, imagens pequenas.
ms.assetid: 15c00e61-543a-4cc8-b329-516985d02359
keywords:
- propriedade Command. SmallImages da faixa de Windows
topic_type:
- apiref
api_name:
- Command.SmallImages
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63445f2dbfce88e9793b3563d0ce8ed9861f45fa0831680a455b1a0a04bb4bd1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119329266"
---
# <a name="commandsmallimages-property"></a>Propriedade Command. SmallImages

Representa um contêiner de imagens; Nesse caso, imagens pequenas.

## <a name="usage"></a>Uso

``` syntax
<Command.SmallImages>
  child elements
</Command.SmallImages>
```

## <a name="attributes"></a>Atributos

Não há atributos.

## <a name="child-elements"></a>Elementos filho



| Elemento                                                 | Descrição                                        |
|---------------------------------------------------------|----------------------------------------------------|
| [**Imagem**](windowsribbon-element-image.md)<br/> | Pode ocorrer uma ou mais vezes<br/> <br/> |



## <a name="parent-elements"></a>Elementos pai



| Elemento                                                     |
|-------------------------------------------------------------|
| [**Comando**](windowsribbon-element-command.md)<br/> |



## <a name="remarks"></a>Comentários

Opcional.

Pode ocorrer no máximo uma vez para cada [**comando**](windowsribbon-element-command.md).

Os recursos de imagem devem estar em conformidade com o formato gráfico BMP (bitmap padrão) usado em Windows.

## <a name="examples"></a>Exemplos

O exemplo a seguir demonstra a marcação básica para o [**SplitButton**](windowsribbon-element-splitbutton.md) com um elemento de [**menu**](windowsribbon-element-menugroup.md) .

Esta seção de código mostra as declarações de comando [**SplitButton**](windowsribbon-element-splitbutton.md) e de [**menu de menus**](windowsribbon-element-menugroup.md) com um recurso de imagem grande e um pequeno. Um [**grupo**](windowsribbon-element-group.md) associado que atua como o contêiner pai do elemento **SplitButton** também é declarado.


```XML
<!-- SplitButton -->
<Command Name="cmdSplitButtonGroup"
         Symbol="cmdSplitButtonGroup"
         Comment="SplitButton Group"
         LabelTitle="SplitButton"/>
<Command Name="cmdSplitButton"
         Symbol="cmdSplitButton"
         Comment="SplitButton"
         LabelTitle="SplitButton"/>
<Command Name="cmdSBButtonItem"
         Symbol="cmdSBButtonItem"
         Comment="SBButtonItem"
         LabelTitle="SB ButtonItem"/>
<Command Name="cmdSBButton1"
         Symbol="cmdSBButton1"
         Comment="SBButton1"
         LabelTitle="SB Button">
  <Command.LargeImages>
    <Image Source="res/copyL_32.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/copyS_16.bmp"/>
  </Command.SmallImages>
  <Command.LargeHighContrastImages>
    <Image Source="res/copyLHC_32.bmp"/>
  </Command.LargeHighContrastImages>
  <Command.SmallHighContrastImages>
    <Image Source="res/copySHC_16.bmp"/>
  </Command.SmallHighContrastImages>
</Command>
<Command Name="cmdSBMajorItems"
         Comment="Major Items Category"
         LabelTitle="Major Items"/>
<Command Name="cmdSBStandardItems"
         Comment="Standard Items Category"
         LabelTitle="Standard Items"/>
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[somente aplicativos de área de trabalho Windows 7\]<br/>              |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do Server 2008 R2\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Especificando recursos de imagem da faixa de uma](windowsribbon-imageformats.md)
</dt> <dt>

[\_SmallImage PKEY \_ UI](windowsribbon-reference-properties-uipkey-smallimage.md)
</dt> </dl>

 

 





