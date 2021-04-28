---
description: 'Método IEnumMedia:: Skip – o método Skip ignora o próximo número especificado de elementos na sequência de enumeração.'
ms.assetid: 825972c9-5303-4c5a-9475-dc67c185af91
title: 'Método IEnumMedia:: Skip (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d8c600a201d6800fcb04dba5f208fd5cb810078
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084184"
---
# <a name="ienummediaskip-method"></a><span data-ttu-id="8128b-103">Método IEnumMedia:: Skip</span><span class="sxs-lookup"><span data-stu-id="8128b-103">IEnumMedia::Skip method</span></span>

<span data-ttu-id="8128b-104">\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="8128b-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="8128b-105">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="8128b-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="8128b-106">O método **Skip** ignora o próximo número especificado de elementos na sequência de enumeração.</span><span class="sxs-lookup"><span data-stu-id="8128b-106">The **Skip** method skips over the next specified number of elements in the enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="8128b-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8128b-107">Syntax</span></span>


```C++
HRESULT Skip(
  [in] ULONG celt
);
```



## <a name="parameters"></a><span data-ttu-id="8128b-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8128b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8128b-109">*celt* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8128b-109">*celt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8128b-110">Número de elementos a serem ignorados.</span><span class="sxs-lookup"><span data-stu-id="8128b-110">Number of elements to skip.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8128b-111">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="8128b-111">Return value</span></span>

<span data-ttu-id="8128b-112">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="8128b-112">This method can return one of these values.</span></span>



| <span data-ttu-id="8128b-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="8128b-113">Return code</span></span>                                                                             | <span data-ttu-id="8128b-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="8128b-114">Description</span></span>                                           |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <span data-ttu-id="8128b-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="8128b-115"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="8128b-116">O número de elementos ignorados foi *celt*.</span><span class="sxs-lookup"><span data-stu-id="8128b-116">Number of elements skipped was *celt*.</span></span><br/>     |
| <dl> <span data-ttu-id="8128b-117"><dt>**\_falso**</dt></span><span class="sxs-lookup"><span data-stu-id="8128b-117"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="8128b-118">O número de elementos ignorados não era *celt*.</span><span class="sxs-lookup"><span data-stu-id="8128b-118">Number of elements skipped was not *celt*.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="8128b-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8128b-119">Requirements</span></span>



| <span data-ttu-id="8128b-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="8128b-120">Requirement</span></span> | <span data-ttu-id="8128b-121">Valor</span><span class="sxs-lookup"><span data-stu-id="8128b-121">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8128b-122">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="8128b-122">TAPI version</span></span><br/> | <span data-ttu-id="8128b-123">Requer TAPI 3,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="8128b-123">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="8128b-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8128b-124">Header</span></span><br/>       | <dl> <span data-ttu-id="8128b-125"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="8128b-125"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="8128b-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8128b-126">Library</span></span><br/>      | <dl> <span data-ttu-id="8128b-127"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8128b-127"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="8128b-128">DLL</span><span class="sxs-lookup"><span data-stu-id="8128b-128">DLL</span></span><br/>          | <dl> <span data-ttu-id="8128b-129"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8128b-129"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8128b-130">Consulte também</span><span class="sxs-lookup"><span data-stu-id="8128b-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8128b-131">**IEnumMedia**</span><span class="sxs-lookup"><span data-stu-id="8128b-131">**IEnumMedia**</span></span>](ienummedia.md)
</dt> </dl>

 

 




