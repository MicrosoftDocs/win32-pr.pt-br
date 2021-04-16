---
description: Recupera o nome do botão da caneta.
ms.assetid: 26fad9bc-43c2-4b00-b76b-bf9f1242da77
title: 'Método ITabletCursorButton:: GetName'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletCursorButton.GetName
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: b21fd92823fb0f60c0936f662982d176a938b4dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105811085"
---
# <a name="itabletcursorbuttongetname-method"></a><span data-ttu-id="f9426-103">Método ITabletCursorButton:: GetName</span><span class="sxs-lookup"><span data-stu-id="f9426-103">ITabletCursorButton::GetName method</span></span>

<span data-ttu-id="f9426-104">Recupera o nome do botão da caneta.</span><span class="sxs-lookup"><span data-stu-id="f9426-104">Retrieves the name of the stylus button.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9426-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f9426-105">Syntax</span></span>


```C++
HRESULT GetName(
  [out] LPWSTR *ppwszName
);
```



## <a name="parameters"></a><span data-ttu-id="f9426-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f9426-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9426-107">*ppwszName* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="f9426-107">*ppwszName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f9426-108">O nome do botão da caneta.</span><span class="sxs-lookup"><span data-stu-id="f9426-108">The name of the stylus button.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f9426-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f9426-109">Return value</span></span>

<span data-ttu-id="f9426-110">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="f9426-110">This method can return one of these values.</span></span>



| <span data-ttu-id="f9426-111">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="f9426-111">Return code</span></span>                                                                            | <span data-ttu-id="f9426-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="f9426-112">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="f9426-113"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f9426-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="f9426-114">Êxito.</span><span class="sxs-lookup"><span data-stu-id="f9426-114">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="f9426-115"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="f9426-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="f9426-116">Ocorreu um erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="f9426-116">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f9426-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="f9426-117">Remarks</span></span>

<span data-ttu-id="f9426-118">É responsabilidade do chamador liberar a memória retornada desse método usando [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span><span class="sxs-lookup"><span data-stu-id="f9426-118">It is the caller's responsibility to free the memory returned from this method by using [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span></span>

## <a name="requirements"></a><span data-ttu-id="f9426-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f9426-119">Requirements</span></span>



| <span data-ttu-id="f9426-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="f9426-120">Requirement</span></span> | <span data-ttu-id="f9426-121">Valor</span><span class="sxs-lookup"><span data-stu-id="f9426-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f9426-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f9426-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f9426-123">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="f9426-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="f9426-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f9426-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f9426-125">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="f9426-125">None supported</span></span><br/>                                                              |
| <span data-ttu-id="f9426-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f9426-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="f9426-127"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f9426-127"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9426-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="f9426-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9426-129">**Interface ITabletCursorButton**</span><span class="sxs-lookup"><span data-stu-id="f9426-129">**ITabletCursorButton Interface**</span></span>](itabletcursorbutton.md)
</dt> </dl>

 

