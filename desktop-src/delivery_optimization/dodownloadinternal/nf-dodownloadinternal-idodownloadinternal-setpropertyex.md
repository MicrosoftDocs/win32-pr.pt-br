---
title: 'Método IDODownloadInternal:: SetPropertyEx'
description: Define uma propriedade de download estendido. O método aceita um ponteiro para uma **variante** que contém um valor de propriedade específico a ser aplicado ao download.
keywords:
- 'Método IDODownloadInternal:: SetPropertyEx'
topic_type:
- apiref
api_name:
- IDODownloadInternal.SetPropertyEx
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/29/2019
ms.openlocfilehash: e6630cc3e767531dd94da39fe73d88284c9ca0d0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917353"
---
# <a name="idodownloadinternalsetpropertyex-method"></a><span data-ttu-id="88d63-105">Método IDODownloadInternal:: SetPropertyEx</span><span class="sxs-lookup"><span data-stu-id="88d63-105">IDODownloadInternal::SetPropertyEx method</span></span>

> [!IMPORTANT]
> <span data-ttu-id="88d63-106">A interface **IDODownloadInternal** foi preterida.</span><span class="sxs-lookup"><span data-stu-id="88d63-106">The **IDODownloadInternal** interface is deprecated.</span></span> <span data-ttu-id="88d63-107">Em vez disso, use a interface [IDODownload](../do/nn-do-idodownload.md) .</span><span class="sxs-lookup"><span data-stu-id="88d63-107">Instead, use the [IDODownload](../do/nn-do-idodownload.md) interface.</span></span>

<span data-ttu-id="88d63-108">Define uma propriedade de download estendido.</span><span class="sxs-lookup"><span data-stu-id="88d63-108">Sets an extended download property.</span></span> <span data-ttu-id="88d63-109">O método aceita um ponteiro para uma **variante** que contém um valor de propriedade específico a ser aplicado ao download.</span><span class="sxs-lookup"><span data-stu-id="88d63-109">The method accepts a pointer to a **VARIANT** that contains a specific property value to apply to the download.</span></span>

## <a name="syntax"></a><span data-ttu-id="88d63-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="88d63-110">Syntax</span></span>

```cpp
HRESULT SetPropertyEx(
  DODownloadPropertyEx propId, 
  VARIANT* propVal
);
```

## <a name="parameters"></a><span data-ttu-id="88d63-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="88d63-111">Parameters</span></span>

`propId`

<span data-ttu-id="88d63-112">A ID de propriedade necessária a ser definida (do tipo **DODownloadPropertyEx**).</span><span class="sxs-lookup"><span data-stu-id="88d63-112">The required property ID to set (of type **DODownloadPropertyEx**).</span></span>

`propVal`

<span data-ttu-id="88d63-113">O valor da propriedade a ser definido, armazenado em uma **variante**.</span><span class="sxs-lookup"><span data-stu-id="88d63-113">The property value to set, stored in a **VARIANT**.</span></span>

## <a name="return-value"></a><span data-ttu-id="88d63-114">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="88d63-114">Return Value</span></span>

<span data-ttu-id="88d63-115">Se a função for realizada com sucesso, ela retornará **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="88d63-115">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="88d63-116">Caso contrário, ele retorna um [código de erro](/windows/desktop/com/com-error-codes-10) [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) .</span><span class="sxs-lookup"><span data-stu-id="88d63-116">Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [error code](/windows/desktop/com/com-error-codes-10).</span></span>

|<span data-ttu-id="88d63-117">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="88d63-117">Return value</span></span>|<span data-ttu-id="88d63-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="88d63-118">Description</span></span>|
|-|-|
|<span data-ttu-id="88d63-119">DO_E_UNKNOWN_PROPERTY_ID</span><span class="sxs-lookup"><span data-stu-id="88d63-119">DO_E_UNKNOWN_PROPERTY_ID</span></span>|<span data-ttu-id="88d63-120">*propId* é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="88d63-120">*propId* is unknown.</span></span>|
|<span data-ttu-id="88d63-121">DO_E_INVALID_STATE</span><span class="sxs-lookup"><span data-stu-id="88d63-121">DO_E_INVALID_STATE</span></span>|<span data-ttu-id="88d63-122">O download não está atualmente em um estado que permita a configuração de propriedades.</span><span class="sxs-lookup"><span data-stu-id="88d63-122">The download is not currently in a state that allows setting properties.</span></span>|

## <a name="requirements"></a><span data-ttu-id="88d63-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="88d63-123">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="88d63-124">**Cliente mínimo com suporte**</span><span class="sxs-lookup"><span data-stu-id="88d63-124">**Minimum supported client**</span></span> | <span data-ttu-id="88d63-125">Somente aplicativos do Windows 10, versão 1809 \[ Win32\]</span><span class="sxs-lookup"><span data-stu-id="88d63-125">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="88d63-126">**Servidor mínimo com suporte**</span><span class="sxs-lookup"><span data-stu-id="88d63-126">**Minimum supported server**</span></span> | <span data-ttu-id="88d63-127">Somente aplicativos do Windows Server, versão 1809 \[ Win32\]</span><span class="sxs-lookup"><span data-stu-id="88d63-127">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="88d63-128">**Cabeçalho**</span><span class="sxs-lookup"><span data-stu-id="88d63-128">**Header**</span></span> | <span data-ttu-id="88d63-129">DODownloadInternal. h</span><span class="sxs-lookup"><span data-stu-id="88d63-129">DODownloadInternal.h</span></span> |