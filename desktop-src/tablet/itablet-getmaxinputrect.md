---
description: Recupera um retângulo que representa a área de entrada máxima do Tablet.
ms.assetid: 98facd24-b019-40d1-afe1-28c9a78cae80
title: 'Método ITablet:: GetMaxInputRect'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet.GetMaxInputRect
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: de2649fe7410e6d335f653c09bfe86a8ddaac813
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829379"
---
# <a name="itabletgetmaxinputrect-method"></a><span data-ttu-id="04454-103">Método ITablet:: GetMaxInputRect</span><span class="sxs-lookup"><span data-stu-id="04454-103">ITablet::GetMaxInputRect method</span></span>

<span data-ttu-id="04454-104">Recupera um retângulo que representa a área de entrada máxima do Tablet.</span><span class="sxs-lookup"><span data-stu-id="04454-104">Retrieves a rectangle that represents maximum input area of the tablet.</span></span>

## <a name="syntax"></a><span data-ttu-id="04454-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="04454-105">Syntax</span></span>


```C++
HRESULT GetMaxInputRect(
  [out] RECT *prcInput
);
```



## <a name="parameters"></a><span data-ttu-id="04454-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="04454-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04454-107">*prcInput* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="04454-107">*prcInput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="04454-108">Ponteiro para retângulo que representa a área de entrada máxima do Tablet.</span><span class="sxs-lookup"><span data-stu-id="04454-108">Pointer to rectangle that represents maximum input area of the tablet.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04454-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="04454-109">Return value</span></span>

<span data-ttu-id="04454-110">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="04454-110">This method can return one of these values.</span></span>



| <span data-ttu-id="04454-111">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="04454-111">Return code</span></span>                                                                            | <span data-ttu-id="04454-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="04454-112">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="04454-113"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="04454-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="04454-114">Êxito.</span><span class="sxs-lookup"><span data-stu-id="04454-114">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="04454-115"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="04454-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="04454-116">Ocorreu um erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="04454-116">An unspecified error occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="04454-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="04454-117">Requirements</span></span>



| <span data-ttu-id="04454-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="04454-118">Requirement</span></span> | <span data-ttu-id="04454-119">Valor</span><span class="sxs-lookup"><span data-stu-id="04454-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="04454-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="04454-120">Minimum supported client</span></span><br/> | <span data-ttu-id="04454-121">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="04454-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="04454-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="04454-122">Minimum supported server</span></span><br/> | <span data-ttu-id="04454-123">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="04454-123">None supported</span></span><br/>                                                              |
| <span data-ttu-id="04454-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="04454-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="04454-125"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="04454-125"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04454-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="04454-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04454-127">**Interface ITablet**</span><span class="sxs-lookup"><span data-stu-id="04454-127">**ITablet Interface**</span></span>](itablet.md)
</dt> </dl>

 

 




