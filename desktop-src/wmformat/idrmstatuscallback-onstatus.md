---
title: Método OnStatus IDRMStatusCallback
description: O método OnStatus recebe mensagens de status de processos DRM assíncronos.
ms.assetid: 2a128088-0924-4c54-b08d-a1c7ea91e541
keywords:
- Método OnStatus Windows Media Format
- Método OnStatus Windows Media Format, interface IDRMStatusCallback
- IDRMStatusCallback interface formato Windows Media, método OnStatus
topic_type:
- apiref
api_name:
- IDRMStatusCallback.OnStatus
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 754d59d74fb0365f423243e92565ac17b46628a5
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104006404"
---
# <a name="idrmstatuscallbackonstatus-method"></a><span data-ttu-id="a8b7c-106">Método IDRMStatusCallback:: OnStatus</span><span class="sxs-lookup"><span data-stu-id="a8b7c-106">IDRMStatusCallback::OnStatus method</span></span>

<span data-ttu-id="a8b7c-107">O método **OnStatus** recebe mensagens de status de processos DRM assíncronos.</span><span class="sxs-lookup"><span data-stu-id="a8b7c-107">The **OnStatus** method receives status messages from asynchronous DRM processes.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8b7c-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a8b7c-108">Syntax</span></span>


```C++
HRESULT OnStatus(
  [in] MSDRM_STATUS      Status,
  [in] HRESULT           hr,
  [in] DRM_ATTR_DATATYPE dwType,
  [in] BYTE              *pValue,
  [in] void              *pvContext
);
```



## <a name="parameters"></a><span data-ttu-id="a8b7c-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a8b7c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8b7c-110">*Status* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="a8b7c-110">*Status* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8b7c-111">Código de status.</span><span class="sxs-lookup"><span data-stu-id="a8b7c-111">Status code.</span></span> <span data-ttu-id="a8b7c-112">Os códigos de mensagem são definidos no tipo de enumeração **\_ status Msdrm** .</span><span class="sxs-lookup"><span data-stu-id="a8b7c-112">Message codes are defined in the **MSDRM\_STATUS** enumeration type.</span></span>

</dd> <dt>

<span data-ttu-id="a8b7c-113">*HR* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a8b7c-113">*hr* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8b7c-114">Código de retorno que dá suporte à mensagem de status.</span><span class="sxs-lookup"><span data-stu-id="a8b7c-114">Return code that supports the status message.</span></span>

</dd> <dt>

<span data-ttu-id="a8b7c-115">*dwType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a8b7c-115">*dwType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8b7c-116">Tipo dos dados apontados *por era*.</span><span class="sxs-lookup"><span data-stu-id="a8b7c-116">Type of the data pointed to by *pValue*.</span></span> <span data-ttu-id="a8b7c-117">Defina como um dos valores da enumeração de [**\_ tipo de \_ dados attr do DRM**](drm-attr-datatype.md) .</span><span class="sxs-lookup"><span data-stu-id="a8b7c-117">Set to one of the values of the [**DRM\_ATTR\_DATATYPE**](drm-attr-datatype.md) enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="a8b7c-118">*valores* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a8b7c-118">*pValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8b7c-119">Ponteiro para dados relacionados à mensagem de status.</span><span class="sxs-lookup"><span data-stu-id="a8b7c-119">Pointer to data related to the status message.</span></span> <span data-ttu-id="a8b7c-120">O tipo de dados é determinado pelo valor do parâmetro *dwType* .</span><span class="sxs-lookup"><span data-stu-id="a8b7c-120">The type of data is determined by the value of the *dwType* parameter.</span></span> <span data-ttu-id="a8b7c-121">Para obter mais informações, consulte a enumeração do [**\_ tipo de \_ dados attr do DRM**](drm-attr-datatype.md) .</span><span class="sxs-lookup"><span data-stu-id="a8b7c-121">For more information, see the [**DRM\_ATTR\_DATATYPE**](drm-attr-datatype.md) enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="a8b7c-122">*pvContext* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a8b7c-122">*pvContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8b7c-123">Parâmetro opcional que pode ser usado para identificar o objeto que enviou a mensagem.</span><span class="sxs-lookup"><span data-stu-id="a8b7c-123">Optional parameter that can be used to identify the object that sent the message.</span></span> <span data-ttu-id="a8b7c-124">Ao definir *pvContext* quando você registra esse retorno de chamada, você pode usar o mesmo retorno de chamada para lidar com vários processos assíncronos.</span><span class="sxs-lookup"><span data-stu-id="a8b7c-124">By setting *pvContext* when you register this callback, you can use the same callback to handle multiple asynchronous processes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8b7c-125">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a8b7c-125">Return value</span></span>

<span data-ttu-id="a8b7c-126">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="a8b7c-126">The method returns an **HRESULT**.</span></span> <span data-ttu-id="a8b7c-127">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="a8b7c-127">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="a8b7c-128">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="a8b7c-128">Return code</span></span>                                                                          | <span data-ttu-id="a8b7c-129">Descrição</span><span class="sxs-lookup"><span data-stu-id="a8b7c-129">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="a8b7c-130"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a8b7c-130"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="a8b7c-131">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="a8b7c-131">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a8b7c-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="a8b7c-132">Remarks</span></span>

<span data-ttu-id="a8b7c-133">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="a8b7c-133">None.</span></span>

## <a name="see-also"></a><span data-ttu-id="a8b7c-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="a8b7c-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8b7c-135">**\_tipo de \_ dados attr DRM**</span><span class="sxs-lookup"><span data-stu-id="a8b7c-135">**DRM\_ATTR\_DATATYPE**</span></span>](drm-attr-datatype.md)
</dt> <dt>

[<span data-ttu-id="a8b7c-136">**Interface IDRMStatusCallback**</span><span class="sxs-lookup"><span data-stu-id="a8b7c-136">**IDRMStatusCallback Interface**</span></span>](idrmstatuscallback.md)
</dt> </dl>

 

 





