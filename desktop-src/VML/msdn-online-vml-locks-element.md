---
title: Elemento de bloqueios de VML
description: Elemento de bloqueios de VML
ms.assetid: 1dfdc23a-0ad1-468f-a850-2068f3cc1803
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46a3d246e486d1b7db99484777355b9160b71b6b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084710"
---
# <a name="vml-locks-element"></a>Elemento de bloqueios de VML

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define um bloqueio para uma forma.

Os atributos a seguir modificam um bloqueio.



| Atributo                                                    | Descrição                                                                 |
|--------------------------------------------------------------|-----------------------------------------------------------------------------|
| [AdjustHandles](msdn-online-vml-adjusthandles-attribute.md) | Determina se os identificadores de uma forma podem ser editados.                    |
| [AspectRatio](msdn-online-vml-aspectratio-attribute.md)     | Determina se a taxa de proporção de uma forma pode ser alterada por um editor. |
| [Corte](msdn-online-vml-cropping-attribute.md)           | Determina se o corte será permitido em um editor.                   |
| [Externa](ext-attribute--lock--vml.md)                          | Define o comportamento de ações de bloqueio para um editor gráfico.             |
| [Agrupamento](msdn-online-vml-grouping-attribute.md)           | Determina se as formas podem ser agrupadas em um editor.                      |
| [Posição](position-attribute--lock--vml.md)                | Determina se a posição de uma forma está bloqueada em um editor.          |
| [Rotação](rotation-attribute--lock--vml.md)                | Determina se a rotação de formas será permitida em um editor.         |
| [Seleção](msdn-online-vml-selection-attribute.md)         | Determina se a forma é selecionável em um editor.                    |
| [Formatype](msdn-online-vml-shapetype-attribute.md)         | Determina se o tipo de AutoFormas pode ser alterado por um editor.         |
| [Text](msdn-online-vml-text-attribute.md)                   | Determina se o texto anexado a uma forma pode ser editado.              |
| [Vértices](msdn-online-vml-vertices-attribute.md)           | Determina se os vértices de um caminho podem ser alterados por um editor.      |



 

**Comentários**

Esse elemento deve ser definido dentro de um elemento [Shape](shape-element--vml.md) .

O elemento **Locks** é uma extensão Microsoft Office para VML.

 

 