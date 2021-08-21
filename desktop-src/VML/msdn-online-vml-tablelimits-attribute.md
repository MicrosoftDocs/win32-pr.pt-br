---
title: Atributo TableLimits do VML
description: Atributo TableLimits do VML
ms.assetid: eef855de-23c5-4894-b7cf-2ea39e372e08
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af52ba570b04e56f1dede169045f7ee1addf374fae5ca4f1cd5de4d9390f1235
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959246"
---
# <a name="vml-tablelimits-attribute"></a>Atributo TableLimits do VML

Este tópico descreve o VML, um recurso que foi preterido a partir Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem do VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [Conteúdo arquivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obter informações, recomendações e diretrizes sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Lista de valores mínimos de altura para cada linha em uma tabela. Leitura/gravação. **VgLengthArray.**

**Aplica-se a**

[Forma](shape-element--vml.md)

**Sintaxe de marca**

<v: *elemento* o:tablelimits=" *expressão* ">

**Comentários**

Usado pelo Microsoft PowerPoint para tabelas nativas. O valor padrão é **Null.**

Embora o valor seja armazenado em uma forma, o atributo só é útil quando a tabela é feita de formas agrupadas. Quando o texto é adicionado às células da tabela, a altura da linha pode aumentar. O **atributo TableLimits** armazena a altura da linha original para que, se o texto for excluído, a altura da linha não ficará abaixo do valor original.

*Microsoft Office Atributo Extensions*

 

 