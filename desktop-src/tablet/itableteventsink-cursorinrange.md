---
description: Ocorre quando uma caneta entra dentro do intervalo de detecção do digitalizador.
ms.assetid: 22be233a-fc33-4a8f-91b6-28b2f2910b69
title: 'Método ITabletEventSink:: CursorInRange'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletEventSink.CursorInRange
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: eec2b4f309480ecaecd50de2120d701c916b6fff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105794449"
---
# <a name="itableteventsinkcursorinrange-method"></a><span data-ttu-id="a376e-103">Método ITabletEventSink:: CursorInRange</span><span class="sxs-lookup"><span data-stu-id="a376e-103">ITabletEventSink::CursorInRange method</span></span>

<span data-ttu-id="a376e-104">Ocorre quando uma caneta entra dentro do intervalo de detecção do digitalizador.</span><span class="sxs-lookup"><span data-stu-id="a376e-104">Occurs when a stylus comes within the digitizer's range of detection.</span></span>

## <a name="syntax"></a><span data-ttu-id="a376e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a376e-105">Syntax</span></span>


```C++
HRESULT CursorInRange(
  [in] TABLET_CONTEXT_ID tcid,
       t                 cid
);
```



## <a name="parameters"></a><span data-ttu-id="a376e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a376e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a376e-107">*TCID* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a376e-107">*tcid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a376e-108">O identificador do objeto do Tablet que detectou a caneta.</span><span class="sxs-lookup"><span data-stu-id="a376e-108">The identifier of the tablet object that detected the stylus.</span></span>

</dd> <dt>

<span data-ttu-id="a376e-109">*CID*</span><span class="sxs-lookup"><span data-stu-id="a376e-109">*cid*</span></span> 
</dt> <dd>

<span data-ttu-id="a376e-110">O identificador do objeto de caneta que vem no intervalo do digitalizador.</span><span class="sxs-lookup"><span data-stu-id="a376e-110">The identifier of the stylus object that has come in range of the digitizer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a376e-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a376e-111">Return value</span></span>

<span data-ttu-id="a376e-112">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="a376e-112">This method can return one of these values.</span></span>



| <span data-ttu-id="a376e-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="a376e-113">Return code</span></span>                                                                            | <span data-ttu-id="a376e-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="a376e-114">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="a376e-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a376e-115"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="a376e-116">Êxito.</span><span class="sxs-lookup"><span data-stu-id="a376e-116">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="a376e-117"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="a376e-117"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="a376e-118">Ocorreu um erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="a376e-118">An unspecified error occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="a376e-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a376e-119">Requirements</span></span>



| <span data-ttu-id="a376e-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="a376e-120">Requirement</span></span> | <span data-ttu-id="a376e-121">Valor</span><span class="sxs-lookup"><span data-stu-id="a376e-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a376e-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a376e-122">Minimum supported client</span></span><br/> | <span data-ttu-id="a376e-123">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="a376e-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="a376e-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a376e-124">Minimum supported server</span></span><br/> | <span data-ttu-id="a376e-125">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="a376e-125">None supported</span></span><br/>                                                              |
| <span data-ttu-id="a376e-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a376e-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="a376e-127"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a376e-127"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a376e-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="a376e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a376e-129">**Interface ITabletEventSink**</span><span class="sxs-lookup"><span data-stu-id="a376e-129">**ITabletEventSink Interface**</span></span>](itableteventsink.md)
</dt> </dl>

 

 




