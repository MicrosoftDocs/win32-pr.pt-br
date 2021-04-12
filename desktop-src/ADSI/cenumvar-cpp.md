---
title: CENUMVAR. CPP
description: No componente de provedor de exemplo, a implementação base para classes derivadas xxxEnumVariant pode ser encontrada em cenumvar. cpp. Os métodos associados são listados na tabela a seguir.
ms.assetid: 6b38bc99-25d4-40af-863a-9cc37f786d9b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d361cb7d3e2657a31645fba05aa2e1a23762a3fc
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104294494"
---
# <a name="cenumvarcpp"></a><span data-ttu-id="0c026-104">CENUMVAR. CPP</span><span class="sxs-lookup"><span data-stu-id="0c026-104">CENUMVAR.CPP</span></span>

<span data-ttu-id="0c026-105">No componente de provedor de exemplo, a implementação base para classes derivadas xxxEnumVariant pode ser encontrada em cenumvar. cpp.</span><span class="sxs-lookup"><span data-stu-id="0c026-105">In the example provider component, the base implementation for xxxEnumVariant derived classes can be found in cenumvar.cpp.</span></span> <span data-ttu-id="0c026-106">Os métodos associados são listados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="0c026-106">Associated methods are listed in the following table.</span></span>



| <span data-ttu-id="0c026-107">Método</span><span class="sxs-lookup"><span data-stu-id="0c026-107">Method</span></span>                                          | <span data-ttu-id="0c026-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="0c026-108">Description</span></span>                                                                           |
|-------------------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0c026-109">**CSampleDSEnumVariant::CSampleDSEnumVariant**</span><span class="sxs-lookup"><span data-stu-id="0c026-109">**CSampleDSEnumVariant::CSampleDSEnumVariant**</span></span>  | <span data-ttu-id="0c026-110">Construtor padrão.</span><span class="sxs-lookup"><span data-stu-id="0c026-110">Standard constructor.</span></span>                                                                 |
| <span data-ttu-id="0c026-111">**CSampleDSEnumVariant:: ~ CSampleDSEnumVariant**</span><span class="sxs-lookup"><span data-stu-id="0c026-111">**CSampleDSEnumVariant::~CSampleDSEnumVariant**</span></span> | <span data-ttu-id="0c026-112">Destruidor padrão.</span><span class="sxs-lookup"><span data-stu-id="0c026-112">Standard destructor.</span></span>                                                                  |
| <span data-ttu-id="0c026-113">**CSampleDSEnumVariant:: QueryInterface**</span><span class="sxs-lookup"><span data-stu-id="0c026-113">**CSampleDSEnumVariant::QueryInterface**</span></span>        | <span data-ttu-id="0c026-114">Implementação padrão [**IUnknown:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) .</span><span class="sxs-lookup"><span data-stu-id="0c026-114">Standard [**IUnknown::QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) implementation.</span></span> |
| <span data-ttu-id="0c026-115">**CSampleDSEnumVariant:: AddRef**</span><span class="sxs-lookup"><span data-stu-id="0c026-115">**CSampleDSEnumVariant::AddRef**</span></span>                | <span data-ttu-id="0c026-116">Implementação padrão [**IUnknown:: AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) .</span><span class="sxs-lookup"><span data-stu-id="0c026-116">Standard [**IUnknown::AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) implementation.</span></span>                 |
| <span data-ttu-id="0c026-117">**CSampleDSEnumVariant:: versão**</span><span class="sxs-lookup"><span data-stu-id="0c026-117">**CSampleDSEnumVariant::Release**</span></span>               | <span data-ttu-id="0c026-118">Implementação padrão [**IUnknown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) .</span><span class="sxs-lookup"><span data-stu-id="0c026-118">Standard [**IUnknown::Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) implementation.</span></span>               |
| <span data-ttu-id="0c026-119">**CSampleDSEnumVariant:: Skip**</span><span class="sxs-lookup"><span data-stu-id="0c026-119">**CSampleDSEnumVariant::Skip**</span></span>                  | <span data-ttu-id="0c026-120">Standard **IEnumXXXX:: ignorar** implementação.</span><span class="sxs-lookup"><span data-stu-id="0c026-120">Standard **IEnumXXXX::Skip** implementation.</span></span>                                          |
| <span data-ttu-id="0c026-121">**CSampleDSEnumVariant:: Reset**</span><span class="sxs-lookup"><span data-stu-id="0c026-121">**CSampleDSEnumVariant::Reset**</span></span>                 | <span data-ttu-id="0c026-122">Implementação padrão **IEnumXXXX:: Reset** .</span><span class="sxs-lookup"><span data-stu-id="0c026-122">Standard **IEnumXXXX::Reset** implementation.</span></span>                                         |
| <span data-ttu-id="0c026-123">**CSampleDSEnumVariant:: clone**</span><span class="sxs-lookup"><span data-stu-id="0c026-123">**CSampleDSEnumVariant::Clone**</span></span>                 | <span data-ttu-id="0c026-124">Implementação Standard **IEnumXXXX:: clone** .</span><span class="sxs-lookup"><span data-stu-id="0c026-124">Standard **IEnumXXXX::Clone** implementation.</span></span>                                         |



 

 

 