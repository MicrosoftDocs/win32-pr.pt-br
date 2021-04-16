---
description: O método ReleaseFormat libera a estrutura associada ao formato.
ms.assetid: 67181773-5a04-4e20-9814-b004d3b549f5
title: 'Método ITFormatControl:: ReleaseFormat (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c91b3eb2a84149054d7ff364cf05290946bca975
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105761359"
---
# <a name="itformatcontrolreleaseformat-method"></a><span data-ttu-id="48b47-103">Método ITFormatControl:: ReleaseFormat</span><span class="sxs-lookup"><span data-stu-id="48b47-103">ITFormatControl::ReleaseFormat method</span></span>

<span data-ttu-id="48b47-104">\[ Esse método não está disponível para uso no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="48b47-104">\[ This method is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="48b47-105">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="48b47-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="48b47-106">O método **ReleaseFormat** libera a estrutura associada ao formato.</span><span class="sxs-lookup"><span data-stu-id="48b47-106">The **ReleaseFormat** method releases the structure associated with the format.</span></span>

## <a name="syntax"></a><span data-ttu-id="48b47-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="48b47-107">Syntax</span></span>


```C++
HRESULT ReleaseFormat(
  [in] AM_MEDIA_TYPE *pMediaType
);
```



## <a name="parameters"></a><span data-ttu-id="48b47-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="48b47-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48b47-109">*pMediaType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="48b47-109">*pMediaType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48b47-110">Ponteiro para um descritor de **\_ \_ tipo de mídia am** do formato de terminal.</span><span class="sxs-lookup"><span data-stu-id="48b47-110">Pointer to an **AM\_MEDIA\_TYPE** descriptor of the terminal format.</span></span> <span data-ttu-id="48b47-111">Para obter mais informações sobre o **\_ \_ tipo de mídia am**, consulte a documentação do DirectX.</span><span class="sxs-lookup"><span data-stu-id="48b47-111">For more information on **AM\_MEDIA\_TYPE**, see the DirectX documentation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="48b47-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="48b47-112">Return value</span></span>

<span data-ttu-id="48b47-113">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="48b47-113">This method can return one of these values.</span></span>



| <span data-ttu-id="48b47-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="48b47-114">Return code</span></span>                                                                                   | <span data-ttu-id="48b47-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="48b47-115">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="48b47-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="48b47-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="48b47-117">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="48b47-117">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="48b47-118"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="48b47-118"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="48b47-119">Há memória insuficiente para executar a operação.</span><span class="sxs-lookup"><span data-stu-id="48b47-119">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="48b47-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="48b47-120">Requirements</span></span>



| <span data-ttu-id="48b47-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="48b47-121">Requirement</span></span> | <span data-ttu-id="48b47-122">Valor</span><span class="sxs-lookup"><span data-stu-id="48b47-122">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="48b47-123">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="48b47-123">TAPI version</span></span><br/> | <span data-ttu-id="48b47-124">Requer TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="48b47-124">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="48b47-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="48b47-125">Header</span></span><br/>       | <dl> <span data-ttu-id="48b47-126"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="48b47-126"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="48b47-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="48b47-127">Library</span></span><br/>      | <dl> <span data-ttu-id="48b47-128"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="48b47-128"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="48b47-129">DLL</span><span class="sxs-lookup"><span data-stu-id="48b47-129">DLL</span></span><br/>          | <dl> <span data-ttu-id="48b47-130"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="48b47-130"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48b47-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="48b47-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48b47-132">**ITFormatControl**</span><span class="sxs-lookup"><span data-stu-id="48b47-132">**ITFormatControl**</span></span>](itformatcontrol.md)
</dt> </dl>

 

 




