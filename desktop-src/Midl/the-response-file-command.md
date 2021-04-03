---
title: O comando arquivo de resposta
description: Um arquivo de resposta é um arquivo de texto que contém uma ou mais opções de linha de comando do compilador MIDL.
ms.assetid: ad47ea1a-fe7a-4354-be2f-599ba77685ee
keywords:
- referência de linha de comando MIDL, comando Response File
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f624f8bb4fd50fa77df604e5d56f48c9e55c89a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916520"
---
# <a name="the-response-file-command"></a><span data-ttu-id="ab6cc-104">O comando arquivo de resposta</span><span class="sxs-lookup"><span data-stu-id="ab6cc-104">The Response File Command</span></span>

<span data-ttu-id="ab6cc-105">Um arquivo de resposta é um arquivo de texto que contém uma ou mais opções de linha de comando do compilador MIDL.</span><span class="sxs-lookup"><span data-stu-id="ab6cc-105">A response file is a text file containing one or more MIDL compiler command-line options.</span></span> <span data-ttu-id="ab6cc-106">Ao contrário de uma linha de comando, um arquivo de resposta permite várias linhas de opções e nomes de arquivo.</span><span class="sxs-lookup"><span data-stu-id="ab6cc-106">Unlike a command line, a response file allows multiple lines of options and file names.</span></span> <span data-ttu-id="ab6cc-107">Isso pode ser útil devido a limitações do seu ambiente de compilação ou como uma conveniência para o processo de compilação.</span><span class="sxs-lookup"><span data-stu-id="ab6cc-107">This may be useful due to limitations of your build environment, or as a convenience for your build process.</span></span>

## <a name="switch-options"></a><span data-ttu-id="ab6cc-108">Opções de comutação</span><span class="sxs-lookup"><span data-stu-id="ab6cc-108">Switch Options</span></span>

``` syntax
midl @response_file
```

<dl> <dt>

<span data-ttu-id="ab6cc-109"><span id="response_file"></span><span id="RESPONSE_FILE"></span>*arquivo de resposta \_*</span><span class="sxs-lookup"><span data-stu-id="ab6cc-109"><span id="response_file"></span><span id="RESPONSE_FILE"></span>*response\_file*</span></span>
</dt> <dd>

<span data-ttu-id="ab6cc-110">Especifica o nome de um arquivo de resposta.</span><span class="sxs-lookup"><span data-stu-id="ab6cc-110">Specifies the name of a response file.</span></span> <span data-ttu-id="ab6cc-111">O nome do arquivo de resposta deve seguir imediatamente o caractere @.</span><span class="sxs-lookup"><span data-stu-id="ab6cc-111">The response file name must immediately follow the @ character.</span></span> <span data-ttu-id="ab6cc-112">Nenhum espaço em branco é permitido entre o caractere @ e o nome do arquivo de resposta.</span><span class="sxs-lookup"><span data-stu-id="ab6cc-112">No white space is allowed between the @ character and the response file name.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ab6cc-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="ab6cc-113">Remarks</span></span>

<span data-ttu-id="ab6cc-114">Como uma alternativa para colocar todas as opções associadas a uma opção na linha de comando, o compilador MIDL aceita arquivos de resposta que contêm opções e argumentos.</span><span class="sxs-lookup"><span data-stu-id="ab6cc-114">As an alternative to placing all options associated with a switch on the command line, the MIDL compiler accepts response files that contain switches and arguments.</span></span> <span data-ttu-id="ab6cc-115">As opções em um arquivo de resposta são interpretadas como se elas estivessem presentes nesse local na linha de comando MIDL.</span><span class="sxs-lookup"><span data-stu-id="ab6cc-115">Options in a response file are interpreted as if they are present in that location in the MIDL command line.</span></span>

<span data-ttu-id="ab6cc-116">Cada argumento em um arquivo de resposta deve começar e terminar na mesma linha.</span><span class="sxs-lookup"><span data-stu-id="ab6cc-116">Each argument in a response file must begin and end on the same line.</span></span> <span data-ttu-id="ab6cc-117">O caractere de barra invertida ( \) não pode ser usado para concatenar linhas.</span><span class="sxs-lookup"><span data-stu-id="ab6cc-117">The backslash character (\) cannot be used to concatenate lines.</span></span> <span data-ttu-id="ab6cc-118">Quando ele faz parte de uma cadeia de caracteres entre aspas no arquivo de resposta, o caractere de barra invertida só pode ser usado antes de outra barra invertida ou antes de um caractere de aspas duplas (").</span><span class="sxs-lookup"><span data-stu-id="ab6cc-118">When it is part of a quoted string in the response file, the backslash character can only be used before another backslash or before a double quotation mark character (").</span></span> <span data-ttu-id="ab6cc-119">Quando não faz parte de uma cadeia de caracteres entre aspas, o caractere de barra invertida só pode ser usado antes de um caractere de aspas duplas.</span><span class="sxs-lookup"><span data-stu-id="ab6cc-119">When it is not part of a quoted string, the backslash character can only be used before a double quotation mark character.</span></span>

<span data-ttu-id="ab6cc-120">O MIDL dá suporte a argumentos de linha de comando que incluem um ou mais arquivos de resposta combinados com outras opções de linha de comando.</span><span class="sxs-lookup"><span data-stu-id="ab6cc-120">MIDL supports command-line arguments that include one or more response files combined with other command-line switches.</span></span>

<span data-ttu-id="ab6cc-121">O compilador MIDL não oferece suporte a arquivos de resposta aninhados.</span><span class="sxs-lookup"><span data-stu-id="ab6cc-121">The MIDL compiler does not support nested response files.</span></span>

## <a name="examples"></a><span data-ttu-id="ab6cc-122">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ab6cc-122">Examples</span></span>

<span data-ttu-id="ab6cc-123">**MIDL @midl.rsp**</span><span class="sxs-lookup"><span data-stu-id="ab6cc-123">**midl @midl.rsp**</span></span>

<span data-ttu-id="ab6cc-124">**MIDL-Oicf @midl1.rsp -env Win32 @midl2.rsp ITF. idl**</span><span class="sxs-lookup"><span data-stu-id="ab6cc-124">**midl -Oicf @midl1.rsp -env win32 @midl2.rsp itf.idl**</span></span>

## <a name="related-topics"></a><span data-ttu-id="ab6cc-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ab6cc-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ab6cc-126">Sintaxe de linha de comando MIDL geral</span><span class="sxs-lookup"><span data-stu-id="ab6cc-126">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> </dl>

 

 




