---
title: Procurando arquivos
description: Por padrão, o RC procura arquivos de cabeçalho e arquivos de recursos (como arquivos de ícone e cursor) primeiro no diretório atual e, em seguida, nos diretórios especificados pela variável de ambiente INCLUDE.
ms.assetid: 6c8c905d-b0f6-4665-9a93-62617ff30137
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 078a04a4cf2f3461d03c7026e0f1d73d8fd38665
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105765702"
---
# <a name="searching-for-files"></a><span data-ttu-id="b6560-103">Procurando arquivos</span><span class="sxs-lookup"><span data-stu-id="b6560-103">Searching for Files</span></span>

<span data-ttu-id="b6560-104">Por padrão, o RC procura arquivos de cabeçalho e arquivos de recursos (como arquivos de ícone e cursor) primeiro no diretório atual e, em seguida, nos diretórios especificados pela variável de ambiente INCLUDE.</span><span class="sxs-lookup"><span data-stu-id="b6560-104">By default, RC searches for header files and resource files (such as icon and cursor files) first in the current directory and then in the directories specified by the INCLUDE environment variable.</span></span> <span data-ttu-id="b6560-105">(A variável de ambiente PATH não tem nenhum efeito sobre quais diretórios RC pesquisa.)</span><span class="sxs-lookup"><span data-stu-id="b6560-105">(The PATH environment variable has no effect on which directories RC searches.)</span></span>

## <a name="adding-a-directory-to-search"></a><span data-ttu-id="b6560-106">Adicionando um diretório para pesquisa</span><span class="sxs-lookup"><span data-stu-id="b6560-106">Adding a Directory to Search</span></span>

<span data-ttu-id="b6560-107">Você pode usar a opção **/i** para adicionar um diretório à lista de pesquisas de diretórios RC.</span><span class="sxs-lookup"><span data-stu-id="b6560-107">You can use the **/i** option to add a directory to the list of directories RC searches.</span></span> <span data-ttu-id="b6560-108">O compilador então pesquisa os diretórios na seguinte ordem:</span><span class="sxs-lookup"><span data-stu-id="b6560-108">The compiler then searches the directories in the following order:</span></span>

1.  <span data-ttu-id="b6560-109">O diretório atual</span><span class="sxs-lookup"><span data-stu-id="b6560-109">The current directory</span></span>
2.  <span data-ttu-id="b6560-110">O diretório ou diretórios que você especifica usando a opção **/i** , na ordem em que aparecem na linha de comando RC</span><span class="sxs-lookup"><span data-stu-id="b6560-110">The directory or directories you specify by using the **/i** option, in the order in which they appear on the RC command line</span></span>
3.  <span data-ttu-id="b6560-111">A lista de diretórios especificada pela variável de ambiente INCLUDE, na ordem em que a variável as lista, a menos que você especifique a opção **/x**</span><span class="sxs-lookup"><span data-stu-id="b6560-111">The list of directories specified by the INCLUDE environment variable, in the order in which the variable lists them, unless you specify the **/x** option</span></span>

<span data-ttu-id="b6560-112">O exemplo a seguir compila o arquivo de definição de recurso MyApp. rc:</span><span class="sxs-lookup"><span data-stu-id="b6560-112">The following example compiles the resource-definition file MyApp.rc:</span></span>

<span data-ttu-id="b6560-113">**RC/i c: \\ origem \\ itens/i d: \\ recursos MyApp. rc**</span><span class="sxs-lookup"><span data-stu-id="b6560-113">**rc /i c:\\source\\stuff /i d:\\resources myapp.rc**</span></span>

<span data-ttu-id="b6560-114">Ao compilar o script MyApp. rc, o RC procura arquivos de cabeçalho e arquivos de recursos primeiro no diretório atual, em C: \\ Source it \\ e D: \\ Resources e, em seguida, nos diretórios especificados pela variável de ambiente INCLUDE.</span><span class="sxs-lookup"><span data-stu-id="b6560-114">When compiling the script MyApp.rc, RC searches for header files and resource files first in the current directory, then in C:\\Source\\Stuff and D:\\Resources, and then in the directories specified by the INCLUDE environment variable.</span></span>

## <a name="ignoring-the-include-environment-variable"></a><span data-ttu-id="b6560-115">Ignorando a variável de ambiente INCLUDE</span><span class="sxs-lookup"><span data-stu-id="b6560-115">Ignoring the INCLUDE Environment Variable</span></span>

<span data-ttu-id="b6560-116">Você pode impedir que o RC use a variável de ambiente INCLUDE ao determinar os diretórios a serem pesquisados.</span><span class="sxs-lookup"><span data-stu-id="b6560-116">You can prevent RC from using the INCLUDE environment variable when determining the directories to search.</span></span> <span data-ttu-id="b6560-117">Para fazer isso, use a opção **/x** .</span><span class="sxs-lookup"><span data-stu-id="b6560-117">To do so, use the **/x** option.</span></span> <span data-ttu-id="b6560-118">O compilador então procura arquivos somente no diretório atual e em todos os diretórios que você especificar usando a opção **/i** .</span><span class="sxs-lookup"><span data-stu-id="b6560-118">The compiler then searches for files only in the current directory and in any directories you specify by using the **/i** option.</span></span>

<span data-ttu-id="b6560-119">O comando a seguir compila o arquivo de script MyApp. rc:</span><span class="sxs-lookup"><span data-stu-id="b6560-119">The following command compiles the script file MyApp.rc:</span></span>

<span data-ttu-id="b6560-120">**RC/x/i c: \\ origem \\ coisas MyApp. rc**</span><span class="sxs-lookup"><span data-stu-id="b6560-120">**rc /x /i c:\\source\\stuff myapp.rc**</span></span>

<span data-ttu-id="b6560-121">Ao compilar o script MyApp. rc, o RC procura arquivos de cabeçalho e arquivos de recursos primeiro no diretório atual e, em seguida, em C: \\ Source \\ .</span><span class="sxs-lookup"><span data-stu-id="b6560-121">When compiling the script MyApp.rc, RC searches for header files and resource files first in the current directory and then in C:\\Source\\Stuff.</span></span> <span data-ttu-id="b6560-122">Ele não pesquisa os diretórios especificados pela variável de ambiente INCLUDE.</span><span class="sxs-lookup"><span data-stu-id="b6560-122">It does not search the directories specified by the INCLUDE environment variable.</span></span>

 

 




