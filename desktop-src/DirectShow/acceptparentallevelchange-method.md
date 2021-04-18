---
description: O método AcceptParentalLevelChange aceita ou rejeita o novo nível temporário de gerenciamento de pais.
ms.assetid: b3d58069-16dc-4598-90ea-6136c2f62ac7
title: Método AcceptParentalLevelChange
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8b2e81d1d82c4ede14580ed65d88566738dac1b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105792571"
---
# <a name="acceptparentallevelchange-method"></a><span data-ttu-id="53270-103">Método AcceptParentalLevelChange</span><span class="sxs-lookup"><span data-stu-id="53270-103">AcceptParentalLevelChange Method</span></span>

> [!Note]  
> <span data-ttu-id="53270-104">Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="53270-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="53270-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="53270-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="53270-106">O método AcceptParentalLevelChange aceita ou rejeita o novo nível temporário de gerenciamento de pais.</span><span class="sxs-lookup"><span data-stu-id="53270-106">The AcceptParentalLevelChange method accepts or rejects the new temporary parental management level.</span></span>

``` syntax
        MSWebDVD.AcceptParentalLevelChange(bAccept)
```

## <a name="parameters"></a><span data-ttu-id="53270-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="53270-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53270-108"><span id="bAccept"></span><span id="baccept"></span><span id="BACCEPT"></span>*bAccept*</span><span class="sxs-lookup"><span data-stu-id="53270-108"><span id="bAccept"></span><span id="baccept"></span><span id="BACCEPT"></span>*bAccept*</span></span>
</dt> <dd>

<span data-ttu-id="53270-109">Especifica o novo nível de pai como um valor booliano.</span><span class="sxs-lookup"><span data-stu-id="53270-109">Specifies the new parental level as a Boolean value.</span></span>



| <span data-ttu-id="53270-110">Valor</span><span class="sxs-lookup"><span data-stu-id="53270-110">Value</span></span> | <span data-ttu-id="53270-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="53270-111">Description</span></span>                               |
|-------|-------------------------------------------|
| <span data-ttu-id="53270-112">true</span><span class="sxs-lookup"><span data-stu-id="53270-112">true</span></span>  | <span data-ttu-id="53270-113">Aceite o novo nível de gerenciamento de pais.</span><span class="sxs-lookup"><span data-stu-id="53270-113">Accept the new parental management level.</span></span> |
| <span data-ttu-id="53270-114">false</span><span class="sxs-lookup"><span data-stu-id="53270-114">false</span></span> | <span data-ttu-id="53270-115">Rejeite o novo nível de gerenciamento de pais.</span><span class="sxs-lookup"><span data-stu-id="53270-115">Reject the new parental management level.</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53270-116">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="53270-116">Return Value</span></span>

<span data-ttu-id="53270-117">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="53270-117">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="53270-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="53270-118">Remarks</span></span>

<span data-ttu-id="53270-119">Chame esse método em resposta a uma \_ notificação de evento de alteração de nível pai de DVD do EC \_ \_ \_ para especificar se o navegador de DVD deve reproduzir o conteúdo com o novo nível de pai ou Branch para onde o disco especifica se o novo nível é rejeitado.</span><span class="sxs-lookup"><span data-stu-id="53270-119">Call this method in response to an EC\_DVD\_PARENTAL\_LEVEL\_CHANGE event notification to specify whether the DVD Navigator should play the content with the new parental level, or branch to where the disc specifies if the new level is rejected.</span></span>

## <a name="see-also"></a><span data-ttu-id="53270-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="53270-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53270-121">Impondo níveis de gerenciamento de pais</span><span class="sxs-lookup"><span data-stu-id="53270-121">Enforcing Parental Management Levels</span></span>](enforcing-parental-management-levels.md)
</dt> <dt>

[<span data-ttu-id="53270-122">**GetPlayerParentalCountry**</span><span class="sxs-lookup"><span data-stu-id="53270-122">**GetPlayerParentalCountry**</span></span>](getplayerparentalcountry-method.md)
</dt> <dt>

[<span data-ttu-id="53270-123">**GetPlayerParentalLevel**</span><span class="sxs-lookup"><span data-stu-id="53270-123">**GetPlayerParentalLevel**</span></span>](getplayerparentallevel-method.md)
</dt> <dt>

[<span data-ttu-id="53270-124">**GetTitleParentalLevels**</span><span class="sxs-lookup"><span data-stu-id="53270-124">**GetTitleParentalLevels**</span></span>](gettitleparentallevels-method.md)
</dt> <dt>

[<span data-ttu-id="53270-125">**NotifyParentalLevelChange**</span><span class="sxs-lookup"><span data-stu-id="53270-125">**NotifyParentalLevelChange**</span></span>](notifyparentallevelchange-method.md)
</dt> <dt>

[<span data-ttu-id="53270-126">**SelectParentalCountry**</span><span class="sxs-lookup"><span data-stu-id="53270-126">**SelectParentalCountry**</span></span>](selectparentalcountry-method.md)
</dt> <dt>

[<span data-ttu-id="53270-127">**SelectParentalLevel**</span><span class="sxs-lookup"><span data-stu-id="53270-127">**SelectParentalLevel**</span></span>](selectparentallevel-method.md)
</dt> </dl>

 

 



