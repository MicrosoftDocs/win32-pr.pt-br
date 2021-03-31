---
description: Serve como uma classe pai para classes que controlam a geração de eventos, como eventos de temporizador.
ms.assetid: 381b06e7-2857-4932-9f52-f1d62efa8b79
ms.tgt_platform: multiple
title: Classe __EventGenerator
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventGenerator
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: b40524405c3b284e7ec61414e36448cb37afeab8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104172145"
---
# <a name="__eventgenerator-class"></a><span data-ttu-id="75669-103">\_\_Classe EventGenerator</span><span class="sxs-lookup"><span data-stu-id="75669-103">\_\_EventGenerator class</span></span>

<span data-ttu-id="75669-104">A classe de sistema **\_ \_ EventGenerator** é uma classe base abstrata que serve como uma classe pai para classes que controlam a geração de eventos, como [eventos de temporizador](receiving-a-timed-or-repeating-event.md).</span><span class="sxs-lookup"><span data-stu-id="75669-104">The **\_\_EventGenerator** system class is an abstract base class that serves as a parent class for classes that control the generation of events, such as [timer events](receiving-a-timed-or-repeating-event.md).</span></span>

<span data-ttu-id="75669-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="75669-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="75669-106">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="75669-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="75669-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="75669-107">Syntax</span></span>

``` syntax
[abstract]
class __EventGenerator : __IndicationRelated
{
};
```

## <a name="members"></a><span data-ttu-id="75669-108">Membros</span><span class="sxs-lookup"><span data-stu-id="75669-108">Members</span></span>

<span data-ttu-id="75669-109">A classe **\_ \_ EventGenerator** não define nenhum membro.</span><span class="sxs-lookup"><span data-stu-id="75669-109">The **\_\_EventGenerator** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="75669-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="75669-110">Remarks</span></span>

<span data-ttu-id="75669-111">A classe **\_ \_ EventGenerator** é derivada de [**\_ \_ IndicationRelated**](--indicationrelated.md), que não tem propriedades.</span><span class="sxs-lookup"><span data-stu-id="75669-111">The **\_\_EventGenerator** class is derived from [**\_\_IndicationRelated**](--indicationrelated.md), which has no properties.</span></span>

## <a name="requirements"></a><span data-ttu-id="75669-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="75669-112">Requirements</span></span>



| <span data-ttu-id="75669-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="75669-113">Requirement</span></span> | <span data-ttu-id="75669-114">Valor</span><span class="sxs-lookup"><span data-stu-id="75669-114">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="75669-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="75669-115">Minimum supported client</span></span><br/> | <span data-ttu-id="75669-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="75669-116">Windows Vista</span></span><br/>       |
| <span data-ttu-id="75669-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="75669-117">Minimum supported server</span></span><br/> | <span data-ttu-id="75669-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="75669-118">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="75669-119">Namespace</span><span class="sxs-lookup"><span data-stu-id="75669-119">Namespace</span></span><br/>                | <span data-ttu-id="75669-120">Todos os namespaces do WMI</span><span class="sxs-lookup"><span data-stu-id="75669-120">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="75669-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="75669-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75669-122">**\_\_IndicationRelated**</span><span class="sxs-lookup"><span data-stu-id="75669-122">**\_\_IndicationRelated**</span></span>](/windows/desktop/WmiSdk/--indicationrelated)
</dt> <dt>

[<span data-ttu-id="75669-123">Classes do sistema WMI</span><span class="sxs-lookup"><span data-stu-id="75669-123">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

