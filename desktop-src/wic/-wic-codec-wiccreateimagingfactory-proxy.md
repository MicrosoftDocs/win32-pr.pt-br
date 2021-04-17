---
description: Função de proxy para criar o IWICImagingFactory.
ms.assetid: e4f575b0-878f-461e-92e7-9494e505ea6f
title: Função WICCreateImagingFactory_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WICCreateImagingFactory_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Windowscodecs.lib
ms.openlocfilehash: 6717764d0c25d64f99ab5d864bd0e77a63b88330
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105765653"
---
# <a name="wiccreateimagingfactory_proxy-function"></a><span data-ttu-id="27dd2-103">\_Função de proxy WICCreateImagingFactory</span><span class="sxs-lookup"><span data-stu-id="27dd2-103">WICCreateImagingFactory\_Proxy function</span></span>

<span data-ttu-id="27dd2-104">Função de proxy para criar o [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory).</span><span class="sxs-lookup"><span data-stu-id="27dd2-104">Proxy function for creating the [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory).</span></span>

## <a name="syntax"></a><span data-ttu-id="27dd2-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="27dd2-105">Syntax</span></span>

```cpp
HRESULT WICCreateImagingFactory_Proxy(
  _In_  UINT               SDKVersion,
  _Out_ IWICImagingFactory **ppIImagingFactory
);
```

## <a name="parameters"></a><span data-ttu-id="27dd2-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="27dd2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="27dd2-107">*SDKVersion* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="27dd2-107">*SDKVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="27dd2-108">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="27dd2-108">Type: **UINT**</span></span>

</dd> <dt>

<span data-ttu-id="27dd2-109">*ppIImagingFactory* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="27dd2-109">*ppIImagingFactory* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="27dd2-110">Tipo: **[ **IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\*\***</span><span class="sxs-lookup"><span data-stu-id="27dd2-110">Type: **[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\*\***</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="27dd2-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="27dd2-111">Return value</span></span>

<span data-ttu-id="27dd2-112">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="27dd2-112">Type: **HRESULT**</span></span>

<span data-ttu-id="27dd2-113">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="27dd2-113">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="27dd2-114">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="27dd2-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="27dd2-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="27dd2-115">Remarks</span></span>

<span data-ttu-id="27dd2-116">Essa função é um auxiliar para criar uma fábrica de WIC para a vinculação de DLL explícita, que era necessária para o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="27dd2-116">This function is a helper for creating a WIC factory for explicit DLL linking, which was needed for Windows XP.</span></span> <span data-ttu-id="27dd2-117">No uso normal, você usaria [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) em vez disso (consulte [fábricas de classe da API do WIC](./-wic-api.md#class-factories)), já que isso é sempre incluído em todas as versões mais recentes do Windows.</span><span class="sxs-lookup"><span data-stu-id="27dd2-117">In normal usage, you would use [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) instead (see [WIC API class factories](./-wic-api.md#class-factories)), since that's always included in all newer versions of Windows.</span></span>

## <a name="requirements"></a><span data-ttu-id="27dd2-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="27dd2-118">Requirements</span></span>



| <span data-ttu-id="27dd2-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="27dd2-119">Requirement</span></span> | <span data-ttu-id="27dd2-120">Valor</span><span class="sxs-lookup"><span data-stu-id="27dd2-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="27dd2-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="27dd2-121">Minimum supported client</span></span><br/> | <span data-ttu-id="27dd2-122">Windows XP com SP2, \[ somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="27dd2-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="27dd2-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="27dd2-123">Minimum supported server</span></span><br/> | <span data-ttu-id="27dd2-124">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="27dd2-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="27dd2-125">DLL</span><span class="sxs-lookup"><span data-stu-id="27dd2-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="27dd2-126"><dt>Windowscodecs.dll; </dt> <dt>WindowsCodecs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="27dd2-126"><dt>Windowscodecs.dll; </dt> <dt>windowscodecs.lib</dt></span></span> </dl> |



 

