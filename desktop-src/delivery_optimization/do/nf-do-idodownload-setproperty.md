---
title: 'Método IDODownload:: SetProperty'
description: Define uma propriedade de download.
keywords:
- 'Método IDODownload:: SetProperty'
topic_type:
- apiref
api_name:
- IDODownload.SetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: 0d496f49851aab665e49f3aaeb51e4b941d6c183
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2019
ms.locfileid: "103638923"
---
# <a name="idodownloadsetproperty-method"></a><span data-ttu-id="c6975-104">Método IDODownload:: SetProperty</span><span class="sxs-lookup"><span data-stu-id="c6975-104">IDODownload::SetProperty method</span></span>

<span data-ttu-id="c6975-105">Define uma propriedade de download.</span><span class="sxs-lookup"><span data-stu-id="c6975-105">Sets a download property.</span></span> <span data-ttu-id="c6975-106">O método aceita um ponteiro para uma **variante** que contém uma propriedade específica a ser aplicada ao download.</span><span class="sxs-lookup"><span data-stu-id="c6975-106">The method accepts a pointer to a **VARIANT** that contains a specific property to apply to the download.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6975-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c6975-107">Syntax</span></span>

```cpp
HRESULT SetProperty(
  DODownloadProperty propId,
  VARIANT* propVal
);
```

## <a name="parameters"></a><span data-ttu-id="c6975-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c6975-108">Parameters</span></span>

`propId`

<span data-ttu-id="c6975-109">A ID de propriedade necessária a ser definida (do tipo **Dodownloadproperty**).</span><span class="sxs-lookup"><span data-stu-id="c6975-109">The required property ID to set (of type **DODownloadProperty**).</span></span>

`propVal`

<span data-ttu-id="c6975-110">O valor da propriedade a ser definido, armazenado em uma **variante**.</span><span class="sxs-lookup"><span data-stu-id="c6975-110">The property value to set, stored in a **VARIANT**.</span></span>

## <a name="return-value"></a><span data-ttu-id="c6975-111">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="c6975-111">Return Value</span></span>

<span data-ttu-id="c6975-112">Se a função for realizada com sucesso, ela retornará **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="c6975-112">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="c6975-113">Caso contrário, ele retorna um [código de erro](/windows/desktop/com/com-error-codes-10) [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) .</span><span class="sxs-lookup"><span data-stu-id="c6975-113">Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [error code](/windows/desktop/com/com-error-codes-10).</span></span>

|<span data-ttu-id="c6975-114">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="c6975-114">Return value</span></span>|<span data-ttu-id="c6975-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="c6975-115">Description</span></span>|
|-|-|
|<span data-ttu-id="c6975-116">DO_E_UNKNOWN_PROPERTY_ID</span><span class="sxs-lookup"><span data-stu-id="c6975-116">DO_E_UNKNOWN_PROPERTY_ID</span></span>|<span data-ttu-id="c6975-117">*propId* é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="c6975-117">*propId* is unknown.</span></span>|
|<span data-ttu-id="c6975-118">DO_E_INVALID_STATE</span><span class="sxs-lookup"><span data-stu-id="c6975-118">DO_E_INVALID_STATE</span></span>|<span data-ttu-id="c6975-119">O download não está atualmente em um estado que permita a configuração de propriedades.</span><span class="sxs-lookup"><span data-stu-id="c6975-119">The download is not currently in a state that allows setting properties.</span></span>|

## <a name="requirements"></a><span data-ttu-id="c6975-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c6975-120">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="c6975-121">**Cliente mínimo com suporte**</span><span class="sxs-lookup"><span data-stu-id="c6975-121">**Minimum supported client**</span></span> | <span data-ttu-id="c6975-122">Somente aplicativos do Windows 10, versão 1809 \[ Win32\]</span><span class="sxs-lookup"><span data-stu-id="c6975-122">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="c6975-123">**Servidor mínimo com suporte**</span><span class="sxs-lookup"><span data-stu-id="c6975-123">**Minimum supported server**</span></span> | <span data-ttu-id="c6975-124">Somente aplicativos do Windows Server, versão 1809 \[ Win32\]</span><span class="sxs-lookup"><span data-stu-id="c6975-124">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="c6975-125">**Cabeçalho**</span><span class="sxs-lookup"><span data-stu-id="c6975-125">**Header**</span></span> | <span data-ttu-id="c6975-126">Do. h</span><span class="sxs-lookup"><span data-stu-id="c6975-126">Do.h</span></span> |
