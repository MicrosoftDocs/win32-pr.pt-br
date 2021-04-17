---
description: É semelhante a uma opção de linha de comando. No entanto, você não precisa inserir novamente um \# comando pragma sempre que compilar um arquivo MOF.
ms.assetid: 3cf22686-dd56-43a3-9584-3d707a20a3a0
ms.tgt_platform: multiple
title: '#pragma'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62ae13d5f960e0b415f34dce97a40cff6cba8056
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105813441"
---
# <a name="pragma"></a><span data-ttu-id="53938-104">\#pragma</span><span class="sxs-lookup"><span data-stu-id="53938-104">\#pragma</span></span>

<span data-ttu-id="53938-105">O comando de pré-processador de **\# pragma** é semelhante a uma opção de linha de comando.</span><span class="sxs-lookup"><span data-stu-id="53938-105">The **\#pragma** preprocessor command is similar to a command-line switch.</span></span> <span data-ttu-id="53938-106">No entanto, você não precisa inserir novamente um comando **\# pragma** sempre que COMPILAR um arquivo MOF.</span><span class="sxs-lookup"><span data-stu-id="53938-106">However, you do not need to reenter a **\#pragma** command each time you compile a MOF file.</span></span> <span data-ttu-id="53938-107">O exemplo a seguir ilustra a sintaxe do comando **\# pragma** :</span><span class="sxs-lookup"><span data-stu-id="53938-107">The following example illustrates **\#pragma** command syntax:</span></span>


```mof
#pragma [command]
```



<span data-ttu-id="53938-108">Normalmente, você coloca um comando **\# pragma** no início de um arquivo MOF.</span><span class="sxs-lookup"><span data-stu-id="53938-108">You usually place a **\#pragma** command at the beginning of a MOF file.</span></span> <span data-ttu-id="53938-109">No entanto, você pode inserir alguns comandos, como o comando **\# pragma** , no corpo do código MOF.</span><span class="sxs-lookup"><span data-stu-id="53938-109">However, you can place some commands, such as the **\#pragma** command, in the body of your MOF code.</span></span> <span data-ttu-id="53938-110">O exemplo a seguir mostra os comandos **\# pragma** que indicam ao compilador MOF que ele deve posicionar classes e instâncias no \\ namespace raiz cimv2 e compilar o arquivo no qual os comandos são incluídos durante a recuperação do repositório:</span><span class="sxs-lookup"><span data-stu-id="53938-110">The following example shows **\#pragma** commands that indicate to the MOF compiler that it must place classes and instances in the root\\cimv2 namespace and compile the file in which the commands are included during repository recovery:</span></span>


```mof
#pragma autorecover
#pragma namespace ("\\\\.\\root\\cimv2")
```



<span data-ttu-id="53938-111">O seguinte lista os comandos de **\# pragma** disponíveis.</span><span class="sxs-lookup"><span data-stu-id="53938-111">The following lists the available **\#pragma** commands.</span></span>



| <span data-ttu-id="53938-112">Comando</span><span class="sxs-lookup"><span data-stu-id="53938-112">Command</span></span>                                         | <span data-ttu-id="53938-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="53938-113">Description</span></span>                                                                                           |
|-------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="53938-114">**aditamento**</span><span class="sxs-lookup"><span data-stu-id="53938-114">**amendment**</span></span>](pragma-amendment.md)           | <span data-ttu-id="53938-115">Direciona o compilador MOF para separar um arquivo MOF em versões de idioma neutros e específicas de idiomas.</span><span class="sxs-lookup"><span data-stu-id="53938-115">Directs the MOF compiler to separate a MOF file into language-neutral and language-specific versions.</span></span> |
| [<span data-ttu-id="53938-116">**AutoRecuperação**</span><span class="sxs-lookup"><span data-stu-id="53938-116">**autorecover**</span></span>](pragma-autorecover.md)       | <span data-ttu-id="53938-117">Adiciona um arquivo MOF à lista de arquivos compilados durante a recuperação do repositório.</span><span class="sxs-lookup"><span data-stu-id="53938-117">Adds a MOF file to the list of files compiled during repository recovery.</span></span>                             |
| [<span data-ttu-id="53938-118">**classflags**</span><span class="sxs-lookup"><span data-stu-id="53938-118">**classflags**</span></span>](pragma-classflags.md)         | <span data-ttu-id="53938-119">Controla a maneira como as classes são criadas ou atualizadas dependendo dos sinalizadores especificados.</span><span class="sxs-lookup"><span data-stu-id="53938-119">Controls the way classes are created or updated depending on the flags specified.</span></span>                     |
| [<span data-ttu-id="53938-120">**deleteclass**</span><span class="sxs-lookup"><span data-stu-id="53938-120">**deleteclass**</span></span>](pragma-deleteclass.md)       | <span data-ttu-id="53938-121">Exclui uma classe existente e suas instâncias do repositório.</span><span class="sxs-lookup"><span data-stu-id="53938-121">Deletes an existing class and its instances from the repository.</span></span>                                      |
| [<span data-ttu-id="53938-122">**deleteinstance**</span><span class="sxs-lookup"><span data-stu-id="53938-122">**deleteinstance**</span></span>](pragma-deleteinstance.md) | <span data-ttu-id="53938-123">Exclui uma instância existente de uma classe do repositório.</span><span class="sxs-lookup"><span data-stu-id="53938-123">Deletes an existing instance of a class from the repository.</span></span>                                          |
| [<span data-ttu-id="53938-124">**instanceflags**</span><span class="sxs-lookup"><span data-stu-id="53938-124">**instanceflags**</span></span>](pragma-instanceflags.md)   | <span data-ttu-id="53938-125">Controla a maneira como as instâncias são criadas ou atualizadas dependendo dos sinalizadores especificados.</span><span class="sxs-lookup"><span data-stu-id="53938-125">Controls the way instances are created or updated depending on the flags specified.</span></span>                   |
| [<span data-ttu-id="53938-126">**namespace**</span><span class="sxs-lookup"><span data-stu-id="53938-126">**namespace**</span></span>](pragma-namespace.md)           | <span data-ttu-id="53938-127">Solicita que o compilador carregue o arquivo MOF no namespace especificado como *NamespacePath*.</span><span class="sxs-lookup"><span data-stu-id="53938-127">Requests that the compiler load the MOF file into the namespace specified as *namespacepath*.</span></span>         |



 

## <a name="related-topics"></a><span data-ttu-id="53938-128">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="53938-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="53938-129">Comandos de pré-processador</span><span class="sxs-lookup"><span data-stu-id="53938-129">Preprocessor Commands</span></span>](preprocessor-commands.md)
</dt> </dl>

 

 



