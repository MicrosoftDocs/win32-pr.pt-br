---
title: Atributo VML ViewpointOrigin
description: Atributo VML ViewpointOrigin
ms.assetid: 4ccb3e12-bae4-4cb2-b48b-80c155ae7e03
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e5e69357eddfe535b3c6164579454260d8f478430f7a9f1c7bede3262b1b040
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120007556"
---
# <a name="vml-viewpointorigin-attribute"></a>Atributo VML ViewpointOrigin

Este tópico descreve o VML, um recurso que foi preterido a partir Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem do VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [Conteúdo arquivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obter informações, recomendações e diretrizes sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Define a origem do ponto de vista dentro da caixa delimitada da forma. Leitura/gravação. **VgVector2D.**

**Aplica-se a**

[Extrusão](msdn-online-vml-extrusion-element.md)

**Sintaxe de marca**

<o: *element* viewpointorigin=" *expressão* ">

**Sintaxe do script**

*element* .viewpointorigin="*expression*"

*expressão* = *elemento*.viewpointorigin

**Comentários**

Define o ponto de vista em termos dos valores x e y da forma original. Os valores x e y variam de 0,5 a -0,5 (50% a -50% da origem da coordenada da forma). O padrão é 0,0.

*Microsoft Office Atributo Extensions*

 

 