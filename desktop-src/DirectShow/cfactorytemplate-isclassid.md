---
description: O método isclassidid determina se um CLSID corresponde a esse modelo de classe.
ms.assetid: de560f7a-2ccb-44e2-ac32-3b0fea0d80b8
title: Método CFactoryTemplate. isclassidid (combase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CFactoryTemplate.IsClassID
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 94564d7e9db52f8be22717a10f73fffb7fb6fa14
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751489"
---
# <a name="cfactorytemplateisclassid-method"></a><span data-ttu-id="d902a-103">Método CFactoryTemplate. isclassidid</span><span class="sxs-lookup"><span data-stu-id="d902a-103">CFactoryTemplate.IsClassID method</span></span>

<span data-ttu-id="d902a-104">O `IsClassID` método determina se um CLSID corresponde a esse modelo de classe.</span><span class="sxs-lookup"><span data-stu-id="d902a-104">The `IsClassID` method determines whether a CLSID matches this class template.</span></span>

## <a name="syntax"></a><span data-ttu-id="d902a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d902a-105">Syntax</span></span>


```C++
BOOL IsClassID(
   REFCLSID rclsid
);
```



## <a name="parameters"></a><span data-ttu-id="d902a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d902a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d902a-107">*rclsid*</span><span class="sxs-lookup"><span data-stu-id="d902a-107">*rclsid*</span></span> 
</dt> <dd>

<span data-ttu-id="d902a-108">Referência a um CLSID.</span><span class="sxs-lookup"><span data-stu-id="d902a-108">Reference to a CLSID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d902a-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d902a-109">Return value</span></span>

<span data-ttu-id="d902a-110">Retornará **true** se o *parâmetro rclsid* for o mesmo CLSID que a variável de membro [**\_ CLSID CFactoryTemplate:: m**](cfactorytemplate-m-clsid.md) ou, caso contrário, retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="d902a-110">Returns **TRUE** if the *rclsid* parameter is the same CLSID as the [**CFactoryTemplate::m\_ClsID**](cfactorytemplate-m-clsid.md) member variable, or else returns **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="d902a-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d902a-111">Requirements</span></span>



| <span data-ttu-id="d902a-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="d902a-112">Requirement</span></span> | <span data-ttu-id="d902a-113">Valor</span><span class="sxs-lookup"><span data-stu-id="d902a-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d902a-114">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d902a-114">Header</span></span><br/>  | <dl> <span data-ttu-id="d902a-115"><dt>Combase. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d902a-115"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d902a-116">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d902a-116">Library</span></span><br/> | <dl> <span data-ttu-id="d902a-117"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="d902a-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d902a-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="d902a-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d902a-119">**Classe CFactoryTemplate**</span><span class="sxs-lookup"><span data-stu-id="d902a-119">**CFactoryTemplate Class**</span></span>](cfactorytemplate.md)
</dt> </dl>

 

 




