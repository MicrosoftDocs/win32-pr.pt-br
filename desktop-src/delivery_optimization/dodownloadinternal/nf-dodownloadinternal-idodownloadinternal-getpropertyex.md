---
title: 'Método IDODownloadInternal:: GetPropertyEx'
description: Recupera um ponteiro para uma **variante** que contém um valor de propriedade de download estendido específico.
keywords:
- 'Método IDODownloadInternal:: GetPropertyEx'
topic_type:
- apiref
api_name:
- IDODownloadInternal.GetPropertyEx
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/29/2019
ms.openlocfilehash: 908f9b15df5c0c4a2769149419ff12d545201e5c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366274"
---
# <a name="idodownloadinternalgetpropertyex-method"></a><span data-ttu-id="a66ab-104">Método IDODownloadInternal:: GetPropertyEx</span><span class="sxs-lookup"><span data-stu-id="a66ab-104">IDODownloadInternal::GetPropertyEx method</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a66ab-105">A interface **IDODownloadInternal** foi preterida.</span><span class="sxs-lookup"><span data-stu-id="a66ab-105">The **IDODownloadInternal** interface is deprecated.</span></span> <span data-ttu-id="a66ab-106">Em vez disso, use a interface [IDODownload](../do/nn-do-idodownload.md) .</span><span class="sxs-lookup"><span data-stu-id="a66ab-106">Instead, use the [IDODownload](../do/nn-do-idodownload.md) interface.</span></span>

<span data-ttu-id="a66ab-107">Recupera um ponteiro para uma **variante** que contém um valor de propriedade de download estendido específico.</span><span class="sxs-lookup"><span data-stu-id="a66ab-107">Retrieves a pointer to a **VARIANT** that contains a specific extended download property value.</span></span>

## <a name="syntax"></a><span data-ttu-id="a66ab-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a66ab-108">Syntax</span></span>

```cpp
HRESULT GetPropertyEx(
  DODownloadPropertyEx propId, 
  VARIANT* propVal
);
```

## <a name="parameters"></a><span data-ttu-id="a66ab-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a66ab-109">Parameters</span></span>

`propId`

<span data-ttu-id="a66ab-110">A ID de propriedade necessária para Get (do tipo **DODownloadPropertyEx**).</span><span class="sxs-lookup"><span data-stu-id="a66ab-110">The required property ID to get (of type **DODownloadPropertyEx**).</span></span>

`propVal`

<span data-ttu-id="a66ab-111">O valor da propriedade resultante, armazenado em uma **variante**.</span><span class="sxs-lookup"><span data-stu-id="a66ab-111">The resulting property value, stored in a **VARIANT**.</span></span>

## <a name="return-value"></a><span data-ttu-id="a66ab-112">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="a66ab-112">Return Value</span></span>

<span data-ttu-id="a66ab-113">Se a função for realizada com sucesso, ela retornará **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="a66ab-113">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="a66ab-114">Caso contrário, ele retorna um [código de erro](/windows/desktop/com/com-error-codes-10) [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) .</span><span class="sxs-lookup"><span data-stu-id="a66ab-114">Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [error code](/windows/desktop/com/com-error-codes-10).</span></span>

|<span data-ttu-id="a66ab-115">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="a66ab-115">Return value</span></span>|<span data-ttu-id="a66ab-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="a66ab-116">Description</span></span>|
|-|-|
|<span data-ttu-id="a66ab-117">DO_E_UNKNOWN_PROPERTY_ID</span><span class="sxs-lookup"><span data-stu-id="a66ab-117">DO_E_UNKNOWN_PROPERTY_ID</span></span>|<span data-ttu-id="a66ab-118">*propId* é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="a66ab-118">*propId* is unknown.</span></span>|
|<span data-ttu-id="a66ab-119">DO_E_WRITE_ONLY_PROPERTY</span><span class="sxs-lookup"><span data-stu-id="a66ab-119">DO_E_WRITE_ONLY_PROPERTY</span></span>|<span data-ttu-id="a66ab-120">A propriedade é somente gravação e não pode ser lida.</span><span class="sxs-lookup"><span data-stu-id="a66ab-120">The property is write-only, and cannot be read.</span></span>|
|<span data-ttu-id="a66ab-121">E_NOT_SET</span><span class="sxs-lookup"><span data-stu-id="a66ab-121">E_NOT_SET</span></span>|<span data-ttu-id="a66ab-122">Essa propriedade não foi definida por meio de **SetPropertyEx**.</span><span class="sxs-lookup"><span data-stu-id="a66ab-122">No such property was set via **SetPropertyEx**.</span></span>|

## <a name="requirements"></a><span data-ttu-id="a66ab-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a66ab-123">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="a66ab-124">**Cliente mínimo com suporte**</span><span class="sxs-lookup"><span data-stu-id="a66ab-124">**Minimum supported client**</span></span> | <span data-ttu-id="a66ab-125">Somente aplicativos do Windows 10, versão 1809 \[ Win32\]</span><span class="sxs-lookup"><span data-stu-id="a66ab-125">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="a66ab-126">**Servidor mínimo com suporte**</span><span class="sxs-lookup"><span data-stu-id="a66ab-126">**Minimum supported server**</span></span> | <span data-ttu-id="a66ab-127">Somente aplicativos do Windows Server, versão 1809 \[ Win32\]</span><span class="sxs-lookup"><span data-stu-id="a66ab-127">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="a66ab-128">**Cabeçalho**</span><span class="sxs-lookup"><span data-stu-id="a66ab-128">**Header**</span></span> | <span data-ttu-id="a66ab-129">DODownloadInternal. h</span><span class="sxs-lookup"><span data-stu-id="a66ab-129">DODownloadInternal.h</span></span> |