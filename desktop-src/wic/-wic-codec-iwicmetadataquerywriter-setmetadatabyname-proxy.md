---
description: Função de proxy para o método SetMetadataByName.
ms.assetid: 467d7735-152a-4e7c-93b1-fd031cc57c19
title: Função IWICMetadataQueryWriter_SetMetadataByName_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICMetadataQueryWriter_SetMetadataByName_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: e27ea57ec5b26fd2bed04ea99f6c6cbfb11c8874
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105768316"
---
# <a name="iwicmetadataquerywriter_setmetadatabyname_proxy-function"></a><span data-ttu-id="861b0-103">\_Função de \_ proxy IWICMetadataQueryWriter SetMetadataByName</span><span class="sxs-lookup"><span data-stu-id="861b0-103">IWICMetadataQueryWriter\_SetMetadataByName\_Proxy function</span></span>

<span data-ttu-id="861b0-104">Função de proxy para o método [**SetMetadataByName**](/windows/desktop/api/Wincodec/nf-wincodec-iwicmetadataquerywriter-setmetadatabyname) .</span><span class="sxs-lookup"><span data-stu-id="861b0-104">Proxy function for the [**SetMetadataByName**](/windows/desktop/api/Wincodec/nf-wincodec-iwicmetadataquerywriter-setmetadatabyname) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="861b0-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="861b0-105">Syntax</span></span>


```C++
HRESULT IWICMetadataQueryWriter_SetMetadataByName_Proxy(
  _In_       IWICMetadataQueryWriter *THIS_PTR,
  _In_       LPCWSTR                 wzName,
  _In_ const PROPVARIANT             *pvarValue
);
```



## <a name="parameters"></a><span data-ttu-id="861b0-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="861b0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="861b0-107">*Isso \_ PTR* \[\]</span><span class="sxs-lookup"><span data-stu-id="861b0-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="861b0-108">Tipo: \**[**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) \** _</span><span class="sxs-lookup"><span data-stu-id="861b0-108">Type: \**[**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\** _</span></span>

<span data-ttu-id="861b0-109">Ponteiro para este objeto [_ *IWICMetadataQueryWriter* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) .</span><span class="sxs-lookup"><span data-stu-id="861b0-109">Pointer to this [_ *IWICMetadataQueryWriter*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) object.</span></span>

</dd> <dt>

<span data-ttu-id="861b0-110">*wzName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="861b0-110">*wzName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="861b0-111">Tipo: **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="861b0-111">Type: **LPCWSTR**</span></span>

<span data-ttu-id="861b0-112">O nome do item de metadados.</span><span class="sxs-lookup"><span data-stu-id="861b0-112">The name of the metadata item.</span></span>

</dd> <dt>

<span data-ttu-id="861b0-113">*pvarValue* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="861b0-113">*pvarValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="861b0-114">Tipo: \**const [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) \** _</span><span class="sxs-lookup"><span data-stu-id="861b0-114">Type: \**const [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)\** _</span></span>

<span data-ttu-id="861b0-115">Os metadados a serem definidos.</span><span class="sxs-lookup"><span data-stu-id="861b0-115">The metadata to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="861b0-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="861b0-116">Return value</span></span>

<span data-ttu-id="861b0-117">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="861b0-117">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="861b0-118">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="861b0-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="861b0-119">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="861b0-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="861b0-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="861b0-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="861b0-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="861b0-121">Requirements</span></span>



| <span data-ttu-id="861b0-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="861b0-122">Requirement</span></span> | <span data-ttu-id="861b0-123">Valor</span><span class="sxs-lookup"><span data-stu-id="861b0-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="861b0-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="861b0-124">Minimum supported client</span></span><br/> | <span data-ttu-id="861b0-125">Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="861b0-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="861b0-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="861b0-126">Minimum supported server</span></span><br/> | <span data-ttu-id="861b0-127">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="861b0-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="861b0-128">DLL</span><span class="sxs-lookup"><span data-stu-id="861b0-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="861b0-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="861b0-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

