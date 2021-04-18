---
description: Retorna o número de objetos de cursor associados ao Tablet.
ms.assetid: 7aa5802c-1255-41a4-b1fa-23e5f56c0b80
title: 'Método ITablet:: GetCursorCount'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet.GetCursorCount
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 2309384e4aa36383277ba72cc407cabef7ab4b27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105788784"
---
# <a name="itabletgetcursorcount-method"></a><span data-ttu-id="f77b1-103">Método ITablet:: GetCursorCount</span><span class="sxs-lookup"><span data-stu-id="f77b1-103">ITablet::GetCursorCount method</span></span>

<span data-ttu-id="f77b1-104">Retorna o número de objetos de cursor associados ao Tablet.</span><span class="sxs-lookup"><span data-stu-id="f77b1-104">Returns the number of cursor objects associated with the tablet.</span></span>

## <a name="syntax"></a><span data-ttu-id="f77b1-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f77b1-105">Syntax</span></span>


```C++
HRESULT GetCursorCount(
  [out] ULONG *pcCurs
);
```



## <a name="parameters"></a><span data-ttu-id="f77b1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f77b1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f77b1-107">*pcCurs* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="f77b1-107">*pcCurs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f77b1-108">O número de objetos de cursor associados ao Tablet.</span><span class="sxs-lookup"><span data-stu-id="f77b1-108">The number of cursor objects associated with the tablet.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f77b1-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f77b1-109">Return value</span></span>

<span data-ttu-id="f77b1-110">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="f77b1-110">This method can return one of these values.</span></span>



| <span data-ttu-id="f77b1-111">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="f77b1-111">Return code</span></span>                                                                            | <span data-ttu-id="f77b1-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="f77b1-112">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="f77b1-113"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f77b1-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="f77b1-114">Êxito.</span><span class="sxs-lookup"><span data-stu-id="f77b1-114">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="f77b1-115"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="f77b1-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="f77b1-116">Ocorreu um erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="f77b1-116">An unspecified error occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="f77b1-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f77b1-117">Requirements</span></span>



| <span data-ttu-id="f77b1-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="f77b1-118">Requirement</span></span> | <span data-ttu-id="f77b1-119">Valor</span><span class="sxs-lookup"><span data-stu-id="f77b1-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f77b1-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f77b1-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f77b1-121">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="f77b1-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="f77b1-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f77b1-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f77b1-123">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="f77b1-123">None supported</span></span><br/>                                                              |
| <span data-ttu-id="f77b1-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f77b1-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="f77b1-125"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f77b1-125"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f77b1-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="f77b1-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f77b1-127">**Interface ITablet**</span><span class="sxs-lookup"><span data-stu-id="f77b1-127">**ITablet Interface**</span></span>](itablet.md)
</dt> </dl>

 

 




