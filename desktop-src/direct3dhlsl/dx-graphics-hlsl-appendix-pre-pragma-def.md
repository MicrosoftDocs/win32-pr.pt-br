---
title: Diretiva pragma def
description: Diretiva pragma que aloca manualmente um registro de sombreador de ponto flutuante.
ms.assetid: 45db94c4-f6f6-4c88-9bf2-4eaa9abf7844
keywords:
- Diretiva pragma def HLSL
topic_type:
- apiref
api_name:
- def pragma Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2a921e17f8ddee4aaabfe50e75f42ce44812863d
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104988541"
---
# <a name="def-pragma-directive"></a><span data-ttu-id="8ad6d-104">Diretiva pragma def</span><span class="sxs-lookup"><span data-stu-id="8ad6d-104">def pragma Directive</span></span>

<span data-ttu-id="8ad6d-105">Diretiva pragma que aloca manualmente um registro de sombreador de ponto flutuante.</span><span class="sxs-lookup"><span data-stu-id="8ad6d-105">Pragma directive that manually allocates a floating-point shader register.</span></span>



| <span data-ttu-id="8ad6d-106">\#pragma def ( *destino*, *registro*, *val1*, *val2*,*Val3*, *val4* )</span><span class="sxs-lookup"><span data-stu-id="8ad6d-106">\#pragma def( *target*, *register*, *val1*, *val2*,*val3*, *val4* )</span></span> |
|---------------------------------------------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="8ad6d-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8ad6d-107">Parameters</span></span>



| <span data-ttu-id="8ad6d-108">Item</span><span class="sxs-lookup"><span data-stu-id="8ad6d-108">Item</span></span>                                                                        | <span data-ttu-id="8ad6d-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="8ad6d-109">Description</span></span>                                                                 |
|-----------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="8ad6d-110"><span id="target"></span><span id="TARGET"></span>*alvo*</span><span class="sxs-lookup"><span data-stu-id="8ad6d-110"><span id="target"></span><span id="TARGET"></span>*target*</span></span><br/>       | <span data-ttu-id="8ad6d-111">Destino que contém o registro a ser alocado.</span><span class="sxs-lookup"><span data-stu-id="8ad6d-111">Target that contains the register to allocate.</span></span> <br/>                  |
| <span data-ttu-id="8ad6d-112"><span id="register"></span><span id="REGISTER"></span>*Registr*</span><span class="sxs-lookup"><span data-stu-id="8ad6d-112"><span id="register"></span><span id="REGISTER"></span>*register*</span></span><br/> | <span data-ttu-id="8ad6d-113">Registro de sombreador de ponto flutuante para alocar.</span><span class="sxs-lookup"><span data-stu-id="8ad6d-113">Floating-point shader register to allocate.</span></span> <br/>                     |
| <span data-ttu-id="8ad6d-114"><span id="val0"></span><span id="VAL0"></span>*val0*</span><span class="sxs-lookup"><span data-stu-id="8ad6d-114"><span id="val0"></span><span id="VAL0"></span>*val0*</span></span><br/>             | <span data-ttu-id="8ad6d-115">Primeiro byte do valor a ser alocado para o registro especificado.</span><span class="sxs-lookup"><span data-stu-id="8ad6d-115">First byte of the value to allocate to the specified register.</span></span> <br/>  |
| <span data-ttu-id="8ad6d-116"><span id="val1"></span><span id="VAL1"></span>*val1*</span><span class="sxs-lookup"><span data-stu-id="8ad6d-116"><span id="val1"></span><span id="VAL1"></span>*val1*</span></span><br/>             | <span data-ttu-id="8ad6d-117">Segundo byte do valor a ser alocado para o registro especificado.</span><span class="sxs-lookup"><span data-stu-id="8ad6d-117">Second byte of the value to allocate to the specified register.</span></span> <br/> |
| <span data-ttu-id="8ad6d-118"><span id="val2"></span><span id="VAL2"></span>*val2*</span><span class="sxs-lookup"><span data-stu-id="8ad6d-118"><span id="val2"></span><span id="VAL2"></span>*val2*</span></span><br/>             | <span data-ttu-id="8ad6d-119">Terceiro byte do valor a ser alocado para o registro especificado.</span><span class="sxs-lookup"><span data-stu-id="8ad6d-119">Third byte of the value to allocate to the specified register.</span></span> <br/>  |
| <span data-ttu-id="8ad6d-120"><span id="val3"></span><span id="VAL3"></span>*val3*</span><span class="sxs-lookup"><span data-stu-id="8ad6d-120"><span id="val3"></span><span id="VAL3"></span>*val3*</span></span><br/>             | <span data-ttu-id="8ad6d-121">Quarto byte do valor a ser alocado para o registro especificado.</span><span class="sxs-lookup"><span data-stu-id="8ad6d-121">Fourth byte of the value to allocate to the specified register.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="8ad6d-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="8ad6d-122">Remarks</span></span>

<span data-ttu-id="8ad6d-123">O pragma def permite que um desenvolvedor preencha um registro de sombreador de ponto flutuante com o valor especificado.</span><span class="sxs-lookup"><span data-stu-id="8ad6d-123">The def pragma allows a developer to prefill a floating-point shader register with the specified value.</span></span> <span data-ttu-id="8ad6d-124">Esse pragma é usado raramente.</span><span class="sxs-lookup"><span data-stu-id="8ad6d-124">This pragma is infrequently used.</span></span>

## <a name="see-also"></a><span data-ttu-id="8ad6d-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="8ad6d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ad6d-126">Diretivas de pré-processador (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8ad6d-126">Preprocessor Directives (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[<span data-ttu-id="8ad6d-127">\#Diretiva pragma (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8ad6d-127">\#pragma Directive (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-pre-pragma.md)
</dt> </dl>

 

 





