---
title: Método GetStats IDeliveryOptimizationFile (Deliveryoptimization. h)
description: Retorna o download e o upload de estatísticas para um arquivo específico.
ms.assetid: 8A3AD658-F1AD-4EA5-B010-AB7B88126FD6
keywords:
- Método GetStats
- Método GetStats, interface IDeliveryOptimizationFile
- Interface IDeliveryOptimizationFile, método GetStats
topic_type:
- apiref
api_name:
- IDeliveryOptimizationFile.GetStats
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 08c5cff0672130049c325a00cb63c8dbc5c2e8ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369831"
---
# <a name="ideliveryoptimizationfilegetstats-method"></a><span data-ttu-id="ab798-106">Método IDeliveryOptimizationFile:: GetStats</span><span class="sxs-lookup"><span data-stu-id="ab798-106">IDeliveryOptimizationFile::GetStats method</span></span>

<span data-ttu-id="ab798-107">Retorna o download e o upload de estatísticas para um arquivo específico.</span><span class="sxs-lookup"><span data-stu-id="ab798-107">Returns download and upload stats for a specific file.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab798-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ab798-108">Syntax</span></span>


```C++
HRESULT GetStats(
  [out] DOSwarmStats *swarmStats
);
```



## <a name="parameters"></a><span data-ttu-id="ab798-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ab798-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab798-110">*swarmStats* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="ab798-110">*swarmStats* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ab798-111">Retorna o download e o upload de estatísticas para um arquivo específico.</span><span class="sxs-lookup"><span data-stu-id="ab798-111">Returns download and upload stats for a specific file.</span></span> <span data-ttu-id="ab798-112">Consulte a estrutura [**DOSwarmStats**](doswarmstats.md) para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="ab798-112">See the [**DOSwarmStats**](doswarmstats.md) structure for details.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ab798-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ab798-113">Return value</span></span>

<span data-ttu-id="ab798-114">Esse método deve retornar **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="ab798-114">This method should return **S_OK**.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab798-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ab798-115">Requirements</span></span>



| <span data-ttu-id="ab798-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="ab798-116">Requirement</span></span> | <span data-ttu-id="ab798-117">Valor</span><span class="sxs-lookup"><span data-stu-id="ab798-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab798-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ab798-118">Minimum supported client</span></span><br/> | <span data-ttu-id="ab798-119">\[Somente aplicativos da área de trabalho do Windows 10, versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="ab798-119">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="ab798-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ab798-120">Minimum supported server</span></span><br/> | <span data-ttu-id="ab798-121">Windows Server, \[ somente aplicativos da área de trabalho da versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="ab798-121">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="ab798-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ab798-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="ab798-123"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="ab798-123"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="ab798-124">INSERI</span><span class="sxs-lookup"><span data-stu-id="ab798-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ab798-125"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ab798-125"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="ab798-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ab798-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="ab798-127"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ab798-127"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="ab798-128">DLL</span><span class="sxs-lookup"><span data-stu-id="ab798-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ab798-129"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ab798-129"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="ab798-130">IID</span><span class="sxs-lookup"><span data-stu-id="ab798-130">IID</span></span><br/>                      | <span data-ttu-id="ab798-131">IID_IDeliveryOptimizationFile é definido como B76B9699-E99E-4101-803F-A20E325D93E2</span><span class="sxs-lookup"><span data-stu-id="ab798-131">IID_IDeliveryOptimizationFile is defined as B76B9699-E99E-4101-803F-A20E325D93E2</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="ab798-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="ab798-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab798-133">**IDeliveryOptimizationFile**</span><span class="sxs-lookup"><span data-stu-id="ab798-133">**IDeliveryOptimizationFile**</span></span>](ideliveryoptimizationfile.md)
</dt> </dl>

 

 





