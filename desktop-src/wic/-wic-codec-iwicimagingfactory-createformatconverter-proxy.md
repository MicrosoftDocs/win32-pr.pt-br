---
description: Função de proxy para o método createformaconverter.
ms.assetid: 1013720a-d00e-4381-af5d-747806546692
title: Função IWICImagingFactory_CreateFormatConverter_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateFormatConverter_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 91e0d87a57326e413e725e056bd5f44aff152934
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171152"
---
# <a name="iwicimagingfactory_createformatconverter_proxy-function"></a><span data-ttu-id="86857-103">\_Função de proxy IWICImagingFactory CreateFormat \_</span><span class="sxs-lookup"><span data-stu-id="86857-103">IWICImagingFactory\_CreateFormatConverter\_Proxy function</span></span>

<span data-ttu-id="86857-104">Função de proxy para o método [**Createformaconverter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createformatconverter) .</span><span class="sxs-lookup"><span data-stu-id="86857-104">Proxy function for the [**CreateFormatConverter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createformatconverter) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="86857-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="86857-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreateFormatConverter_Proxy(
  _In_  IWICImagingFactory  *pFactory,
  _Out_ IWICFormatConverter **ppIFormatConverter
);
```



## <a name="parameters"></a><span data-ttu-id="86857-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="86857-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86857-107">*pFactory* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="86857-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86857-108">Tipo: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="86857-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

</dd> <dt>

<span data-ttu-id="86857-109">_ppIFormatConverter \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="86857-109">_ppIFormatConverter\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="86857-110">Tipo: **[ **IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter)\*\***</span><span class="sxs-lookup"><span data-stu-id="86857-110">Type: **[**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter)\*\***</span></span>

<span data-ttu-id="86857-111">Um ponteiro que recebe um ponteiro para um novo [**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter).</span><span class="sxs-lookup"><span data-stu-id="86857-111">A pointer that receives a pointer to a new [**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86857-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="86857-112">Return value</span></span>

<span data-ttu-id="86857-113">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="86857-113">Type: **HRESULT**</span></span>

<span data-ttu-id="86857-114">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="86857-114">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="86857-115">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="86857-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="86857-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="86857-116">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="86857-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="86857-117">Requirements</span></span>



| <span data-ttu-id="86857-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="86857-118">Requirement</span></span> | <span data-ttu-id="86857-119">Valor</span><span class="sxs-lookup"><span data-stu-id="86857-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="86857-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="86857-120">Minimum supported client</span></span><br/> | <span data-ttu-id="86857-121">Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="86857-121">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="86857-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="86857-122">Minimum supported server</span></span><br/> | <span data-ttu-id="86857-123">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="86857-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="86857-124">DLL</span><span class="sxs-lookup"><span data-stu-id="86857-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="86857-125"><dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt></span><span class="sxs-lookup"><span data-stu-id="86857-125"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




