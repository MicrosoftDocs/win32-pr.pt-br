---
title: Propriedade Image.Source
description: Representa o caminho do diretório de uma imagem.
ms.assetid: 174a518a-e9a3-4461-a9a3-d61b62d2b718
keywords:
- Propriedade Image.Source Windows Faixa de Opções
topic_type:
- apiref
api_name:
- Image.Source
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20612f0d25f914cb4c80ae77bb001a678af79e4605c3e1358ed7e33f6b19d805
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118202401"
---
# <a name="imagesource-property"></a>Propriedade Image.Source

Representa o caminho do diretório de uma imagem.

## <a name="usage"></a>Uso

``` syntax
<Image.Source/>
```

## <a name="attributes"></a>Atributos

Não há atributos.

## <a name="child-elements"></a>Elementos filho

Não há elementos filho.

## <a name="parent-elements"></a>Elementos pai



| Elemento                                                 |
|---------------------------------------------------------|
| [**Imagem**](windowsribbon-element-image.md)<br/> |



## <a name="remarks"></a>Comentários

Opcional.

Pode ocorrer no máximo uma vez para cada [**Imagem**](windowsribbon-element-image.md).

Esse elemento contém um valor do tipo *xs:anyURI* ou qualquer sequência de caracteres que representa um Uniform Resource Identifier (URI). O valor de URI é um caminho de diretório absoluto ou relativo (ao arquivo de marcação faixa de opções) de um recurso de imagem do tipo bitmap (BMP).

## <a name="examples"></a>Exemplos

O exemplo de código a seguir mostra a marcação necessária para declarar, por meio de um conjunto de elementos [**Image,**](windowsribbon-element-image.md) uma coleção de recursos de imagem projetados para dar suporte a quatro configurações específicas de dpi de tela. A **propriedade Image.Source** é usada para especificar o caminho para o recurso de imagem.


```C++
<Command Name="cmdSizeAndColor" Symbol="IDR_CMD_SIZEANDCOLOR">
  <Command.LabelTitle>
    <String Id="250">Size and Color</String>
  </Command.LabelTitle>
  <Command.LargeImages>
    <Image Id="251" MinDPI="96">
      <Image.Source>res/sizeAndColor_96.bmp</Image.Source>
    </Image>
    <Image Id="252" MinDPI="120">
      <Image.Source>res/sizeAndColor_120.bmp</Image.Source>
    </Image>
    <Image Id="253" MinDPI="144">
      <Image.Source>res/sizeAndColor_144.bmp</Image.Source>
    </Image>
    <Image Id="254" MinDPI="192">
      <Image.Source>res/sizeAndColor_192.bmp</Image.Source>
    </Image>
  </Command.LargeImages>
</Command>
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>              |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do Server 2008 R2 \[\]<br/> |



 

 





