---
title: Convertendo para Java de Visual Basic
description: Convertendo para Java de Visual Basic
ms.assetid: 2bd61efc-f4f4-46f7-aa5a-f6cefc54d86b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f2660162500ba506fcf8b1a5c24819e60b8765439bb7d033fa9d5312711611e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119793583"
---
# <a name="translating-to-java-from-visual-basic"></a>Convertendo para Java de Visual Basic

por padrão, Visual Basic passa parâmetros por referência. Parâmetros que devem ser passados pelo valor somente são especificados pela palavra-chave **ByVal**.

O Java não oferece suporte a matrizes multidimensionais. Métodos que aceitam ou retornam matrizes multidimensionais não estão disponíveis no Java.

Java e Visual Basic diferem ligeiramente na forma como representam propriedades. No Java, as propriedades são representadas como um conjunto de funções de acessador, uma que define o valor da propriedade e outra que recupera o valor da propriedade. em Visual Basic, as propriedades são representadas como um único item que pode ser usado para recuperar ou definir o valor da propriedade.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Convertendo para Java](translating-to-java.md)
</dt> </dl>

 

 




