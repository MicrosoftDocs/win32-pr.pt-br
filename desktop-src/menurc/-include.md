---
title: " include"
description: A diretiva \ include faz com que o compilador de recurso processe o arquivo especificado no parâmetro filename.
ms.assetid: 9a3505c6-c19f-4c4f-85a4-94fbcfc0f9c6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a8d36f1d0ae24f3dc21d67eec57056872aabdbd
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104369170"
---
# <a name="-include"></a><span data-ttu-id="69a01-103">incluir</span><span class="sxs-lookup"><span data-stu-id="69a01-103">' include'</span></span>

<span data-ttu-id="69a01-104">A diretiva **\# include** faz com que o compilador de recurso processe o arquivo especificado no parâmetro *filename* .</span><span class="sxs-lookup"><span data-stu-id="69a01-104">The **\#include** directive causes the resource compiler to process the file specified in the *filename* parameter.</span></span> <span data-ttu-id="69a01-105">Esse arquivo deve ser um arquivo de cabeçalho que define as constantes usadas no arquivo de definição de recurso.</span><span class="sxs-lookup"><span data-stu-id="69a01-105">This file should be a header file that defines the constants used in the resource-definition file.</span></span> <span data-ttu-id="69a01-106">O arquivo pode usar caracteres de byte único, dois bytes ou Unicode.</span><span class="sxs-lookup"><span data-stu-id="69a01-106">The file can use single-byte, double-byte, or Unicode characters.</span></span>

``` syntax
#include filename
```

<dl> <dt>

<span data-ttu-id="69a01-107"><span id="filename"></span><span id="FILENAME"></span>*nome do arquivo*</span><span class="sxs-lookup"><span data-stu-id="69a01-107"><span id="filename"></span><span id="FILENAME"></span>*filename*</span></span>
</dt> <dd>

<span data-ttu-id="69a01-108">Nome do arquivo a ser incluído.</span><span class="sxs-lookup"><span data-stu-id="69a01-108">Name of the file to be included.</span></span> <span data-ttu-id="69a01-109">Se o arquivo estiver no diretório atual, a cadeia de caracteres deverá ser colocada entre aspas duplas; Se o arquivo estiver no diretório especificado pela variável de ambiente INCLUDE, a cadeia de caracteres deverá ser colocada entre os caracteres inferior e maior que (<>).</span><span class="sxs-lookup"><span data-stu-id="69a01-109">If the file is in the current directory, the string must be enclosed in double quotation marks; if the file is in the directory specified by the INCLUDE environment variable, the string must be enclosed in less-than and greater-than characters (<>).</span></span> <span data-ttu-id="69a01-110">Você deve fornecer um caminho completo entre aspas duplas (") se o arquivo não estiver no diretório atual ou no diretório especificado pela variável de ambiente INCLUDE.</span><span class="sxs-lookup"><span data-stu-id="69a01-110">You must give a full path enclosed in double quotation marks (") if the file is not in the current directory or in the directory specified by the INCLUDE environment variable.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="69a01-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="69a01-111">Remarks</span></span>

<span data-ttu-id="69a01-112">Use a instrução a seguir no arquivo de cabeçalho para instruções surround que podem ser compiladas por um compilador C, mas não por RC:</span><span class="sxs-lookup"><span data-stu-id="69a01-112">Use the following statement in your header file to surround statements that can be compiled by a C compiler but not RC:</span></span>

``` syntax
#ifndef RC_INVOKED
```

<span data-ttu-id="69a01-113">Dessa forma, você pode usar os mesmos arquivos de inclusão nos arquivos. c e. rc.</span><span class="sxs-lookup"><span data-stu-id="69a01-113">This way, you can use the same include files in your .c and .rc files.</span></span>

## <a name="example"></a><span data-ttu-id="69a01-114">Exemplo</span><span class="sxs-lookup"><span data-stu-id="69a01-114">Example</span></span>

<span data-ttu-id="69a01-115">Este exemplo processa os arquivos de cabeçalho Windows. h e MyDefs. h durante a compilação do arquivo de definição de recurso:</span><span class="sxs-lookup"><span data-stu-id="69a01-115">This example processes the header files Windows.h and MyDefs.h while compiling the resource-definition file:</span></span>

``` syntax
#include <windows.h>
#include "headers\mydefs.h"
```

## <a name="related-topics"></a><span data-ttu-id="69a01-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="69a01-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="69a01-117">Diretivas de pré-processador</span><span class="sxs-lookup"><span data-stu-id="69a01-117">Preprocessor Directives</span></span>](preprocessor-directives.md)
</dt> </dl>

 

 




