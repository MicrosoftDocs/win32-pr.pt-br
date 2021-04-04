---
title: Elemento ShapeType de VML
description: Elemento ShapeType de VML
ms.assetid: 4e0288c9-ab0f-4399-982a-97dcf16f4ec4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebbb35eef0a3c987fe1e6ec35d15701236ae0af1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104162308"
---
# <a name="vml-shapetype-element"></a>Elemento ShapeType de VML

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define uma forma que pode ser usada para criar outras formas.

O atributo a seguir modifica um **ShapeType**.



| Atributo                                      | Descrição                                             |
|------------------------------------------------|---------------------------------------------------------|
| [Vários](msdn-online-vml-master-attribute.md) | Determina se um **ShapeType** é um elemento mestre. |



 

**Comentários**

**ShapeType** é idêntico ao elemento **Shape** , exceto que não pode fazer referência a outro elemento **ShapeType** .

Quando um elemento **Shape** faz referência a um **ShapeType**, a **forma** pode duplicar algumas das propriedades que já foram especificadas no **ShapeType**. Nesses casos, os atributos na **forma** substituem aqueles do **ShapeType**.

O atributo **Type** não pode ser usado com **ShapeType**.

Os atributos de posicionamento CSS (como **Top**, **Left**, etc.) não são passados para uma **forma** de um **ShapeType**.

Para usar esse elemento, crie um **ShapeType** com um atributo de [ID](id-attribute--vml.md) específico. Em seguida, crie uma **forma** e referencie a **formatype** com o atributo **Type** . Consulte o atributo [Type](type-attribute--shape--vml.md) para obter mais informações.

 

 