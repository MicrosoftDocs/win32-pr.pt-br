---
title: Atributo de tipo (forma) (VML)
description: Atributo de tipo (forma) (VML)
ms.assetid: 41f0d1d3-3a2c-47cf-b2ec-d983b14aea87
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82b20f663f8a403acca03ff8ab516a86dc91f7dd8d478eadedaa6be8b919ad48
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119513146"
---
# <a name="type-attribute-shapevml"></a>Atributo de tipo (forma) (VML)

este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). para obter informações, recomendações e orientações sobre a versão atual do Windows Internet explorer, consulte [internet explorer developer Center](https://msdn.microsoft.com/ie/).

 

Define uma referência à ID de um elemento [ShapeType](msdn-online-vml-shapetype-element.md) . Leitura/gravação. **Cadeia de caracteres**.

**Aplica-se a**

[Forma](shape-element--vml.md)

**Sintaxe de marca**

``` syntax
<v:
          element 
          type=" expression ">
```

**Sintaxe do script**

``` syntax
element 
          .type="#expression"
```

``` syntax
expression=element .type
```

**Comentários**

Se o atributo **Type** referenciar a ID de um elemento **ShapeType** , os preenchimentos, os caminhos e os traços do **ShapeType** serão usados como modelos para criar a forma. Os valores derivados de **ShapeType** podem ser substituídos por valores de forma individuais.

Se usado em marcas, o valor da cadeia de caracteres deve começar com um símbolo de sinal numérico ( \# ).

**Atributo padrão da VML**

**Exemplo**

Uma forma **ShapeType** é criada com o "com MyType" como uma ID.


```HTML
   <v:shapetype id="mytype"
   fillcolor="red" strokecolor="blue"
   coordorigin="0 0" coordsize="200 200">
   <v:path v="m 0,0 l 0,200, 200,200, 200,0 x e"/>
   </v:shapetype>
```



Em seguida, se você criar uma forma usando os valores **ShapeType** , a forma terá os atributos da **forma**"com MyType". ou seja, "shape01" terá um preenchimento vermelho com um traço azul.


```HTML
   <v:shape id="shape01" type="#mytype"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:shape>
```



Você pode substituir os valores herdados, por exemplo, alterando a cor para verde.


```HTML
   <v:shape id="shape02" type="#mytype"
   fillcolor="green"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:shape>
```



[Exemplo do atributo Type](/previous-versions/bb264099(v=vs.85)). (Requer o Microsoft Internet Explorer 5 ou superior.)

 

 