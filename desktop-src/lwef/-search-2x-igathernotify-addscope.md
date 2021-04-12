---
title: Método IGatherNotify addscope (preterido)
description: Este tópico da interface do Windows Desktop Search foi preterido e é substituído pela API ISearchPersistentItemsChangedSink do Windows Search no SDK do Windows. | Método IGatherNotify addscope (preterido)
ms.assetid: 3b250818-1876-40b2-9a85-91f2bf6f52ec
keywords:
- Método addscope (preterido) recursos de ambiente herdado do Windows
- Método addscope (preterido) recursos de ambiente herdados do Windows, interface IGatherNotify
- Recursos do ambiente Windows herdado da interface IGatherNotify, método addscope (preterido)
topic_type:
- apiref
api_name:
- IGatherNotify.AddScope (Deprecated)
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 967dc4f30acee2f8d8adbcfec04f0508e53bba15
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104298251"
---
# <a name="igathernotifyaddscope-deprecated-method"></a><span data-ttu-id="d6f5f-107">Método IGatherNotify:: addscope (preterido)</span><span class="sxs-lookup"><span data-stu-id="d6f5f-107">IGatherNotify::AddScope (Deprecated) method</span></span>

<span data-ttu-id="d6f5f-108">\[**Addscope** pode ser alterado ou indisponível nas versões subsequentes do sistema operacional ou produto.\]</span><span class="sxs-lookup"><span data-stu-id="d6f5f-108">\[**AddScope** may be altered or unavailable in subsequent versions of the operating system or product.\]</span></span>

<span data-ttu-id="d6f5f-109">Este tópico da interface do Windows Desktop Search foi preterido e é substituído pela API [**ISearchPersistentItemsChangedSink**](/windows/desktop/api/searchapi/nn-searchapi-isearchpersistentitemschangedsink) do Windows Search no SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="d6f5f-109">This Windows Desktop Search interface topic is deprecated and is superseded by the Windows Search [**ISearchPersistentItemsChangedSink**](/windows/desktop/api/searchapi/nn-searchapi-isearchpersistentitemschangedsink) API in the Windows SDK.</span></span>

<span data-ttu-id="d6f5f-110">Adiciona a página inicial ou a URL que você está monitorando.</span><span class="sxs-lookup"><span data-stu-id="d6f5f-110">Adds the start page or URL you are monitoring.</span></span> <span data-ttu-id="d6f5f-111">Isso inicia um rastreamento incremental quando você se conecta e, em seguida, pressupõe que todas as alterações de URL adicionais sejam feitas por notificação.</span><span class="sxs-lookup"><span data-stu-id="d6f5f-111">This initiates an incremental crawl when you connect, and then assumes all further URL changes are by notification.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6f5f-112">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d6f5f-112">Syntax</span></span>


```C++
void AddScope (Deprecated)(
  [in] BSTR bstrScope
);
```



## <a name="parameters"></a><span data-ttu-id="d6f5f-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d6f5f-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6f5f-114">*bstrScope* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d6f5f-114">*bstrScope* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6f5f-115">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="d6f5f-115">Type: **BSTR**</span></span>

<span data-ttu-id="d6f5f-116">Uma cadeia de caracteres que especifica a página inicial ou URL que você está monitorando.</span><span class="sxs-lookup"><span data-stu-id="d6f5f-116">A string that specifies the start page or URLthat you are monitoring.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6f5f-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d6f5f-117">Return value</span></span>

<span data-ttu-id="d6f5f-118">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="d6f5f-118">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d6f5f-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="d6f5f-119">Remarks</span></span>

<span data-ttu-id="d6f5f-120">Chamar esse método inicia um rastreamento incremental quando conectado à loja.</span><span class="sxs-lookup"><span data-stu-id="d6f5f-120">Calling this method starts an incremental crawl when connected to the store.</span></span> <span data-ttu-id="d6f5f-121">Depois disso, supõe-se que todas as alterações de URL sejam feitas por notificação após a atualização inicial.</span><span class="sxs-lookup"><span data-stu-id="d6f5f-121">Thereafter, it is assumed that all URL changes are by notification after the initial update.</span></span>

 

 
