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
# <a name="itableteventsinkcursornew-method"></a><span data-ttu-id="456f3-103">Método ITabletEventSink:: CursorNew</span><span class="sxs-lookup"><span data-stu-id="456f3-103">ITabletEventSink::CursorNew method</span></span>

<span data-ttu-id="456f3-104">Ocorre quando uma nova caneta é adicionada ao sistema.</span><span class="sxs-lookup"><span data-stu-id="456f3-104">Occurs when a new stylus is added to the system.</span></span>

## <a name="syntax"></a><span data-ttu-id="456f3-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="456f3-105">Syntax</span></span>


```C++
HRESULT CursorNew(
  [in] TABLET_CONTEXT_ID tcid,
       t                 cid
);
```



## <a name="parameters"></a><span data-ttu-id="456f3-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="456f3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="456f3-107">*TCID* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="456f3-107">*tcid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="456f3-108">O identificador do contexto do Tablet em que a nova caneta foi adicionada.</span><span class="sxs-lookup"><span data-stu-id="456f3-108">The identifier of the tablet context where the new stylus was added.</span></span>

</dd> <dt>

<span data-ttu-id="456f3-109">*CID*</span><span class="sxs-lookup"><span data-stu-id="456f3-109">*cid*</span></span> 
</dt> <dd>

<span data-ttu-id="456f3-110">O identificador do novo objeto de caneta.</span><span class="sxs-lookup"><span data-stu-id="456f3-110">The identifier of the new stylus object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="456f3-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="456f3-111">Return value</span></span>

<span data-ttu-id="456f3-112">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="456f3-112">This method can return one of these values.</span></span>



| <span data-ttu-id="456f3-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="456f3-113">Return code</span></span>                                                                            | <span data-ttu-id="456f3-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="456f3-114">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="456f3-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="456f3-115"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="456f3-116">Êxito.</span><span class="sxs-lookup"><span data-stu-id="456f3-116">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="456f3-117"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="456f3-117"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="456f3-118">Ocorreu um erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="456f3-118">An unspecified error occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="456f3-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="456f3-119">Requirements</span></span>



| <span data-ttu-id="456f3-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="456f3-120">Requirement</span></span> | <span data-ttu-id="456f3-121">Valor</span><span class="sxs-lookup"><span data-stu-id="456f3-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="456f3-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="456f3-122">Minimum supported client</span></span><br/> | <span data-ttu-id="456f3-123">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="456f3-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="456f3-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="456f3-124">Minimum supported server</span></span><br/> | <span data-ttu-id="456f3-125">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="456f3-125">None supported</span></span><br/>                                                              |
| <span data-ttu-id="456f3-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="456f3-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="456f3-127"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="456f3-127"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="456f3-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="456f3-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="456f3-129">**Interface ITabletEventSink**</span><span class="sxs-lookup"><span data-stu-id="456f3-129">**ITabletEventSink Interface**</span></span>](itableteventsink.md)
</dt> </dl>

 

 




