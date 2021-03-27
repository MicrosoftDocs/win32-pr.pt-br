---
description: A interface do usuário do Windows fornece aos usuários acesso a uma ampla variedade de objetos necessários para executar aplicativos e gerenciar o sistema operacional.
title: Guia do desenvolvedor do Shell
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 8f88ef25-3645-4f54-9453-41f919c0fc0a
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 1be17ca90b7138294be3e1b34fa3fcb4dcb4227a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988776"
---
# <a name="shell-developers-guide"></a><span data-ttu-id="920c7-103">Guia do desenvolvedor do Shell</span><span class="sxs-lookup"><span data-stu-id="920c7-103">Shell Developer's Guide</span></span>

<span data-ttu-id="920c7-104">A interface do usuário do Windows fornece aos usuários acesso a uma ampla variedade de objetos necessários para executar aplicativos e gerenciar o sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="920c7-104">The Windows UI provides users with access to a wide variety of objects necessary to run applications and manage the operating system.</span></span> <span data-ttu-id="920c7-105">Os mais numerosos e familiares desses objetos são as pastas e os arquivos que residem nas unidades de disco do computador.</span><span class="sxs-lookup"><span data-stu-id="920c7-105">The most numerous and familiar of these objects are the folders and files that reside on computer disk drives.</span></span> <span data-ttu-id="920c7-106">Também há uma série de objetos virtuais que permitem ao usuário realizar tarefas como enviar arquivos para impressoras remotas ou acessar a lixeira.</span><span class="sxs-lookup"><span data-stu-id="920c7-106">There are also a number of virtual objects that allow the user to do tasks such as sending files to remote printers or accessing the Recycle Bin.</span></span> <span data-ttu-id="920c7-107">O Shell organiza esses objetos em um namespace hierárquico e fornece aos usuários e aplicativos uma maneira consistente e eficiente de acessar e gerenciar objetos.</span><span class="sxs-lookup"><span data-stu-id="920c7-107">The Shell organizes these objects into a hierarchical namespace, and provides users and applications with a consistent and efficient way to access and manage objects.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="920c7-108">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="920c7-108">In this section</span></span>

-   [<span data-ttu-id="920c7-109">Considerações de segurança: Shell do Microsoft Windows</span><span class="sxs-lookup"><span data-stu-id="920c7-109">Security Considerations: Microsoft Windows Shell</span></span>](sec-shell.md)
-   [<span data-ttu-id="920c7-110">Diretrizes para implementar extensões de In-Process</span><span class="sxs-lookup"><span data-stu-id="920c7-110">Guidance for Implementing In-Process Extensions</span></span>](shell-and-managed-code.md)
-   [<span data-ttu-id="920c7-111">Versões do Shell e de controles comuns</span><span class="sxs-lookup"><span data-stu-id="920c7-111">Shell and Common Controls Versions</span></span>](versions.md)
-   [<span data-ttu-id="920c7-112">Implementando as interfaces de objeto de pasta básica</span><span class="sxs-lookup"><span data-stu-id="920c7-112">Implementing the Basic Folder Object Interfaces</span></span>](nse-implement.md)
-   [<span data-ttu-id="920c7-113">Implementando um formato de arquivo personalizado</span><span class="sxs-lookup"><span data-stu-id="920c7-113">Implementing a Custom File Format</span></span>](customizing-file-types-bumper.md)
-   [<span data-ttu-id="920c7-114">Extensibilidade do Shell (criando uma fonte de dados)</span><span class="sxs-lookup"><span data-stu-id="920c7-114">Shell Extensibility (Creating a Data Source)</span></span>](shell-extensibility-bumper.md)
-   [<span data-ttu-id="920c7-115">Implementando itens do painel de controle</span><span class="sxs-lookup"><span data-stu-id="920c7-115">Implementing Control Panel Items</span></span>](control-panel-applications.md)
-   [<span data-ttu-id="920c7-116">Suporte a aplicativos do Shell</span><span class="sxs-lookup"><span data-stu-id="920c7-116">Supporting Shell Applications</span></span>](application-support-bumper.md)
-   [<span data-ttu-id="920c7-117">Tópicos de shell herdados</span><span class="sxs-lookup"><span data-stu-id="920c7-117">Legacy Shell Topics</span></span>](miscellaneous-topics-bumper.md)

## <a name="document-conventions"></a><span data-ttu-id="920c7-118">Convenções de documento</span><span class="sxs-lookup"><span data-stu-id="920c7-118">Document Conventions</span></span>

<span data-ttu-id="920c7-119">O guia de desenvolvedores do Shell segue as convenções de documento comuns do SDK (Software Development Kit) do Windows.</span><span class="sxs-lookup"><span data-stu-id="920c7-119">The Shell Developers's Guide follows the usual Windows Software Development Kit (SDK) document conventions.</span></span> <span data-ttu-id="920c7-120">Duas convenções em particular devem ser observadas:</span><span class="sxs-lookup"><span data-stu-id="920c7-120">Two conventions in particular should be noted:</span></span>

-   <span data-ttu-id="920c7-121">O código de exemplo omite o código de correção de erro normal.</span><span class="sxs-lookup"><span data-stu-id="920c7-121">Sample code omits normal error-correction code.</span></span> <span data-ttu-id="920c7-122">Esse código foi removido apenas para tornar o código mais legível.</span><span class="sxs-lookup"><span data-stu-id="920c7-122">This code has been removed only to make the code more readable.</span></span> <span data-ttu-id="920c7-123">Você deve incluir todo o código de correção de erro apropriado em seus próprios aplicativos.</span><span class="sxs-lookup"><span data-stu-id="920c7-123">You should include all appropriate error-correction code in your own applications.</span></span>
-   <span data-ttu-id="920c7-124">Para tornar as entradas de registro de exemplo clara, chave, subchave e nomes de entrada, bem como os valores são exibidos com uma fonte padrão.</span><span class="sxs-lookup"><span data-stu-id="920c7-124">To make sample registry entries clear, key, subkey, and entry names as well as values are displayed with a standard font.</span></span> <span data-ttu-id="920c7-125">Os nomes de itens definidos pelo usuário ou pelo aplicativo estão em itálico.</span><span class="sxs-lookup"><span data-stu-id="920c7-125">User or application-defined item names are italicized.</span></span>

 

 



