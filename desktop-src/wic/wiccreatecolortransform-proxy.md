---
description: Cria um objeto de transformação de cor que implementa IWICColorTransform. Este objeto COM dá suporte ao modelo de objeto de thread livre.
ms.assetid: 43DCC3FB-B687-45F0-AAC6-DED76214716C
title: Função WICCreateColorTransform_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WICCreateColorTransform_Proxy
api_type:
- DllExport
api_location:
- WindowsCodecsExt.dll
ms.openlocfilehash: 451b549aa44e785e406f50ccf4eb7a8317edf6b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810868"
---
# <a name="wiccreatecolortransform_proxy-function"></a><span data-ttu-id="73d4c-104">\_Função de proxy WICCreateColorTransform</span><span class="sxs-lookup"><span data-stu-id="73d4c-104">WICCreateColorTransform\_Proxy function</span></span>

<span data-ttu-id="73d4c-105">Cria um objeto de transformação de cor que implementa [**IWICColorTransform**](/windows/win32/api/wincodec/nn-wincodec-iwiccolortransform).</span><span class="sxs-lookup"><span data-stu-id="73d4c-105">Creates an color transform object that implements [**IWICColorTransform**](/windows/win32/api/wincodec/nn-wincodec-iwiccolortransform).</span></span> <span data-ttu-id="73d4c-106">Este objeto COM dá suporte ao modelo de objeto de thread livre.</span><span class="sxs-lookup"><span data-stu-id="73d4c-106">This COM object supports the free-threaded object model.</span></span>

## <a name="syntax"></a><span data-ttu-id="73d4c-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="73d4c-107">Syntax</span></span>


```C++
HRESULT WINAPI WICCreateColorTransform_Proxy(
  _Out_  **ppIColorTransform
);
```



## <a name="parameters"></a><span data-ttu-id="73d4c-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="73d4c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73d4c-109">*ppIColorTransform* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="73d4c-109">*ppIColorTransform* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="73d4c-110">A transformação de cor criada.</span><span class="sxs-lookup"><span data-stu-id="73d4c-110">The color transform created.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73d4c-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="73d4c-111">Return value</span></span>

<span data-ttu-id="73d4c-112">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="73d4c-112">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="73d4c-113">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="73d4c-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="73d4c-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="73d4c-114">Requirements</span></span>



| <span data-ttu-id="73d4c-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="73d4c-115">Requirement</span></span> | <span data-ttu-id="73d4c-116">Valor</span><span class="sxs-lookup"><span data-stu-id="73d4c-116">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="73d4c-117">DLL</span><span class="sxs-lookup"><span data-stu-id="73d4c-117">DLL</span></span><br/> | <dl> <span data-ttu-id="73d4c-118"><dt>WindowsCodecsExt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="73d4c-118"><dt>WindowsCodecsExt.dll</dt></span></span> </dl> |



 

 
