---
title: Método de redefinição de IEnumBackgroundCopyFiles (Deliveryoptimization. h)
description: 'Método IEnumBackgroundCopyFiles:: Reset – redefine a sequência de enumeração para o início.'
ms.assetid: 6A303069-105C-4053-A8C5-2ECF60E789DE
keywords:
- Método Reset
- Método Reset, interface IEnumBackgroundCopyFiles
- Interface IEnumBackgroundCopyFiles, Método Reset
topic_type:
- apiref
api_name:
- IEnumBackgroundCopyFiles.Reset
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d6800095d0a6f20ef8b632830a224d4da27356bf
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105484"
---
# <a name="ienumbackgroundcopyfilesreset-method"></a><span data-ttu-id="07f1f-106">Método IEnumBackgroundCopyFiles:: Reset</span><span class="sxs-lookup"><span data-stu-id="07f1f-106">IEnumBackgroundCopyFiles::Reset method</span></span>

<span data-ttu-id="07f1f-107">Redefine a sequência de enumeração para o início.</span><span class="sxs-lookup"><span data-stu-id="07f1f-107">Resets the enumeration sequence to the beginning.</span></span>

## <a name="syntax"></a><span data-ttu-id="07f1f-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="07f1f-108">Syntax</span></span>


```C++
HRESULT Reset();
```



## <a name="parameters"></a><span data-ttu-id="07f1f-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="07f1f-109">Parameters</span></span>

<span data-ttu-id="07f1f-110">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="07f1f-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="07f1f-111">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="07f1f-111">Return value</span></span>

<span data-ttu-id="07f1f-112">Esse método retorna **S_OK** em caso de êxito ou um dos valores padrão com **HRESULT** em erro.</span><span class="sxs-lookup"><span data-stu-id="07f1f-112">This method returns **S_OK** on success or one of the standard COM **HRESULT** values on error.</span></span>

## <a name="requirements"></a><span data-ttu-id="07f1f-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="07f1f-113">Requirements</span></span>



| <span data-ttu-id="07f1f-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="07f1f-114">Requirement</span></span> | <span data-ttu-id="07f1f-115">Valor</span><span class="sxs-lookup"><span data-stu-id="07f1f-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07f1f-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="07f1f-116">Minimum supported client</span></span><br/> | <span data-ttu-id="07f1f-117">\[Somente aplicativos da área de trabalho do Windows 10, versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="07f1f-117">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="07f1f-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="07f1f-118">Minimum supported server</span></span><br/> | <span data-ttu-id="07f1f-119">Windows Server, \[ somente aplicativos da área de trabalho da versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="07f1f-119">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="07f1f-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="07f1f-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="07f1f-121"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="07f1f-121"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="07f1f-122">INSERI</span><span class="sxs-lookup"><span data-stu-id="07f1f-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="07f1f-123"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="07f1f-123"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="07f1f-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="07f1f-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="07f1f-125"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="07f1f-125"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="07f1f-126">DLL</span><span class="sxs-lookup"><span data-stu-id="07f1f-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="07f1f-127"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="07f1f-127"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="07f1f-128">IID</span><span class="sxs-lookup"><span data-stu-id="07f1f-128">IID</span></span><br/>                      | <span data-ttu-id="07f1f-129">IID_IEnumBackgroundCopyFiles é definido como CA51E165-C365-424C-8D41-24AAA4FF3C40</span><span class="sxs-lookup"><span data-stu-id="07f1f-129">IID_IEnumBackgroundCopyFiles is defined as CA51E165-C365-424C-8D41-24AAA4FF3C40</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="07f1f-130">Consulte também</span><span class="sxs-lookup"><span data-stu-id="07f1f-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07f1f-131">**IEnumBackgroundCopyFiles**</span><span class="sxs-lookup"><span data-stu-id="07f1f-131">**IEnumBackgroundCopyFiles**</span></span>](ienumbackgroundcopyfiles-.md)
</dt> </dl>

 

 





