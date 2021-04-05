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
# <a name="mof-strings"></a><span data-ttu-id="dbb71-103">Cadeias de caracteres MOF</span><span class="sxs-lookup"><span data-stu-id="dbb71-103">MOF strings</span></span>

<span data-ttu-id="dbb71-104">Uma cadeia de caracteres é um tipo de dados que contém uma cadeia de caracteres geralmente pretendida como texto legível por humanos.</span><span class="sxs-lookup"><span data-stu-id="dbb71-104">A string is a data type that contains a string of characters usually intended as human-readable text.</span></span> <span data-ttu-id="dbb71-105">O MOF descreve dois tipos de cadeias de caracteres, que usam para conter um ou vários.</span><span class="sxs-lookup"><span data-stu-id="dbb71-105">MOF describes two types of strings, which use to hold single or multiple characters.</span></span> <span data-ttu-id="dbb71-106">O MOF também tem uma série de regras que descrevem o uso de aspas dentro de uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="dbb71-106">MOF also has a series of rules describing the use of quotes within a string.</span></span>

<span data-ttu-id="dbb71-107">A tabela a seguir lista os tipos de dados de cadeia de caracteres para o MOF.</span><span class="sxs-lookup"><span data-stu-id="dbb71-107">The following table lists the string data types for MOF.</span></span>



| <span data-ttu-id="dbb71-108">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="dbb71-108">Data type</span></span>  | <span data-ttu-id="dbb71-109">Tipo de automação</span><span class="sxs-lookup"><span data-stu-id="dbb71-109">Automation type</span></span> | <span data-ttu-id="dbb71-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="dbb71-110">Description</span></span>                                                                            |
|------------|-----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="dbb71-111">**char16**</span><span class="sxs-lookup"><span data-stu-id="dbb71-111">**char16**</span></span> | <span data-ttu-id="dbb71-112">**\_I2 VT**</span><span class="sxs-lookup"><span data-stu-id="dbb71-112">**VT\_I2**</span></span>      | <span data-ttu-id="dbb71-113">Caractere Unicode de 16 bits único no formato do conjunto de caracteres universal 2 (UCS-2)</span><span class="sxs-lookup"><span data-stu-id="dbb71-113">Single 16-bit Unicode character in Universal Character Set 2 (UCS-2) format</span></span><br/> |
| <span data-ttu-id="dbb71-114">**cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="dbb71-114">**string**</span></span> | <span data-ttu-id="dbb71-115">**VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="dbb71-115">**VT\_BSTR**</span></span>    | <span data-ttu-id="dbb71-116">Cadeia de caracteres Unicode</span><span class="sxs-lookup"><span data-stu-id="dbb71-116">Unicode character string</span></span><br/>                                                    |



 

<span data-ttu-id="dbb71-117">Use as seguintes diretrizes ao gravar cadeias de caracteres para o MOF:</span><span class="sxs-lookup"><span data-stu-id="dbb71-117">Use the following guidelines when writing strings for MOF:</span></span>

-   <span data-ttu-id="dbb71-118">Coloque constantes de caractere único entre aspas simples.</span><span class="sxs-lookup"><span data-stu-id="dbb71-118">Surround single-character constants with single quotes.</span></span>

    <span data-ttu-id="dbb71-119">Se você não usar aspas simples com constantes de caractere único, deverá usar a representação de inteiro do valor de caractere Unicode.</span><span class="sxs-lookup"><span data-stu-id="dbb71-119">If you do not use single quotes with single character constants, you must use the integer representation of the Unicode character value.</span></span> <span data-ttu-id="dbb71-120">Opcionalmente, você pode especificar o caractere literalmente com a \\ sequência de escape x do padrão de American National Standards Institute (ANSI) C, conforme mostrado:</span><span class="sxs-lookup"><span data-stu-id="dbb71-120">Optionally, you could specify the character literally with the \\x escape sequence from the American National Standards Institute (ANSI) C standard, as shown:</span></span>

    ``` syntax
    char16  TestChar1 = '\x4133';
    char16  Testchar2 = 'A';
    ```

    <span data-ttu-id="dbb71-121">Como o MOF é baseado em Unicode, você também pode especificar valores de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="dbb71-121">Because MOF is based on Unicode, you can also specify 16-bit values.</span></span>

    <span data-ttu-id="dbb71-122">Lembre-se de que as constantes de caractere único no formato ANSI C estão entre aspas duplas.</span><span class="sxs-lookup"><span data-stu-id="dbb71-122">Be aware that single-character constants in ANSI C format are surrounded by double quotes.</span></span>

-   <span data-ttu-id="dbb71-123">Coloque as cadeias de caracteres entre aspas duplas.</span><span class="sxs-lookup"><span data-stu-id="dbb71-123">Surround character strings with double quotes.</span></span>

    ``` syntax
    DTime    = "19940107140332.000000-300";
    ```

-   <span data-ttu-id="dbb71-124">Concatenar cadeias de caracteres de aspas sucessivas com um ou mais espaços em branco.</span><span class="sxs-lookup"><span data-stu-id="dbb71-124">Concatenate successive quote strings with one or more white spaces.</span></span>

    ``` syntax
    DString = "This" "becomes a long string";
    ```

-   <span data-ttu-id="dbb71-125">Use uma sequência de escape começando com uma barra invertida para inserir aspas em uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="dbb71-125">Use an escape sequence beginning with a backslash to embed quotes into a string.</span></span>

    ``` syntax
    DMyString = "This is an \"embedded quote\" example."
    ```

<span data-ttu-id="dbb71-126">O exemplo a seguir descreve como inicializar propriedades de cadeia de caracteres e um parâmetro de cadeia de caracteres:</span><span class="sxs-lookup"><span data-stu-id="dbb71-126">The following example describes how to initialize string properties and a string parameter:</span></span>

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

 

 




