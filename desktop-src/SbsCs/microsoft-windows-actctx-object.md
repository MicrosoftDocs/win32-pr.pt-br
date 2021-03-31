---
description: O objeto Microsoft. Windows. ActCtx faz referência a manifestos e fornece uma maneira para os mecanismos de script acessarem assemblies lado a lado. O objeto Microsoft. Windows. ActCtx pode ser usado para criar uma instância de um assembly lado a lado com componentes COM.
ms.assetid: 818e175e-2c58-4c44-87ce-4e97352fc3f3
title: Objeto Microsoft. Windows. ActCtx
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Microsoft.Windows.ActCtx
api_type:
- COM
api_location: ''
ms.openlocfilehash: 58290ec9d36d8e8428000422d0e1014335870149
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827936"
---
# <a name="microsoftwindowsactctx-object"></a><span data-ttu-id="4e062-104">Objeto Microsoft. Windows. ActCtx</span><span class="sxs-lookup"><span data-stu-id="4e062-104">Microsoft.Windows.ActCtx object</span></span>

<span data-ttu-id="4e062-105">O objeto **Microsoft. Windows. ActCtx** faz referência a manifestos e fornece uma maneira para os mecanismos de script acessarem assemblies lado a lado.</span><span class="sxs-lookup"><span data-stu-id="4e062-105">The **Microsoft.Windows.ActCtx** object references manifests and provides a way for scripting engines to access side-by-side assemblies.</span></span> <span data-ttu-id="4e062-106">O objeto **Microsoft. Windows. ActCtx** pode ser usado para criar uma instância de um assembly lado a lado COM componentes com.</span><span class="sxs-lookup"><span data-stu-id="4e062-106">The **Microsoft.Windows.ActCtx** object can be used to create an instance of a side-by-side assembly with COM components.</span></span>

<span data-ttu-id="4e062-107">O objeto **Microsoft. Windows. ActCtx** é fornecido como um assembly no Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="4e062-107">The **Microsoft.Windows.ActCtx** object comes as an assembly in Windows Server 2003.</span></span> <span data-ttu-id="4e062-108">Ele também pode ser instalado por aplicativos que usam o Windows Installer para instalação e o incluem como um módulo de mesclagem em seu pacote de instalação.</span><span class="sxs-lookup"><span data-stu-id="4e062-108">It can also be installed by applications that use the Windows Installer for setup and include it as a merge module in their installation package.</span></span>

## <a name="members"></a><span data-ttu-id="4e062-109">Membros</span><span class="sxs-lookup"><span data-stu-id="4e062-109">Members</span></span>

<span data-ttu-id="4e062-110">O objeto **Microsoft. Windows. ActCtx** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="4e062-110">The **Microsoft.Windows.ActCtx** object has these types of members:</span></span>

-   [<span data-ttu-id="4e062-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="4e062-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="4e062-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="4e062-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="4e062-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="4e062-113">Methods</span></span>

<span data-ttu-id="4e062-114">O objeto **Microsoft. Windows. ActCtx** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="4e062-114">The **Microsoft.Windows.ActCtx** object has these methods.</span></span>



| <span data-ttu-id="4e062-115">Método</span><span class="sxs-lookup"><span data-stu-id="4e062-115">Method</span></span>                               | <span data-ttu-id="4e062-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="4e062-116">Description</span></span>                                                                     |
|:-------------------------------------|:--------------------------------------------------------------------------------|
| [<span data-ttu-id="4e062-117">**CreateObject**</span><span class="sxs-lookup"><span data-stu-id="4e062-117">**CreateObject**</span></span>](createobject.md) | <span data-ttu-id="4e062-118">Cria um objeto no contexto do manifesto atual.</span><span class="sxs-lookup"><span data-stu-id="4e062-118">Creates an object in the context of the current manifest.</span></span><br/>            |
| [<span data-ttu-id="4e062-119">**GetObject**</span><span class="sxs-lookup"><span data-stu-id="4e062-119">**GetObject**</span></span>](getobject.md)       | <span data-ttu-id="4e062-120">Obtém uma instância de um objeto **Microsoft. Windows. ActCtx** existente.</span><span class="sxs-lookup"><span data-stu-id="4e062-120">Gets an instance of an existing **Microsoft.Windows.ActCtx** object.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="4e062-121">Propriedades</span><span class="sxs-lookup"><span data-stu-id="4e062-121">Properties</span></span>

<span data-ttu-id="4e062-122">O objeto **Microsoft. Windows. ActCtx** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="4e062-122">The **Microsoft.Windows.ActCtx** object has these properties.</span></span>



| <span data-ttu-id="4e062-123">Propriedade</span><span class="sxs-lookup"><span data-stu-id="4e062-123">Property</span></span>                                | <span data-ttu-id="4e062-124">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="4e062-124">Access type</span></span>          | <span data-ttu-id="4e062-125">Descrição</span><span class="sxs-lookup"><span data-stu-id="4e062-125">Description</span></span>                                    |
|:----------------------------------------|:---------------------|:-----------------------------------------------|
| [<span data-ttu-id="4e062-126">**Manifesto**</span><span class="sxs-lookup"><span data-stu-id="4e062-126">**Manifest**</span></span>](manifest.md)<br/> | <span data-ttu-id="4e062-127">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4e062-127">Read-only</span></span><br/> | <span data-ttu-id="4e062-128">Obtém o contexto de ativação ativa.</span><span class="sxs-lookup"><span data-stu-id="4e062-128">Gets the active activation context.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="4e062-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4e062-129">Requirements</span></span>



| <span data-ttu-id="4e062-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="4e062-130">Requirement</span></span> | <span data-ttu-id="4e062-131">Valor</span><span class="sxs-lookup"><span data-stu-id="4e062-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="4e062-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4e062-132">Minimum supported client</span></span><br/> | <span data-ttu-id="4e062-133">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="4e062-133">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="4e062-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4e062-134">Minimum supported server</span></span><br/> | <span data-ttu-id="4e062-135">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="4e062-135">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



 

 




