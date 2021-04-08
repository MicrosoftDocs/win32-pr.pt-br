---
description: Recupera o identificador exclusivo do botão da caneta.
ms.assetid: 06bd6a84-46cd-4c62-92d6-50caae359e43
title: 'Método ITabletCursorButton:: GetGuid'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletCursorButton.GetGuid
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 21d63ef0c934e96bc93b5384cab1e67f9dd452d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011477"
---
# <a name="itabletcursorbuttongetguid-method"></a><span data-ttu-id="9cd9a-103">Método ITabletCursorButton:: GetGuid</span><span class="sxs-lookup"><span data-stu-id="9cd9a-103">ITabletCursorButton::GetGuid method</span></span>

<span data-ttu-id="9cd9a-104">Recupera o identificador exclusivo do botão da caneta.</span><span class="sxs-lookup"><span data-stu-id="9cd9a-104">Retrieves the unique identifier of the stylus button.</span></span>

## <a name="syntax"></a><span data-ttu-id="9cd9a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9cd9a-105">Syntax</span></span>


```C++
HRESULT GetGuid(
  [out] GUID *pguidBtn
);
```



## <a name="parameters"></a><span data-ttu-id="9cd9a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9cd9a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9cd9a-107">*pguidBtn* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="9cd9a-107">*pguidBtn* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9cd9a-108">Um valor exclusivo que identifica o botão da caneta.</span><span class="sxs-lookup"><span data-stu-id="9cd9a-108">A unique value that identifies the stylus button.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9cd9a-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9cd9a-109">Return value</span></span>

<span data-ttu-id="9cd9a-110">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="9cd9a-110">This method can return one of these values.</span></span>



| <span data-ttu-id="9cd9a-111">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="9cd9a-111">Return code</span></span>                                                                            | <span data-ttu-id="9cd9a-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="9cd9a-112">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="9cd9a-113"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="9cd9a-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="9cd9a-114">Êxito.</span><span class="sxs-lookup"><span data-stu-id="9cd9a-114">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="9cd9a-115"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="9cd9a-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="9cd9a-116">Ocorreu um erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="9cd9a-116">An unspecified error occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="9cd9a-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9cd9a-117">Requirements</span></span>



| <span data-ttu-id="9cd9a-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="9cd9a-118">Requirement</span></span> | <span data-ttu-id="9cd9a-119">Valor</span><span class="sxs-lookup"><span data-stu-id="9cd9a-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9cd9a-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9cd9a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="9cd9a-121">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="9cd9a-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="9cd9a-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9cd9a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="9cd9a-123">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="9cd9a-123">None supported</span></span><br/>                                                              |
| <span data-ttu-id="9cd9a-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9cd9a-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="9cd9a-125"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9cd9a-125"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9cd9a-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="9cd9a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9cd9a-127">**Interface ITabletCursorButton**</span><span class="sxs-lookup"><span data-stu-id="9cd9a-127">**ITabletCursorButton Interface**</span></span>](itabletcursorbutton.md)
</dt> </dl>

 

 




