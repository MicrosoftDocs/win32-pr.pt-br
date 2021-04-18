---
title: ErrorItem. Condition
description: A Propriedade Condition recupera um valor que indica a condição do erro.
ms.assetid: efb54b48-cfaa-479f-9ee6-ce6724dca24c
keywords:
- ErrorItem. Condition Windows Media Player
topic_type:
- apiref
api_name:
- ErrorItem.condition
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c498e7479a7a3e067dea2d8a562800351effd672
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759715"
---
# <a name="erroritemcondition"></a><span data-ttu-id="55366-104">ErrorItem. Condition</span><span class="sxs-lookup"><span data-stu-id="55366-104">ErrorItem.condition</span></span>

<span data-ttu-id="55366-105">A propriedade **Condition** recupera um valor que indica a condição do erro.</span><span class="sxs-lookup"><span data-stu-id="55366-105">The **condition** property retrieves a value indicating the condition for the error.</span></span>

``` syntax
player.error.item(
        index
        ).condition
      
```

## <a name="possible-values"></a><span data-ttu-id="55366-106">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="55366-106">Possible Values</span></span>

<span data-ttu-id="55366-107">Essa propriedade é um **número** somente leitura (**Long**) que representa o código de condição.</span><span class="sxs-lookup"><span data-stu-id="55366-107">This property is a read-only **Number** (**long**) that represents the condition code.</span></span>

## <a name="remarks"></a><span data-ttu-id="55366-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="55366-108">Remarks</span></span>

<span data-ttu-id="55366-109">O código de condição é um valor que é usado pela Microsoft para fornecer informações adicionais para a equipe de suporte técnico.</span><span class="sxs-lookup"><span data-stu-id="55366-109">The condition code is a value that is used by Microsoft to provide additional information for technical support personnel.</span></span>

<span data-ttu-id="55366-110">**Windows Media Player 10 Mobile:** Essa propriedade sempre retorna 0.</span><span class="sxs-lookup"><span data-stu-id="55366-110">**Windows Media Player 10 Mobile:** This property always returns 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="55366-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="55366-111">Requirements</span></span>



| <span data-ttu-id="55366-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="55366-112">Requirement</span></span> | <span data-ttu-id="55366-113">Valor</span><span class="sxs-lookup"><span data-stu-id="55366-113">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="55366-114">Versão</span><span class="sxs-lookup"><span data-stu-id="55366-114">Version</span></span><br/> | <span data-ttu-id="55366-115">Windows Media Player 9 Series ou posterior.</span><span class="sxs-lookup"><span data-stu-id="55366-115">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="55366-116">DLL</span><span class="sxs-lookup"><span data-stu-id="55366-116">DLL</span></span><br/>     | <dl> <span data-ttu-id="55366-117"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="55366-117"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="55366-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="55366-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55366-119">**Objeto ErrorItem**</span><span class="sxs-lookup"><span data-stu-id="55366-119">**ErrorItem Object**</span></span>](erroritem-object.md)
</dt> </dl>

 

 





