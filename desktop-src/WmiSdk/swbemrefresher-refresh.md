---
description: O método SWbemRefresher. Refresh atualiza todos os itens contidos no objeto SWbemRefresher. Objeto SWbemRefresher.
ms.assetid: 85a4777a-4be7-44f2-b7a6-e18b5e57f7af
ms.tgt_platform: multiple
title: Método SWbemRefresher. Refresh (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefresher.Refresh
- ISWbemRefresher.Refresh
- ISWbemRefresher.Refresh
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: d8b2522227041858770c7256d7d2520cc661948e
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105768213"
---
# <a name="swbemrefresherrefresh-method"></a><span data-ttu-id="b327a-103">Método SWbemRefresher. Refresh</span><span class="sxs-lookup"><span data-stu-id="b327a-103">SWbemRefresher.Refresh method</span></span>

<span data-ttu-id="b327a-104">O método **SWbemRefresher. Refresh** atualiza todos os itens contidos no objeto [**SWbemRefresher**](swbemrefresher.md) .</span><span class="sxs-lookup"><span data-stu-id="b327a-104">The **SWbemRefresher.Refresh** method updates all the items that are contained in the [**SWbemRefresher**](swbemrefresher.md) object.</span></span>

<span data-ttu-id="b327a-105">Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="b327a-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="b327a-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b327a-106">Syntax</span></span>


```VB
SWbemRefresher.Refresh( _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="b327a-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b327a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b327a-108">*iFlags* \[ adicional\]</span><span class="sxs-lookup"><span data-stu-id="b327a-108">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b327a-109">Os sinalizadores devem ser definidos como 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="b327a-109">Flags must be set to 0 (zero).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b327a-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b327a-110">Return value</span></span>

<span data-ttu-id="b327a-111">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="b327a-111">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="b327a-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b327a-112">Requirements</span></span>



| <span data-ttu-id="b327a-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="b327a-113">Requirement</span></span> | <span data-ttu-id="b327a-114">Valor</span><span class="sxs-lookup"><span data-stu-id="b327a-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b327a-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b327a-115">Minimum supported client</span></span><br/> | <span data-ttu-id="b327a-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b327a-116">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b327a-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b327a-117">Minimum supported server</span></span><br/> | <span data-ttu-id="b327a-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b327a-118">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b327a-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b327a-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="b327a-120"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="b327a-120"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="b327a-121">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="b327a-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="b327a-122"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="b327a-122"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="b327a-123">DLL</span><span class="sxs-lookup"><span data-stu-id="b327a-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b327a-124"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b327a-124"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="b327a-125">CLSID</span><span class="sxs-lookup"><span data-stu-id="b327a-125">CLSID</span></span><br/>                    | <span data-ttu-id="b327a-126">\_SWBEMREFRESHER CLSID</span><span class="sxs-lookup"><span data-stu-id="b327a-126">CLSID\_SWbemRefresher</span></span><br/>                                                        |
| <span data-ttu-id="b327a-127">IID</span><span class="sxs-lookup"><span data-stu-id="b327a-127">IID</span></span><br/>                      | <span data-ttu-id="b327a-128">ISWbemRefresher de IID \_</span><span class="sxs-lookup"><span data-stu-id="b327a-128">IID\_ISWbemRefresher</span></span><br/>                                                         |



## <a name="see-also"></a><span data-ttu-id="b327a-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="b327a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b327a-130">**SWbemRefresher**</span><span class="sxs-lookup"><span data-stu-id="b327a-130">**SWbemRefresher**</span></span>](swbemrefresher.md)
</dt> </dl>

 

 




