---
title: Convertendo para Java do C++
description: Usando a linguagem de programação C++, os desenvolvedores podem acessar diretamente a memória que armazena uma variável específica. Os ponteiros de memória fornecem esse acesso direto. No Java, os ponteiros são tratados para você.
ms.assetid: 2c8de3d9-3410-4153-b612-4afab8a69a18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73efe022fa09ce13a2d5e4e04978033fc3ab8f33abb6afb3b5abf493dab12178
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047744"
---
# <a name="translating-to-java-from-c"></a>Convertendo para Java do C++

Usando a linguagem de programação C++, os desenvolvedores podem acessar diretamente a memória que armazena uma variável específica. Os ponteiros de memória fornecem esse acesso direto. No Java, os ponteiros são tratados para você.

Nos tipos de dados de composição Java, **struct**, **Union** e **typedef** são tratados exclusivamente pelo uso de classes. Por exemplo, o tipo de dados **variante** do C++ é mapeado para **com. ms. com. Variant** em Java.

Em C++, Strings são uma matriz de caracteres. No Java, cadeias de caracteres são objetos. Os métodos que atuam em cadeias de caracteres tratam a cadeia como um objeto completo.

Os métodos COM retornam um valor conhecido como **HRESULT**, que é um código de erro de 32 bits. O suporte Java para o Microsoft Internet Explorer define uma classe, **com. ms. com. COMException**, que encapsula o código de erro **HRESULT** .

O Java não oferece suporte a tipos de dados não assinados, exceto **Char**, que é um inteiro sem sinal de 16 bits. Os métodos que aceitam ou retornam outros tipos de dados não assinados não podem ser usados no Java.

O Java não oferece suporte a matrizes multidimensionais. Métodos que aceitam ou retornam matrizes multidimensionais não estão disponíveis no Java.

Valores Boolianos em Java não podem ser convertidos em 0 e 1.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Convertendo para Java](translating-to-java.md)
</dt> </dl>

 

 




