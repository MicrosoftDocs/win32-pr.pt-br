---
description: Recupera o número de tablets anexados ao sistema.
ms.assetid: b2027336-611b-4d17-8943-f16770effaf8
title: 'Método ITabletManager:: GetTabletCount'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletManager.GetTabletCount
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: fbdd485c44bc67b3ecaec5aa279d4bc20e18d167
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171854"
---
# <a name="itabletmanagergettabletcount-method"></a><span data-ttu-id="758c9-103">Método ITabletManager:: GetTabletCount</span><span class="sxs-lookup"><span data-stu-id="758c9-103">ITabletManager::GetTabletCount method</span></span>

<span data-ttu-id="758c9-104">Recupera o número de tablets anexados ao sistema.</span><span class="sxs-lookup"><span data-stu-id="758c9-104">Retrieves the number of tablets attached to the system.</span></span>

## <a name="syntax"></a><span data-ttu-id="758c9-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="758c9-105">Syntax</span></span>


```C++
HRESULT GetTabletCount(
  [out] ULONG *pcTablets
);
```



## <a name="parameters"></a><span data-ttu-id="758c9-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="758c9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="758c9-107">*pcTablets* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="758c9-107">*pcTablets* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="758c9-108">O número de tablets anexados ao sistema.</span><span class="sxs-lookup"><span data-stu-id="758c9-108">The number of tablets attached to the system.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="758c9-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="758c9-109">Return value</span></span>

<span data-ttu-id="758c9-110">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="758c9-110">This method can return one of these values.</span></span>



| <span data-ttu-id="758c9-111">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="758c9-111">Return code</span></span>                                                                            | <span data-ttu-id="758c9-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="758c9-112">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="758c9-113"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="758c9-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="758c9-114">Êxito.</span><span class="sxs-lookup"><span data-stu-id="758c9-114">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="758c9-115"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="758c9-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="758c9-116">Ocorreu um erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="758c9-116">An unspecified error occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="758c9-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="758c9-117">Requirements</span></span>



| <span data-ttu-id="758c9-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="758c9-118">Requirement</span></span> | <span data-ttu-id="758c9-119">Valor</span><span class="sxs-lookup"><span data-stu-id="758c9-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="758c9-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="758c9-120">Minimum supported client</span></span><br/> | <span data-ttu-id="758c9-121">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="758c9-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="758c9-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="758c9-122">Minimum supported server</span></span><br/> | <span data-ttu-id="758c9-123">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="758c9-123">None supported</span></span><br/>                                                              |
| <span data-ttu-id="758c9-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="758c9-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="758c9-125"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="758c9-125"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="758c9-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="758c9-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="758c9-127">**Interface ITabletManager**</span><span class="sxs-lookup"><span data-stu-id="758c9-127">**ITabletManager Interface**</span></span>](itabletmanager.md)
</dt> </dl>

 

 




