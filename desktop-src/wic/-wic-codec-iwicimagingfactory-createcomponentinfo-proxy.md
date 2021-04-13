---
description: Função de proxy para o método CreateComponentInfo.
ms.assetid: 7d3b791a-d65e-4b90-8050-373a949e6d9c
title: Função IWICImagingFactory_CreateComponentInfo_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateComponentInfo_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 208b8b09b402e01f59a925f3dc6de6694b196db2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297221"
---
# <a name="iwicimagingfactory_createcomponentinfo_proxy-function"></a><span data-ttu-id="a3e2e-103">\_Função de \_ proxy IWICImagingFactory CreateComponentInfo</span><span class="sxs-lookup"><span data-stu-id="a3e2e-103">IWICImagingFactory\_CreateComponentInfo\_Proxy function</span></span>

<span data-ttu-id="a3e2e-104">Função de proxy para o método [**CreateComponentInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createcomponentinfo) .</span><span class="sxs-lookup"><span data-stu-id="a3e2e-104">Proxy function for the [**CreateComponentInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createcomponentinfo) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3e2e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a3e2e-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreateComponentInfo_Proxy(
  _In_  IWICImagingFactory *pFactory,
  _In_  REFCLSID           clsidComponent,
  _Out_ IWICComponentInfo  **ppIInfo
);
```



## <a name="parameters"></a><span data-ttu-id="a3e2e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a3e2e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3e2e-107">*pFactory* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a3e2e-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3e2e-108">Tipo: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="a3e2e-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

</dd> <dt>

<span data-ttu-id="a3e2e-109">_clsidComponent \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a3e2e-109">_clsidComponent\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3e2e-110">Tipo: **REFCLSID**</span><span class="sxs-lookup"><span data-stu-id="a3e2e-110">Type: **REFCLSID**</span></span>

<span data-ttu-id="a3e2e-111">O CLSID para o componente desejado.</span><span class="sxs-lookup"><span data-stu-id="a3e2e-111">The CLSID for the desired component.</span></span>

</dd> <dt>

<span data-ttu-id="a3e2e-112">*ppIInfo* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="a3e2e-112">*ppIInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a3e2e-113">Tipo: **[ **IWICComponentInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo)\*\***</span><span class="sxs-lookup"><span data-stu-id="a3e2e-113">Type: **[**IWICComponentInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo)\*\***</span></span>

<span data-ttu-id="a3e2e-114">Um ponteiro que recebe um ponteiro para um novo [**IWICComponentInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo).</span><span class="sxs-lookup"><span data-stu-id="a3e2e-114">A pointer that receives a pointer to a new [**IWICComponentInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3e2e-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a3e2e-115">Return value</span></span>

<span data-ttu-id="a3e2e-116">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="a3e2e-116">Type: **HRESULT**</span></span>

<span data-ttu-id="a3e2e-117">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="a3e2e-117">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a3e2e-118">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a3e2e-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="a3e2e-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="a3e2e-119">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="a3e2e-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a3e2e-120">Requirements</span></span>



| <span data-ttu-id="a3e2e-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="a3e2e-121">Requirement</span></span> | <span data-ttu-id="a3e2e-122">Valor</span><span class="sxs-lookup"><span data-stu-id="a3e2e-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3e2e-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a3e2e-123">Minimum supported client</span></span><br/> | <span data-ttu-id="a3e2e-124">Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a3e2e-124">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="a3e2e-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a3e2e-125">Minimum supported server</span></span><br/> | <span data-ttu-id="a3e2e-126">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a3e2e-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="a3e2e-127">DLL</span><span class="sxs-lookup"><span data-stu-id="a3e2e-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a3e2e-128"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a3e2e-128"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




