---
description: Construtor de CBasePropertyPage. CBasePropertyPage-método de construtor.
ms.assetid: 5d9863e7-fdd9-4df2-a603-34a240a2286c
title: Construtor CBasePropertyPage. CBasePropertyPage (cProp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.CBasePropertyPage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 95821062b6b1199ea98a5329934d76e2197901d4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119944"
---
# <a name="cbasepropertypagecbasepropertypage-constructor"></a><span data-ttu-id="1dd8d-103">Construtor CBasePropertyPage. CBasePropertyPage</span><span class="sxs-lookup"><span data-stu-id="1dd8d-103">CBasePropertyPage.CBasePropertyPage constructor</span></span>

<span data-ttu-id="1dd8d-104">Método de construtor.</span><span class="sxs-lookup"><span data-stu-id="1dd8d-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="1dd8d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1dd8d-105">Syntax</span></span>


```C++
CBasePropertyPage(
   TCHAR     *pName,
   LPUNKNOWN pUnk,
   int       DialogId,
   int       TitleId
);
```



## <a name="parameters"></a><span data-ttu-id="1dd8d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1dd8d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1dd8d-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="1dd8d-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="1dd8d-108">Cadeia de caracteres que contém o nome do objeto, para fins de depuração.</span><span class="sxs-lookup"><span data-stu-id="1dd8d-108">String that contains the name of the object, for debugging purposes.</span></span> <span data-ttu-id="1dd8d-109">Para obter mais informações, consulte [**CBaseObject:: CBaseObject**](cbaseobject-cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="1dd8d-109">For more information, see [**CBaseObject::CBaseObject**](cbaseobject-cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="1dd8d-110">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="1dd8d-110">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="1dd8d-111">Ponteiro para a interface **IUnknown** de agregação.</span><span class="sxs-lookup"><span data-stu-id="1dd8d-111">Pointer to the aggregating **IUnknown** interface.</span></span>

</dd> <dt>

<span data-ttu-id="1dd8d-112">*Caixa de diálogo*</span><span class="sxs-lookup"><span data-stu-id="1dd8d-112">*DialogId*</span></span> 
</dt> <dd>

<span data-ttu-id="1dd8d-113">ID do recurso da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="1dd8d-113">Resource ID for the dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="1dd8d-114">*Título da*</span><span class="sxs-lookup"><span data-stu-id="1dd8d-114">*TitleId*</span></span> 
</dt> <dd>

<span data-ttu-id="1dd8d-115">ID de recurso da cadeia de caracteres que contém o título da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="1dd8d-115">Resource ID for the string that contains the dialog box title.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="1dd8d-116">Exemplos</span><span class="sxs-lookup"><span data-stu-id="1dd8d-116">Examples</span></span>


```C++
CMyProp::CMyProp(IUnknown *pUnk) : 
    CBasePropertyPage(NAME("MyPropPage"), pUnk, IDD_PROPPAGE, IDS_TITLE),
```



## <a name="requirements"></a><span data-ttu-id="1dd8d-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1dd8d-117">Requirements</span></span>



| <span data-ttu-id="1dd8d-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="1dd8d-118">Requirement</span></span> | <span data-ttu-id="1dd8d-119">Valor</span><span class="sxs-lookup"><span data-stu-id="1dd8d-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1dd8d-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1dd8d-120">Header</span></span><br/>  | <dl> <span data-ttu-id="1dd8d-121"><dt>CProp. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1dd8d-121"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="1dd8d-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1dd8d-122">Library</span></span><br/> | <dl> <span data-ttu-id="1dd8d-123"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="1dd8d-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1dd8d-124">Consulte também</span><span class="sxs-lookup"><span data-stu-id="1dd8d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1dd8d-125">**Classe CBasePropertyPage**</span><span class="sxs-lookup"><span data-stu-id="1dd8d-125">**CBasePropertyPage Class**</span></span>](cbasepropertypage.md)
</dt> </dl>

 

 




