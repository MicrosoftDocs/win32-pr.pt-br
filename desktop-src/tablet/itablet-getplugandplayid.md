---
description: Retorna uma cadeia de caracteres que contém a ID de Plug and Play para o dispositivo tablet.
ms.assetid: a0b6619b-f80c-470b-aa3f-f0b30a9dbda8
title: 'Método ITablet:: GetPlugAndPlayId'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet.GetPlugAndPlayId
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 3fb6ce7d59cb29aac4b06b7245bc6246b0688a7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105793721"
---
# <a name="itabletgetplugandplayid-method"></a><span data-ttu-id="bb431-103">Método ITablet:: GetPlugAndPlayId</span><span class="sxs-lookup"><span data-stu-id="bb431-103">ITablet::GetPlugAndPlayId method</span></span>

<span data-ttu-id="bb431-104">Retorna uma cadeia de caracteres que contém a ID de Plug and Play para o dispositivo tablet.</span><span class="sxs-lookup"><span data-stu-id="bb431-104">Returns a string containing the Plug and Play ID for the tablet device.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb431-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bb431-105">Syntax</span></span>


```C++
HRESULT GetPlugAndPlayId(
  [out] LPWSTR *ppwszPPId
);
```



## <a name="parameters"></a><span data-ttu-id="bb431-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bb431-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb431-107">*ppwszPPId* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="bb431-107">*ppwszPPId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bb431-108">Ponteiro para uma cadeia de caracteres que contém a ID de Plug and Play para o dispositivo tablet.</span><span class="sxs-lookup"><span data-stu-id="bb431-108">Pointer to a string containing the Plug and Play ID for the tablet device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb431-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bb431-109">Return value</span></span>

<span data-ttu-id="bb431-110">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="bb431-110">This method can return one of these values.</span></span>



| <span data-ttu-id="bb431-111">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="bb431-111">Return code</span></span>                                                                            | <span data-ttu-id="bb431-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="bb431-112">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="bb431-113"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="bb431-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="bb431-114">Êxito.</span><span class="sxs-lookup"><span data-stu-id="bb431-114">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="bb431-115"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="bb431-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="bb431-116">Ocorreu um erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="bb431-116">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="bb431-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="bb431-117">Remarks</span></span>

<span data-ttu-id="bb431-118">É responsabilidade do chamador liberar a memória retornada desse método usando [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span><span class="sxs-lookup"><span data-stu-id="bb431-118">It is the caller's responsibility to free the memory returned from this method by using [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span></span>

## <a name="requirements"></a><span data-ttu-id="bb431-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bb431-119">Requirements</span></span>



| <span data-ttu-id="bb431-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="bb431-120">Requirement</span></span> | <span data-ttu-id="bb431-121">Valor</span><span class="sxs-lookup"><span data-stu-id="bb431-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bb431-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bb431-122">Minimum supported client</span></span><br/> | <span data-ttu-id="bb431-123">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="bb431-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="bb431-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bb431-124">Minimum supported server</span></span><br/> | <span data-ttu-id="bb431-125">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="bb431-125">None supported</span></span><br/>                                                              |
| <span data-ttu-id="bb431-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bb431-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="bb431-127"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="bb431-127"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb431-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="bb431-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb431-129">**Interface ITablet**</span><span class="sxs-lookup"><span data-stu-id="bb431-129">**ITablet Interface**</span></span>](itablet.md)
</dt> </dl>

 

