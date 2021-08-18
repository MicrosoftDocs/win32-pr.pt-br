---
title: Matrizes de caracteres contadas
description: O atributo \ size is\ indica o limite superior da matriz enquanto o atributo \ length is\ indica o número \_ de elementos de matriz a \_ transmitir.
ms.assetid: bed10259-3034-4be8-91f5-5201c2e19c6b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea8abb7a391c617cadae5af396c4b4216dc9d14abf0f6d31ead3a6e075c7357b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118931125"
---
# <a name="counted-character-arrays"></a>Matrizes de caracteres contadas

O atributo size é indica o limite superior da matriz enquanto o atributo length is indica o número de elementos de matriz a \[ [ \_ ](/windows/desktop/Midl/size-is) \] \[ [ \_ ](/windows/desktop/Midl/length-is) \] transmitir. Além da matriz, o protótipo de procedimento remoto deve incluir quaisquer variáveis que representem tamanho ou tamanho que determinem os elementos de matriz transmitidos (eles podem ser parâmetros separados ou agrupados com a cadeia de caracteres em uma estrutura). Esses atributos podem ser usados com matrizes de caracteres de caractere largo ou de byte único, assim como seriam com matrizes de outros tipos.

As informações nesta seção descrevem protótipos de parâmetro de procedimento remoto para matrizes de caracteres. Ele é dividido nos seguintes tópicos:

-   [\[in, out, size \_ is \] Prototype](-in-out-size-is-prototype.md)
-   [\[in, size \_ is and out, size \_ is \] Prototype](-in-size-is-and-out-size-is-prototype.md)

 

 