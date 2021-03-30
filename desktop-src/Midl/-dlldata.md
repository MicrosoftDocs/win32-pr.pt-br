---
title: comutador/dlldata nomedearquivo
description: A opção/dlldata nomedearquivo é usada para especificar o nome do arquivo dlldata gerado para uma DLL de proxy. O nome de arquivo padrão dlldata. c será usado se a opção/dlldata nomedearquivo não for especificada.
ms.assetid: 5211498b-c641-447f-9514-a98766e26ea9
keywords:
- MIDL do comutador/dlldata nomedearquivo
topic_type:
- apiref
api_name:
- /dlldata
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0e9c1d7f27c56f81905081fd9ef24c8c490391b
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103638632"
---
# <a name="dlldata-switch"></a><span data-ttu-id="66a8f-105">comutador/dlldata nomedearquivo</span><span class="sxs-lookup"><span data-stu-id="66a8f-105">/dlldata switch</span></span>

<span data-ttu-id="66a8f-106">A opção **/dlldata nomedearquivo** é usada para especificar o nome do arquivo dlldata gerado para uma DLL de proxy.</span><span class="sxs-lookup"><span data-stu-id="66a8f-106">The **/dlldata** switch is used to specify the file name for the generated dlldata file for a proxy DLL.</span></span> <span data-ttu-id="66a8f-107">O nome de arquivo padrão dlldata. c será usado se a opção **/dlldata nomedearquivo** não for especificada.</span><span class="sxs-lookup"><span data-stu-id="66a8f-107">The default file name Dlldata.c is used if the **/dlldata** switch is not specified.</span></span>

``` syntax
midl /dlldata file-name
```

## <a name="switch-options"></a><span data-ttu-id="66a8f-108">Opções de comutação</span><span class="sxs-lookup"><span data-stu-id="66a8f-108">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="66a8f-109">*nome do arquivo*</span><span class="sxs-lookup"><span data-stu-id="66a8f-109">*file-name*</span></span> 
</dt> <dd>

<span data-ttu-id="66a8f-110">O nome do arquivo de origem C que o compilador MIDL irá gerar para a DLL de proxy.</span><span class="sxs-lookup"><span data-stu-id="66a8f-110">The name of the C source file the MIDL compiler will generate for the proxy DLL.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="66a8f-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="66a8f-111">Remarks</span></span>

<span data-ttu-id="66a8f-112">O arquivo especificado por *nome de arquivo* deve ser vinculado à dll de proxy.</span><span class="sxs-lookup"><span data-stu-id="66a8f-112">The file specified by *file-name* must be linked to the proxy DLL.</span></span> <span data-ttu-id="66a8f-113">O arquivo dlldata contém pontos de entrada e estruturas de dados exigidos pela fábrica de classes para a DLL de proxy.</span><span class="sxs-lookup"><span data-stu-id="66a8f-113">The dlldata file contains entry points and data structures required by the class factory for the proxy DLL.</span></span> <span data-ttu-id="66a8f-114">Essas estruturas de dados especificam as interfaces de objeto contidas na DLL de proxy.</span><span class="sxs-lookup"><span data-stu-id="66a8f-114">These data structures specify the object interfaces contained in the proxy DLL.</span></span> <span data-ttu-id="66a8f-115">O arquivo dlldata também especifica o identificador de classe da fábrica de classes para a DLL de proxy.</span><span class="sxs-lookup"><span data-stu-id="66a8f-115">The dlldata file also specifies the class identifier of the class factory for the proxy DLL.</span></span> <span data-ttu-id="66a8f-116">Esse é sempre o UUID (IID) da primeira interface do primeiro arquivo de proxy (por ordem alfabética).</span><span class="sxs-lookup"><span data-stu-id="66a8f-116">This is always the UUID (IID) of the first interface of the first proxy file (by alphabetical order).</span></span>

<span data-ttu-id="66a8f-117">O mesmo arquivo dlldata deve ser especificado ao invocar MIDL em todos os arquivos IDL que entrarão em uma DLL de proxy específica.</span><span class="sxs-lookup"><span data-stu-id="66a8f-117">The same dlldata file should be specified when invoking MIDL on all the IDL files that will go into a particular proxy DLL.</span></span> <span data-ttu-id="66a8f-118">O arquivo dlldata é criado ou atualizado durante cada compilação de MIDL, criando incrementalmente uma lista das interfaces que entrarão na DLL de proxy.</span><span class="sxs-lookup"><span data-stu-id="66a8f-118">The dlldata file is created or updated during each MIDL compilation, incrementally building a list of the interfaces that will go into the proxy DLL.</span></span>

## <a name="examples"></a><span data-ttu-id="66a8f-119">Exemplos</span><span class="sxs-lookup"><span data-stu-id="66a8f-119">Examples</span></span>

<span data-ttu-id="66a8f-120">**MIDL/dlldata nomedearquivo Data. c**</span><span class="sxs-lookup"><span data-stu-id="66a8f-120">**midl /dlldata data.c**</span></span>

## <a name="see-also"></a><span data-ttu-id="66a8f-121">Consulte também</span><span class="sxs-lookup"><span data-stu-id="66a8f-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66a8f-122">Sintaxe de linha de comando MIDL geral</span><span class="sxs-lookup"><span data-stu-id="66a8f-122">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> </dl>

 

 




