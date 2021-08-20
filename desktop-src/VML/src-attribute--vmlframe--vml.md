---
title: Atributo Src (VMLFrame)(VML)
description: Atributo Src (VMLFrame)(VML)
ms.assetid: 6ac7a3b5-3c1d-43a0-ab92-a03e3bd45733
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a44f7761a55304eefc655d00ed58d84b7af8f7ce5daf86a3aaf462308b43c193
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119057574"
---
# <a name="src-attribute-vmlframevml"></a>Atributo Src (VMLFrame)(VML)

Este tópico descreve o VML, um recurso que foi preterido a partir Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem do VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [Conteúdo arquivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obter informações, recomendações e diretrizes sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Define a fonte de dados para o quadro. Leitura/gravação. **Cadeia de caracteres**.

**Aplica-se a**

[VMLFrame](msdn-online-vml-vmlframe-element.md)

**Sintaxe de marca**

<v: *elemento* src=" *expressão* ">

**Sintaxe do script**

*expressão* element .src=""

*expressão* = *elemento*.src

**Comentários**

O **atributo Src** pode envolver as seguintes sintaxes:

-   URL para arquivo externo. O arquivo deve ser um arquivo XML com o seguinte formato:
    ```HTML
       <xml xmlns:v = "urn:schemas-microsoft-com:vml">
       .
       .
       .
       </xml>
    ```

    

-   Dentro do arquivo, você deve ter uma ou mais formas VML com IDs válidas que podem ser referenciadas usando esta sintaxe:
    ```HTML
       filename#shapename
    ```

    

-   Na referência a seguir, os arquivos externos têm a extensão .vml, mas qualquer extensão pode ser usada:
    ```HTML
       external.vml#image01
    ```

    

-   Você pode referenciar uma forma dentro do mesmo arquivo usando a seguinte sintaxe:
    ```HTML
       #shapename
    ```

    

Se **Clip** for **False**, a forma será dimensionado para se ajustar ao quadro. Se **True**, todas as partes da forma que estão fora do quadro não serão exibidas.

Observe que [a origem](origin-attribute--vmlframe--vml.md) [e o tamanho](size-attribute--vmlframe.md) não serão usados, a menos que Clip **seja** **True.**

**Atributo padrão VML**

**Exemplo**

A imagem definida no arquivo externo será recortada.


```HTML
   <v:vmlframe id="frame01" clip="True"
   origin="100pt,100pt" size="50pt,50pt"
   src="external.vml#shape01"
   style='top:160pt; left:100pt; width:50pt; height:50pt'>
   </v:vmlframe>
```



 

 