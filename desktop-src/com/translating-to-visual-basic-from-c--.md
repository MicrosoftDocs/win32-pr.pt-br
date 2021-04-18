---
title: Convertendo para Visual Basic do C++
description: Convertendo para Visual Basic do C++
ms.assetid: fce7ea25-cb24-4cc4-8f36-0e8aed2f3ada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffba519cbdb0305fe3a2eae4cc8e658fdde1eac3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105750347"
---
# <a name="translating-to-visual-basic-from-c"></a>Convertendo para Visual Basic do C++

Usando a linguagem de programação C++, os desenvolvedores podem acessar diretamente a memória que armazena uma variável específica. Os ponteiros de memória fornecem esse acesso direto. No Visual Basic, os ponteiros são tratados para você. Por exemplo, um parâmetro declarado como um ponteiro para um **int** em C++ é equivalente a um parâmetro declarado em Visual Basic como um  **inteiro** ByRef.

Um parâmetro declarado **como cadeia de caracteres** em Visual Basic é declarado como um ponteiro para um **BSTR** em C++. Definir um ponteiro de cadeia de caracteres como **nulo** em C++ é equivalente a definir a cadeia de caracteres para a constante **vbNullString** em Visual Basic. A passagem de uma cadeia de caracteres de comprimento zero ("") para uma função criada para receber **NULL** não funciona, pois isso passa um ponteiro para uma cadeia de caracteres de comprimento zero em vez de um ponteiro zero.

O C++ dá suporte a contêineres de dados, estruturas e uniões, que não têm equivalente em versões anteriores do Visual Basic. Por esse motivo, os objetos COM normalmente encapsulam informações que geralmente são armazenadas em estruturas e uniões em classes de objetos. No entanto, alguns objetos COM podem conter estruturas, fazendo com que partes dos métodos ou funcionalidades do objeto fiquem inacessíveis para Visual Basic.

Alguns tipos de dados C++ não têm suporte em Visual Basic, por exemplo, tipos não assinados e tipos de **HWND** . Os métodos que aceitam ou retornam esses tipos de dados não estão disponíveis no Visual Basic.

Visual Basic usa tipos de dados compatíveis com a automação como seus tipos de dados internos. Portanto, os tipos de dados do C++ que são compatíveis com a automação também são compatíveis com Visual Basic. Os tipos de dados que não são compatíveis com a automação talvez não possam ser convertidos em Visual Basic.

A tabela a seguir lista os tipos de dados com suporte pelo Visual Basic e seus equivalentes **VarType** . **VarType** é uma enumeração que lista os tipos de variantes de automação.



| Tipo de dados do Visual Basic  | Devartyper equivalente                |
|-------------------------|-----------------------------------|
| **Inteiro**<br/>  | 16 bits, assinado, VT \_ i2<br/> |
| **Long**<br/>     | 32 bits, assinado, VT \_ i4<br/> |
| **Data**<br/>     | Data de VT \_<br/>               |
| **Moeda**<br/> | VT \_ Cy<br/>                 |
| **Objeto**<br/>   | \*expedição de VT \_<br/>         |
| **Cadeia de caracteres**<br/>   | VT \_ BSTR<br/>               |
| **Booliano**<br/>  | BOOL do VT \_<br/>               |
| **Moeda**<br/> | \_decimal VT<br/>            |
| **Single**<br/>   | VT \_ R4<br/>                 |
| **Double**<br/>   | R8 de VT \_<br/>                 |
| **Decimal**<br/>  | \_decimal VT<br/>            |
| **Byte**<br/>     | \_decimal VT<br/>            |
| **Variante**<br/>  | variante do VT \_<br/>            |



 

Todos os parâmetros em Visual Basic, a menos que rotulado com a palavra-chave **ByVal**, sejam passados por referência (como ponteiros) em vez de por valor.

C++ e Visual Basic diferem ligeiramente na forma como representam propriedades. No C++, as propriedades são representadas como um conjunto de funções de acessador, uma que define o valor da propriedade e outra que recupera o valor da propriedade. Em Visual Basic, as propriedades são representadas como um único item que pode ser usado para recuperar ou definir o valor da propriedade.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Convertendo para Visual Basic](translating-to-visual-basic.md)
</dt> </dl>

 

 





