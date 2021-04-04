---
title: Referência de driver instalável
description: Referência de driver instalável
ms.assetid: 869b92f1-2711-4198-9911-3df1ebc58d5f
keywords:
- Multimídia do Windows, referência de driver instalável
- multimídia, referência de driver instalável
- drivers instaláveis, referência
- referência de driver instalável, sobre
- referência para drivers instaláveis, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e90475063f9d9211e841902fe73d2f09dc6130d8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103823693"
---
# <a name="installable-driver-reference"></a><span data-ttu-id="12057-108">Referência de driver instalável</span><span class="sxs-lookup"><span data-stu-id="12057-108">Installable Driver Reference</span></span>

<span data-ttu-id="12057-109">As funções e mensagens associadas a drivers instaláveis são agrupadas da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="12057-109">The functions and messages associated with installable drivers are grouped as follows.</span></span>

## <a name="loading-and-unloading-drivers"></a><span data-ttu-id="12057-110">Carregando e descarregando drivers</span><span class="sxs-lookup"><span data-stu-id="12057-110">Loading and Unloading Drivers</span></span>

-   [<span data-ttu-id="12057-111">GetDriverModuleHandle</span><span class="sxs-lookup"><span data-stu-id="12057-111">GetDriverModuleHandle</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-getdrivermodulehandle)
-   [<span data-ttu-id="12057-112">OpenDriver</span><span class="sxs-lookup"><span data-stu-id="12057-112">OpenDriver</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-opendriver)
-   [<span data-ttu-id="12057-113">SendDriverMessage</span><span class="sxs-lookup"><span data-stu-id="12057-113">SendDriverMessage</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-senddrivermessage)

## <a name="closedriver"></a><span data-ttu-id="12057-114">CloseDriver</span><span class="sxs-lookup"><span data-stu-id="12057-114">CloseDriver</span></span>

-   [<span data-ttu-id="12057-115">**fechamento de DRV \_**</span><span class="sxs-lookup"><span data-stu-id="12057-115">**DRV\_CLOSE**</span></span>](drv-close.md)
-   [<span data-ttu-id="12057-116">**\_desabilitar drv**</span><span class="sxs-lookup"><span data-stu-id="12057-116">**DRV\_DISABLE**</span></span>](drv-disable.md)
-   [<span data-ttu-id="12057-117">**\_habilitar drv**</span><span class="sxs-lookup"><span data-stu-id="12057-117">**DRV\_ENABLE**</span></span>](drv-enable.md)
-   [<span data-ttu-id="12057-118">**DRV \_ Free**</span><span class="sxs-lookup"><span data-stu-id="12057-118">**DRV\_FREE**</span></span>](drv-free.md)
-   [<span data-ttu-id="12057-119">**carregamento de DRV \_**</span><span class="sxs-lookup"><span data-stu-id="12057-119">**DRV\_LOAD**</span></span>](drv-load.md)
-   [<span data-ttu-id="12057-120">**DRV \_ Open**</span><span class="sxs-lookup"><span data-stu-id="12057-120">**DRV\_OPEN**</span></span>](drv-open.md)

## <a name="configuring-a-driver"></a><span data-ttu-id="12057-121">Configurando um driver</span><span class="sxs-lookup"><span data-stu-id="12057-121">Configuring a Driver</span></span>

-   [<span data-ttu-id="12057-122">**\_Configurar drv**</span><span class="sxs-lookup"><span data-stu-id="12057-122">**DRV\_CONFIGURE**</span></span>](drv-configure.md)
-   [<span data-ttu-id="12057-123">**\_QUERYCONFIGURE drv**</span><span class="sxs-lookup"><span data-stu-id="12057-123">**DRV\_QUERYCONFIGURE**</span></span>](drv-queryconfigure.md)
-   [<span data-ttu-id="12057-124">**DRVCONFIGINFO**</span><span class="sxs-lookup"><span data-stu-id="12057-124">**DRVCONFIGINFO**</span></span>](/windows/win32/api/mmiscapi/ns-mmiscapi-drvconfiginfo)

## <a name="installing-a-driver"></a><span data-ttu-id="12057-125">Instalando um driver</span><span class="sxs-lookup"><span data-stu-id="12057-125">Installing a Driver</span></span>

-   [<span data-ttu-id="12057-126">**instalação do DRV \_**</span><span class="sxs-lookup"><span data-stu-id="12057-126">**DRV\_INSTALL**</span></span>](drv-install.md)
-   [<span data-ttu-id="12057-127">**remoção de DRV \_**</span><span class="sxs-lookup"><span data-stu-id="12057-127">**DRV\_REMOVE**</span></span>](drv-remove.md)

## <a name="driver-functions"></a><span data-ttu-id="12057-128">Funções de driver</span><span class="sxs-lookup"><span data-stu-id="12057-128">Driver Functions</span></span>

-   [<span data-ttu-id="12057-129">DefDriverProc</span><span class="sxs-lookup"><span data-stu-id="12057-129">DefDriverProc</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-defdriverproc)
-   [<span data-ttu-id="12057-130">DriverCallback</span><span class="sxs-lookup"><span data-stu-id="12057-130">DriverCallback</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-drivercallback)
-   [<span data-ttu-id="12057-131">DriverProc</span><span class="sxs-lookup"><span data-stu-id="12057-131">DriverProc</span></span>](/windows/win32/api/mmiscapi/nc-mmiscapi-driverproc)

## <a name="related-topics"></a><span data-ttu-id="12057-132">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="12057-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="12057-133">Drivers instaláveis</span><span class="sxs-lookup"><span data-stu-id="12057-133">Installable Drivers</span></span>](installable-drivers.md)
</dt> </dl>

 

 