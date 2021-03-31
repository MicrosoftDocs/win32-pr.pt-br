---
description: Ocorre quando uma nova caneta é adicionada ao sistema.
ms.assetid: bd0f0d2a-c0d9-48fc-bc90-f63f038639f3
title: 'Método ITabletEventSink:: CursorNew'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletEventSink.CursorNew
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 31db152eb15d6f980234dc556e277691d3f14959
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171857"
---
# <a name="itableteventsinkcursornew-method"></a><span data-ttu-id="3b1da-103">Método ITabletEventSink:: CursorNew</span><span class="sxs-lookup"><span data-stu-id="3b1da-103">ITabletEventSink::CursorNew method</span></span>

<span data-ttu-id="3b1da-104">Ocorre quando uma nova caneta é adicionada ao sistema.</span><span class="sxs-lookup"><span data-stu-id="3b1da-104">Occurs when a new stylus is added to the system.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b1da-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3b1da-105">Syntax</span></span>


```C++
HRESULT CursorNew(
  [in] TABLET_CONTEXT_ID tcid,
       t                 cid
);
```



## <a name="parameters"></a><span data-ttu-id="3b1da-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3b1da-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b1da-107">*TCID* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3b1da-107">*tcid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b1da-108">O identificador do contexto do Tablet em que a nova caneta foi adicionada.</span><span class="sxs-lookup"><span data-stu-id="3b1da-108">The identifier of the tablet context where the new stylus was added.</span></span>

</dd> <dt>

<span data-ttu-id="3b1da-109">*CID*</span><span class="sxs-lookup"><span data-stu-id="3b1da-109">*cid*</span></span> 
</dt> <dd>

<span data-ttu-id="3b1da-110">O identificador do novo objeto de caneta.</span><span class="sxs-lookup"><span data-stu-id="3b1da-110">The identifier of the new stylus object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b1da-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3b1da-111">Return value</span></span>

<span data-ttu-id="3b1da-112">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="3b1da-112">This method can return one of these values.</span></span>



| <span data-ttu-id="3b1da-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="3b1da-113">Return code</span></span>                                                                            | <span data-ttu-id="3b1da-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="3b1da-114">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="3b1da-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="3b1da-115"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="3b1da-116">Êxito.</span><span class="sxs-lookup"><span data-stu-id="3b1da-116">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="3b1da-117"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="3b1da-117"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="3b1da-118">Ocorreu um erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="3b1da-118">An unspecified error occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="3b1da-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3b1da-119">Requirements</span></span>



| <span data-ttu-id="3b1da-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b1da-120">Requirement</span></span> | <span data-ttu-id="3b1da-121">Valor</span><span class="sxs-lookup"><span data-stu-id="3b1da-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3b1da-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3b1da-122">Minimum supported client</span></span><br/> | <span data-ttu-id="3b1da-123">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="3b1da-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="3b1da-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3b1da-124">Minimum supported server</span></span><br/> | <span data-ttu-id="3b1da-125">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="3b1da-125">None supported</span></span><br/>                                                              |
| <span data-ttu-id="3b1da-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3b1da-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="3b1da-127"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3b1da-127"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b1da-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="3b1da-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b1da-129">**Interface ITabletEventSink**</span><span class="sxs-lookup"><span data-stu-id="3b1da-129">**ITabletEventSink Interface**</span></span>](itableteventsink.md)
</dt> </dl>

 

 




