---
title: Cadeias de caracteres MOF
description: Uma cadeia de caracteres é um tipo de dados que contém uma cadeia de caracteres geralmente pretendida como texto legível por humanos.
ms.assetid: 08a07184-6d23-4988-a3de-e5bfc3e177f8
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a1427accbdb3a4dae0240563656785968d4bd075
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827727"
---
# <a name="mof-strings"></a>Cadeias de caracteres MOF

Uma cadeia de caracteres é um tipo de dados que contém uma cadeia de caracteres geralmente pretendida como texto legível por humanos. O MOF descreve dois tipos de cadeias de caracteres, que usam para conter um ou vários. O MOF também tem uma série de regras que descrevem o uso de aspas dentro de uma cadeia de caracteres.

A tabela a seguir lista os tipos de dados de cadeia de caracteres para o MOF.



| Tipo de dados  | Tipo de automação | Descrição                                                                            |
|------------|-----------------|----------------------------------------------------------------------------------------|
| **char16** | **\_I2 VT**      | Caractere Unicode de 16 bits único no formato do conjunto de caracteres universal 2 (UCS-2)<br/> |
| **cadeia de caracteres** | **VT \_ BSTR**    | Cadeia de caracteres Unicode<br/>                                                    |



 

Use as seguintes diretrizes ao gravar cadeias de caracteres para o MOF:

-   Coloque constantes de caractere único entre aspas simples.

    Se você não usar aspas simples com constantes de caractere único, deverá usar a representação de inteiro do valor de caractere Unicode. Opcionalmente, você pode especificar o caractere literalmente com a \\ sequência de escape x do padrão de American National Standards Institute (ANSI) C, conforme mostrado:

    ``` syntax
    char16  TestChar1 = '\x4133';
    char16  Testchar2 = 'A';
    ```

    Como o MOF é baseado em Unicode, você também pode especificar valores de 16 bits.

    Lembre-se de que as constantes de caractere único no formato ANSI C estão entre aspas duplas.

-   Coloque as cadeias de caracteres entre aspas duplas.

    ``` syntax
    DTime    = "19940107140332.000000-300";
    ```

-   Concatenar cadeias de caracteres de aspas sucessivas com um ou mais espaços em branco.

    ``` syntax
    DString = "This" "becomes a long string";
    ```

-   Use uma sequência de escape começando com uma barra invertida para inserir aspas em uma cadeia de caracteres.

    ``` syntax
    DMyString = "This is an \"embedded quote\" example."
    ```

O exemplo a seguir descreve como inicializar propriedades de cadeia de caracteres e um parâmetro de cadeia de caracteres:

``` syntax
class  StringDataClass
{
    [key]  String    Dstring;
    DateTime         DTime;
    char16           CharVal1;
    char16           CharVal2;
    sint32 DiskMethod ([in, Id(0)] string Description = "Disk 1");
};

instance of StringDataClass
{
    Dstring = "this can go on for " " some time"
       " before it is complete";
    DTime    = "19940107140332.000000-300";
    CharVal1 = '\x16';
    CharVal2 = '\x32';
};
```

 

 




