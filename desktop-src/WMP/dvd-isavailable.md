---
title: DVD. IsAvailable
description: A propriedade IsAvailable indica se um tipo especificado de informação está disponível ou se uma ação especificada pode ser executada. | DVD. IsAvailable
ms.assetid: ed34a943-b9c3-40a8-8845-b83f16951a3e
keywords:
- DVD. isdisponível Windows Media Player
topic_type:
- apiref
api_name:
- DVD.isAvailable
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5088b4b6365dd60d859fda8ec563cc9c8ff8a4c8
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105796432"
---
# <a name="dvdisavailable"></a><span data-ttu-id="ec8f5-105">DVD. IsAvailable</span><span class="sxs-lookup"><span data-stu-id="ec8f5-105">DVD.isAvailable</span></span>

<span data-ttu-id="ec8f5-106">A propriedade **IsAvailable** indica se um tipo especificado de informação está disponível ou se uma ação especificada pode ser executada.</span><span class="sxs-lookup"><span data-stu-id="ec8f5-106">The **isAvailable** property indicates whether a specified type of information is available or a specified action can be performed.</span></span>

``` syntax
player.dvd.isAvailable(
        name
        )
```

## <a name="parameters"></a><span data-ttu-id="ec8f5-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ec8f5-107">Parameters</span></span>

<span data-ttu-id="ec8f5-108">*name*</span><span class="sxs-lookup"><span data-stu-id="ec8f5-108">*name*</span></span>

<span data-ttu-id="ec8f5-109">**Cadeia de caracteres** que contém um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="ec8f5-109">**String** containing one of the following values.</span></span>



| <span data-ttu-id="ec8f5-110">String</span><span class="sxs-lookup"><span data-stu-id="ec8f5-110">String</span></span>     | <span data-ttu-id="ec8f5-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="ec8f5-111">Description</span></span>                                                                            |
|------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ec8f5-112">voltar</span><span class="sxs-lookup"><span data-stu-id="ec8f5-112">back</span></span>       | <span data-ttu-id="ec8f5-113">Determina se o método **back** está disponível.</span><span class="sxs-lookup"><span data-stu-id="ec8f5-113">Determines whether the **back** method is available.</span></span>                                   |
| <span data-ttu-id="ec8f5-114">DVD</span><span class="sxs-lookup"><span data-stu-id="ec8f5-114">dvd</span></span>        | <span data-ttu-id="ec8f5-115">Determina se o DVD está carregado.</span><span class="sxs-lookup"><span data-stu-id="ec8f5-115">Determines whether the DVD is loaded.</span></span>                                                  |
| <span data-ttu-id="ec8f5-116">dvdDecoder</span><span class="sxs-lookup"><span data-stu-id="ec8f5-116">dvdDecoder</span></span> | <span data-ttu-id="ec8f5-117">Determina se o decodificador de DVD está instalado no sistema.</span><span class="sxs-lookup"><span data-stu-id="ec8f5-117">Determines whether the DVD decoder is installed on system.</span></span>                             |
| <span data-ttu-id="ec8f5-118">resume</span><span class="sxs-lookup"><span data-stu-id="ec8f5-118">resume</span></span>     | <span data-ttu-id="ec8f5-119">Determina se o método **resume** está disponível.</span><span class="sxs-lookup"><span data-stu-id="ec8f5-119">Determines whether the **resume** method is available.</span></span>                                 |
| <span data-ttu-id="ec8f5-120">titleMenu</span><span class="sxs-lookup"><span data-stu-id="ec8f5-120">titleMenu</span></span>  | <span data-ttu-id="ec8f5-121">Determina se o método **titleMenu** está disponível.</span><span class="sxs-lookup"><span data-stu-id="ec8f5-121">Determines whether the **titleMenu** method is available.</span></span>                              |
| <span data-ttu-id="ec8f5-122">topMenu</span><span class="sxs-lookup"><span data-stu-id="ec8f5-122">topMenu</span></span>    | <span data-ttu-id="ec8f5-123">Determina se o método **topMenu** está disponível.</span><span class="sxs-lookup"><span data-stu-id="ec8f5-123">Determines whether the **topMenu** method is available.</span></span> <span data-ttu-id="ec8f5-124">Normalmente chamado de menu raiz.</span><span class="sxs-lookup"><span data-stu-id="ec8f5-124">Commonly called the root menu.</span></span> |



 

## <a name="return-values"></a><span data-ttu-id="ec8f5-125">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="ec8f5-125">Return Values</span></span>

<span data-ttu-id="ec8f5-126">Esse método retorna um **valor booleano** somente leitura que indica se o parâmetro especificado está disponível.</span><span class="sxs-lookup"><span data-stu-id="ec8f5-126">This method returns a read-only **Boolean** indicating whether the specified parameter is available.</span></span>

## <a name="remarks"></a><span data-ttu-id="ec8f5-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="ec8f5-127">Remarks</span></span>

<span data-ttu-id="ec8f5-128">Os recursos de DVD do Windows Media Player não funcionarão em computadores que não têm decodificadores de DVD de terceiros instalados.</span><span class="sxs-lookup"><span data-stu-id="ec8f5-128">The DVD features of Windows Media Player will not work on computers that do not have third-party DVD decoders installed.</span></span> <span data-ttu-id="ec8f5-129">Você pode determinar se um decodificador está disponível chamando **IsAvailable**("dvdDecoder").</span><span class="sxs-lookup"><span data-stu-id="ec8f5-129">You can determine whether a decoder is available by calling **isAvailable**("dvdDecoder").</span></span>

<span data-ttu-id="ec8f5-130">Cada DVD é criado de maneira diferente.</span><span class="sxs-lookup"><span data-stu-id="ec8f5-130">Every DVD is authored differently.</span></span> <span data-ttu-id="ec8f5-131">Os métodos disponíveis durante a reprodução e navegação em DVD dependem de como o DVD é criado.</span><span class="sxs-lookup"><span data-stu-id="ec8f5-131">The methods available during DVD playback and navigation depend on how the DVD is authored.</span></span>

<span data-ttu-id="ec8f5-132">**Windows Media Player 10 Mobile:** Essa propriedade sempre retorna **false**.</span><span class="sxs-lookup"><span data-stu-id="ec8f5-132">**Windows Media Player 10 Mobile:** This property always returns **false**.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec8f5-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ec8f5-133">Requirements</span></span>



| <span data-ttu-id="ec8f5-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="ec8f5-134">Requirement</span></span> | <span data-ttu-id="ec8f5-135">Valor</span><span class="sxs-lookup"><span data-stu-id="ec8f5-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ec8f5-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ec8f5-136">Minimum supported client</span></span><br/> | <span data-ttu-id="ec8f5-137">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="ec8f5-137">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ec8f5-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ec8f5-138">Minimum supported server</span></span><br/> | <span data-ttu-id="ec8f5-139">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ec8f5-139">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="ec8f5-140">Versão</span><span class="sxs-lookup"><span data-stu-id="ec8f5-140">Version</span></span><br/>                  | <span data-ttu-id="ec8f5-141">Windows Media Player para Windows XP ou posterior</span><span class="sxs-lookup"><span data-stu-id="ec8f5-141">Windows Media Player for Windows XP or later</span></span><br/>                            |
| <span data-ttu-id="ec8f5-142">DLL</span><span class="sxs-lookup"><span data-stu-id="ec8f5-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ec8f5-143"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ec8f5-143"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ec8f5-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="ec8f5-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec8f5-145">**Objeto de DVD**</span><span class="sxs-lookup"><span data-stu-id="ec8f5-145">**DVD Object**</span></span>](dvd-object.md)
</dt> </dl>

 

 





