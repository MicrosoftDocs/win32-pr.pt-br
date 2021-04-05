---
description: Gerencie o compartilhamento de assembly e o controle de versão de DLL no armazenamento de assembly lado a lado dos programas. Escrever manifestos de assembly e descrever automaticamente os aplicativos para compartilhamento de assembly e redirecionamento de DLLs.
ms.assetid: 2f841eb6-9a6c-4c9b-b057-a3da6cd6b0b0
title: Aplicativos isolados e assemblies lado a lado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59abfbd5392040856c66ef9eb786b66d2a84500f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090207"
---
# <a name="isolated-applications-and-side-by-side-assemblies"></a><span data-ttu-id="a4d30-104">Aplicativos isolados e assemblies lado a lado</span><span class="sxs-lookup"><span data-stu-id="a4d30-104">Isolated Applications and Side-by-side Assemblies</span></span>

## <a name="purpose"></a><span data-ttu-id="a4d30-105">Finalidade</span><span class="sxs-lookup"><span data-stu-id="a4d30-105">Purpose</span></span>

<span data-ttu-id="a4d30-106">Os aplicativos isolados e os assemblies lado a lado são uma solução do Microsoft Windows que reduz conflitos de controle de versão em aplicativos cliente do Windows.</span><span class="sxs-lookup"><span data-stu-id="a4d30-106">Isolated Applications and Side-by-side Assemblies is a Microsoft Windows solution that reduces versioning conflicts in Windows-client applications.</span></span> <span data-ttu-id="a4d30-107">Com o Windows, os desenvolvedores de aplicativos podem criar aplicativos isolados totalmente autodescritivos e não afetados por alterações no registro, em outros aplicativos ou em outras versões de assemblies em execução no sistema.</span><span class="sxs-lookup"><span data-stu-id="a4d30-107">With Windows, application developers can build isolated applications that are fully self-describing and unaffected by changes to the registry, other applications, or other versions of assemblies running on the system.</span></span> <span data-ttu-id="a4d30-108">Os autores e administradores de aplicativos podem usar manifestos para gerenciar o compartilhamento de assemblies lado a lado após a implantação em uma base global ou por aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a4d30-108">Application authors and administrators can use manifests to manage the sharing of side-by-side assemblies after deployment on either a global or per-application basis.</span></span> <span data-ttu-id="a4d30-109">Os clientes se beneficiam de aplicativos isolados que são mais estáveis e mais confiáveis.</span><span class="sxs-lookup"><span data-stu-id="a4d30-109">Customers benefit from isolated applications that are more stable and more reliably updated.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="a4d30-110">Quando aplicável</span><span class="sxs-lookup"><span data-stu-id="a4d30-110">Where applicable</span></span>

<span data-ttu-id="a4d30-111">Os aplicativos isolados e o compartilhamento de assembly lado a lado podem ser usados para desenvolver aplicativos que compartilhem com segurança os assemblies do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="a4d30-111">Isolated applications and side-by-side assembly sharing can be used to develop applications that safely share operating system assemblies.</span></span> <span data-ttu-id="a4d30-112">Os desenvolvedores podem usar essa tecnologia para corrigir conflitos de versão de DLL causados por uma versão incompatível de um assembly compartilhado.</span><span class="sxs-lookup"><span data-stu-id="a4d30-112">Developers can use this technology to correct DLL versioning conflicts caused by an incompatible version of a shared assembly.</span></span>

<span data-ttu-id="a4d30-113">Se seu aplicativo precisar obter consistentemente a versão de um componente que você testou, é possível isolar seu aplicativo para que ele seja sempre executado com a versão testada do componente no computador do usuário.</span><span class="sxs-lookup"><span data-stu-id="a4d30-113">If your application must consistently get the version of a component you have tested, it is possible to isolate your application so that it will always be run with the tested version of the component on the user's computer.</span></span>

<span data-ttu-id="a4d30-114">Os aplicativos isolados e os assemblies lado a lado são destinados ao desenvolvimento de aplicativos de estilo de área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="a4d30-114">Isolated Applications and Side-by-side Assemblies is intended for the development of desktop style applications.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="a4d30-115">Público de desenvolvedores</span><span class="sxs-lookup"><span data-stu-id="a4d30-115">Developer audience</span></span>

<span data-ttu-id="a4d30-116">Esta documentação destina-se principalmente a desenvolvedores de software, desenvolvedores de aplicativos e administradores de rede:</span><span class="sxs-lookup"><span data-stu-id="a4d30-116">This documentation is primarily intended for software developers, application developers, and network administrators:</span></span>

-   <span data-ttu-id="a4d30-117">Os desenvolvedores de software que desejam criar aplicativos isolados que usarão os assemblies lado a lado disponibilizados pela Microsoft e por outros publicadores de assembly lado a lado.</span><span class="sxs-lookup"><span data-stu-id="a4d30-117">Software developers who want to create isolated applications that will use the side-by-side assemblies made available by Microsoft and other side-by-side assembly publishers.</span></span>
-   <span data-ttu-id="a4d30-118">Desenvolvedores de aplicativos interessados em criar seus próprios assemblies lado a lado para isolar seus aplicativos.</span><span class="sxs-lookup"><span data-stu-id="a4d30-118">Application developers who are interested in creating their own side-by-side assemblies to isolate their applications.</span></span>
-   <span data-ttu-id="a4d30-119">Administradores de rede que desejam mais informações sobre aplicativos isolados.</span><span class="sxs-lookup"><span data-stu-id="a4d30-119">Network administrators who want more information about isolated applications.</span></span>

<span data-ttu-id="a4d30-120">Como referência principal para compartilhamento de assembly lado a lado e aplicativos isolados, esta documentação fornece informações gerais básicas sobre a criação de manifestos e assemblies lado a lado, instalação de aplicativos isolados e assemblies lado a lado e uso da API de contexto de ativação.</span><span class="sxs-lookup"><span data-stu-id="a4d30-120">As the primary reference for side-by-side assembly sharing and isolated applications, this documentation provides general background information about authoring manifests and side-by-side assemblies, installing isolated applications and side-by-side assemblies, and using the Activation Context API.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="a4d30-121">Requisitos de tempo de execução</span><span class="sxs-lookup"><span data-stu-id="a4d30-121">Run-time requirements</span></span>

<span data-ttu-id="a4d30-122">O Windows Server 2003 e posterior ou o Windows XP e posterior é necessário para usar assemblies e manifestos lado a lado para isolar aplicativos e usar a API de contexto de ativação.</span><span class="sxs-lookup"><span data-stu-id="a4d30-122">Windows Server 2003 and later or Windows XP and later is required to use side-by-side assemblies and manifests to isolate applications and to use the Activation Context API.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="a4d30-123">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="a4d30-123">In this section</span></span>



| <span data-ttu-id="a4d30-124">Tópico</span><span class="sxs-lookup"><span data-stu-id="a4d30-124">Topic</span></span>                                                         | <span data-ttu-id="a4d30-125">Descrição</span><span class="sxs-lookup"><span data-stu-id="a4d30-125">Description</span></span>                                                                    |
|---------------------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="a4d30-126">Referência</span><span class="sxs-lookup"><span data-stu-id="a4d30-126">Reference</span></span>](side-by-side-assemblies-reference.md)<br/> | <span data-ttu-id="a4d30-127">Documentação de aplicativos isolados e assemblies lado a lado.</span><span class="sxs-lookup"><span data-stu-id="a4d30-127">Documentation of Isolated Applications and Side-by-side Assemblies.</span></span><br/> |



 

 

 




