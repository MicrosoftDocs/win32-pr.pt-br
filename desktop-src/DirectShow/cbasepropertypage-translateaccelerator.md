---
description: 'O método TranslateAccelerator instrui a página de propriedades a processar um pressionamento de tecla. Esse método implementa o método IPropertyPage:: TranslateAccelerator.'
ms.assetid: 2da214c9-35dc-470c-9b7f-2f4ef6bcd40a
title: Método CBasePropertyPage. TranslateAccelerator (cProp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.TranslateAccelerator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3116e85eec8fbf3a00bf434a1f88c8cac662ed0a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747402"
---
# <a name="cbasepropertypagetranslateaccelerator-method"></a><span data-ttu-id="707f6-104">Método CBasePropertyPage. TranslateAccelerator</span><span class="sxs-lookup"><span data-stu-id="707f6-104">CBasePropertyPage.TranslateAccelerator method</span></span>

<span data-ttu-id="707f6-105">O `TranslateAccelerator` método instrui a página de propriedades a processar um pressionamento de tecla.</span><span class="sxs-lookup"><span data-stu-id="707f6-105">The `TranslateAccelerator` method instructs the property page to process a keystroke.</span></span> <span data-ttu-id="707f6-106">Esse método implementa o método **IPropertyPage:: TranslateAccelerator** .</span><span class="sxs-lookup"><span data-stu-id="707f6-106">This method implements the **IPropertyPage::TranslateAccelerator** method.</span></span>

## <a name="syntax"></a><span data-ttu-id="707f6-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="707f6-107">Syntax</span></span>


```C++
HRESULT TranslateAccelerator(
   LPMSG lpMsg
);
```



## <a name="parameters"></a><span data-ttu-id="707f6-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="707f6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="707f6-109">*lpMsg*</span><span class="sxs-lookup"><span data-stu-id="707f6-109">*lpMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="707f6-110">Ponteiro para uma estrutura **msg** que descreve a tecla para processar.</span><span class="sxs-lookup"><span data-stu-id="707f6-110">Pointer to a **MSG** structure describing the keystroke to process.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="707f6-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="707f6-111">Return value</span></span>

<span data-ttu-id="707f6-112">Retorna E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="707f6-112">Returns E\_NOTIMPL.</span></span>

## <a name="remarks"></a><span data-ttu-id="707f6-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="707f6-113">Remarks</span></span>

<span data-ttu-id="707f6-114">Substitua esse método se desejar fornecer aceleradores de teclado para a página de propriedades.</span><span class="sxs-lookup"><span data-stu-id="707f6-114">Override this method if you want to provide keyboard accelerators for the property page.</span></span>

## <a name="requirements"></a><span data-ttu-id="707f6-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="707f6-115">Requirements</span></span>



| <span data-ttu-id="707f6-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="707f6-116">Requirement</span></span> | <span data-ttu-id="707f6-117">Valor</span><span class="sxs-lookup"><span data-stu-id="707f6-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="707f6-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="707f6-118">Header</span></span><br/>  | <dl> <span data-ttu-id="707f6-119"><dt>CProp. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="707f6-119"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="707f6-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="707f6-120">Library</span></span><br/> | <dl> <span data-ttu-id="707f6-121"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="707f6-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="707f6-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="707f6-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="707f6-123">**Classe CBasePropertyPage**</span><span class="sxs-lookup"><span data-stu-id="707f6-123">**CBasePropertyPage Class**</span></span>](cbasepropertypage.md)
</dt> </dl>

 

 




