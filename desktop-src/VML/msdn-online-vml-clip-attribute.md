---
title: Atributo de clipe VML
description: Atributo de clipe VML
ms.assetid: 8839c10e-96dd-4419-9f02-80033a4633e9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cab4afdef2a10c9c6f6a0561dedf5b4df3538a97152cb53181452b8ac531bb3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999286"
---
# <a name="vml-clip-attribute"></a>Atributo de clipe VML

Este tópico descreve o VML, um recurso que foi preterido a partir Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem do VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [Conteúdo arquivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obter informações, recomendações e diretrizes sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Determina se o recorte está em. Leitura/gravação. **VgTriState.**

**Aplica-se a**

[VMLFrame](msdn-online-vml-vmlframe-element.md)

**Sintaxe de marca**

<v: *elemento* clip=" *expressão* ">

**Sintaxe do script**

*elemento* .clip="*expression*"

*expressão* = *elemento*.clip

**Comentários**

Se **Clip** for **False**, a forma será dimensionado para se ajustar ao quadro. Se **True**, todas as partes da forma que estão fora do quadro não serão exibidas.

Observe que [a origem](origin-attribute--vmlframe--vml.md) [e o tamanho](size-attribute--vmlframe.md) não serão usados, a menos que Clip **seja** **True.**

*Atributo padrão VML*

**Exemplo**

A imagem definida no arquivo externo será recortada.


```HTML
   <v:vmlframe id="frame01" clip="True"
   origin="100pt,100pt" size="50pt,50pt"
   src="external.vml#shape01"
   style='top:160pt; left:100pt; width:50pt; height:50pt'>
   </v:vmlframe>
```



 

 