---
title: Convertendo para C++ de Visual Basic
description: Visual Basic manipula ponteiros implicitamente. Em C++, seu aplicativo é responsável por executar qualquer aritmética de ponteiro necessária.
ms.assetid: bbbcaba1-cf5a-4768-ad1d-22a040bfe384
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53de112f19b51be92657fb3293bb35e1d41ff9b7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159771"
---
# <a name="translating-to-c-from-visual-basic"></a>Convertendo para C++ de Visual Basic

Visual Basic manipula ponteiros implicitamente. Em C++, seu aplicativo é responsável por executar qualquer aritmética de ponteiro necessária.

Por padrão, Visual Basic passa parâmetros por referência (como ponteiros). Parâmetros que devem ser passados pelo valor somente são especificados pela palavra-chave **ByVal**. Por exemplo, um parâmetro  **inteiro** **ByVal** Â em Visual Basic é equivalente a um parâmetro **curto** em C++, enquanto um parâmetro de  **inteiro** **ByRef** em Visual Basic é equivalente a um **parâmetro \* curto** .

Um parâmetro declarado **como cadeia de caracteres** em Visual Basic é declarado como um ponteiro para um **BSTR** em C++. Definir um ponteiro de cadeia de caracteres como **nulo** em C++ é equivalente a definir a cadeia de caracteres para a constante **vbNullString** em Visual Basic. A passagem de uma cadeia de caracteres de comprimento zero ("") para uma função criada para receber **NULL** não funciona, porque isso passa um ponteiro para uma cadeia de caracteres de comprimento zero em vez de um ponteiro de zero.

C++ e Visual Basic diferem ligeiramente na forma como representam propriedades. No C++, as propriedades são representadas como um conjunto de funções de acessador, uma que define o valor da propriedade e outra que recupera o valor da propriedade. Em Visual Basic, as propriedades são representadas como um único item que pode ser usado para recuperar ou definir o valor da propriedade.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Convertendo para C++](translating-to-c--.md)
</dt> </dl>

 

 




