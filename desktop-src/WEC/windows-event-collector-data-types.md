---
title: Tipos de dados do coletor de eventos do Windows (Evcoll. h)
description: Os tipos de dados do coletor de eventos do Windows são usados como tipos de variável de objeto de assinatura de evento, tipos de parâmetro de função e tipos de retorno de função.
ms.assetid: b78bdaf8-e034-40fe-acf8-632313e4fd94
ms.tgt_platform: multiple
keywords:
- EC_HANDLE
- EC_OBJECT_ARRAY_PROPERTY_HANDLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ccec141317644aa091eac44033b87b9e4495ddc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105796463"
---
# <a name="windows-event-collector-data-types"></a><span data-ttu-id="92507-105">Tipos de dados do coletor de eventos do Windows</span><span class="sxs-lookup"><span data-stu-id="92507-105">Windows Event Collector Data Types</span></span>

<span data-ttu-id="92507-106">Os tipos de dados do coletor de eventos do Windows são usados como tipos de variável de objeto de assinatura de evento, tipos de parâmetro de função e tipos de retorno de função.</span><span class="sxs-lookup"><span data-stu-id="92507-106">The data types for the Windows Event Collector are used as event subscription object variable types, function parameter types, and function return types.</span></span>


```C++
typedef HANDLE EC_HANDLE;
typedef HANDLE EC_OBJECT_ARRAY_PROPERTY_HANDLE;
```



<dl> <dt>

<span data-ttu-id="92507-107">**identificador do EC \_**</span><span class="sxs-lookup"><span data-stu-id="92507-107">**EC\_HANDLE**</span></span>
</dt> <dd>

<span data-ttu-id="92507-108">Identificador para um objeto de assinatura.</span><span class="sxs-lookup"><span data-stu-id="92507-108">Handle to a subscription object.</span></span> <span data-ttu-id="92507-109">Usado para representar uma assinatura do coletor de eventos.</span><span class="sxs-lookup"><span data-stu-id="92507-109">Used to represent an event collector subscription.</span></span>

</dd> <dt>

<span data-ttu-id="92507-110">**\_identificador de \_ propriedade da matriz de objetos do EC \_ \_**</span><span class="sxs-lookup"><span data-stu-id="92507-110">**EC\_OBJECT\_ARRAY\_PROPERTY\_HANDLE**</span></span>
</dt> <dd>

<span data-ttu-id="92507-111">Identificador para uma matriz de valores de propriedade para as origens de evento de uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="92507-111">Handle to an array of property values for the event sources of a subscription.</span></span> <span data-ttu-id="92507-112">O identificador de matriz é retornado pelo método [**EcGetSubscriptionProperty**](/windows/desktop/api/Evcoll/nf-evcoll-ecgetsubscriptionproperty) quando o valor de **EcSubscriptionEventSources** é passado para o parâmetro *PropertyId* .</span><span class="sxs-lookup"><span data-stu-id="92507-112">The array handle is returned by the [**EcGetSubscriptionProperty**](/windows/desktop/api/Evcoll/nf-evcoll-ecgetsubscriptionproperty) method when the **EcSubscriptionEventSources** value is passed into the *PropertyId* parameter.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="92507-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="92507-113">Requirements</span></span>



| <span data-ttu-id="92507-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="92507-114">Requirement</span></span> | <span data-ttu-id="92507-115">Valor</span><span class="sxs-lookup"><span data-stu-id="92507-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="92507-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="92507-116">Minimum supported client</span></span><br/> | <span data-ttu-id="92507-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="92507-117">Windows Vista</span></span><br/>                                                            |
| <span data-ttu-id="92507-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="92507-118">Minimum supported server</span></span><br/> | <span data-ttu-id="92507-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="92507-119">Windows Server 2008</span></span><br/>                                                      |
| <span data-ttu-id="92507-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="92507-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="92507-121"><dt>Evcoll. h</dt></span><span class="sxs-lookup"><span data-stu-id="92507-121"><dt>Evcoll.h</dt></span></span> </dl> |



 

 





