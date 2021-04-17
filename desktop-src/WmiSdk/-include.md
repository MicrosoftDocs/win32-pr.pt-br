---
description: Inclui o conteúdo de um arquivo MOF em outro arquivo MOF.
ms.assetid: 06765956-e4ee-467b-9b3b-d5da17b9cd82
ms.tgt_platform: multiple
title: '#include'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5eb3d203cff5bca7e5096082cca7ba531580ae27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105761153"
---
# <a name="include"></a><span data-ttu-id="39e98-103">' #include '</span><span class="sxs-lookup"><span data-stu-id="39e98-103">'#include'</span></span>
<span data-ttu-id="39e98-104">/\* Título: MyMof. mof                           *//*   title: MyMof2. mof \*/</span><span class="sxs-lookup"><span data-stu-id="39e98-104">/\*   Title: MyMof.Mof                           */ /*   Title: MyMof2.Mof                               \*/</span></span>

<span data-ttu-id="39e98-105">O \# comando incluir pré-processador inclui o conteúdo de um arquivo MOF em outro arquivo MOF.</span><span class="sxs-lookup"><span data-stu-id="39e98-105">The \#include preprocessor command includes the contents of one MOF file into another MOF file.</span></span> <span data-ttu-id="39e98-106">O exemplo de código a seguir descreve a sintaxe para o \# comando include.</span><span class="sxs-lookup"><span data-stu-id="39e98-106">The following code example describes the syntax for the \#include command.</span></span>

``` syntax
#include ("Moffile.mof")
```

<span data-ttu-id="39e98-107">No exemplo anterior, Moffile. mof é o nome do arquivo MOF a ser incluído.</span><span class="sxs-lookup"><span data-stu-id="39e98-107">In the previous example, Moffile.mof is the name of the MOF file to include.</span></span>

<span data-ttu-id="39e98-108">O exemplo a seguir mostra dois arquivos MOF.</span><span class="sxs-lookup"><span data-stu-id="39e98-108">The following example shows two MOF files.</span></span> <span data-ttu-id="39e98-109">Quando você compila o primeiro arquivo MOF, o compilador compila automaticamente o segundo arquivo MOF (Mymof2. MOF) no local em que você coloca a \# instrução include.</span><span class="sxs-lookup"><span data-stu-id="39e98-109">When you compile the first MOF file, the compiler automatically compiles the second MOF file (Mymof2.mof) in the location you place the \#include statement.</span></span>

``` syntax
/*   Title: MyMof.Mof                           */
/*                                              */ 
/*   This MOF file shows how to include  */
/*   an MOF file in another MOF file             */

#pragma namespace("\\\\.\\root")            

#include ("mymof2.mof")

class myclass1 
{
    [key] string Description;
};


instance of myclass1
{
    Description = "Description of myclass1";
};
/*   End of MyMof.Mof                           */
```

<span data-ttu-id="39e98-110">O seguinte arquivo MOF está incluído no exemplo anterior:</span><span class="sxs-lookup"><span data-stu-id="39e98-110">The following MOF file is included in the previous example:</span></span>

``` syntax
/*   Title: MyMof2.Mof                               */
/*                                                   */
/*   This MOF is included when MyMof.MOF is compiled */

class myclass2 
{
    [key] string Description;
};


instance of myclass2
{
    Description = "Description of myclass2";
    
};
```

## <a name="related-topics"></a><span data-ttu-id="39e98-111">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="39e98-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="39e98-112">Comandos de pré-processador</span><span class="sxs-lookup"><span data-stu-id="39e98-112">Preprocessor Commands</span></span>](preprocessor-commands.md)
</dt> </dl>

 

 



