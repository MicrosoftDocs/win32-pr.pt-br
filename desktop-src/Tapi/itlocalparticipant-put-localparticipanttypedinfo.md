---
description: O \_ método Put LocalParticipantTypedInfo define informações do participante.
ms.assetid: c4afd1d3-6fe4-4e5b-a9bf-81b7dffa9914
title: 'ITLocalParticipant: método de ut_LocalParticipantTypedInfo de:p (Confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77809a9a3858b6a098fa3ff6a93878cf38518f92
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105792624"
---
# <a name="itlocalparticipantput_localparticipanttypedinfo-method"></a><span data-ttu-id="ac069-103">ITLocalParticipant: método UT \_ LocalParticipantTypedInfo:p</span><span class="sxs-lookup"><span data-stu-id="ac069-103">ITLocalParticipant::put\_LocalParticipantTypedInfo method</span></span>

<span data-ttu-id="ac069-104">O método **Put \_ LocalParticipantTypedInfo** define informações do participante.</span><span class="sxs-lookup"><span data-stu-id="ac069-104">The **put\_LocalParticipantTypedInfo** method sets participant information.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac069-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ac069-105">Syntax</span></span>


```C++
HRESULT put_LocalParticipantTypedInfo(
  [in] PARTICIPANT_TYPED_INFO InfoType,
  [in] BSTR                   ppInfo
);
```



## <a name="parameters"></a><span data-ttu-id="ac069-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ac069-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac069-107">*InfoType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ac069-107">*InfoType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac069-108">[**Participante \_ do Identificador de \_ informações digitadas**](participant-typed-info.md) do tipo de informação necessário.</span><span class="sxs-lookup"><span data-stu-id="ac069-108">[**PARTICIPANT\_TYPED\_INFO**](participant-typed-info.md) identifier of the type of information required.</span></span>

</dd> <dt>

<span data-ttu-id="ac069-109">*ppInfo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ac069-109">*ppInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac069-110">**BSTR** que contém o novo valor necessário para as informações.</span><span class="sxs-lookup"><span data-stu-id="ac069-110">**BSTR** containing the required new value for the information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac069-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ac069-111">Return value</span></span>

<span data-ttu-id="ac069-112">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="ac069-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ac069-113">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ac069-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="ac069-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="ac069-114">Remarks</span></span>

<span data-ttu-id="ac069-115">O aplicativo deve usar [SysAllocString](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) para alocar memória para o parâmetro *PpInfo* e usar [SysFreeString](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) para liberar a memória quando a variável não for mais necessária.</span><span class="sxs-lookup"><span data-stu-id="ac069-115">The application must use [SysAllocString](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) to allocate memory for the *ppInfo* parameter and use [SysFreeString](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory when the variable is no longer needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac069-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ac069-116">Requirements</span></span>



| <span data-ttu-id="ac069-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="ac069-117">Requirement</span></span> | <span data-ttu-id="ac069-118">Valor</span><span class="sxs-lookup"><span data-stu-id="ac069-118">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ac069-119">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="ac069-119">TAPI version</span></span><br/> | <span data-ttu-id="ac069-120">Requer TAPI 3,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="ac069-120">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="ac069-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ac069-121">Header</span></span><br/>       | <dl> <span data-ttu-id="ac069-122"><dt>Confpriv. h</dt></span><span class="sxs-lookup"><span data-stu-id="ac069-122"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="ac069-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ac069-123">Library</span></span><br/>      | <dl> <span data-ttu-id="ac069-124"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ac069-124"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="ac069-125">DLL</span><span class="sxs-lookup"><span data-stu-id="ac069-125">DLL</span></span><br/>          | <dl> <span data-ttu-id="ac069-126"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ac069-126"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="ac069-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="ac069-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac069-128">**ITLocalParticipant**</span><span class="sxs-lookup"><span data-stu-id="ac069-128">**ITLocalParticipant**</span></span>](itlocalparticipant.md)
</dt> <dt>

[<span data-ttu-id="ac069-129">**\_informações de tipo de participante \_**</span><span class="sxs-lookup"><span data-stu-id="ac069-129">**PARTICIPANT\_TYPED\_INFO**</span></span>](participant-typed-info.md)
</dt> </dl>

 

