---
title: Método SetParam IConfigAsfWriter2
description: O método SetParam define o valor do parâmetro de configuração de filtro especificado.
ms.assetid: b8067fb2-c379-4b26-b4f7-c790604e3edc
keywords:
- Método SetParam Windows Media Format
- Método SetParam Windows Media Format, interface IConfigAsfWriter2
- IConfigAsfWriter2 interface formato Windows Media, método SetParam
topic_type:
- apiref
api_name:
- IConfigAsfWriter2.SetParam
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8f123bf11c8297f3a7ce0d4b0047874d8d7b31b1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105811536"
---
# <a name="iconfigasfwriter2setparam-method"></a><span data-ttu-id="e023d-106">Método IConfigAsfWriter2:: SetParam</span><span class="sxs-lookup"><span data-stu-id="e023d-106">IConfigAsfWriter2::SetParam method</span></span>

<span data-ttu-id="e023d-107">O método **SetParam** define o valor do parâmetro de configuração de filtro especificado.</span><span class="sxs-lookup"><span data-stu-id="e023d-107">The **SetParam** method sets the value of the specified filter configuration parameter.</span></span>

## <a name="syntax"></a><span data-ttu-id="e023d-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e023d-108">Syntax</span></span>


```C++
HRESULT SetParam(
  [in] DWORD dwParam,
  [in] DWORD dwParam1,
  [in] DWORD dwParam2
);
```



## <a name="parameters"></a><span data-ttu-id="e023d-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e023d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e023d-110">*dwParam* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e023d-110">*dwParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e023d-111">Especifica o parâmetro a ser definido.</span><span class="sxs-lookup"><span data-stu-id="e023d-111">Specifies the parameter to set.</span></span> <span data-ttu-id="e023d-112">Ele deve ser um valor definido na enumeração do [ \_ \_ \_ parâmetro am ASFWRITERCONFIG](/previous-versions/windows/desktop/legacy/dd758054(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="e023d-112">It must be a value defined in the [\_AM\_ASFWRITERCONFIG\_PARAM](/previous-versions/windows/desktop/legacy/dd758054(v=vs.85)) enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="e023d-113">*dwParam1* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e023d-113">*dwParam1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e023d-114">Especifica o valor a ser atribuído ao parâmetro *dwParam* .</span><span class="sxs-lookup"><span data-stu-id="e023d-114">Specifies the value to assign to the *dwParam* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="e023d-115">*dwParam2* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e023d-115">*dwParam2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e023d-116">Não usado; deve ser 0.</span><span class="sxs-lookup"><span data-stu-id="e023d-116">Not used; must be 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e023d-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e023d-117">Return value</span></span>

<span data-ttu-id="e023d-118">Se o método for bem sucedido, ele retornará S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e023d-118">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="e023d-119">Se falhar, ele retornará um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e023d-119">If it fails, it returns an **HRESULT** error code.</span></span>

## <a name="see-also"></a><span data-ttu-id="e023d-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="e023d-120">See also</span></span>

<dl> <dt>

<span data-ttu-id="e023d-121">[**Interface IConfigAsfWriter2**](/previous-versions/windows/desktop/legacy/dd743206(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e023d-121">[**IConfigAsfWriter2 Interface**](/previous-versions/windows/desktop/legacy/dd743206(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="e023d-122">**IConfigAsfWriter2:: GetParam**</span><span class="sxs-lookup"><span data-stu-id="e023d-122">**IConfigAsfWriter2::GetParam**</span></span>](iconfigasfwriter2-getparam.md)
</dt> </dl>

 

 