---
description: Função de proxy para o método GetCount.
ms.assetid: 441bbbaf-5a6a-4d1e-bb8d-f79af6aa2708
title: Função IWICMetadataBlockReader_GetCount_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICMetadataBlockReader_GetCount_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 09c3c33185791c2c2eefd3963a3d39977c706963
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171007"
---
# <a name="iwicmetadatablockreader_getcount_proxy-function"></a><span data-ttu-id="6f61e-103">Função de proxy do IWICMetadataBlockReader \_ GetCount \_</span><span class="sxs-lookup"><span data-stu-id="6f61e-103">IWICMetadataBlockReader\_GetCount\_Proxy function</span></span>

<span data-ttu-id="6f61e-104">Função de proxy para o método [**GetCount**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getcount) .</span><span class="sxs-lookup"><span data-stu-id="6f61e-104">Proxy function for the [**GetCount**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getcount) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f61e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6f61e-105">Syntax</span></span>


```C++
HRESULT IWICMetadataBlockReader_GetCount_Proxy(
  _In_  IWICMetadataBlockReader *THIS_PTR,
  _Out_ UINT                    *pcCount
);
```



## <a name="parameters"></a><span data-ttu-id="6f61e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6f61e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f61e-107">*Isso \_ PTR* \[\]</span><span class="sxs-lookup"><span data-stu-id="6f61e-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f61e-108">Tipo: \**[**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) \** _</span><span class="sxs-lookup"><span data-stu-id="6f61e-108">Type: \**[**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)\** _</span></span>

<span data-ttu-id="6f61e-109">Ponteiro para este objeto [_ *IWICMetadataBlockReader* \*](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) .</span><span class="sxs-lookup"><span data-stu-id="6f61e-109">Pointer to this [_ *IWICMetadataBlockReader*\*](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) object.</span></span>

</dd> <dt>

<span data-ttu-id="6f61e-110">*pcCount* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="6f61e-110">*pcCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6f61e-111">Tipo: \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="6f61e-111">Type: \**UINT\** _</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6f61e-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6f61e-112">Return value</span></span>

<span data-ttu-id="6f61e-113">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="6f61e-113">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="6f61e-114">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="6f61e-114">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="6f61e-115">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6f61e-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="6f61e-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="6f61e-116">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="6f61e-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6f61e-117">Requirements</span></span>



| <span data-ttu-id="6f61e-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="6f61e-118">Requirement</span></span> | <span data-ttu-id="6f61e-119">Valor</span><span class="sxs-lookup"><span data-stu-id="6f61e-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f61e-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6f61e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="6f61e-121">Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6f61e-121">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="6f61e-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6f61e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="6f61e-123">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="6f61e-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="6f61e-124">DLL</span><span class="sxs-lookup"><span data-stu-id="6f61e-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6f61e-125"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6f61e-125"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




