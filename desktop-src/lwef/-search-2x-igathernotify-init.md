---
title: Método IGatherNotify init (preterido)
description: Este tópico da interface do Windows Desktop Search foi preterido e é substituído pela API ISearchPersistentItemsChangedSink do Windows Search no SDK do Windows. | Método IGatherNotify init (preterido)
ms.assetid: 6a5f89eb-10f4-4262-89bf-b47e345f12eb
keywords:
- Método init (preterido) recursos de ambiente herdado do Windows
- Método init (preterido) recursos de ambiente herdado do Windows, interface IGatherNotify
- Recursos do ambiente Windows herdado da interface IGatherNotify, método init (preterido)
topic_type:
- apiref
api_name:
- IGatherNotify.Init (Deprecated)
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 81379bb4a9a7c6099912bfc9ebca170141d76cd2
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105781439"
---
# <a name="igathernotifyinit-deprecated-method"></a><span data-ttu-id="06d24-107">Método IGatherNotify:: init (preterido)</span><span class="sxs-lookup"><span data-stu-id="06d24-107">IGatherNotify::Init (Deprecated) method</span></span>

<span data-ttu-id="06d24-108">\[**Init** pode ser alterado ou indisponível nas versões subsequentes do sistema operacional ou produto.\]</span><span class="sxs-lookup"><span data-stu-id="06d24-108">\[**Init** may be altered or unavailable in subsequent versions of the operating system or product.\]</span></span>

<span data-ttu-id="06d24-109">Este tópico da interface do Windows Desktop Search foi preterido e é substituído pela API [**ISearchPersistentItemsChangedSink**](/windows/desktop/api/searchapi/nn-searchapi-isearchpersistentitemschangedsink) do Windows Search no SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="06d24-109">This Windows Desktop Search interface topic is deprecated and is superseded by the Windows Search [**ISearchPersistentItemsChangedSink**](/windows/desktop/api/searchapi/nn-searchapi-isearchpersistentitemschangedsink) API in the Windows SDK.</span></span>

<span data-ttu-id="06d24-110">Inicializa a interface do gatherer.</span><span class="sxs-lookup"><span data-stu-id="06d24-110">Initializes the Gatherer interface.</span></span> <span data-ttu-id="06d24-111">Também especifica o índice a ser notificado e a loja de aplicativos a ser monitorada.</span><span class="sxs-lookup"><span data-stu-id="06d24-111">Also specifies the index to notify and the application store to monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="06d24-112">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="06d24-112">Syntax</span></span>


```C++
void Init (Deprecated)(
  [in] BSTR    bstrApplication,
  [in] BSTR    bstrProject,
  [in] variant varScopesBstrArray
);
```



## <a name="parameters"></a><span data-ttu-id="06d24-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="06d24-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06d24-114">*bstrApplication* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="06d24-114">*bstrApplication* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06d24-115">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="06d24-115">Type: **BSTR**</span></span>

<span data-ttu-id="06d24-116">Uma cadeia de caracteres que especifica o aplicativo de destino.</span><span class="sxs-lookup"><span data-stu-id="06d24-116">A string that specifies the target application.</span></span>

</dd> <dt>

<span data-ttu-id="06d24-117">*bstrProject* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="06d24-117">*bstrProject* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06d24-118">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="06d24-118">Type: **BSTR**</span></span>

<span data-ttu-id="06d24-119">Uma cadeia de caracteres que especifica o nome do indexador para o qual passar informações do gatherer.</span><span class="sxs-lookup"><span data-stu-id="06d24-119">A string that specifies the name of the indexer to pass gatherer information to.</span></span>

</dd> <dt>

<span data-ttu-id="06d24-120">*varScopesBstrArray* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="06d24-120">*varScopesBstrArray* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06d24-121">Tipo: **variante**</span><span class="sxs-lookup"><span data-stu-id="06d24-121">Type: **variant**</span></span>

<span data-ttu-id="06d24-122">Parâmetro opcional, que permite que você passe uma matriz de escopos a ser inicializada.</span><span class="sxs-lookup"><span data-stu-id="06d24-122">Optional parameter, that enables you to pass an array of scopes to be initialized.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06d24-123">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="06d24-123">Return value</span></span>

<span data-ttu-id="06d24-124">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="06d24-124">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="06d24-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="06d24-125">Remarks</span></span>

<span data-ttu-id="06d24-126">Inicialize com Application = "RSApp", Project = "MyIndex".</span><span class="sxs-lookup"><span data-stu-id="06d24-126">Initialize with application="RSApp", Project="MyIndex".</span></span>

 

 
