---
description: Indica se a caneta está de cabeça para baixo.
ms.assetid: 04b05287-000d-455f-88e5-821c7fdb8119
title: 'Método ITabletCursor:: inverted'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletCursor.IsInverted
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 041b81c38f3370421c96a4c0d66201254a715e62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105769083"
---
# <a name="itabletcursorisinverted-method"></a><span data-ttu-id="07876-103">Método ITabletCursor:: inverted</span><span class="sxs-lookup"><span data-stu-id="07876-103">ITabletCursor::IsInverted method</span></span>

<span data-ttu-id="07876-104">Indica se a caneta está de cabeça para baixo.</span><span class="sxs-lookup"><span data-stu-id="07876-104">Indicates if the stylus is upside down.</span></span>

## <a name="syntax"></a><span data-ttu-id="07876-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="07876-105">Syntax</span></span>


```C++
HRESULT IsInverted();
```



## <a name="parameters"></a><span data-ttu-id="07876-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="07876-106">Parameters</span></span>

<span data-ttu-id="07876-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="07876-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="07876-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="07876-108">Return value</span></span>

<span data-ttu-id="07876-109">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="07876-109">This method can return one of these values.</span></span>



| <span data-ttu-id="07876-110">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="07876-110">Return code</span></span>                                                                             | <span data-ttu-id="07876-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="07876-111">Description</span></span>                               |
|-----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="07876-112"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="07876-112"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="07876-113">A caneta é invertida.</span><span class="sxs-lookup"><span data-stu-id="07876-113">The stylus is inverted.</span></span><br/>        |
| <dl> <span data-ttu-id="07876-114"><dt>**\_falso**</dt></span><span class="sxs-lookup"><span data-stu-id="07876-114"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="07876-115">A caneta não está invertida.</span><span class="sxs-lookup"><span data-stu-id="07876-115">The stylus is not inverted.</span></span><br/>    |
| <dl> <span data-ttu-id="07876-116"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="07876-116"><dt>**E\_FAIL**</dt></span></span> </dl>  | <span data-ttu-id="07876-117">Ocorreu um erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="07876-117">An unspecified error occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="07876-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="07876-118">Requirements</span></span>



| <span data-ttu-id="07876-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="07876-119">Requirement</span></span> | <span data-ttu-id="07876-120">Valor</span><span class="sxs-lookup"><span data-stu-id="07876-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="07876-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="07876-121">Minimum supported client</span></span><br/> | <span data-ttu-id="07876-122">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="07876-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="07876-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="07876-123">Minimum supported server</span></span><br/> | <span data-ttu-id="07876-124">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="07876-124">None supported</span></span><br/>                                                              |
| <span data-ttu-id="07876-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="07876-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="07876-126"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="07876-126"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07876-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="07876-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07876-128">**ITabletCursor**</span><span class="sxs-lookup"><span data-stu-id="07876-128">**ITabletCursor**</span></span>](itabletcursor.md)
</dt> <dt>

[<span data-ttu-id="07876-129">**Interface ITabletCursorButton**</span><span class="sxs-lookup"><span data-stu-id="07876-129">**ITabletCursorButton Interface**</span></span>](itabletcursorbutton.md)
</dt> </dl>

 

 




