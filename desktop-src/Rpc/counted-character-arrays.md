---
title: Matrizes de caracteres contadas
description: O atributo \ Size \_ is \ indica o limite superior da matriz, enquanto o atributo \ length \_ is \ indica o número de elementos da matriz a serem transmitidos.
ms.assetid: bed10259-3034-4be8-91f5-5201c2e19c6b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 360652436a73b445aa2dbb013e0e05145154e20e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104454197"
---
# <a name="counted-character-arrays"></a>Matrizes de caracteres contadas

O \[ atributo [Size \_ é](/windows/desktop/Midl/size-is) \] indica o limite superior da matriz, enquanto o \[ [comprimento \_ é](/windows/desktop/Midl/length-is) \] atributo indica o número de elementos da matriz a serem transmitidos. Além da matriz, o protótipo de procedimento remoto deve incluir todas as variáveis que representam o comprimento ou o tamanho que determinam os elementos da matriz transmitida (eles podem ser parâmetros separados ou agrupados com a cadeia de caracteres em uma estrutura). Esses atributos podem ser usados com matrizes de caracteres largos ou de byte único da mesma forma que seriam com matrizes de outros tipos.

As informações nesta seção descrevem os protótipos de parâmetro de procedimento remoto para matrizes de caracteres. Ele é dividido nos seguintes tópicos:

-   [\[in, out, o tamanho \_ é \] protótipo](-in-out-size-is-prototype.md)
-   [\[em, tamanho \_ é e out, o tamanho \_ é \] protótipo](-in-size-is-and-out-size-is-prototype.md)

 

 