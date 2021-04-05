---
description: Recupera as configurações de contexto padrão para o Tablet.
ms.assetid: 59d1bab0-a8b8-4e23-9311-2921f9035dc4
title: 'Método ITablet:: GetDefaultContextSettings'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet.GetDefaultContextSettings
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 7e2f0977257553d8405b337dcc1f22d8b0fdff5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662438"
---
# <a name="itabletgetdefaultcontextsettings-method"></a><span data-ttu-id="78f7b-103">Método ITablet:: GetDefaultContextSettings</span><span class="sxs-lookup"><span data-stu-id="78f7b-103">ITablet::GetDefaultContextSettings method</span></span>

<span data-ttu-id="78f7b-104">Recupera as configurações de contexto padrão para o Tablet.</span><span class="sxs-lookup"><span data-stu-id="78f7b-104">Retrieves the default context settings for the tablet.</span></span>

## <a name="syntax"></a><span data-ttu-id="78f7b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="78f7b-105">Syntax</span></span>


```C++
HRESULT GetDefaultContextSettings(
  [out] TABLET_CONTEXT_SETTINGS **ppTCS
);
```



## <a name="parameters"></a><span data-ttu-id="78f7b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="78f7b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78f7b-107">*ppTCS* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="78f7b-107">*ppTCS* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="78f7b-108">As configurações de contexto padrão para o Tablet.</span><span class="sxs-lookup"><span data-stu-id="78f7b-108">The default context settings for the tablet.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78f7b-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="78f7b-109">Return value</span></span>

<span data-ttu-id="78f7b-110">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="78f7b-110">This method can return one of these values.</span></span>



| <span data-ttu-id="78f7b-111">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="78f7b-111">Return code</span></span>                                                                            | <span data-ttu-id="78f7b-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="78f7b-112">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="78f7b-113"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="78f7b-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="78f7b-114">Êxito.</span><span class="sxs-lookup"><span data-stu-id="78f7b-114">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="78f7b-115"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="78f7b-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="78f7b-116">Ocorreu um erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="78f7b-116">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="78f7b-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="78f7b-117">Remarks</span></span>

<span data-ttu-id="78f7b-118">É responsabilidade do chamador liberar a memória retornada desse método usando [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span><span class="sxs-lookup"><span data-stu-id="78f7b-118">It is the caller's responsibility to free the memory returned from this method by using [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).</span></span>

## <a name="requirements"></a><span data-ttu-id="78f7b-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="78f7b-119">Requirements</span></span>



| <span data-ttu-id="78f7b-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="78f7b-120">Requirement</span></span> | <span data-ttu-id="78f7b-121">Valor</span><span class="sxs-lookup"><span data-stu-id="78f7b-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="78f7b-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="78f7b-122">Minimum supported client</span></span><br/> | <span data-ttu-id="78f7b-123">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="78f7b-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="78f7b-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="78f7b-124">Minimum supported server</span></span><br/> | <span data-ttu-id="78f7b-125">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="78f7b-125">None supported</span></span><br/>                                                              |
| <span data-ttu-id="78f7b-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="78f7b-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="78f7b-127"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="78f7b-127"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="78f7b-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="78f7b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78f7b-129">**Interface ITablet**</span><span class="sxs-lookup"><span data-stu-id="78f7b-129">**ITablet Interface**</span></span>](itablet.md)
</dt> </dl>

 

