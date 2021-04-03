---
description: Ocorre quando a caneta deixa o intervalo de detecção física (proximidade) do Tablet.
ms.assetid: ded01278-126d-415d-9a7b-1e6fe3650a37
title: 'Método ITabletEventSink:: CursorOutOfRange'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletEventSink.CursorOutOfRange
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: e2250401f3888bd07ff250549c11c34e6a54576d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837219"
---
# <a name="itableteventsinkcursoroutofrange-method"></a><span data-ttu-id="8d8a1-103">Método ITabletEventSink:: CursorOutOfRange</span><span class="sxs-lookup"><span data-stu-id="8d8a1-103">ITabletEventSink::CursorOutOfRange method</span></span>

<span data-ttu-id="8d8a1-104">Ocorre quando a caneta deixa o intervalo de detecção física (proximidade) do Tablet.</span><span class="sxs-lookup"><span data-stu-id="8d8a1-104">Occurs when the stylus leaves the physical detection range (proximity) of the tablet.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d8a1-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8d8a1-105">Syntax</span></span>


```C++
HRESULT CursorOutOfRange(
  [in] TABLET_CONTEXT_ID tcid,
       t                 cid
);
```



## <a name="parameters"></a><span data-ttu-id="8d8a1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8d8a1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d8a1-107">*TCID* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8d8a1-107">*tcid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d8a1-108">O identificador do Tablet.</span><span class="sxs-lookup"><span data-stu-id="8d8a1-108">The identifier of the tablet.</span></span>

</dd> <dt>

<span data-ttu-id="8d8a1-109">*CID*</span><span class="sxs-lookup"><span data-stu-id="8d8a1-109">*cid*</span></span> 
</dt> <dd>

<span data-ttu-id="8d8a1-110">O identificador da caneta.</span><span class="sxs-lookup"><span data-stu-id="8d8a1-110">The identifier of the stylus.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d8a1-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8d8a1-111">Return value</span></span>

<span data-ttu-id="8d8a1-112">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="8d8a1-112">This method can return one of these values.</span></span>



| <span data-ttu-id="8d8a1-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="8d8a1-113">Return code</span></span>                                                                            | <span data-ttu-id="8d8a1-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="8d8a1-114">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="8d8a1-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="8d8a1-115"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="8d8a1-116">Êxito.</span><span class="sxs-lookup"><span data-stu-id="8d8a1-116">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="8d8a1-117"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="8d8a1-117"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="8d8a1-118">Ocorreu um erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="8d8a1-118">An unspecified error occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="8d8a1-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8d8a1-119">Requirements</span></span>



| <span data-ttu-id="8d8a1-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="8d8a1-120">Requirement</span></span> | <span data-ttu-id="8d8a1-121">Valor</span><span class="sxs-lookup"><span data-stu-id="8d8a1-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8d8a1-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8d8a1-122">Minimum supported client</span></span><br/> | <span data-ttu-id="8d8a1-123">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="8d8a1-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="8d8a1-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8d8a1-124">Minimum supported server</span></span><br/> | <span data-ttu-id="8d8a1-125">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="8d8a1-125">None supported</span></span><br/>                                                              |
| <span data-ttu-id="8d8a1-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8d8a1-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="8d8a1-127"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8d8a1-127"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8d8a1-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="8d8a1-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d8a1-129">**Interface ITabletEventSink**</span><span class="sxs-lookup"><span data-stu-id="8d8a1-129">**ITabletEventSink Interface**</span></span>](itableteventsink.md)
</dt> </dl>

 

 




