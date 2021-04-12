---
description: Define padrões de bit que habilitam planos de recorte definidos pelo usuário. Essas macros são definidas como uma conveniência ao definir valores para o \_ estado de RENDERIZAÇÃO D3DRS CLIPPLANEENABLE.
ms.assetid: 5bca2401-a3fb-4b1c-bb59-621b15da10f1
title: Macro D3DCLIPPLANEn (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCLIPPLANEn
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 4508f1654a357eb80b3847b7562e230c6a9be4d0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104370934"
---
# <a name="d3dclipplanen-macro"></a><span data-ttu-id="c88c8-104">Macro D3DCLIPPLANEn</span><span class="sxs-lookup"><span data-stu-id="c88c8-104">D3DCLIPPLANEn macro</span></span>

<span data-ttu-id="c88c8-105">Define padrões de bit que habilitam planos de recorte definidos pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="c88c8-105">Defines bit patterns that enable user-defined clipping planes.</span></span> <span data-ttu-id="c88c8-106">Essas macros são definidas como uma conveniência ao definir valores para o \_ estado de RENDERIZAÇÃO D3DRS CLIPPLANEENABLE.</span><span class="sxs-lookup"><span data-stu-id="c88c8-106">These macros are defined as a convenience when setting values for the D3DRS\_CLIPPLANEENABLE render state.</span></span>

## <a name="syntax"></a><span data-ttu-id="c88c8-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c88c8-107">Syntax</span></span>


```C++
void D3DCLIPPLANEn(void);
```



## <a name="parameters"></a><span data-ttu-id="c88c8-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c88c8-108">Parameters</span></span>

<span data-ttu-id="c88c8-109">Esta macro não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="c88c8-109">This macro has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c88c8-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c88c8-110">Return value</span></span>

<span data-ttu-id="c88c8-111">Essa macro não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="c88c8-111">This macro does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c88c8-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="c88c8-112">Remarks</span></span>

<span data-ttu-id="c88c8-113">Os planos de recorte definidos pelo usuário são habilitados quando o valor definido no \_ estado de RENDERIZAÇÃO D3DRS CLIPPLANEENABLE contém um ou mais conjuntos de bits (ou seja, não é 0).</span><span class="sxs-lookup"><span data-stu-id="c88c8-113">User-defined clipping planes are enabled when the value set in the D3DRS\_CLIPPLANEENABLE render state contains one or more set bits (that is, is not 0).</span></span> <span data-ttu-id="c88c8-114">O valor do estado render não é importante; o sistema não interpreta o valor como um número.</span><span class="sxs-lookup"><span data-stu-id="c88c8-114">The value of the render-state is not important; the system does not interpret the value as a number.</span></span> <span data-ttu-id="c88c8-115">Em vez disso, o valor habilita o plano de recorte cujo bit correspondente está definido.</span><span class="sxs-lookup"><span data-stu-id="c88c8-115">Rather, the value enables the clipping plane whose corresponding bit is set.</span></span> <span data-ttu-id="c88c8-116">O bit 0 controla o estado do primeiro plano de recorte (no índice 0), bit 1 o segundo plano e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="c88c8-116">Bit 0 controls the state of the first clipping plane (at index 0), bit 1 the second plane, and so on.</span></span>

<span data-ttu-id="c88c8-117">Os padrões de bits criados por essas macros podem ser combinados usando uma operação OR lógica para habilitar simultaneamente vários planos de recorte.</span><span class="sxs-lookup"><span data-stu-id="c88c8-117">The bit patterns that these macros create can be combined by using a logical OR operation to simultaneously enable multiple clipping planes.</span></span> <span data-ttu-id="c88c8-118">Omitir uma dessas macros da combinação efetivamente desabilita o plano de recorte nesse índice.</span><span class="sxs-lookup"><span data-stu-id="c88c8-118">Omitting one of these macros from the combination effectively disables the clipping plane at that index.</span></span>

## <a name="requirements"></a><span data-ttu-id="c88c8-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c88c8-119">Requirements</span></span>



| <span data-ttu-id="c88c8-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="c88c8-120">Requirement</span></span> | <span data-ttu-id="c88c8-121">Valor</span><span class="sxs-lookup"><span data-stu-id="c88c8-121">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c88c8-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c88c8-122">Header</span></span><br/> | <dl> <span data-ttu-id="c88c8-123"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="c88c8-123"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c88c8-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="c88c8-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c88c8-125">Macros</span><span class="sxs-lookup"><span data-stu-id="c88c8-125">Macros</span></span>](dx9-graphics-reference-d3d-macros.md)
</dt> </dl>

 

 




