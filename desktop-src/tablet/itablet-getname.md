---
description: Retorna uma cadeia de caracteres que contém o nome do dispositivo tablet.
ms.assetid: 025620b5-ab68-4e36-ae26-2226a2fdeb61
title: 'Método ITablet:: GetName'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet.GetName
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: c2d6bd20a011b1bf5cfbe7582445de45728bbd7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104169898"
---
# <a name="itabletgetname-method"></a><span data-ttu-id="00b89-103">Método ITablet:: GetName</span><span class="sxs-lookup"><span data-stu-id="00b89-103">ITablet::GetName method</span></span>

<span data-ttu-id="00b89-104">Retorna uma cadeia de caracteres que contém o nome do dispositivo tablet.</span><span class="sxs-lookup"><span data-stu-id="00b89-104">Returns a string containing the name of the tablet device.</span></span>

## <a name="syntax"></a><span data-ttu-id="00b89-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="00b89-105">Syntax</span></span>


```C++
HRESULT GetName(
  [out] LPWSTR *ppwszName
);
```



## <a name="parameters"></a><span data-ttu-id="00b89-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="00b89-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00b89-107">*ppwszName* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="00b89-107">*ppwszName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="00b89-108">Ponteiro para uma cadeia de caracteres que contém o nome do dispositivo tablet.</span><span class="sxs-lookup"><span data-stu-id="00b89-108">Pointer to a string containing the name of the tablet device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00b89-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="00b89-109">Return value</span></span>

<span data-ttu-id="00b89-110">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="00b89-110">This method can return one of these values.</span></span>



| <span data-ttu-id="00b89-111">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="00b89-111">Return code</span></span>                                                                            | <span data-ttu-id="00b89-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="00b89-112">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="00b89-113"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="00b89-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="00b89-114">Êxito.</span><span class="sxs-lookup"><span data-stu-id="00b89-114">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="00b89-115"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="00b89-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="00b89-116">Ocorreu um erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="00b89-116">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="00b89-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="00b89-117">Remarks</span></span>

<span data-ttu-id="00b89-118">É responsabilidade do chamador liberar a memória retornada desse método usando [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span><span class="sxs-lookup"><span data-stu-id="00b89-118">It is the caller's responsibility to free the memory returned from this method by using [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span></span>

## <a name="requirements"></a><span data-ttu-id="00b89-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="00b89-119">Requirements</span></span>



| <span data-ttu-id="00b89-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="00b89-120">Requirement</span></span> | <span data-ttu-id="00b89-121">Valor</span><span class="sxs-lookup"><span data-stu-id="00b89-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="00b89-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="00b89-122">Minimum supported client</span></span><br/> | <span data-ttu-id="00b89-123">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="00b89-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="00b89-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="00b89-124">Minimum supported server</span></span><br/> | <span data-ttu-id="00b89-125">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="00b89-125">None supported</span></span><br/>                                                              |
| <span data-ttu-id="00b89-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="00b89-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="00b89-127"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="00b89-127"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="00b89-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="00b89-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00b89-129">**Interface ITablet**</span><span class="sxs-lookup"><span data-stu-id="00b89-129">**ITablet Interface**</span></span>](itablet.md)
</dt> </dl>

 

