---
title: Sobre arquivos de recurso
description: Descreve como incluir recursos em seu aplicativo baseado no Windows com o RC.
ms.assetid: af7c7aed-5d28-40ac-ad00-da0986fd89c1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c43e9df59cf0b6507b6c6a53c42299b8792634f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005523"
---
# <a name="about-resource-files"></a><span data-ttu-id="80777-103">Sobre arquivos de recurso</span><span class="sxs-lookup"><span data-stu-id="80777-103">About Resource Files</span></span>

<span data-ttu-id="80777-104">Para incluir recursos em seu aplicativo baseado no Windows com o RC, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="80777-104">To include resources in your Windows-based application with RC, do the following:</span></span>

1.  <span data-ttu-id="80777-105">Crie arquivos individuais para seus cursores, ícones, bitmaps, caixas de diálogo e fontes.</span><span class="sxs-lookup"><span data-stu-id="80777-105">Create individual files for your cursors, icons, bitmaps, dialog boxes, and fonts.</span></span>
2.  <span data-ttu-id="80777-106">Crie um script de definição de recurso (arquivo. rc) que descreve os recursos usados pelo seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="80777-106">Create a resource-definition script (.rc file) that describes the resources used by your application.</span></span>
3.  <span data-ttu-id="80777-107">Compile o script com o RC.</span><span class="sxs-lookup"><span data-stu-id="80777-107">Compile the script with RC.</span></span> <span data-ttu-id="80777-108">Para obter mais informações, consulte [usando o RC (a linha de comando RC)](using-rc-the-rc-command-line-.md).</span><span class="sxs-lookup"><span data-stu-id="80777-108">For more information, see [Using RC (The RC Command Line)](using-rc-the-rc-command-line-.md).</span></span>
4.  <span data-ttu-id="80777-109">Vincule o arquivo de recurso compilado (. res) no arquivo executável do aplicativo com o vinculador.</span><span class="sxs-lookup"><span data-stu-id="80777-109">Link the compiled resource (.res) file into the application's executable file with your linker.</span></span>

<span data-ttu-id="80777-110">Um arquivo de recurso é um arquivo de texto com a extensão. rc.</span><span class="sxs-lookup"><span data-stu-id="80777-110">A resource file is a text file with the extension .rc.</span></span> <span data-ttu-id="80777-111">O arquivo pode usar caracteres de byte único, dois bytes ou Unicode.</span><span class="sxs-lookup"><span data-stu-id="80777-111">The file can use single-byte, double-byte, or Unicode characters.</span></span> <span data-ttu-id="80777-112">A sintaxe e a semântica do pré-processador do RC são semelhantes às do compilador do Microsoft C/C++.</span><span class="sxs-lookup"><span data-stu-id="80777-112">The syntax and semantics for the RC preprocessor are similar to those of the Microsoft C/C++ compiler.</span></span> <span data-ttu-id="80777-113">No entanto, o RC dá suporte a um subconjunto de diretivas de pré-processador, define e pragmas em um script.</span><span class="sxs-lookup"><span data-stu-id="80777-113">However, RC supports a subset of the preprocessor directives, defines, and pragmas in a script.</span></span>

<span data-ttu-id="80777-114">O arquivo de script define os recursos.</span><span class="sxs-lookup"><span data-stu-id="80777-114">The script file defines resources.</span></span> <span data-ttu-id="80777-115">Para um recurso que existe em um arquivo separado, como um ícone ou cursor, o script especifica o recurso e o arquivo que o contém.</span><span class="sxs-lookup"><span data-stu-id="80777-115">For a resource that exists in a separate file, such as an icon or cursor, the script specifies the resource and the file that contains it.</span></span> <span data-ttu-id="80777-116">Para alguns recursos, como um menu, toda a definição do recurso existe no script.</span><span class="sxs-lookup"><span data-stu-id="80777-116">For some resources, such as a menu, the entire definition of the resource exists within the script.</span></span>

<span data-ttu-id="80777-117">Os tópicos a seguir descrevem as informações que um arquivo de script pode conter:</span><span class="sxs-lookup"><span data-stu-id="80777-117">The following topics describe the information a script file can contain:</span></span>

-   <span data-ttu-id="80777-118">[Comentários](comments.md), que são observações a serem ignoradas pelo RC.</span><span class="sxs-lookup"><span data-stu-id="80777-118">[Comments](comments.md), which are notes to be ignored by RC.</span></span>
-   <span data-ttu-id="80777-119">[Macros predefinidas](predefined-macros.md), que não usam argumentos e não podem ser redefinidas.</span><span class="sxs-lookup"><span data-stu-id="80777-119">[Predefined macros](predefined-macros.md), which take no arguments and cannot be redefined.</span></span>
-   <span data-ttu-id="80777-120">[Diretivas](preprocessor-directives.md)de pré-processador, que instruem o RC a executar ações no script antes de compilá-lo.</span><span class="sxs-lookup"><span data-stu-id="80777-120">[Preprocessor directives](preprocessor-directives.md), which instruct RC to perform actions on the script before compiling it.</span></span>
-   <span data-ttu-id="80777-121">[Operadores de pré-processador](preprocessor-operators.md), que são usados com a diretiva **\# define** .</span><span class="sxs-lookup"><span data-stu-id="80777-121">[Preprocessor operators](preprocessor-operators.md), which are used with the **\#define** directive.</span></span>
-   [<span data-ttu-id="80777-122">Diretivas pragma</span><span class="sxs-lookup"><span data-stu-id="80777-122">Pragma directives</span></span>](pragma-directives.md)
-   <span data-ttu-id="80777-123">[Instruções de definição de recurso](resource-definition-statements.md), que nome e descrevem recursos.</span><span class="sxs-lookup"><span data-stu-id="80777-123">[Resource-definition statements](resource-definition-statements.md), which name and describe resources.</span></span>

 

 




