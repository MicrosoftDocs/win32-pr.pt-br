---
title: Método IGatherNotify OnDataChange (preterido)
description: Este tópico da interface do Windows Desktop Search foi preterido e é substituído pela API ISearchPersistentItemsChangedSink do Windows Search no SDK do Windows. | Método IGatherNotify OnDataChange (preterido)
ms.assetid: 0cbfa6b7-44f0-41f0-93a3-d5941b5822de
keywords:
- Método OnDataChange (preterido) recursos de ambiente herdado do Windows
- Método OnDataChange (preterido) recursos de ambiente herdado do Windows, interface IGatherNotify
- Recursos do ambiente Windows herdado da interface IGatherNotify, método OnDataChange (preterido)
topic_type:
- apiref
api_name:
- IGatherNotify.OnDataChange (Deprecated)
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d41edeaa591a7f3cbc9494064906af1815597737
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105788969"
---
# <a name="igathernotifyondatachange-deprecated-method"></a><span data-ttu-id="ca486-107">Método IGatherNotify:: OnDataChange (preterido)</span><span class="sxs-lookup"><span data-stu-id="ca486-107">IGatherNotify::OnDataChange (Deprecated) method</span></span>

<span data-ttu-id="ca486-108">\[**OnDataChange** pode ser alterado ou não estar disponível nas versões subsequentes do sistema operacional ou produto.\]</span><span class="sxs-lookup"><span data-stu-id="ca486-108">\[**OnDataChange** may be altered or unavailable in subsequent versions of the operating system or product.\]</span></span>

<span data-ttu-id="ca486-109">Este tópico da interface do Windows Desktop Search foi preterido e é substituído pela API [**ISearchPersistentItemsChangedSink**](/windows/desktop/api/searchapi/nn-searchapi-isearchpersistentitemschangedsink) do Windows Search no SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="ca486-109">This Windows Desktop Search interface topic is deprecated and is superseded by the Windows Search [**ISearchPersistentItemsChangedSink**](/windows/desktop/api/searchapi/nn-searchapi-isearchpersistentitemschangedsink) API in the Windows SDK.</span></span>

<span data-ttu-id="ca486-110">Esse método notifica o indexador de dados que foram alterados.</span><span class="sxs-lookup"><span data-stu-id="ca486-110">This method notifies the indexer of data that has changed.</span></span> <span data-ttu-id="ca486-111">Quando ele envia a notificação para o indexador, ele inclui o tipo de alteração, endereço físico e endereço lógico.</span><span class="sxs-lookup"><span data-stu-id="ca486-111">When it sends the notification to the indexer, it includes the type of change, physical address, and logical address.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca486-112">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ca486-112">Syntax</span></span>


```C++
void OnDataChange (Deprecated)(
  [in] long eChangeAdvise,
  [in] BSTR bstrPhysicalAddress,
  [in] BSTR bstrLogicalAddress
);
```



## <a name="parameters"></a><span data-ttu-id="ca486-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ca486-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca486-114">*eChangeAdvise* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ca486-114">*eChangeAdvise* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca486-115">Tipo: **longo**</span><span class="sxs-lookup"><span data-stu-id="ca486-115">Type: **long**</span></span>

<span data-ttu-id="ca486-116">Um valor enumerado que especifica o tipo de alteração.</span><span class="sxs-lookup"><span data-stu-id="ca486-116">An enumerated value that specifies the type of change.</span></span>

</dd> <dt>

<span data-ttu-id="ca486-117">*bstrPhysicalAddress* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ca486-117">*bstrPhysicalAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca486-118">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="ca486-118">Type: **BSTR**</span></span>

<span data-ttu-id="ca486-119">O endereço físico do item que foi alterado.</span><span class="sxs-lookup"><span data-stu-id="ca486-119">The physical address of the item that changed.</span></span>

</dd> <dt>

<span data-ttu-id="ca486-120">*bstrLogicalAddress* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ca486-120">*bstrLogicalAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca486-121">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="ca486-121">Type: **BSTR**</span></span>

<span data-ttu-id="ca486-122">O endereço lógico do item que foi alterado.</span><span class="sxs-lookup"><span data-stu-id="ca486-122">The logical address of the item that changed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ca486-123">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ca486-123">Return value</span></span>

<span data-ttu-id="ca486-124">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="ca486-124">This method does not return a value.</span></span>

 

 
