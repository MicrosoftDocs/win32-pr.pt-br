---
title: Atributo de especificação VML
description: Atributo de especificação VML
ms.assetid: df04c15c-cfad-4172-81fa-a28e13f205fc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28b44cc9e8d266ba5ca9c7acb960425d7d4b246145c2d29ba0cc23f668d4aa24
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120098936"
---
# <a name="vml-specularity-attribute"></a>Atributo de especificação VML

Este tópico descreve o VML, um recurso que foi preterido a partir Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem do VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [Conteúdo arquivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obter informações, recomendações e diretrizes sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Define a especificação de uma forma extrudada. Leitura/gravação. **VgNumber.**

**Aplica-se a**

[Extrusão](msdn-online-vml-extrusion-element.md)

**Sintaxe de marca**

<o: *elemento* specularity=" *expressão* ">

**Sintaxe do script**

*element* .specularity="*expression*"

*expressão* = *elemento*.specularity

**Comentários**

Esse valor define a taxa de luz do incidente para luz refletida especularmente. Os valores normais variam de 0 a 1. O valor padrão é 0.

Se valores maiores que 1 são especificados, podem resultar efeitos incomuns.

Microsoft Office Atributo Extensions

 

 