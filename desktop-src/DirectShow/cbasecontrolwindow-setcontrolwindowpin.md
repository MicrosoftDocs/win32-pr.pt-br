---
description: O método SetControlWindowPin define o PIN com o qual sincronizar.
ms.assetid: 6373c046-5448-4159-88b9-9b2babdb938b
title: Método CBaseControlWindow. SetControlWindowPin (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.SetControlWindowPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c1aa3d4960799c2286e17709258ea90b76332bc2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751276"
---
# <a name="cbasecontrolwindowsetcontrolwindowpin-method"></a><span data-ttu-id="3eadc-103">Método CBaseControlWindow. SetControlWindowPin</span><span class="sxs-lookup"><span data-stu-id="3eadc-103">CBaseControlWindow.SetControlWindowPin method</span></span>

<span data-ttu-id="3eadc-104">O `SetControlWindowPin` método define o PIN com o qual sincronizar.</span><span class="sxs-lookup"><span data-stu-id="3eadc-104">The `SetControlWindowPin` method sets the pin with which to synchronize.</span></span>

## <a name="syntax"></a><span data-ttu-id="3eadc-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3eadc-105">Syntax</span></span>


```C++
void SetControlWindowPin(
   CBasePin *pPin
);
```



## <a name="parameters"></a><span data-ttu-id="3eadc-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3eadc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3eadc-107">*pPin*</span><span class="sxs-lookup"><span data-stu-id="3eadc-107">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="3eadc-108">Ponteiro para o PIN com o qual a interface é sincronizada.</span><span class="sxs-lookup"><span data-stu-id="3eadc-108">Pointer to the pin with which the interface is synchronized.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3eadc-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3eadc-109">Return value</span></span>

<span data-ttu-id="3eadc-110">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="3eadc-110">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3eadc-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="3eadc-111">Remarks</span></span>

<span data-ttu-id="3eadc-112">Essa função de membro define a \_ variável de membro m pPin igual ao parâmetro pPin.</span><span class="sxs-lookup"><span data-stu-id="3eadc-112">This member function sets the m\_pPin member variable equal to the pPin parameter.</span></span> <span data-ttu-id="3eadc-113">Conforme descrito no construtor, a interface pode ser chamada somente quando o filtro tiver sido conectado com êxito.</span><span class="sxs-lookup"><span data-stu-id="3eadc-113">As described in the constructor, the interface can be called only when the filter has been connected successfully.</span></span> <span data-ttu-id="3eadc-114">O objeto é transmitido por meio dessa função de membro para o PIN com o qual deve ser sincronizado; na maioria dos casos, ele determinará se o PIN está conectado sempre que ele tiver um método de interface chamado e retornará VFW \_ e \_ não \_ conectado se falhar.</span><span class="sxs-lookup"><span data-stu-id="3eadc-114">The object is passed in through this member function to the pin with which it should synchronize; in most cases, it will determine if the pin is connected whenever it has an interface method called and will return VFW\_E\_NOT\_CONNECTED if it fails.</span></span>

## <a name="requirements"></a><span data-ttu-id="3eadc-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3eadc-115">Requirements</span></span>



| <span data-ttu-id="3eadc-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="3eadc-116">Requirement</span></span> | <span data-ttu-id="3eadc-117">Valor</span><span class="sxs-lookup"><span data-stu-id="3eadc-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3eadc-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3eadc-118">Header</span></span><br/>  | <dl> <span data-ttu-id="3eadc-119"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3eadc-119"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="3eadc-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3eadc-120">Library</span></span><br/> | <dl> <span data-ttu-id="3eadc-121"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="3eadc-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3eadc-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="3eadc-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3eadc-123">**Classe CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="3eadc-123">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




