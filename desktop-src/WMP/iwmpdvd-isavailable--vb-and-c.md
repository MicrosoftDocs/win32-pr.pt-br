---
title: IWMPDVD. IsAvailable (VB e C)
description: A propriedade IsAvailable (o \_ método Get IsAvailable em C \) Obtém um valor que indica se um tipo de informação especificado está disponível ou uma ação especificada pode ser executada.
ms.assetid: 55690783-df2f-473d-a6f2-a4907b7e8a78
keywords:
- IWMPDVD. IsAvailable (VB e C) Windows Media Player
topic_type:
- apiref
api_name:
- IWMPDVD.isAvailable (VB and C )
api_location:
- Interop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e3409da619f337b61606baaf546cebbb438087c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760434"
---
# <a name="iwmpdvdisavailable-vb-and-c"></a><span data-ttu-id="eed0c-104">IWMPDVD. IsAvailable (VB e C#)</span><span class="sxs-lookup"><span data-stu-id="eed0c-104">IWMPDVD.isAvailable (VB and C#)</span></span>

<span data-ttu-id="eed0c-105">A propriedade **IsAvailable** (o método **Get \_ IsAvailable** em C#) Obtém um valor que indica se um tipo especificado de informação está disponível ou se uma ação especificada pode ser executada.</span><span class="sxs-lookup"><span data-stu-id="eed0c-105">The **isAvailable** property (the **get\_isAvailable** method in C#) gets a value that indicates whether a specified type of information is available or a specified action can be performed.</span></span>


```
[Visual Basic]
ReadOnly Property isAvailable(
  bstrItem As System.String
) As System.Boolean
```




```
[C#]
System.Boolean get_isAvailable (
  System.String bstrItem
)
```



## <a name="parameters"></a><span data-ttu-id="eed0c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="eed0c-106">Parameters</span></span>

<span data-ttu-id="eed0c-107">*bstrItem*</span><span class="sxs-lookup"><span data-stu-id="eed0c-107">*bstrItem*</span></span>

<span data-ttu-id="eed0c-108">Um System. String que é um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="eed0c-108">A System.String that is one of the following values.</span></span>



| <span data-ttu-id="eed0c-109">Valor</span><span class="sxs-lookup"><span data-stu-id="eed0c-109">Value</span></span>      | <span data-ttu-id="eed0c-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="eed0c-110">Description</span></span>                                                                                   |
|------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="eed0c-111">voltar</span><span class="sxs-lookup"><span data-stu-id="eed0c-111">back</span></span>       | <span data-ttu-id="eed0c-112">Descobre se o método **IWMPDVD. back** está disponível.</span><span class="sxs-lookup"><span data-stu-id="eed0c-112">Discovers whether the **IWMPDVD.back** method is available.</span></span>                                   |
| <span data-ttu-id="eed0c-113">DVD</span><span class="sxs-lookup"><span data-stu-id="eed0c-113">dvd</span></span>        | <span data-ttu-id="eed0c-114">Descobre se o DVD está carregado.</span><span class="sxs-lookup"><span data-stu-id="eed0c-114">Discovers whether the DVD is loaded.</span></span>                                                          |
| <span data-ttu-id="eed0c-115">dvdDecoder</span><span class="sxs-lookup"><span data-stu-id="eed0c-115">dvdDecoder</span></span> | <span data-ttu-id="eed0c-116">Descobre se o decodificador de DVD está instalado no sistema.</span><span class="sxs-lookup"><span data-stu-id="eed0c-116">Discovers whether the DVD decoder is installed on system.</span></span>                                     |
| <span data-ttu-id="eed0c-117">resume</span><span class="sxs-lookup"><span data-stu-id="eed0c-117">resume</span></span>     | <span data-ttu-id="eed0c-118">Descobre se o método **IWMPDVD. resume** está disponível.</span><span class="sxs-lookup"><span data-stu-id="eed0c-118">Discovers whether the **IWMPDVD.resume** method is available.</span></span>                                 |
| <span data-ttu-id="eed0c-119">titleMenu</span><span class="sxs-lookup"><span data-stu-id="eed0c-119">titleMenu</span></span>  | <span data-ttu-id="eed0c-120">Descobre se o método **IWMPDVD. titleMenu** está disponível.</span><span class="sxs-lookup"><span data-stu-id="eed0c-120">Discovers whether the **IWMPDVD.titleMenu** method is available.</span></span>                              |
| <span data-ttu-id="eed0c-121">topMenu</span><span class="sxs-lookup"><span data-stu-id="eed0c-121">topMenu</span></span>    | <span data-ttu-id="eed0c-122">Descobre se o método **IWMPDVD. topMenu** está disponível.</span><span class="sxs-lookup"><span data-stu-id="eed0c-122">Discovers whether the **IWMPDVD.topMenu** method is available.</span></span> <span data-ttu-id="eed0c-123">Normalmente chamado de menu raiz.</span><span class="sxs-lookup"><span data-stu-id="eed0c-123">Commonly called the root menu.</span></span> |



 

## <a name="property-value"></a><span data-ttu-id="eed0c-124">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="eed0c-124">Property Value</span></span>

<span data-ttu-id="eed0c-125">**System.Boolean**</span><span class="sxs-lookup"><span data-stu-id="eed0c-125">**System.Boolean**</span></span>

<span data-ttu-id="eed0c-126">Um **System. Boolean** que indica se um tipo especificado de informações está disponível ou se uma ação especificada pode ser executada.</span><span class="sxs-lookup"><span data-stu-id="eed0c-126">A **System.Boolean** that indicates whether a specified type of information is available or a specified action can be performed.</span></span>

## <a name="remarks"></a><span data-ttu-id="eed0c-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="eed0c-127">Remarks</span></span>

<span data-ttu-id="eed0c-128">Os recursos de DVD do Windows Media Player não funcionarão em computadores que não têm um decodificador de DVD instalado.</span><span class="sxs-lookup"><span data-stu-id="eed0c-128">The DVD features of Windows Media Player will not work on computers that do not have a DVD decoder installed.</span></span> <span data-ttu-id="eed0c-129">Você pode determinar se um decodificador está disponível chamando a propriedade **IsAvailable** (o método **Get \_ IsAvailable** em C#) e passando o valor de **System. String** "dvdDecoder".</span><span class="sxs-lookup"><span data-stu-id="eed0c-129">You can determine whether a decoder is available by calling the **isAvailable** property (the **get\_isAvailable** method in C#) and passing in the **System.String** value "dvdDecoder".</span></span>

<span data-ttu-id="eed0c-130">Cada DVD é criado de maneira diferente.</span><span class="sxs-lookup"><span data-stu-id="eed0c-130">Every DVD is authored differently.</span></span> <span data-ttu-id="eed0c-131">Os métodos disponíveis durante a reprodução e navegação em DVD dependem de como o DVD é criado.</span><span class="sxs-lookup"><span data-stu-id="eed0c-131">The methods available during DVD playback and navigation depend on how the DVD is authored.</span></span>

## <a name="requirements"></a><span data-ttu-id="eed0c-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eed0c-132">Requirements</span></span>



| <span data-ttu-id="eed0c-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="eed0c-133">Requirement</span></span> | <span data-ttu-id="eed0c-134">Valor</span><span class="sxs-lookup"><span data-stu-id="eed0c-134">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eed0c-135">Versão</span><span class="sxs-lookup"><span data-stu-id="eed0c-135">Version</span></span><br/>   | <span data-ttu-id="eed0c-136">Windows Media Player 9 Series ou posterior</span><span class="sxs-lookup"><span data-stu-id="eed0c-136">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="eed0c-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="eed0c-137">Namespace</span></span><br/> | <span data-ttu-id="eed0c-138">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="eed0c-138">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="eed0c-139">Assembly</span><span class="sxs-lookup"><span data-stu-id="eed0c-139">Assembly</span></span><br/>  | <dl> <span data-ttu-id="eed0c-140"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="eed0c-140"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eed0c-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="eed0c-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eed0c-142">**Interface IWMPDVD (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="eed0c-142">**IWMPDVD Interface (VB and C#)**</span></span>](iwmpdvd--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="eed0c-143">**IWMPDVD. Back (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="eed0c-143">**IWMPDVD.back (VB and C#)**</span></span>](wmplibiwmpdvd-iwmpdvd-back--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="eed0c-144">**IWMPDVD. resume (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="eed0c-144">**IWMPDVD.resume (VB and C#)**</span></span>](wmplibiwmpdvd-iwmpdvd-resume--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="eed0c-145">**IWMPDVD. titleMenu (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="eed0c-145">**IWMPDVD.titleMenu (VB and C#)**</span></span>](wmplibiwmpdvd-iwmpdvd-titlemenu--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="eed0c-146">**IWMPDVD. topMenu (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="eed0c-146">**IWMPDVD.topMenu (VB and C#)**</span></span>](wmplibiwmpdvd-iwmpdvd-topmenu--vb-and-c.md)
</dt> </dl>

 

 





