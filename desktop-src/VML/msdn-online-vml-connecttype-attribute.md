---
title: Atributo Connecttype de VML
description: Atributo Connecttype de VML
ms.assetid: 907803c8-687b-4823-8252-b59acbbd9aa4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a54135dcb4ffe0a86f781d68b8babe1259029be
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084555"
---
# <a name="vml-connecttype-attribute"></a>Atributo Connecttype de VML

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define o tipo de pontos de conexão usados para anexar formas a outras formas. Leitura/gravação. **Cadeia de caracteres**.

**Aplica-se a**

[Caminho](msdn-online-vml-path-element.md)

**Sintaxe de marca**

<v: *Element* o:connecttype = " *expressão* " >

**Comentários**

Os valores são:



| Valor    | Descrição                                                                                                                           |
|----------|---------------------------------------------------------------------------------------------------------------------------------------|
| none     | Nenhum site de conexão. Padrão.                                                                                                         |
| rect     | Os quatro pontos de conexão padrão, em pontos médios, dos lados superior, inferior, esquerdo e direito.                                                   |
| segmentos | Os pontos de edição da forma são usados. Os pontos de edição são os pontos pretos em um editor gráfico que são usados para selecionar partes de uma forma. |
| custom   | Uma matriz personalizada de locais de conexão.                                                                                               |



 

*Atributo de extensões de Microsoft Office*

 

 