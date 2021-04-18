---
description: Recupera o número de botões na caneta digitalizadora.
ms.assetid: ae4ce670-769a-4f00-b728-285020f09934
title: 'Método ITabletCursor:: GetButtonCount'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletCursor.GetButtonCount
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 08fdf24b2a0b69b7830a683786f18fc5df0805b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105812115"
---
# <a name="itabletcursorgetbuttoncount-method"></a><span data-ttu-id="42a70-103">Método ITabletCursor:: GetButtonCount</span><span class="sxs-lookup"><span data-stu-id="42a70-103">ITabletCursor::GetButtonCount method</span></span>

<span data-ttu-id="42a70-104">Recupera o número de botões na caneta digitalizadora.</span><span class="sxs-lookup"><span data-stu-id="42a70-104">Retrieves the number of buttons on the tablet stylus.</span></span>

## <a name="syntax"></a><span data-ttu-id="42a70-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="42a70-105">Syntax</span></span>


```C++
HRESULT GetButtonCount(
  [out] ULONG *pcButtons
);
```



## <a name="parameters"></a><span data-ttu-id="42a70-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="42a70-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42a70-107">*pcButtons* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="42a70-107">*pcButtons* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="42a70-108">A contagem de botões na caneta digitalizadora.</span><span class="sxs-lookup"><span data-stu-id="42a70-108">The count of buttons on the tablet stylus.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42a70-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="42a70-109">Return value</span></span>

<span data-ttu-id="42a70-110">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="42a70-110">This method can return one of these values.</span></span>



| <span data-ttu-id="42a70-111">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="42a70-111">Return code</span></span>                                                                            | <span data-ttu-id="42a70-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="42a70-112">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="42a70-113"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="42a70-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="42a70-114">Êxito.</span><span class="sxs-lookup"><span data-stu-id="42a70-114">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="42a70-115"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="42a70-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="42a70-116">Ocorreu um erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="42a70-116">An unspecified error occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="42a70-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="42a70-117">Requirements</span></span>



| <span data-ttu-id="42a70-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="42a70-118">Requirement</span></span> | <span data-ttu-id="42a70-119">Valor</span><span class="sxs-lookup"><span data-stu-id="42a70-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="42a70-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="42a70-120">Minimum supported client</span></span><br/> | <span data-ttu-id="42a70-121">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="42a70-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="42a70-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="42a70-122">Minimum supported server</span></span><br/> | <span data-ttu-id="42a70-123">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="42a70-123">None supported</span></span><br/>                                                              |
| <span data-ttu-id="42a70-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="42a70-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="42a70-125"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="42a70-125"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42a70-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="42a70-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42a70-127">**Interface ITabletCursor**</span><span class="sxs-lookup"><span data-stu-id="42a70-127">**ITabletCursor Interface**</span></span>](itabletcursor.md)
</dt> </dl>

 

 




