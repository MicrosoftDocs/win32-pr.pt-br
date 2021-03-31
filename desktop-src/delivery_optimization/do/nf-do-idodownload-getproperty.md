---
title: 'Método IDODownload:: GetProperty'
description: Recupera um ponteiro para uma **variante** que contém uma propriedade de download específica.
keywords:
- 'Método IDODownload:: GetProperty'
topic_type:
- apiref
api_name:
- IDODownload.GetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: e734f109e596663ee699c764ca85f1ee45ad7947
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2019
ms.locfileid: "103823484"
---
# <a name="idodownloadgetproperty-method"></a><span data-ttu-id="564e5-104">Método IDODownload:: GetProperty</span><span class="sxs-lookup"><span data-stu-id="564e5-104">IDODownload::GetProperty method</span></span>

<span data-ttu-id="564e5-105">Recupera um ponteiro para uma **variante** que contém uma propriedade de download específica.</span><span class="sxs-lookup"><span data-stu-id="564e5-105">Retrieves a pointer to a **VARIANT** that contains a specific download property.</span></span>

## <a name="syntax"></a><span data-ttu-id="564e5-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="564e5-106">Syntax</span></span>

```cpp
HRESULT GetProperty(
  DODownloadProperty propId, 
  VARIANT* propVal
);
```

## <a name="parameters"></a><span data-ttu-id="564e5-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="564e5-107">Parameters</span></span>

`propId`

<span data-ttu-id="564e5-108">A ID de propriedade necessária para Get (do tipo **Dodownloadproperty**).</span><span class="sxs-lookup"><span data-stu-id="564e5-108">The required property ID to get (of type **DODownloadProperty**).</span></span>

`propVal`

<span data-ttu-id="564e5-109">O valor da propriedade resultante, armazenado em uma **variante**.</span><span class="sxs-lookup"><span data-stu-id="564e5-109">The resulting property value, stored in a **VARIANT**.</span></span>

## <a name="return-value"></a><span data-ttu-id="564e5-110">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="564e5-110">Return Value</span></span>

<span data-ttu-id="564e5-111">Se a função for realizada com sucesso, ela retornará **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="564e5-111">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="564e5-112">Caso contrário, ele retorna um [código de erro](/windows/desktop/com/com-error-codes-10) [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) .</span><span class="sxs-lookup"><span data-stu-id="564e5-112">Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [error code](/windows/desktop/com/com-error-codes-10).</span></span>

|<span data-ttu-id="564e5-113">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="564e5-113">Return value</span></span>|<span data-ttu-id="564e5-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="564e5-114">Description</span></span>|
|-|-|
|<span data-ttu-id="564e5-115">DO_E_UNKNOWN_PROPERTY_ID</span><span class="sxs-lookup"><span data-stu-id="564e5-115">DO_E_UNKNOWN_PROPERTY_ID</span></span>|<span data-ttu-id="564e5-116">*propId* é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="564e5-116">*propId* is unknown.</span></span>|
|<span data-ttu-id="564e5-117">DO_E_WRITE_ONLY_PROPERTY</span><span class="sxs-lookup"><span data-stu-id="564e5-117">DO_E_WRITE_ONLY_PROPERTY</span></span>|<span data-ttu-id="564e5-118">A propriedade é somente gravação e não pode ser lida.</span><span class="sxs-lookup"><span data-stu-id="564e5-118">The property is write-only, and cannot be read.</span></span>|
|<span data-ttu-id="564e5-119">E_NOT_SET</span><span class="sxs-lookup"><span data-stu-id="564e5-119">E_NOT_SET</span></span>|<span data-ttu-id="564e5-120">Essa propriedade não foi definida por meio de **SetProperty**.</span><span class="sxs-lookup"><span data-stu-id="564e5-120">No such property was set via **SetProperty**.</span></span>|

## <a name="requirements"></a><span data-ttu-id="564e5-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="564e5-121">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="564e5-122">**Cliente mínimo com suporte**</span><span class="sxs-lookup"><span data-stu-id="564e5-122">**Minimum supported client**</span></span> | <span data-ttu-id="564e5-123">Somente aplicativos do Windows 10, versão 1809 \[ Win32\]</span><span class="sxs-lookup"><span data-stu-id="564e5-123">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="564e5-124">**Servidor mínimo com suporte**</span><span class="sxs-lookup"><span data-stu-id="564e5-124">**Minimum supported server**</span></span> | <span data-ttu-id="564e5-125">Somente aplicativos do Windows Server, versão 1809 \[ Win32\]</span><span class="sxs-lookup"><span data-stu-id="564e5-125">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="564e5-126">**Cabeçalho**</span><span class="sxs-lookup"><span data-stu-id="564e5-126">**Header**</span></span> | <span data-ttu-id="564e5-127">Do. h</span><span class="sxs-lookup"><span data-stu-id="564e5-127">Do.h</span></span> |
