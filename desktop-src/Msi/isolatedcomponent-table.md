---
description: Cada registro da tabela IsolatedComponent associa o componente especificado na \_ coluna aplicativo de componente (normalmente um. exe) com o componente especificado na \_ coluna compartilhada componente (normalmente, uma DLL compartilhada).
ms.assetid: dc30e4c7-a938-4060-be4f-744de9c20fd9
title: Tabela IsolatedComponent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c3e6c5bdba6efc546a36e77fa793c0b397f6d5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105759220"
---
# <a name="isolatedcomponent-table"></a><span data-ttu-id="118a8-103">Tabela IsolatedComponent</span><span class="sxs-lookup"><span data-stu-id="118a8-103">IsolatedComponent Table</span></span>

<span data-ttu-id="118a8-104">Cada registro da tabela IsolatedComponent associa o componente especificado na \_ coluna aplicativo de componente (normalmente um. exe) com o componente especificado na \_ coluna compartilhada componente (normalmente, uma DLL compartilhada).</span><span class="sxs-lookup"><span data-stu-id="118a8-104">Each record of the IsolatedComponent table associates the component specified in the Component\_Application column (commonly an .exe) with the component specified in the Component\_Shared column (commonly a shared DLL).</span></span> <span data-ttu-id="118a8-105">A [ação IsolateComponents](isolatecomponents-action.md) instala uma cópia do componente \_ compartilhado em um local privado para uso por aplicativo de componente \_ .</span><span class="sxs-lookup"><span data-stu-id="118a8-105">The [IsolateComponents action](isolatecomponents-action.md) installs a copy of Component\_Shared into a private location for use by Component\_Application.</span></span> <span data-ttu-id="118a8-106">Isso isola o aplicativo de componente \_ de outras cópias de componentes \_ compartilhados que podem ser instalados em um local compartilhado no computador.</span><span class="sxs-lookup"><span data-stu-id="118a8-106">This isolates the Component\_Application from other copies of Component\_Shared that may be installed to a shared location on the computer.</span></span> <span data-ttu-id="118a8-107">Consulte [componentes isolados](isolated-components.md).</span><span class="sxs-lookup"><span data-stu-id="118a8-107">See [Isolated Components](isolated-components.md).</span></span>

<span data-ttu-id="118a8-108">Para vincular um componente \_ compartilhado a vários aplicativos de componente \_ , inclua um registro separado para cada par na tabela IsolatedComponents.</span><span class="sxs-lookup"><span data-stu-id="118a8-108">To link one Component\_Shared to multiple Component\_Application, include a separate record for each pair in the IsolatedComponents table.</span></span> <span data-ttu-id="118a8-109">O instalador copia os arquivos do componente \_ compartilhado para o diretório de cada aplicativo de componente \_ que está instalado.</span><span class="sxs-lookup"><span data-stu-id="118a8-109">The installer copies the files of Component\_Shared into the directory of each Component\_Application that is installed.</span></span>

<span data-ttu-id="118a8-110">A tabela IsolatedComponent tem as colunas a seguir.</span><span class="sxs-lookup"><span data-stu-id="118a8-110">The IsolatedComponent table has the following columns.</span></span>



| <span data-ttu-id="118a8-111">Coluna</span><span class="sxs-lookup"><span data-stu-id="118a8-111">Column</span></span>                 | <span data-ttu-id="118a8-112">Tipo</span><span class="sxs-lookup"><span data-stu-id="118a8-112">Type</span></span>                         | <span data-ttu-id="118a8-113">Chave</span><span class="sxs-lookup"><span data-stu-id="118a8-113">Key</span></span> | <span data-ttu-id="118a8-114">Nullable</span><span class="sxs-lookup"><span data-stu-id="118a8-114">Nullable</span></span> |
|------------------------|------------------------------|-----|----------|
| <span data-ttu-id="118a8-115">Componente \_ compartilhado</span><span class="sxs-lookup"><span data-stu-id="118a8-115">Component\_Shared</span></span>      | [<span data-ttu-id="118a8-116">Identificador</span><span class="sxs-lookup"><span data-stu-id="118a8-116">Identifier</span></span>](identifier.md) | <span data-ttu-id="118a8-117">S</span><span class="sxs-lookup"><span data-stu-id="118a8-117">Y</span></span>   | <span data-ttu-id="118a8-118">N</span><span class="sxs-lookup"><span data-stu-id="118a8-118">N</span></span>        |
| <span data-ttu-id="118a8-119">Aplicativo de componente \_</span><span class="sxs-lookup"><span data-stu-id="118a8-119">Component\_Application</span></span> | [<span data-ttu-id="118a8-120">Identificador</span><span class="sxs-lookup"><span data-stu-id="118a8-120">Identifier</span></span>](identifier.md) | <span data-ttu-id="118a8-121">S</span><span class="sxs-lookup"><span data-stu-id="118a8-121">Y</span></span>   | <span data-ttu-id="118a8-122">N</span><span class="sxs-lookup"><span data-stu-id="118a8-122">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="118a8-123">Colunas</span><span class="sxs-lookup"><span data-stu-id="118a8-123">Columns</span></span>

<dl> <dt>

<span data-ttu-id="118a8-124"><span id="Component_Shared"></span><span id="component_shared"></span><span id="COMPONENT_SHARED"></span>Componente \_ compartilhado</span><span class="sxs-lookup"><span data-stu-id="118a8-124"><span id="Component_Shared"></span><span id="component_shared"></span><span id="COMPONENT_SHARED"></span>Component\_Shared</span></span>
</dt> <dd>

<span data-ttu-id="118a8-125">Chave estrangeira na [tabela de componentes](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="118a8-125">Foreign key into the [Component table](component-table.md).</span></span> <span data-ttu-id="118a8-126">O componente que contém o arquivo compartilhado, geralmente uma DLL.</span><span class="sxs-lookup"><span data-stu-id="118a8-126">The component that contains the shared file, usually a DLL.</span></span> <span data-ttu-id="118a8-127">A DLL deve ser o arquivo de chave para esse componente.</span><span class="sxs-lookup"><span data-stu-id="118a8-127">The DLL should be the key file for this component.</span></span> <span data-ttu-id="118a8-128">Ele deve ser um componente diferente do listado na \_ coluna aplicativo de componente.</span><span class="sxs-lookup"><span data-stu-id="118a8-128">This must be a different component than listed in the Component\_Application column.</span></span>

<span data-ttu-id="118a8-129">O componente compartilhado controla o registro de todas as cópias isoladas do componente e deve ter o sinalizador **msidbComponentAttributesSharedDllRefCount** definido na coluna atributos da tabela de componentes.</span><span class="sxs-lookup"><span data-stu-id="118a8-129">The shared component controls the registration for all the isolated copies of the component and must have the **msidbComponentAttributesSharedDllRefCount** flag set in the Attributes column of the Component table.</span></span> <span data-ttu-id="118a8-130">Isso garante que o instalador possa gerenciar a vida útil do componente compartilhado.</span><span class="sxs-lookup"><span data-stu-id="118a8-130">This ensures that the installer can manage the life of the shared component.</span></span>

</dd> <dt>

<span data-ttu-id="118a8-131"><span id="Component_Application"></span><span id="component_application"></span><span id="COMPONENT_APPLICATION"></span>Aplicativo de componente \_</span><span class="sxs-lookup"><span data-stu-id="118a8-131"><span id="Component_Application"></span><span id="component_application"></span><span id="COMPONENT_APPLICATION"></span>Component\_Application</span></span>
</dt> <dd>

<span data-ttu-id="118a8-132">Chave estrangeira na [tabela de componentes](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="118a8-132">Foreign key into the [Component table](component-table.md).</span></span> <span data-ttu-id="118a8-133">O componente que contém o. exe que carrega o arquivo compartilhado.</span><span class="sxs-lookup"><span data-stu-id="118a8-133">The component that contains the .exe which loads the shared file.</span></span> <span data-ttu-id="118a8-134">O. exe deve ser o arquivo de chave para esse componente.</span><span class="sxs-lookup"><span data-stu-id="118a8-134">The .exe should be the key file for this component.</span></span> <span data-ttu-id="118a8-135">Ele deve ser um componente diferente do listado na \_ coluna compartilhada do componente.</span><span class="sxs-lookup"><span data-stu-id="118a8-135">This must be a different component than listed in the Component\_Shared column.</span></span>

</dd> </dl>

## <a name="validation"></a><span data-ttu-id="118a8-136">Validação</span><span class="sxs-lookup"><span data-stu-id="118a8-136">Validation</span></span>

<dl>

[<span data-ttu-id="118a8-137">ICE03</span><span class="sxs-lookup"><span data-stu-id="118a8-137">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="118a8-138">ICE06</span><span class="sxs-lookup"><span data-stu-id="118a8-138">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="118a8-139">ICE32</span><span class="sxs-lookup"><span data-stu-id="118a8-139">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="118a8-140">ICE62</span><span class="sxs-lookup"><span data-stu-id="118a8-140">ICE62</span></span>](ice62.md)  
[<span data-ttu-id="118a8-141">ICE66</span><span class="sxs-lookup"><span data-stu-id="118a8-141">ICE66</span></span>](ice66.md)  
[<span data-ttu-id="118a8-142">ICE97</span><span class="sxs-lookup"><span data-stu-id="118a8-142">ICE97</span></span>](ice97.md)  
</dl>

 

 



