---
title: Interface IDeliveryOptimizationJob (Deliveryoptimization. h)
description: Use a interface IDeliveryOptimizationJob para baixar intervalos de um arquivo.
ms.assetid: 7549F3B2-47E9-44DA-BD9C-AEFB0C36FF15
keywords:
- Interface IDeliveryOptimizationJob
- Interface IDeliveryOptimizationJob, descrita
topic_type:
- apiref
api_name:
- IDeliveryOptimizationJob
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6ee2ce35b8089e9b05b7291f535361e39140f856
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085547"
---
# <a name="ideliveryoptimizationjob-interface"></a><span data-ttu-id="616e4-105">Interface IDeliveryOptimizationJob</span><span class="sxs-lookup"><span data-stu-id="616e4-105">IDeliveryOptimizationJob interface</span></span>

<span data-ttu-id="616e4-106">Use a interface **IDeliveryOptimizationJob** para baixar intervalos de um arquivo.</span><span class="sxs-lookup"><span data-stu-id="616e4-106">Use the **IDeliveryOptimizationJob** interface to download ranges of a file.</span></span>

## <a name="members"></a><span data-ttu-id="616e4-107">Membros</span><span class="sxs-lookup"><span data-stu-id="616e4-107">Members</span></span>

<span data-ttu-id="616e4-108">A interface **IDeliveryOptimizationJob** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="616e4-108">The **IDeliveryOptimizationJob** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="616e4-109">**IDeliveryOptimizationJob** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="616e4-109">**IDeliveryOptimizationJob** also has these types of members:</span></span>

- [<span data-ttu-id="616e4-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="616e4-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="616e4-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="616e4-111">Methods</span></span>

<span data-ttu-id="616e4-112">A interface **IDeliveryOptimizationJob** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="616e4-112">The **IDeliveryOptimizationJob** interface has these methods.</span></span>



| <span data-ttu-id="616e4-113">Método</span><span class="sxs-lookup"><span data-stu-id="616e4-113">Method</span></span>                                                                  | <span data-ttu-id="616e4-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="616e4-114">Description</span></span>                                                                                         |
|:------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="616e4-115">**AddFileWithRanges**</span><span class="sxs-lookup"><span data-stu-id="616e4-115">**AddFileWithRanges**</span></span>](ideliveryoptimizationjob-addfilewithranges.md) | <span data-ttu-id="616e4-116">Adiciona um arquivo a um trabalho de download e especifica os intervalos do arquivo que você deseja baixar.</span><span class="sxs-lookup"><span data-stu-id="616e4-116">Adds a file to a download job and specifies the ranges of the file you want to download.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="616e4-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="616e4-117">Requirements</span></span>



| <span data-ttu-id="616e4-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="616e4-118">Requirement</span></span> | <span data-ttu-id="616e4-119">Valor</span><span class="sxs-lookup"><span data-stu-id="616e4-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="616e4-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="616e4-120">Minimum supported client</span></span><br/> | <span data-ttu-id="616e4-121">\[Somente aplicativos da área de trabalho do Windows 10, versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="616e4-121">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="616e4-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="616e4-122">Minimum supported server</span></span><br/> | <span data-ttu-id="616e4-123">Windows Server, \[ somente aplicativos da área de trabalho da versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="616e4-123">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="616e4-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="616e4-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="616e4-125"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="616e4-125"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="616e4-126">INSERI</span><span class="sxs-lookup"><span data-stu-id="616e4-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="616e4-127"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="616e4-127"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="616e4-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="616e4-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="616e4-129"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="616e4-129"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="616e4-130">DLL</span><span class="sxs-lookup"><span data-stu-id="616e4-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="616e4-131"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="616e4-131"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="616e4-132">IID</span><span class="sxs-lookup"><span data-stu-id="616e4-132">IID</span></span><br/>                      | <span data-ttu-id="616e4-133">IID_IDeliveryOptimizationJob é definido como EE2584CF-A69C-4848-B633-2649962B3EF7</span><span class="sxs-lookup"><span data-stu-id="616e4-133">IID_IDeliveryOptimizationJob is defined as EE2584CF-A69C-4848-B633-2649962B3EF7</span></span><br/>         |



 

