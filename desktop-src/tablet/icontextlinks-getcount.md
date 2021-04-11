---
description: Obtém o número de objetos IContextLink nesta coleção.
ms.assetid: c3becacd-2df0-401c-88c8-5fad3e9f8c02
title: 'Método IContextLinks:: GetCount (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextLinks.GetCount
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: c12fae76eb41bf05d60712cf9f69639c713066c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164548"
---
# <a name="icontextlinksgetcount-method"></a><span data-ttu-id="69dca-103">Método IContextLinks:: GetCount</span><span class="sxs-lookup"><span data-stu-id="69dca-103">IContextLinks::GetCount method</span></span>

<span data-ttu-id="69dca-104">Obtém o número de objetos [**IContextLink**](icontextlink.md) nesta coleção.</span><span class="sxs-lookup"><span data-stu-id="69dca-104">Gets the number of [**IContextLink**](icontextlink.md) objects in this collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="69dca-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="69dca-105">Syntax</span></span>


```C++
HRESULT GetCount(
  [out, retval] ULONG *pulCount
);
```



## <a name="parameters"></a><span data-ttu-id="69dca-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="69dca-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69dca-107">*pulCount* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="69dca-107">*pulCount* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="69dca-108">O número de objetos [**IContextLink**](icontextlink.md) contidos nesta coleção.</span><span class="sxs-lookup"><span data-stu-id="69dca-108">The number of [**IContextLink**](icontextlink.md) objects that are contained in this collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69dca-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="69dca-109">Return value</span></span>

<span data-ttu-id="69dca-110">Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="69dca-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="69dca-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="69dca-111">Requirements</span></span>



| <span data-ttu-id="69dca-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="69dca-112">Requirement</span></span> | <span data-ttu-id="69dca-113">Valor</span><span class="sxs-lookup"><span data-stu-id="69dca-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="69dca-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="69dca-114">Minimum supported client</span></span><br/> | <span data-ttu-id="69dca-115">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="69dca-115">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="69dca-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="69dca-116">Minimum supported server</span></span><br/> | <span data-ttu-id="69dca-117">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="69dca-117">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="69dca-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="69dca-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="69dca-119"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="69dca-119"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="69dca-120">DLL</span><span class="sxs-lookup"><span data-stu-id="69dca-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="69dca-121"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="69dca-121"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="69dca-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="69dca-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69dca-123">**IContextLinks**</span><span class="sxs-lookup"><span data-stu-id="69dca-123">**IContextLinks**</span></span>](icontextlinks.md)
</dt> <dt>

[<span data-ttu-id="69dca-124">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="69dca-124">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




