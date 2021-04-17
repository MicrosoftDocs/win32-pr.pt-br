---
title: Conversões de tipo de dados
description: Conversões de tipo de dados
ms.assetid: 54688ee9-2dd7-466b-b278-13d6f9d1e6ce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8135a3fb86fda9ac9ab9666ec42991a8d04d9e6
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "105811652"
---
# <a name="data-type-conversions"></a>Conversões de tipo de dados

Cada linguagem de programação define determinados tipos e contêineres para dados. A maioria desses tipos de dados, especialmente os primitivos, é facilmente mapeada para outras linguagens de programação. Alguns tipos de dados, no entanto, não têm nenhum equivalente em outra linguagem e não podem ser convertidos.

Para obter informações específicas sobre os tipos de dados não reconhecidos pela linguagem de programação, consulte os seguintes tópicos:

-   [Convertendo para C++](translating-to-c--.md)
-   [Convertendo para Visual Basic](translating-to-visual-basic.md)
-   [Convertendo para Java](translating-to-java.md)

A tabela a seguir lista as conversões entre linguagens de programação para tipos de dados comuns.



| C++                                     | Visual Basic             | Java                               | Contém                                                                                       |
|-----------------------------------------|--------------------------|------------------------------------|------------------------------------------------------------------------------------------------|
| **signed char**<br/>              | Sem suporte<br/> | **byte**<br/>                | inteiro com sinal de 1 byte <br/> (VT \_ I1, \[ T \] )<br/>                                   |
| **unsigned char**<br/>            | **Byte**<br/>      | Sem suporte<br/>           | inteiro não assinado de 1 byte <br/> (VT \_ UI1, \[ V \] \[ T \] \[ P \] \[ S \] )<br/>                 |
| **unsigned char**<br/>            | **Caractere**<br/> | **char**<br/>                | caractere Unicode de 2 bytes <br/> (VT \_ UI2, \[ T \] \[ P \] )<br/>                          |
| **short**<br/>                    | **Inteiro**<br/>   | **short**<br/>               | inteiro com sinal de 2 bytes <br/> (VT \_ I2, \[ V \] \[ T \] \[ P \] \[ S \] )<br/>                    |
| **unsigned short**<br/>           | Sem suporte<br/> | Sem suporte<br/>           | inteiro sem sinal de 2 bytes <br/> (VT \_ UI2, \[ T \] \[ P \] )<br/>                           |
| **int**<br/>                      | **Long**<br/>      | **int**<br/>                 | inteiro com sinal de 4 bytes <br/> (VT \_ I4, \[ V \] \[ T \] \[ P \] \[ S \] )<br/>                    |
| **unsigned int**<br/>             | Sem suporte<br/> | Sem suporte<br/>           | inteiro sem sinal de 4 bytes <br/> (VT \_ UI4, \[ T \] \[ P \] )<br/>                           |
| **\_\_Int64**<br/>                | Sem suporte<br/> | **longo**<br/>                | inteiro com sinal de 8 bytes <br/> (VT \_ I8, \[ T \] \[ P \] )<br/>                              |
| **Int64 não assinado \_ \_**<br/>       | Sem suporte<br/> | Sem suporte<br/>           | inteiro sem sinal de 8 bytes <br/> (VT \_ UI8, \[ T \] \[ P \] )<br/>                           |
| **float**<br/>                    | **Single**<br/>    | **float**<br/>               | número de ponto flutuante de 4 bytes <br/> (VT \_ R4, \[ V \] \[ T \] \[ P \] \[ S \] )<br/>             |
| **double**<br/>                   | **Double**<br/>    | **double**<br/>              | número de ponto flutuante de 8 bytes <br/> (VT \_ R8, \[ V \] \[ T \] \[ P \] \[ S \] )<br/>             |
| **BSTR**<br/>                     | **Cadeia de caracteres**<br/>    | **Java. lang. String**<br/>    | Cadeia de caracteres de automação <br/> (VT \_ BSTR, \[ V \] \[ T \] \[ P \] \[ S \] )<br/>                      |
| **BOOL**<br/>                     | **Booliano**<br/>   | **booleano**<br/>             | Boolean <br/> (VT \_ BOOL, \[ V \] \[ T \] \[ P \] \[ S \] )<br/>                                |
| **VARIANTE**<br/>                  | **Variante**<br/>   | **com. ms. com. Variant**<br/>  | VARIANTE PARA LONGE\* <br/> (VT \_ VARIANT, \[ V \] \[ T \] \[ P \] \[ S \] )<br/>                       |
| [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown)<br/> | **object**<br/>    | **com. ms. com. IUnknown**<br/> | Ponteiro de interface IDispatch <br/> (VT \_ EXPEDIÇÃO, \[ V \] \[ T \] \[ P \] \[ S \] )<br/>        |
| **DATE**<br/>                     | **Data**<br/>      | **com. ms. com. Variant**<br/>  | Data <br/> (VT \_ Data, \[ V \] \[ T \] \[ P \] \[ S \] )<br/>                                   |
| **CURRENCY**<br/>                 | **Moeda**<br/>  | **com. ms. com. Variant**<br/>  | Moeda <br/> (VT \_ CY, \[ v \] \[ t \] \[ P \] \[ \] ou VT \_ decimal, \[ v \] \[ t \] \[ S \] )<br/> |



 

Para obter informações sobre valores VARTYPE e como usá-los, consulte o tópico [tipos de dados e estruturas de IDispatch](/previous-versions/ms221600(v=vs.100)).

As conversões de tipo de dados entre linguagens de script são mais simples do que aquelas para linguagens de programação. O JScript e o JavaScript oferecem suporte aos mesmos tipos de dados, e o VBScript dá suporte apenas a um único tipo de dados, **Variant**. Assim, todos os tipos de dados JScript e JavaScript se tornam tipos **variantes** quando convertidos em VBScript. Quando você converte VBScript em JScript ou JavaScript, os tipos **variantes** se tornam números, cadeias de caracteres, valores Boolianos e assim por diante.

 

