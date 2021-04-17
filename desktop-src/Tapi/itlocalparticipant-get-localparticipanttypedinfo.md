---
description: O \_ método Get LocalParticipantTypedInfo Obtém informações do participante, como nome de email ou localização geográfica.
ms.assetid: 46bb70a7-7dc9-463d-8416-737122412750
title: 'Método ITLocalParticipant:: get_LocalParticipantTypedInfo (Confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: caabaf503963c09898c06659884fd3ac3858e704
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105779310"
---
# <a name="itlocalparticipantget_localparticipanttypedinfo-method"></a><span data-ttu-id="5c99d-103">Método ITLocalParticipant:: get \_ LocalParticipantTypedInfo</span><span class="sxs-lookup"><span data-stu-id="5c99d-103">ITLocalParticipant::get\_LocalParticipantTypedInfo method</span></span>

<span data-ttu-id="5c99d-104">O método **Get \_ LocalParticipantTypedInfo** Obtém informações do participante, como nome de email ou localização geográfica.</span><span class="sxs-lookup"><span data-stu-id="5c99d-104">The **get\_LocalParticipantTypedInfo** method gets participant information, such as e-mail name or geographical location.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c99d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5c99d-105">Syntax</span></span>


```C++
HRESULT get_LocalParticipantTypedInfo(
  [in]  PARTICIPANT_TYPED_INFO InfoType,
  [out] BSTR                   *ppInfo
);
```



## <a name="parameters"></a><span data-ttu-id="5c99d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5c99d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c99d-107">*InfoType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5c99d-107">*InfoType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5c99d-108">[**Participante \_ do Identificador de \_ informações digitados**](participant-typed-info.md) do tipo de informação necessário.</span><span class="sxs-lookup"><span data-stu-id="5c99d-108">[**PARTICIPANT\_TYPED\_INFO**](participant-typed-info.md) identifier of type of information required.</span></span>

</dd> <dt>

<span data-ttu-id="5c99d-109">*ppInfo* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="5c99d-109">*ppInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5c99d-110">Ponteiro para um **BSTR** que conterá as informações necessárias após um retorno bem-sucedido do método.</span><span class="sxs-lookup"><span data-stu-id="5c99d-110">Pointer to a **BSTR** that will contain the required information following a successful return of the method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5c99d-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5c99d-111">Return value</span></span>

<span data-ttu-id="5c99d-112">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="5c99d-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5c99d-113">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5c99d-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="5c99d-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="5c99d-114">Remarks</span></span>

<span data-ttu-id="5c99d-115">O aplicativo deve usar [SysFreeString](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) para liberar a memória alocada para o parâmetro *ppInfo* .</span><span class="sxs-lookup"><span data-stu-id="5c99d-115">The application must use [SysFreeString](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory allocated for the *ppInfo* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="5c99d-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5c99d-116">Requirements</span></span>



| <span data-ttu-id="5c99d-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="5c99d-117">Requirement</span></span> | <span data-ttu-id="5c99d-118">Valor</span><span class="sxs-lookup"><span data-stu-id="5c99d-118">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5c99d-119">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="5c99d-119">TAPI version</span></span><br/> | <span data-ttu-id="5c99d-120">Requer TAPI 3,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="5c99d-120">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="5c99d-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5c99d-121">Header</span></span><br/>       | <dl> <span data-ttu-id="5c99d-122"><dt>Confpriv. h</dt></span><span class="sxs-lookup"><span data-stu-id="5c99d-122"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="5c99d-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5c99d-123">Library</span></span><br/>      | <dl> <span data-ttu-id="5c99d-124"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5c99d-124"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="5c99d-125">DLL</span><span class="sxs-lookup"><span data-stu-id="5c99d-125">DLL</span></span><br/>          | <dl> <span data-ttu-id="5c99d-126"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5c99d-126"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="5c99d-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="5c99d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c99d-128">**ITLocalParticipant**</span><span class="sxs-lookup"><span data-stu-id="5c99d-128">**ITLocalParticipant**</span></span>](itlocalparticipant.md)
</dt> <dt>

[<span data-ttu-id="5c99d-129">**\_informações de tipo de participante \_**</span><span class="sxs-lookup"><span data-stu-id="5c99d-129">**PARTICIPANT\_TYPED\_INFO**</span></span>](participant-typed-info.md)
</dt> </dl>

 

