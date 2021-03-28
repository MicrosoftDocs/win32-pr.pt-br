---
description: A interface do usuário do Windows fornece aos usuários acesso a uma ampla variedade de objetos necessários para executar aplicativos e gerenciar o sistema operacional.
title: Shell do Windows
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 1d0d4ed7-9b85-4d70-bf1f-82567a1687fb
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 448e1d5265ec34ce1889ca36f234622e2b082553
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104967988"
---
# <a name="windows-shell"></a><span data-ttu-id="61588-103">Shell do Windows</span><span class="sxs-lookup"><span data-stu-id="61588-103">Windows Shell</span></span>

<span data-ttu-id="61588-104">A interface do usuário do Windows fornece aos usuários acesso a uma ampla variedade de objetos necessários para executar aplicativos e gerenciar o sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="61588-104">The Windows UI provides users with access to a wide variety of objects necessary for running applications and managing the operating system.</span></span> <span data-ttu-id="61588-105">Os mais numerosos e familiares desses objetos são as pastas e os arquivos que residem nas unidades de disco do computador.</span><span class="sxs-lookup"><span data-stu-id="61588-105">The most numerous and familiar of these objects are the folders and files that reside on computer disk drives.</span></span> <span data-ttu-id="61588-106">Também há uma série de objetos virtuais que permitem ao usuário executar tarefas como enviar arquivos para impressoras remotas ou acessar a lixeira.</span><span class="sxs-lookup"><span data-stu-id="61588-106">There are also a number of virtual objects that allow the user to perform tasks such as sending files to remote printers or accessing the Recycle Bin.</span></span> <span data-ttu-id="61588-107">O Shell organiza esses objetos em um namespace hierárquico e fornece aos usuários e aplicativos uma maneira consistente e eficiente de acessar e gerenciar objetos.</span><span class="sxs-lookup"><span data-stu-id="61588-107">The Shell organizes these objects into a hierarchical namespace and provides users and applications with a consistent and efficient way to access and manage objects.</span></span>

## <a name="shell-development-scenarios"></a><span data-ttu-id="61588-108">Cenários de desenvolvimento do Shell</span><span class="sxs-lookup"><span data-stu-id="61588-108">Shell Development Scenarios</span></span>

<span data-ttu-id="61588-109">Os cenários de desenvolvimento a seguir estão relacionados ao desenvolvimento de aplicativos:</span><span class="sxs-lookup"><span data-stu-id="61588-109">The following development scenarios relate to application development:</span></span>

-   <span data-ttu-id="61588-110">Estendendo o Shell, que consiste em criar uma fonte de dados (versus consumir o modelo de dados do Shell)</span><span class="sxs-lookup"><span data-stu-id="61588-110">Extending the Shell, which consists of creating a data source (versus consuming the Shell data model)</span></span>
-   <span data-ttu-id="61588-111">Implementando um subconjunto das tarefas da fonte de dados do Shell</span><span class="sxs-lookup"><span data-stu-id="61588-111">Implementing a subset of the Shell data source tasks</span></span>
-   <span data-ttu-id="61588-112">Suporte a bibliotecas e exibições de itens no Windows Explorer</span><span class="sxs-lookup"><span data-stu-id="61588-112">Supporting libraries and item views in Windows Explorer</span></span>
-   <span data-ttu-id="61588-113">Usando a caixa de diálogo arquivo comum</span><span class="sxs-lookup"><span data-stu-id="61588-113">Using the common file dialog</span></span>
-   <span data-ttu-id="61588-114">Implementando itens do painel de controle</span><span class="sxs-lookup"><span data-stu-id="61588-114">Implementing Control Panel items</span></span>
-   <span data-ttu-id="61588-115">Gerenciando notificações</span><span class="sxs-lookup"><span data-stu-id="61588-115">Managing notifications</span></span>

<span data-ttu-id="61588-116">Os cenários de desenvolvimento a seguir estão relacionados à propriedade do formato de arquivo:</span><span class="sxs-lookup"><span data-stu-id="61588-116">The following development scenarios relate to file format ownership:</span></span>

-   <span data-ttu-id="61588-117">Implementando um subconjunto das tarefas da fonte de dados do Shell</span><span class="sxs-lookup"><span data-stu-id="61588-117">Implementing a subset of the Shell data source tasks</span></span>
-   <span data-ttu-id="61588-118">Implementando qualquer manipulador</span><span class="sxs-lookup"><span data-stu-id="61588-118">Implementing any handler</span></span>
-   <span data-ttu-id="61588-119">Suporte à pesquisa na área de trabalho</span><span class="sxs-lookup"><span data-stu-id="61588-119">Supporting desktop search</span></span>

<span data-ttu-id="61588-120">Os cenários de desenvolvimento a seguir estão relacionados à propriedade de armazenamento de dados:</span><span class="sxs-lookup"><span data-stu-id="61588-120">The following development scenarios relate to data storage ownership:</span></span>

-   <span data-ttu-id="61588-121">Suporte à pesquisa de desktop e OpenSearch</span><span class="sxs-lookup"><span data-stu-id="61588-121">Supporting desktop search and OpenSearch</span></span>
-   <span data-ttu-id="61588-122">Implementando um subconjunto das tarefas da fonte de dados do Shell (pastas virtuais)</span><span class="sxs-lookup"><span data-stu-id="61588-122">Implementing a subset of the Shell data source tasks (virtual folders)</span></span>
-   <span data-ttu-id="61588-123">Suporte a bibliotecas no Windows Explorer</span><span class="sxs-lookup"><span data-stu-id="61588-123">Supporting libraries in Windows Explorer</span></span>

<span data-ttu-id="61588-124">O cenário de desenvolvimento a seguir está relacionado ao suporte do dispositivo:</span><span class="sxs-lookup"><span data-stu-id="61588-124">The following development scenario relates to device support:</span></span>

-   <span data-ttu-id="61588-125">Execução automática e reprodução automática</span><span class="sxs-lookup"><span data-stu-id="61588-125">Auto run and auto play</span></span>

## <a name="windows-shell-sdk-documentation"></a><span data-ttu-id="61588-126">Documentação do SDK do shell do Windows</span><span class="sxs-lookup"><span data-stu-id="61588-126">Windows Shell SDK Documentation</span></span>

<span data-ttu-id="61588-127">Esta documentação é dividida em três seções principais:</span><span class="sxs-lookup"><span data-stu-id="61588-127">This documentation is broken into three major sections:</span></span>

-   <span data-ttu-id="61588-128">O [Guia do desenvolvedor do Shell](intro.md) fornece material conceitual sobre como o Shell funciona e como usar a API do Shell em seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="61588-128">The [Shell Developer's Guide](intro.md) provides conceptual material about how the Shell works and how to use the Shell's API in your application.</span></span>
-   <span data-ttu-id="61588-129">A seção de [referência do Shell](shell-reference-bumper.md) documenta os elementos de programação que compõem as várias APIs do Shell.</span><span class="sxs-lookup"><span data-stu-id="61588-129">The [Shell Reference](shell-reference-bumper.md) section documents programming elements that make up the various Shell APIs.</span></span>
-   <span data-ttu-id="61588-130">[Exemplos de shell](samples-entry.md) fornece links para exemplos de código relacionados.</span><span class="sxs-lookup"><span data-stu-id="61588-130">[Shell Samples](samples-entry.md) provides links to related code samples.</span></span>

<span data-ttu-id="61588-131">A tabela a seguir fornece uma descrição da seção de referência do Shell.</span><span class="sxs-lookup"><span data-stu-id="61588-131">The following table provides an outline of the Shell Reference section.</span></span> <span data-ttu-id="61588-132">Salvo indicação em contrário, todos os elementos de programação são documentados em C++ não gerenciado.</span><span class="sxs-lookup"><span data-stu-id="61588-132">Unless otherwise noted, all programming elements are documented in unmanaged C++.</span></span>



| <span data-ttu-id="61588-133">Seção</span><span class="sxs-lookup"><span data-stu-id="61588-133">Section</span></span>                                                               | <span data-ttu-id="61588-134">Descrição</span><span class="sxs-lookup"><span data-stu-id="61588-134">Description</span></span>                                                                                                          |
|-----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="61588-135">Classes de Shell</span><span class="sxs-lookup"><span data-stu-id="61588-135">Shell Classes</span></span>](classes.md)                                          | <span data-ttu-id="61588-136">Esta seção descreve a seleção de classes de shell do Windows.</span><span class="sxs-lookup"><span data-stu-id="61588-136">This section describes select Windows Shell classes.</span></span>                                                                 |
| [<span data-ttu-id="61588-137">Interfaces do Shell</span><span class="sxs-lookup"><span data-stu-id="61588-137">Shell Interfaces</span></span>](interfaces.md)                                    | <span data-ttu-id="61588-138">Esta seção descreve as interfaces do Windows Shell Component Object Model (COM).</span><span class="sxs-lookup"><span data-stu-id="61588-138">This section describes the Windows Shell Component Object Model (COM) interfaces.</span></span>                                    |
| [<span data-ttu-id="61588-139">Funções do Shell</span><span class="sxs-lookup"><span data-stu-id="61588-139">Shell Functions</span></span>](functions.md)                                      | <span data-ttu-id="61588-140">Esta seção descreve as funções do shell do Windows.</span><span class="sxs-lookup"><span data-stu-id="61588-140">This section describes the Windows Shell functions.</span></span>                                                                  |
| [<span data-ttu-id="61588-141">Funções de retorno de chamada do Shell</span><span class="sxs-lookup"><span data-stu-id="61588-141">Shell Callback Functions</span></span>](callbacks.md)                             | <span data-ttu-id="61588-142">Esta seção descreve os modelos de funções de retorno de chamada do shell do Windows.</span><span class="sxs-lookup"><span data-stu-id="61588-142">This section describes the Windows Shell callback functions templates.</span></span>                                               |
| [<span data-ttu-id="61588-143">Constantes, enumerações e sinalizadores do Shell</span><span class="sxs-lookup"><span data-stu-id="61588-143">Shell Constants, Enumerations, and Flags</span></span>](consts-enums-flags.md)    | <span data-ttu-id="61588-144">Esta seção descreve as constantes do shell do Windows, as enumerações e os sinalizadores usados nas APIs do Shell.</span><span class="sxs-lookup"><span data-stu-id="61588-144">This section describes the Windows Shell constants, enumerations, and flags used in the Shell APIs.</span></span>                  |
| [<span data-ttu-id="61588-145">Funções do utilitário Lightweight do Shell</span><span class="sxs-lookup"><span data-stu-id="61588-145">Shell Lightweight Utility Functions</span></span>](shlwapi.md)                    | <span data-ttu-id="61588-146">Esta seção descreve as funções do utilitário Windows Shell Lightweight fornecidas no Shlwapi.dll.</span><span class="sxs-lookup"><span data-stu-id="61588-146">This section describes the Windows Shell lightweight utility functions provided in Shlwapi.dll.</span></span>                      |
| [<span data-ttu-id="61588-147">Macros do Shell</span><span class="sxs-lookup"><span data-stu-id="61588-147">Shell Macros</span></span>](macros.md)                                            | <span data-ttu-id="61588-148">Esta seção descreve as macros do utilitário de shell do Windows.</span><span class="sxs-lookup"><span data-stu-id="61588-148">This section describes the Windows Shell utility macros.</span></span>                                                             |
| [<span data-ttu-id="61588-149">Mensagens e notificações do Shell</span><span class="sxs-lookup"><span data-stu-id="61588-149">Shell Messages and Notifications</span></span>](messages.md)                      | <span data-ttu-id="61588-150">Esta seção descreve as mensagens e notificações enviadas por elementos do shell do Windows.</span><span class="sxs-lookup"><span data-stu-id="61588-150">This section describes the messages and notifications sent by elements of the Windows Shell.</span></span>                         |
| [<span data-ttu-id="61588-151">Objetos do Shell para scripts e Microsoft Visual Basic</span><span class="sxs-lookup"><span data-stu-id="61588-151">Shell Objects for Scripting and Microsoft Visual Basic</span></span>](objects.md) | <span data-ttu-id="61588-152">Esta seção descreve os objetos do Windows implementados pelo shell para uso no script e no Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="61588-152">This section describes the Windows objects implemented by the Shell for use in scripting and Microsoft Visual Basic.</span></span> |
| [<span data-ttu-id="61588-153">Objetos do Shell para C++</span><span class="sxs-lookup"><span data-stu-id="61588-153">Shell Objects for C++</span></span>](objects-cpp.md)                              | <span data-ttu-id="61588-154">Esta seção descreve os objetos C++ do Windows implementados pelo shell.</span><span class="sxs-lookup"><span data-stu-id="61588-154">This section describes the C++ Windows objects implemented by the Shell.</span></span>                                             |
| [<span data-ttu-id="61588-155">Esquemas de Shell</span><span class="sxs-lookup"><span data-stu-id="61588-155">Shell Schemas</span></span>](schemas.md)                                          | <span data-ttu-id="61588-156">Esta seção descreve a biblioteca, a propriedade e os esquemas de manifesto de transferência usados pelo shell do Windows.</span><span class="sxs-lookup"><span data-stu-id="61588-156">This section describes library, property, and transfer manifest schemas used by the Windows Shell.</span></span>                   |
| [<span data-ttu-id="61588-157">Estruturas do Shell</span><span class="sxs-lookup"><span data-stu-id="61588-157">Shell Structures</span></span>](structures.md)                                    | <span data-ttu-id="61588-158">Esta seção descreve as estruturas de shell do Windows usadas nas APIs do Shell.</span><span class="sxs-lookup"><span data-stu-id="61588-158">This section describes the Windows Shell structures used in the Shell APIs.</span></span>                                          |



 

 

 



