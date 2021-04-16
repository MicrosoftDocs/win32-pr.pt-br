---
title: 'Método IDOManager:: EnumDownloads'
description: Recupera um ponteiro de interface para um objeto enumerador que é usado para enumerar os downloads existentes.
keywords:
- 'Método IDOManager:: EnumDownloads'
topic_type:
- apiref
api_name:
- IDOManager.EnumDownloads
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: a1e7fed2955fdc1b5ac0c11cfebc34aa95517603
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2019
ms.locfileid: "105772744"
---
# <a name="idomanagerenumdownloads-method"></a><span data-ttu-id="aa40f-104">Método IDOManager:: EnumDownloads</span><span class="sxs-lookup"><span data-stu-id="aa40f-104">IDOManager::EnumDownloads method</span></span>

<span data-ttu-id="aa40f-105">Recupera um ponteiro de interface para um objeto enumerador que é usado para enumerar os downloads existentes.</span><span class="sxs-lookup"><span data-stu-id="aa40f-105">Retrieves an interface pointer to an enumerator object that is used to enumerate existing downloads.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa40f-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="aa40f-106">Syntax</span></span>

```cpp
HRESULT EnumDownloads(
  DO_DOWNLOAD_ENUM_CATEGORY *category, 
  IEnumUnknown **ppEnum
);
```

## <a name="parameters"></a><span data-ttu-id="aa40f-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="aa40f-107">Parameters</span></span>

`category`

<span data-ttu-id="aa40f-108">Opcional.</span><span class="sxs-lookup"><span data-stu-id="aa40f-108">Optional.</span></span> <span data-ttu-id="aa40f-109">O nome da propriedade a ser usada como uma categoria a ser enumerada.</span><span class="sxs-lookup"><span data-stu-id="aa40f-109">The property name to be used as a category to enumerate.</span></span> <span data-ttu-id="aa40f-110">A passagem `nullptr` irá recuperar todos os downloads existentes.</span><span class="sxs-lookup"><span data-stu-id="aa40f-110">Passing `nullptr` will retrieve all existing downloads.</span></span> <span data-ttu-id="aa40f-111">As propriedades a seguir têm suporte como uma categoria.</span><span class="sxs-lookup"><span data-stu-id="aa40f-111">The following properties are supported as a category.</span></span>

- <span data-ttu-id="aa40f-112">**DODownloadProperty_Id**</span><span class="sxs-lookup"><span data-stu-id="aa40f-112">**DODownloadProperty_Id**</span></span>
- <span data-ttu-id="aa40f-113">**DODownloadProperty_Uri**</span><span class="sxs-lookup"><span data-stu-id="aa40f-113">**DODownloadProperty_Uri**</span></span>
- <span data-ttu-id="aa40f-114">**DODownloadProperty_ContentId**</span><span class="sxs-lookup"><span data-stu-id="aa40f-114">**DODownloadProperty_ContentId**</span></span>
- <span data-ttu-id="aa40f-115">**DODownloadProperty_DisplayName**</span><span class="sxs-lookup"><span data-stu-id="aa40f-115">**DODownloadProperty_DisplayName**</span></span>
- <span data-ttu-id="aa40f-116">**DODownloadProperty_LocalPath**</span><span class="sxs-lookup"><span data-stu-id="aa40f-116">**DODownloadProperty_LocalPath**</span></span>

`ppEnum`

<span data-ttu-id="aa40f-117">O endereço de um ponteiro de interface para **IEnumUnknown**, que é usado para enumerar os downloads existentes.</span><span class="sxs-lookup"><span data-stu-id="aa40f-117">The address of an interface pointer to **IEnumUnknown**, which is used to enumerate existing downloads.</span></span> <span data-ttu-id="aa40f-118">O conteúdo do enumerador depende do valor da *categoria*.</span><span class="sxs-lookup"><span data-stu-id="aa40f-118">The contents of the enumerator depend on the value of *category*.</span></span> <span data-ttu-id="aa40f-119">Os downloads incluídos na interface de enumeração são aqueles que foram criados anteriormente pelo mesmo chamador para essa função.</span><span class="sxs-lookup"><span data-stu-id="aa40f-119">The downloads included in the enumeration interface are the ones that were previously created by the same caller to this function.</span></span> 

## <a name="return-value"></a><span data-ttu-id="aa40f-120">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="aa40f-120">Return Value</span></span>

<span data-ttu-id="aa40f-121">Se a função for realizada com sucesso, ela retornará **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="aa40f-121">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="aa40f-122">Caso contrário, ele retorna um [código de erro](/windows/desktop/com/com-error-codes-10) [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) .</span><span class="sxs-lookup"><span data-stu-id="aa40f-122">Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [error code](/windows/desktop/com/com-error-codes-10).</span></span>

## <a name="requirements"></a><span data-ttu-id="aa40f-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aa40f-123">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="aa40f-124">**Cliente mínimo com suporte**</span><span class="sxs-lookup"><span data-stu-id="aa40f-124">**Minimum supported client**</span></span> | <span data-ttu-id="aa40f-125">Somente aplicativos do Windows 10, versão 1809 \[ Win32\]</span><span class="sxs-lookup"><span data-stu-id="aa40f-125">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="aa40f-126">**Servidor mínimo com suporte**</span><span class="sxs-lookup"><span data-stu-id="aa40f-126">**Minimum supported server**</span></span> | <span data-ttu-id="aa40f-127">Somente aplicativos do Windows Server, versão 1809 \[ Win32\]</span><span class="sxs-lookup"><span data-stu-id="aa40f-127">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="aa40f-128">**Cabeçalho**</span><span class="sxs-lookup"><span data-stu-id="aa40f-128">**Header**</span></span> | <span data-ttu-id="aa40f-129">Do. h</span><span class="sxs-lookup"><span data-stu-id="aa40f-129">Do.h</span></span> |
