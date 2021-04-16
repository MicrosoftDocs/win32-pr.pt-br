---
description: 'O método IsPageDirty indica se a página de propriedades foi alterada desde que foi ativada ou desde a chamada mais recente para IPropertyPage:: apply. Esse método implementa o método IPropertyPage:: IsPageDirty.'
ms.assetid: 95eeec26-7dbb-4add-a827-6505b40afe48
title: Método CBasePropertyPage. IsPageDirty (cProp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.IsPageDirty
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c69c2e7d480f63542e146c73e56b9e692693f665
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750064"
---
# <a name="cbasepropertypageispagedirty-method"></a><span data-ttu-id="ec495-104">Método CBasePropertyPage. IsPageDirty</span><span class="sxs-lookup"><span data-stu-id="ec495-104">CBasePropertyPage.IsPageDirty method</span></span>

<span data-ttu-id="ec495-105">O `IsPageDirty` método indica se a página de propriedades foi alterada desde que foi ativada ou desde a chamada mais recente para **IPropertyPage:: apply**.</span><span class="sxs-lookup"><span data-stu-id="ec495-105">The `IsPageDirty` method indicates whether the property page has changed since it was activated or since the most recent call to **IPropertyPage::Apply**.</span></span> <span data-ttu-id="ec495-106">Esse método implementa o método **IPropertyPage:: IsPageDirty** .</span><span class="sxs-lookup"><span data-stu-id="ec495-106">This method implements the **IPropertyPage::IsPageDirty** method.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec495-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ec495-107">Syntax</span></span>


```C++
HRESULT IsPageDirty();
```



## <a name="parameters"></a><span data-ttu-id="ec495-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ec495-108">Parameters</span></span>

<span data-ttu-id="ec495-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="ec495-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ec495-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ec495-110">Return value</span></span>

<span data-ttu-id="ec495-111">Retorna S \_ OK se [**CBasePropertyPage:: m \_ bDirty**](cbasepropertypage-m-bdirty.md) for **true** ou S \_ false, caso contrário.</span><span class="sxs-lookup"><span data-stu-id="ec495-111">Returns S\_OK if [**CBasePropertyPage::m\_bDirty**](cbasepropertypage-m-bdirty.md) is **TRUE**, or S\_FALSE otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec495-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ec495-112">Requirements</span></span>



| <span data-ttu-id="ec495-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="ec495-113">Requirement</span></span> | <span data-ttu-id="ec495-114">Valor</span><span class="sxs-lookup"><span data-stu-id="ec495-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec495-115">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ec495-115">Header</span></span><br/>  | <dl> <span data-ttu-id="ec495-116"><dt>CProp. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ec495-116"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="ec495-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ec495-117">Library</span></span><br/> | <dl> <span data-ttu-id="ec495-118"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="ec495-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ec495-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="ec495-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec495-120">**Classe CBasePropertyPage**</span><span class="sxs-lookup"><span data-stu-id="ec495-120">**CBasePropertyPage Class**</span></span>](cbasepropertypage.md)
</dt> </dl>

 

 




