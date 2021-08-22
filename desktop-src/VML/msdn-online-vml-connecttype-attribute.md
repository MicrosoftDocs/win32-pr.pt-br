---
title: Atributo ConnectType do VML
description: Atributo ConnectType do VML
ms.assetid: 907803c8-687b-4823-8252-b59acbbd9aa4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76910977c0673500be2e91d9f387b1e61782a1460e5de0d513784caa6f0f1633
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999256"
---
# <a name="vml-connecttype-attribute"></a>Atributo ConnectType do VML

Este tópico descreve o VML, um recurso que foi preterido a partir Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem do VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [Conteúdo arquivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obter informações, recomendações e diretrizes sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Define o tipo de pontos de conexão usados para anexar formas a outras formas. Leitura/gravação. **Cadeia de caracteres**.

**Aplica-se a**

[Caminho](msdn-online-vml-path-element.md)

**Sintaxe de marca**

<v: *elemento* o:connecttype=" *expressão* ">

**Comentários**

Os valores são:



| Valor    | Descrição                                                                                                                           |
|----------|---------------------------------------------------------------------------------------------------------------------------------------|
| nenhum     | Nenhum site de conexão. Padrão.                                                                                                         |
| rect     | Quatro pontos de conexão padrão nos pontos médios dos lados superior, inferior, esquerdo e direito.                                                   |
| segmentos | Os pontos de edição da forma são usados. Os pontos de edição são os pontos pretos em um editor gráfico que são usados para selecionar partes de uma forma. |
| custom   | Uma matriz personalizada de locais de conexão.                                                                                               |



 

*Microsoft Office Atributo Extensions*

 

 