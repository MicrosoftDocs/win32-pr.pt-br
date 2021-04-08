---
title: Saída do compilador MIDL
description: Com os arquivos IDL e ACF como entrada, o compilador MIDL gera até cinco arquivos de origem em linguagem C.
ms.assetid: 151bd643-1da0-4b33-b8a3-3d7037e63319
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebb45bb369ea9d5faa695bf2658f3bafe2b3cb3d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005152"
---
# <a name="midl-compiler-output"></a><span data-ttu-id="9f07f-103">Saída do compilador MIDL</span><span class="sxs-lookup"><span data-stu-id="9f07f-103">MIDL Compiler Output</span></span>

<span data-ttu-id="9f07f-104">Com os arquivos IDL e ACF como entrada, o compilador MIDL gera até cinco arquivos de origem em linguagem C.</span><span class="sxs-lookup"><span data-stu-id="9f07f-104">With the IDL and ACF files as input, the MIDL compiler generates up to five C-language source files.</span></span> <span data-ttu-id="9f07f-105">Por padrão, o compilador MIDL usa o nome de arquivo base do arquivo IDL como parte dos arquivos stub gerados.</span><span class="sxs-lookup"><span data-stu-id="9f07f-105">By default, the MIDL compiler uses the base file name of the IDL file as part of the generated stub files.</span></span> <span data-ttu-id="9f07f-106">Quando mais de seis caracteres estão presentes no nome do arquivo base, alguns sistemas de arquivos podem não aceitar o nome completo do stub.</span><span class="sxs-lookup"><span data-stu-id="9f07f-106">When more than six characters are present in the base file name, some file systems may not accept the full stub name.</span></span> <span data-ttu-id="9f07f-107">A tabela a seguir mostra as convenções usadas para nomes de arquivo.</span><span class="sxs-lookup"><span data-stu-id="9f07f-107">The following table shows conventions used for file names.</span></span>



| <span data-ttu-id="9f07f-108">Arquivo</span><span class="sxs-lookup"><span data-stu-id="9f07f-108">File</span></span>        | <span data-ttu-id="9f07f-109">Parte padrão do nome do arquivo base</span><span class="sxs-lookup"><span data-stu-id="9f07f-109">Default portion of base file name</span></span> | <span data-ttu-id="9f07f-110">Exemplo</span><span class="sxs-lookup"><span data-stu-id="9f07f-110">Example</span></span>      |
|-------------|-----------------------------------|--------------|
| <span data-ttu-id="9f07f-111">Arquivo IDL</span><span class="sxs-lookup"><span data-stu-id="9f07f-111">IDL file</span></span>    | ---                               | <span data-ttu-id="9f07f-112">Abcdefgh. idl</span><span class="sxs-lookup"><span data-stu-id="9f07f-112">Abcdefgh.idl</span></span> |
| <span data-ttu-id="9f07f-113">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9f07f-113">Header</span></span>      | <span data-ttu-id="9f07f-114">.h</span><span class="sxs-lookup"><span data-stu-id="9f07f-114">.h</span></span>                                | <span data-ttu-id="9f07f-115">Abcdef. h</span><span class="sxs-lookup"><span data-stu-id="9f07f-115">Abcdef.h</span></span>     |
| <span data-ttu-id="9f07f-116">Stub do cliente</span><span class="sxs-lookup"><span data-stu-id="9f07f-116">Client stub</span></span> | <span data-ttu-id="9f07f-117">\_c. c</span><span class="sxs-lookup"><span data-stu-id="9f07f-117">\_c.c</span></span>                             | <span data-ttu-id="9f07f-118">Abcdef \_ c. c</span><span class="sxs-lookup"><span data-stu-id="9f07f-118">Abcdef\_c.c</span></span>  |
| <span data-ttu-id="9f07f-119">Stub de servidor</span><span class="sxs-lookup"><span data-stu-id="9f07f-119">Server stub</span></span> | <span data-ttu-id="9f07f-120">\_s. c</span><span class="sxs-lookup"><span data-stu-id="9f07f-120">\_s.c</span></span>                             | <span data-ttu-id="9f07f-121">Abcdef \_ s. c</span><span class="sxs-lookup"><span data-stu-id="9f07f-121">Abcdef\_s.c</span></span>  |



 

 

 




