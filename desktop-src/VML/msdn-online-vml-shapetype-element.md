---
title: Elemento ShapeType VML
description: Elemento ShapeType VML
ms.assetid: 4e0288c9-ab0f-4399-982a-97dcf16f4ec4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0632919a141ae04f80b0b6cd6782ea907aa8cfe1d720e599964110c038f3998e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099086"
---
# <a name="vml-shapetype-element"></a>Elemento ShapeType VML

Este tópico descreve o VML, um recurso que foi preterido a partir Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem do VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [Conteúdo arquivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obter informações, recomendações e diretrizes sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Define uma forma que pode ser usada para criar outras formas.

O atributo a seguir modifica um **ShapeType.**



| Atributo                                      | Descrição                                             |
|------------------------------------------------|---------------------------------------------------------|
| [Mestre](msdn-online-vml-master-attribute.md) | Determina se um **ShapeType** é um elemento mestre. |



 

**Comentários**

**ShapeType** é idêntico ao elemento **Shape,** exceto que não pode referenciar outro **elemento ShapeType.**

Quando um **elemento Shape** faz referência a **um ShapeType**, a **Forma** pode duplicar algumas das propriedades que já foram especificadas no **ShapeType.** Nesses casos, os atributos na Forma **substituem** aqueles do **ShapeType**.

O **atributo Type** não pode ser usado com **ShapeType**.

Atributos de posicionamento CSS (como **Top**, **Left** etc.) não são passados para uma **Forma** de um **ShapeType.**

Para usar esse elemento, crie um **ShapeType** com um atributo [de ID](id-attribute--vml.md) específico. Em seguida, **crie uma Forma** e referencia o **ShapeType** com o **atributo** Type. Consulte o [atributo Type](type-attribute--shape--vml.md) para obter mais informações.

 

 