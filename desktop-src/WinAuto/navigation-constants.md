---
title: Constantes de navegação (OleAcc. h)
description: Este tópico descreve os valores constantes, definidos em OleAcc. h, que indicam a direção espacial (acima, abaixo, esquerda e direita) ou lógica (primeiro filho, última, próxima e anterior) observada quando os clientes usam o IAccessible accNavigate para navegar de um elemento de interface do usuário para outro dentro do mesmo contêiner.
ms.assetid: 5859a7a3-bcd3-443e-8ff0-4952f4639517
topic_type:
- apiref
api_name:
- NAVDIR_DOWN
- NAVDIR_FIRSTCHILD
- NAVDIR_LASTCHILD
- NAVDIR_LEFT
- NAVDIR_NEXT
- NAVDIR_PREVIOUS
- NAVDIR_RIGHT
- NAVDIR_UP
api_location:
- oleacc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8de5f4eaa3fc7fb24583e49bdd14acb9633b2bd4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750349"
---
# <a name="navigation-constants"></a><span data-ttu-id="382c6-103">Constantes de navegação</span><span class="sxs-lookup"><span data-stu-id="382c6-103">Navigation Constants</span></span>

<span data-ttu-id="382c6-104">Este tópico descreve os valores constantes, definidos em OleAcc. h, que indicam a direção *espacial* (acima, abaixo, esquerda e direita) ou *lógica* (primeiro filho, última, próxima e anterior) observada quando os clientes usam [**IAccessible:: accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) para navegar de um elemento de interface do usuário para outro dentro do mesmo contêiner.</span><span class="sxs-lookup"><span data-stu-id="382c6-104">This topic describes the constant values, defined in oleacc.h, that indicate the *spatial* (up, down, left, and right) or *logical* (first child, last, next, and previous) direction observed when clients use [**IAccessible::accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) to navigate from one user interface element to another within the same container.</span></span> <span data-ttu-id="382c6-105">Para obter mais informações, consulte [Propriedades e métodos de navegação de objetos](object-navigation-properties-and-methods.md).</span><span class="sxs-lookup"><span data-stu-id="382c6-105">For more information, see [Object Navigation Properties and Methods](object-navigation-properties-and-methods.md).</span></span>

<span data-ttu-id="382c6-106">As constantes de navegação da Microsoft Acessibilidade Ativa são as seguintes:</span><span class="sxs-lookup"><span data-stu-id="382c6-106">The Microsoft Active Accessibility navigation constants are as follows:</span></span>



| <span data-ttu-id="382c6-107">Constante</span><span class="sxs-lookup"><span data-stu-id="382c6-107">Constant</span></span>                                                                                                                                                                  | <span data-ttu-id="382c6-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="382c6-108">Description</span></span>                                                                                                                                           |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="NAVDIR_DOWN"></span><span id="navdir_down"></span><dl> <span data-ttu-id="382c6-109"><dt>**NAVDIR \_ para baixo**</dt></span><span class="sxs-lookup"><span data-stu-id="382c6-109"><dt>**NAVDIR\_DOWN**</dt></span></span> </dl>                   | <span data-ttu-id="382c6-110">Navegue até o objeto irmão que está localizado abaixo do objeto inicial.</span><span class="sxs-lookup"><span data-stu-id="382c6-110">Navigate to the sibling object that is located below the starting object.</span></span><br/>                                                                  |
| <span id="NAVDIR_FIRSTCHILD"></span><span id="navdir_firstchild"></span><dl> <span data-ttu-id="382c6-111"><dt>**NAVDIR \_ FIRSTCHILD**</dt></span><span class="sxs-lookup"><span data-stu-id="382c6-111"><dt>**NAVDIR\_FIRSTCHILD**</dt></span></span> </dl> | <span data-ttu-id="382c6-112">Navegue até o primeiro filho deste objeto.</span><span class="sxs-lookup"><span data-stu-id="382c6-112">Navigate to the first child of this object.</span></span> <span data-ttu-id="382c6-113">Quando esse sinalizador é usado, o membro **lVal** do parâmetro *VARSTART* deve ser filhaid por \_ conta própria.</span><span class="sxs-lookup"><span data-stu-id="382c6-113">When this flag is used, the **lVal** member of the *varStart* parameter must be CHILDID\_SELF.</span></span><br/> |
| <span id="NAVDIR_LASTCHILD"></span><span id="navdir_lastchild"></span><dl> <span data-ttu-id="382c6-114"><dt>**NAVDIR \_ LASTCHILD**</dt></span><span class="sxs-lookup"><span data-stu-id="382c6-114"><dt>**NAVDIR\_LASTCHILD**</dt></span></span> </dl>    | <span data-ttu-id="382c6-115">Navegue até o último filho deste objeto.</span><span class="sxs-lookup"><span data-stu-id="382c6-115">Navigate to the last child of this object.</span></span> <span data-ttu-id="382c6-116">Ao usar esse sinalizador, o membro **lVal** do parâmetro *VARSTART* deve ser filhaid por \_ conta própria.</span><span class="sxs-lookup"><span data-stu-id="382c6-116">When using this flag, the **lVal** member of the *varStart* parameter must be CHILDID\_SELF.</span></span><br/>    |
| <span id="NAVDIR_LEFT"></span><span id="navdir_left"></span><dl> <span data-ttu-id="382c6-117"><dt>**NAVDIR \_ à esquerda**</dt></span><span class="sxs-lookup"><span data-stu-id="382c6-117"><dt>**NAVDIR\_LEFT**</dt></span></span> </dl>                   | <span data-ttu-id="382c6-118">Navegue até o objeto irmão localizado à esquerda do objeto inicial.</span><span class="sxs-lookup"><span data-stu-id="382c6-118">Navigate to the sibling object located to the left of the starting object.</span></span><br/>                                                                 |
| <span id="NAVDIR_NEXT"></span><span id="navdir_next"></span><dl> <span data-ttu-id="382c6-119"><dt>**NAVDIR \_ próximo**</dt></span><span class="sxs-lookup"><span data-stu-id="382c6-119"><dt>**NAVDIR\_NEXT**</dt></span></span> </dl>                   | <span data-ttu-id="382c6-120">Navegar para o próximo objeto lógico; em geral, é um irmão do objeto inicial.</span><span class="sxs-lookup"><span data-stu-id="382c6-120">Navigate to the next logical object; generally, it is a sibling of the starting object.</span></span><br/>                                                    |
| <span id="NAVDIR_PREVIOUS"></span><span id="navdir_previous"></span><dl> <span data-ttu-id="382c6-121"><dt>**NAVDIR \_ anterior**</dt></span><span class="sxs-lookup"><span data-stu-id="382c6-121"><dt>**NAVDIR\_PREVIOUS**</dt></span></span> </dl>       | <span data-ttu-id="382c6-122">Navegar até o objeto lógico anterior; em geral, é um irmão do objeto inicial.</span><span class="sxs-lookup"><span data-stu-id="382c6-122">Navigate to the previous logical object; generally, it is a sibling of the starting object.</span></span><br/>                                                |
| <span id="NAVDIR_RIGHT"></span><span id="navdir_right"></span><dl> <span data-ttu-id="382c6-123"><dt>**NAVDIR \_ à direita**</dt></span><span class="sxs-lookup"><span data-stu-id="382c6-123"><dt>**NAVDIR\_RIGHT**</dt></span></span> </dl>                | <span data-ttu-id="382c6-124">Navegue até o objeto irmão que está localizado à direita do objeto inicial.</span><span class="sxs-lookup"><span data-stu-id="382c6-124">Navigate to the sibling object that is located to the right of the starting object.</span></span><br/>                                                        |
| <span id="NAVDIR_UP"></span><span id="navdir_up"></span><dl> <span data-ttu-id="382c6-125"><dt>**NAVDIR \_ up**</dt></span><span class="sxs-lookup"><span data-stu-id="382c6-125"><dt>**NAVDIR\_UP**</dt></span></span> </dl>                         | <span data-ttu-id="382c6-126">Navegue até o objeto irmão que está localizado acima do objeto inicial.</span><span class="sxs-lookup"><span data-stu-id="382c6-126">Navigate to the sibling object that is located above the starting object.</span></span><br/>                                                                  |



## <a name="requirements"></a><span data-ttu-id="382c6-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="382c6-127">Requirements</span></span>



| <span data-ttu-id="382c6-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="382c6-128">Requirement</span></span> | <span data-ttu-id="382c6-129">Valor</span><span class="sxs-lookup"><span data-stu-id="382c6-129">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="382c6-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="382c6-130">Header</span></span><br/> | <dl> <span data-ttu-id="382c6-131"><dt>OleAcc. h</dt></span><span class="sxs-lookup"><span data-stu-id="382c6-131"><dt>Oleacc.h</dt></span></span> </dl> |



 

 





