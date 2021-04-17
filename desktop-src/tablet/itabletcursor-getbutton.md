---
description: Recupera o objeto de botão especificado de uma caneta digitalizadora.
ms.assetid: 83a26703-4501-4f43-9e86-c5c753347012
title: 'Método ITabletCursor:: getbutton'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletCursor.GetButton
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 0b9e8e1337cacdb26d8c124d10e0a886748e70fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105762151"
---
# <a name="itabletcursorgetbutton-method"></a><span data-ttu-id="4d37f-103">Método ITabletCursor:: getbutton</span><span class="sxs-lookup"><span data-stu-id="4d37f-103">ITabletCursor::GetButton method</span></span>

<span data-ttu-id="4d37f-104">Recupera o objeto de botão especificado de uma caneta digitalizadora.</span><span class="sxs-lookup"><span data-stu-id="4d37f-104">Retrieves the specified button object from a tablet stylus.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d37f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4d37f-105">Syntax</span></span>


```C++
HRESULT GetButton(
  [in]  ULONG               iButton,
  [out] ITabletCursorButton **ppButton
);
```



## <a name="parameters"></a><span data-ttu-id="4d37f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4d37f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d37f-107">*iButton* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4d37f-107">*iButton* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d37f-108">Identificador do botão a ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="4d37f-108">Identifier of the button to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="4d37f-109">*ppButton* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="4d37f-109">*ppButton* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4d37f-110">O objeto Button especificado pelo parâmetro *iButton* .</span><span class="sxs-lookup"><span data-stu-id="4d37f-110">The button object specified by the *iButton* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4d37f-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4d37f-111">Return value</span></span>

<span data-ttu-id="4d37f-112">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="4d37f-112">This method can return one of these values.</span></span>



| <span data-ttu-id="4d37f-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="4d37f-113">Return code</span></span>                                                                            | <span data-ttu-id="4d37f-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="4d37f-114">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="4d37f-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="4d37f-115"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="4d37f-116">Êxito.</span><span class="sxs-lookup"><span data-stu-id="4d37f-116">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="4d37f-117"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="4d37f-117"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="4d37f-118">Ocorreu um erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="4d37f-118">An unspecified error occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="4d37f-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4d37f-119">Requirements</span></span>



| <span data-ttu-id="4d37f-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="4d37f-120">Requirement</span></span> | <span data-ttu-id="4d37f-121">Valor</span><span class="sxs-lookup"><span data-stu-id="4d37f-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4d37f-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4d37f-122">Minimum supported client</span></span><br/> | <span data-ttu-id="4d37f-123">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="4d37f-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="4d37f-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4d37f-124">Minimum supported server</span></span><br/> | <span data-ttu-id="4d37f-125">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="4d37f-125">None supported</span></span><br/>                                                              |
| <span data-ttu-id="4d37f-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4d37f-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="4d37f-127"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4d37f-127"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4d37f-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="4d37f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d37f-129">**Interface ITabletCursor**</span><span class="sxs-lookup"><span data-stu-id="4d37f-129">**ITabletCursor Interface**</span></span>](itabletcursor.md)
</dt> </dl>

 

 




