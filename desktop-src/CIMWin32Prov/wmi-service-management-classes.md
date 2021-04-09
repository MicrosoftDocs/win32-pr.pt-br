---
description: As classes de gerenciamento de serviço WMI são usadas para gerenciar o próprio serviço WMI e não o sistema de computador ou a rede corporativa. O gerenciamento do WMI abrange tanto a configuração do serviço WMI quanto o gerenciamento de operações do WMI.
ms.assetid: EF58AC04-FE04-4D0C-A5F7-3491C885A0E4
ms.tgt_platform: multiple
title: Classes de gerenciamento de serviço WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b502abebbddfd2ce90562045a8b0d7acd3974171
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104088961"
---
# <a name="wmi-service-management-classes"></a><span data-ttu-id="f2ec1-104">Classes de gerenciamento de serviço WMI</span><span class="sxs-lookup"><span data-stu-id="f2ec1-104">WMI Service Management Classes</span></span>

<span data-ttu-id="f2ec1-105">As classes de gerenciamento de serviço WMI são usadas para gerenciar o próprio serviço WMI e não o sistema de computador ou a rede corporativa.</span><span class="sxs-lookup"><span data-stu-id="f2ec1-105">WMI service management classes are used to manage the WMI service itself and not the computer system or enterprise network.</span></span> <span data-ttu-id="f2ec1-106">O gerenciamento do WMI abrange tanto a configuração do serviço WMI quanto o gerenciamento de operações do WMI.</span><span class="sxs-lookup"><span data-stu-id="f2ec1-106">Managing WMI encompasses both configuring the WMI service and managing WMI operations.</span></span>

<span data-ttu-id="f2ec1-107">A categoria gerenciamento de serviços WMI inclui as seguintes subcategorias de classes:</span><span class="sxs-lookup"><span data-stu-id="f2ec1-107">The WMI Service Management category includes the following subcategories of classes:</span></span>

-   [<span data-ttu-id="f2ec1-108">Classes de configuração do WMI</span><span class="sxs-lookup"><span data-stu-id="f2ec1-108">WMI configuration classes</span></span>](#wmi-configuration-classes)
-   [<span data-ttu-id="f2ec1-109">Classes de gerenciamento do WMI</span><span class="sxs-lookup"><span data-stu-id="f2ec1-109">WMI management classes</span></span>](#wmi-management-classes)

## <a name="wmi-configuration-classes"></a><span data-ttu-id="f2ec1-110">Classes de configuração do WMI</span><span class="sxs-lookup"><span data-stu-id="f2ec1-110">WMI Configuration Classes</span></span>

<span data-ttu-id="f2ec1-111">A classe de configuração do WMI deriva métodos que configuram o serviço WMI.</span><span class="sxs-lookup"><span data-stu-id="f2ec1-111">The WMI Configuration class derives methods that configure the WMI service.</span></span>

<span data-ttu-id="f2ec1-112">Veja a seguir uma tabela de classes de configuração do WMI.</span><span class="sxs-lookup"><span data-stu-id="f2ec1-112">The following is a table of WMI configuration classes.</span></span>



| <span data-ttu-id="f2ec1-113">Classe</span><span class="sxs-lookup"><span data-stu-id="f2ec1-113">Class</span></span>                                                             | <span data-ttu-id="f2ec1-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="f2ec1-114">Description</span></span>                                                                     |
|-------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [<span data-ttu-id="f2ec1-115">**\_MethodParameterClass Win32**</span><span class="sxs-lookup"><span data-stu-id="f2ec1-115">**Win32\_MethodParameterClass**</span></span>](win32-methodparameterclass.md) | <span data-ttu-id="f2ec1-116">Abstrata, classe base que implementa parâmetros de método derivados desta classe.</span><span class="sxs-lookup"><span data-stu-id="f2ec1-116">Abstract, base class that implements method parameters derived from this class.</span></span> |



 

## <a name="wmi-management-classes"></a><span data-ttu-id="f2ec1-117">Classes de gerenciamento do WMI</span><span class="sxs-lookup"><span data-stu-id="f2ec1-117">WMI Management Classes</span></span>

<span data-ttu-id="f2ec1-118">As classes de gerenciamento do WMI representam parâmetros operacionais para o serviço WMI.</span><span class="sxs-lookup"><span data-stu-id="f2ec1-118">The WMI management classes represent operational parameters for the WMI service.</span></span>

<span data-ttu-id="f2ec1-119">Veja a seguir uma tabela de classes de gerenciamento de WMI.</span><span class="sxs-lookup"><span data-stu-id="f2ec1-119">The following is a table of WMI management classes.</span></span>



| <span data-ttu-id="f2ec1-120">Classe</span><span class="sxs-lookup"><span data-stu-id="f2ec1-120">Class</span></span>                                                       | <span data-ttu-id="f2ec1-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="f2ec1-121">Description</span></span>                                                                                   |
|-------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f2ec1-122">**\_WMISetting Win32**</span><span class="sxs-lookup"><span data-stu-id="f2ec1-122">**Win32\_WMISetting**</span></span>](win32-wmisetting.md)               | <span data-ttu-id="f2ec1-123">Contém os parâmetros operacionais para o serviço WMI.</span><span class="sxs-lookup"><span data-stu-id="f2ec1-123">Contains the operational parameters for the WMI service.</span></span>                                      |
| [<span data-ttu-id="f2ec1-124">**\_WMIElementSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="f2ec1-124">**Win32\_WMIElementSetting**</span></span>](win32-wmielementsetting.md) | <span data-ttu-id="f2ec1-125">Associação entre um serviço em execução no sistema Windows e as configurações de WMI que ele pode usar.</span><span class="sxs-lookup"><span data-stu-id="f2ec1-125">Association between a service running in the Windows system, and the WMI settings it can use.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="f2ec1-126">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f2ec1-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f2ec1-127">Classes Win32</span><span class="sxs-lookup"><span data-stu-id="f2ec1-127">Win32 Classes</span></span>](./win32-provider.md)
</dt> </dl>

 

 
