---
title: Método IGatherNotify OnDataMove (preterido)
description: Este tópico da interface do Windows Desktop Search foi preterido e é substituído pela API ISearchPersistentItemsChangedSink do Windows Search no SDK do Windows. | Método IGatherNotify OnDataMove (preterido)
ms.assetid: cc223d0f-6508-4e38-b365-c60660db5324
keywords:
- Método OnDataMove (preterido) recursos de ambiente herdado do Windows
- Método OnDataMove (preterido) recursos de ambiente herdado do Windows, interface IGatherNotify
- Recursos do ambiente Windows herdado da interface IGatherNotify, método OnDataMove (preterido)
topic_type:
- apiref
api_name:
- IGatherNotify.OnDataMove (Deprecated)
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9fe38cd11e9072981334e5b724445ea3393d4361
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104298250"
---
# <a name="igathernotifyondatamove-deprecated-method"></a><span data-ttu-id="f028c-107">Método IGatherNotify:: OnDataMove (preterido)</span><span class="sxs-lookup"><span data-stu-id="f028c-107">IGatherNotify::OnDataMove (Deprecated) method</span></span>

<span data-ttu-id="f028c-108">\[**OnDataMove** pode ser alterado ou não estar disponível nas versões subsequentes do sistema operacional ou produto.\]</span><span class="sxs-lookup"><span data-stu-id="f028c-108">\[**OnDataMove** may be altered or unavailable in subsequent versions of the operating system or product.\]</span></span>

<span data-ttu-id="f028c-109">Este tópico da interface do Windows Desktop Search foi preterido e é substituído pela API [**ISearchPersistentItemsChangedSink**](/windows/desktop/api/searchapi/nn-searchapi-isearchpersistentitemschangedsink) do Windows Search no SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="f028c-109">This Windows Desktop Search interface topic is deprecated and is superseded by the Windows Search [**ISearchPersistentItemsChangedSink**](/windows/desktop/api/searchapi/nn-searchapi-isearchpersistentitemschangedsink) API in the Windows SDK.</span></span>

<span data-ttu-id="f028c-110">Esse método notifica o indexador de dados que foram movidos.</span><span class="sxs-lookup"><span data-stu-id="f028c-110">This method notifies the indexer of data that has been moved.</span></span> <span data-ttu-id="f028c-111">Quando ele envia a notificação para o indexador, ele inclui o endereço antigo, o novo endereço e o endereço lógico.</span><span class="sxs-lookup"><span data-stu-id="f028c-111">When it sends the notification to the indexer, it includes the old address, new address, and logical address.</span></span>

## <a name="syntax"></a><span data-ttu-id="f028c-112">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f028c-112">Syntax</span></span>


```C++
void OnDataMove (Deprecated)(
  [in] long eChangeAdviseSemantics,
  [in] BSTR bstrOldAddress,
  [in] BSTR bstrNewAddress,
  [in] BSTR bstrLogicalAddress
);
```



## <a name="parameters"></a><span data-ttu-id="f028c-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f028c-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f028c-114">*eChangeAdviseSemantics* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f028c-114">*eChangeAdviseSemantics* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f028c-115">Tipo: **longo**</span><span class="sxs-lookup"><span data-stu-id="f028c-115">Type: **long**</span></span>

<span data-ttu-id="f028c-116">Um parâmetro enumerado que descreve o tipo de movimentação que ocorreu.</span><span class="sxs-lookup"><span data-stu-id="f028c-116">An enumerated parameter that describes the type of move that occurred.</span></span>

</dd> <dt>

<span data-ttu-id="f028c-117">*bstrOldAddress* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f028c-117">*bstrOldAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f028c-118">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="f028c-118">Type: **BSTR**</span></span>

<span data-ttu-id="f028c-119">O endereço antigo do item que foi movido.</span><span class="sxs-lookup"><span data-stu-id="f028c-119">The old address of the item that moved.</span></span> <span data-ttu-id="f028c-120">Para arquivos normais,*eChangeAdviseSematics* é **nulo**.</span><span class="sxs-lookup"><span data-stu-id="f028c-120">For normal files,*eChangeAdviseSematics* is **NULL**.</span></span> <span data-ttu-id="f028c-121">Para uma pasta ou diretório, defina *eChangeAdviseSematics* para o \_ diretório de semântica da AC \_ \_ do GTHR.</span><span class="sxs-lookup"><span data-stu-id="f028c-121">For a folder or directory, set *eChangeAdviseSematics* to GTHR\_CA\_SEMANTICS\_DIRECTORY.</span></span>

</dd> <dt>

<span data-ttu-id="f028c-122">*bstrNewAddress* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f028c-122">*bstrNewAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f028c-123">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="f028c-123">Type: **BSTR**</span></span>

<span data-ttu-id="f028c-124">O novo endereço do item que foi movido.</span><span class="sxs-lookup"><span data-stu-id="f028c-124">The new address of the item that moved.</span></span>

</dd> <dt>

<span data-ttu-id="f028c-125">*bstrLogicalAddress* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f028c-125">*bstrLogicalAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f028c-126">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="f028c-126">Type: **BSTR**</span></span>

<span data-ttu-id="f028c-127">O endereço lógico do item que foi movido.</span><span class="sxs-lookup"><span data-stu-id="f028c-127">The logical address of the item that moved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f028c-128">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f028c-128">Return value</span></span>

<span data-ttu-id="f028c-129">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="f028c-129">This method does not return a value.</span></span>

 

 
