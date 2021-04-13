---
title: Método setnotify IAMWMBufferPass
description: O método setnotificate é usado por aplicativos para fornecer o filtro de leitura ASF do WM ou do leitor ASF do WM com um ponteiro para a interface IAMWMBufferPassCallback do aplicativo.
ms.assetid: b0fff344-a20c-4cfc-828b-c6fc49d990ea
keywords:
- Método setnotify Windows Media Format
- Método setnotify Windows Media Format, interface IAMWMBufferPass
- IAMWMBufferPass interface Windows Media Format, método setnotificate
topic_type:
- apiref
api_name:
- IAMWMBufferPass.SetNotify
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9739952792fcfa49da1b5656db513c3af41a419c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366547"
---
# <a name="iamwmbufferpasssetnotify-method"></a><span data-ttu-id="f2e12-106">Método IAMWMBufferPass:: setnotificar</span><span class="sxs-lookup"><span data-stu-id="f2e12-106">IAMWMBufferPass::SetNotify method</span></span>

<span data-ttu-id="f2e12-107">O método **Setnotificate** é usado por aplicativos para fornecer o filtro de leitura ASF do WM ou do [leitor ASF do WM](wm-asf-reader-filter.md) com um ponteiro para a interface [**IAMWMBufferPassCallback**](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpasscallback) do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f2e12-107">The **SetNotify** method is used by applications to provide the WM ASF Writer or [WM ASF Reader](wm-asf-reader-filter.md) filter with a pointer to the application's [**IAMWMBufferPassCallback**](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpasscallback) interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2e12-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f2e12-108">Syntax</span></span>


```C++
HRESULT SetNotify(
  [in] IAMWMBufferPassCallback *pCallback
);
```



## <a name="parameters"></a><span data-ttu-id="f2e12-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f2e12-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2e12-110">*pCallback* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f2e12-110">*pCallback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2e12-111">Ponteiro para a interface **IAMWMBufferPassCallback** do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f2e12-111">Pointer to the application's **IAMWMBufferPassCallback** interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2e12-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f2e12-112">Return value</span></span>

<span data-ttu-id="f2e12-113">Se o método for bem sucedido, ele retornará S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f2e12-113">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="f2e12-114">Se falhar, ele retornará um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f2e12-114">If it fails, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f2e12-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="f2e12-115">Remarks</span></span>

<span data-ttu-id="f2e12-116">Chame esse método antes de colocar o gráfico de filtro no estado de execução.</span><span class="sxs-lookup"><span data-stu-id="f2e12-116">Call this method before putting the filter graph into the run state.</span></span>

## <a name="see-also"></a><span data-ttu-id="f2e12-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="f2e12-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2e12-118">**Interface IAMWMBufferPass**</span><span class="sxs-lookup"><span data-stu-id="f2e12-118">**IAMWMBufferPass Interface**</span></span>](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpass)
</dt> </dl>

 

 