---
title: Tipo de dados IVgAdjustments de VML
description: Tipo de dados IVgAdjustments de VML
ms.assetid: d605632b-3ee2-44fd-8122-f38b1f91e965
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a29f85f93218db098ca247fa66b1f493e9c622a5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104454144"
---
# <a name="vml-ivgadjustments-data-type"></a>Tipo de dados IVgAdjustments de VML

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Coleção de ajustes em uma forma que pode ser usada em fórmulas. Os ajustes podem ser usados como espaços reservados temporários ou por qualquer motivo que você usaria variáveis. Há apenas oito ajustes na coleção.



| Atributos | Descrição                                                                                                                                                                                                                                                                                                                            |
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Comprimento     | **Integer**. Número de ajustes. Não pode ser maior que 8.                                                                                                                                                                                                                                                                          |
| Item       | **Longo**. Matriz de ajustes indexados de 0 a 7. Observe que os ajustes podem ser do SPARC especificado; ou seja, os valores intermediários da matriz nem sempre podem ser preenchidos. Por exemplo, item 1, 3 e 5 podem ter valores para um comprimento de 3, com item (0), Item (2) e item (4) especificado. Para ver se existe um item, use o atributo Exists. |
| Exists     | **IVgTriState**. Determina se existe um ajuste especificado. Observe que um índice deve ser usado; ou seja, Exists (item) deve ser usado para recuperar a existência de um item.                                                                                                                                                           |
| Valor      | **Cadeia de caracteres**. Representação de texto de valores numéricos, com vírgulas entre cada número.                                                                                                                                                                                                                                                    |



 

 

 