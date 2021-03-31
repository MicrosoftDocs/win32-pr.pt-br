---
title: Atributo TableLimits de VML
description: Atributo TableLimits de VML
ms.assetid: eef855de-23c5-4894-b7cf-2ea39e372e08
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b35a7449cc2f348e6040161c1fb599c29972803
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641169"
---
# <a name="vml-tablelimits-attribute"></a>Atributo TableLimits de VML

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Lista de valores de altura mínima para cada linha em uma tabela. Leitura/gravação. **VgLengthArray**.

**Aplica-se a**

[Forma](shape-element--vml.md)

**Sintaxe de marca**

<v: *Element* o:tablelimits = " *expressão* " >

**Comentários**

Usado pelo Microsoft PowerPoint para tabelas nativas. O valor padrão é **NULL**.

Embora o valor seja armazenado em uma forma, o atributo só é útil quando a tabela é composta de formas agrupadas. Quando o texto é adicionado às células da tabela, a altura da linha pode aumentar. O atributo **TableLimits** armazena a altura da linha original para que, se o texto for excluído, a altura da linha não fique abaixo do valor original.

*Atributo de extensões de Microsoft Office*

 

 