---
title: Atributo src (VMLFrame) (VML)
description: Atributo src (VMLFrame) (VML)
ms.assetid: 6ac7a3b5-3c1d-43a0-ab92-a03e3bd45733
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28a9c3ec4849098c9469fba56f26d4c3dd514746
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294179"
---
# <a name="src-attribute-vmlframevml"></a>Atributo src (VMLFrame) (VML)

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define a fonte de dados para o quadro. Leitura/gravação. **Cadeia de caracteres**.

**Aplica-se a**

[VMLFrame](msdn-online-vml-vmlframe-element.md)

**Sintaxe de marca**

<v: *Element* src = " *expressão* " >

**Sintaxe do script**

*Element* . src = "*expressão*"

*expressão* = de *elemento*. src

**Comentários**

O atributo **src** pode envolver as seguintes sintaxes:

-   URL para o arquivo externo. O arquivo deve ser um arquivo XML com o seguinte formato:
    ```HTML
       <xml xmlns:v = "urn:schemas-microsoft-com:vml">
       .
       .
       .
       </xml>
    ```

    

-   Dentro do arquivo, você deve ter uma ou mais formas de VML com IDs válidas que podem ser referenciadas usando essa sintaxe:
    ```HTML
       filename#shapename
    ```

    

-   Na referência a seguir, os arquivos externos têm a extensão. VML, mas qualquer extensão pode ser usada:
    ```HTML
       external.vml#image01
    ```

    

-   Você pode fazer referência a uma forma dentro do mesmo arquivo usando a seguinte sintaxe:
    ```HTML
       #shapename
    ```

    

Se **clip** for **false**, a forma será dimensionada para caber no quadro. Se **for true**, qualquer parte da forma que estiver fora do quadro não será exibida.

Observe que a [origem](origin-attribute--vmlframe--vml.md) e o [tamanho](size-attribute--vmlframe.md) não serão usados, a menos que o **clipe** seja **verdadeiro**.

**Atributo padrão da VML**

**Exemplo**

A imagem definida no arquivo externo será recortada.


```HTML
   <v:vmlframe id="frame01" clip="True"
   origin="100pt,100pt" size="50pt,50pt"
   src="external.vml#shape01"
   style='top:160pt; left:100pt; width:50pt; height:50pt'>
   </v:vmlframe>
```



 

 