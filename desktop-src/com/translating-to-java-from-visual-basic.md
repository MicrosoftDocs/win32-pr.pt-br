---
title: Convertendo para Java de Visual Basic
description: Convertendo para Java de Visual Basic
ms.assetid: 2bd61efc-f4f4-46f7-aa5a-f6cefc54d86b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b84d02071641901c5217069d997c22fa04c94cef
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104363712"
---
# <a name="translating-to-java-from-visual-basic"></a>Convertendo para Java de Visual Basic

Por padrão, Visual Basic passa parâmetros por referência. Parâmetros que devem ser passados pelo valor somente são especificados pela palavra-chave **ByVal**.

O Java não oferece suporte a matrizes multidimensionais. Métodos que aceitam ou retornam matrizes multidimensionais não estão disponíveis no Java.

Java e Visual Basic diferem ligeiramente na forma como representam propriedades. No Java, as propriedades são representadas como um conjunto de funções de acessador, uma que define o valor da propriedade e outra que recupera o valor da propriedade. Em Visual Basic, as propriedades são representadas como um único item que pode ser usado para recuperar ou definir o valor da propriedade.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Convertendo para Java](translating-to-java.md)
</dt> </dl>

 

 




