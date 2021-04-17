---
title: Método GetParam IConfigAsfWriter2
description: O método GetParam recupera o valor atual do parâmetro de configuração de filtro especificado.
ms.assetid: 81d915a1-6190-46e3-a5cb-7f5fc242b8dd
keywords:
- Método GetParam formato de mídia do Windows
- Método GetParam Windows Media Format, interface IConfigAsfWriter2
- IConfigAsfWriter2 interface formato Windows Media, método GetParam
topic_type:
- apiref
api_name:
- IConfigAsfWriter2.GetParam
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d72b8011072424679729686dd5a14c92bae90f66
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105811537"
---
# <a name="iconfigasfwriter2getparam-method"></a><span data-ttu-id="4e46d-106">Método IConfigAsfWriter2:: GetParam</span><span class="sxs-lookup"><span data-stu-id="4e46d-106">IConfigAsfWriter2::GetParam method</span></span>

<span data-ttu-id="4e46d-107">O método **GetParam** recupera o valor atual do parâmetro de configuração de filtro especificado.</span><span class="sxs-lookup"><span data-stu-id="4e46d-107">The **GetParam** method retrieves the current value of the specified filter configuration parameter.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e46d-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4e46d-108">Syntax</span></span>


```C++
HRESULT GetParam(
  [in]  DWORD dwParam,
  [out] DWORD *pdwParam1,
  [out] DWORD *pdwParam2
);
```



## <a name="parameters"></a><span data-ttu-id="4e46d-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4e46d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e46d-110">*dwParam* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4e46d-110">*dwParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e46d-111">Especifica o parâmetro a recuperar.</span><span class="sxs-lookup"><span data-stu-id="4e46d-111">Specifies the parameter to retrieve.</span></span> <span data-ttu-id="4e46d-112">Ele deve ser um valor definido na enumeração do [ \_ \_ \_ parâmetro am ASFWRITERCONFIG](/previous-versions/windows/desktop/legacy/dd758054(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="4e46d-112">It must be a value defined in the [\_AM\_ASFWRITERCONFIG\_PARAM](/previous-versions/windows/desktop/legacy/dd758054(v=vs.85)) enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="4e46d-113">*pdwParam1* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="4e46d-113">*pdwParam1* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4e46d-114">Ponteiro para uma variável que recupera o valor do parâmetro especificado em *dwParam*.</span><span class="sxs-lookup"><span data-stu-id="4e46d-114">Pointer to a variable that retrieves the value of the parameter specified in *dwParam*.</span></span>

</dd> <dt>

<span data-ttu-id="4e46d-115">*pdwParam2* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="4e46d-115">*pdwParam2* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4e46d-116">Não usado, deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="4e46d-116">Not used, must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e46d-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4e46d-117">Return value</span></span>

<span data-ttu-id="4e46d-118">Se o método for bem sucedido, ele retornará S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="4e46d-118">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="4e46d-119">Se falhar, ele retornará um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4e46d-119">If it fails, it returns an **HRESULT** error code.</span></span>

## <a name="see-also"></a><span data-ttu-id="4e46d-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="4e46d-120">See also</span></span>

<dl> <dt>

<span data-ttu-id="4e46d-121">[**Interface IConfigAsfWriter2**](/previous-versions/windows/desktop/legacy/dd743206(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4e46d-121">[**IConfigAsfWriter2 Interface**](/previous-versions/windows/desktop/legacy/dd743206(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="4e46d-122">**IConfigAsfWriter2:: SetParam**</span><span class="sxs-lookup"><span data-stu-id="4e46d-122">**IConfigAsfWriter2::SetParam**</span></span>](iconfigasfwriter2-setparam.md)
</dt> </dl>

 

 