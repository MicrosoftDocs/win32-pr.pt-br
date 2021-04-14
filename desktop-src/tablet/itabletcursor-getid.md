---
description: Recupera o identificador da caneta.
ms.assetid: 27320a2f-1e4a-4d7d-a1f8-5244f4a03415
title: 'Método ITabletCursor:: GetId'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletCursor.GetId
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 5d4f71d2cd465bfd2d1ff4c245154a300c431df2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104370750"
---
# <a name="itabletcursorgetid-method"></a><span data-ttu-id="8b66d-103">Método ITabletCursor:: GetId</span><span class="sxs-lookup"><span data-stu-id="8b66d-103">ITabletCursor::GetId method</span></span>

<span data-ttu-id="8b66d-104">Recupera o identificador da caneta.</span><span class="sxs-lookup"><span data-stu-id="8b66d-104">Retrieves the stylus identifier.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b66d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8b66d-105">Syntax</span></span>


```C++
HRESULT GetId(
  [out] CURSOR_ID *pCid
);
```



## <a name="parameters"></a><span data-ttu-id="8b66d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8b66d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b66d-107">*pCid* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="8b66d-107">*pCid* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8b66d-108">O identificador da caneta digitalizadora.</span><span class="sxs-lookup"><span data-stu-id="8b66d-108">The identifier of the tablet stylus.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b66d-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8b66d-109">Return value</span></span>

<span data-ttu-id="8b66d-110">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="8b66d-110">This method can return one of these values.</span></span>



| <span data-ttu-id="8b66d-111">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="8b66d-111">Return code</span></span>                                                                            | <span data-ttu-id="8b66d-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="8b66d-112">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="8b66d-113"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="8b66d-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="8b66d-114">Êxito.</span><span class="sxs-lookup"><span data-stu-id="8b66d-114">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="8b66d-115"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="8b66d-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="8b66d-116">Ocorreu um erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="8b66d-116">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="8b66d-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="8b66d-117">Remarks</span></span>

<span data-ttu-id="8b66d-118">\_A ID do cursor é definida como um DWORD.</span><span class="sxs-lookup"><span data-stu-id="8b66d-118">CURSOR\_ID is defined as a DWORD.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b66d-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8b66d-119">Requirements</span></span>



| <span data-ttu-id="8b66d-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="8b66d-120">Requirement</span></span> | <span data-ttu-id="8b66d-121">Valor</span><span class="sxs-lookup"><span data-stu-id="8b66d-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8b66d-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8b66d-122">Minimum supported client</span></span><br/> | <span data-ttu-id="8b66d-123">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="8b66d-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="8b66d-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8b66d-124">Minimum supported server</span></span><br/> | <span data-ttu-id="8b66d-125">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="8b66d-125">None supported</span></span><br/>                                                              |
| <span data-ttu-id="8b66d-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8b66d-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="8b66d-127"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8b66d-127"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8b66d-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="8b66d-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b66d-129">**Interface ITabletCursor**</span><span class="sxs-lookup"><span data-stu-id="8b66d-129">**ITabletCursor Interface**</span></span>](itabletcursor.md)
</dt> </dl>

 

 




