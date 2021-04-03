---
title: Interface IDODownloadInternal
description: Usado para obter ou definir propriedades de download estendido.
keywords:
- Interface IDODownloadInternal
topic_type:
- apiref
api_name:
- IDODownloadInternal
api_location:
- do.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/29/2019
ms.openlocfilehash: 89dcf0e397e9761c1b156a4ad4b245209cf50020
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084731"
---
# <a name="idodownloadinternal-interface"></a><span data-ttu-id="adfdb-104">Interface IDODownloadInternal</span><span class="sxs-lookup"><span data-stu-id="adfdb-104">IDODownloadInternal interface</span></span>

> [!IMPORTANT]
> <span data-ttu-id="adfdb-105">A interface **IDODownloadInternal** foi preterida.</span><span class="sxs-lookup"><span data-stu-id="adfdb-105">The **IDODownloadInternal** interface is deprecated.</span></span> <span data-ttu-id="adfdb-106">Em vez disso, use a interface [IDODownload](../do/nn-do-idodownload.md) .</span><span class="sxs-lookup"><span data-stu-id="adfdb-106">Instead, use the [IDODownload](../do/nn-do-idodownload.md) interface.</span></span>

<span data-ttu-id="adfdb-107">A interface **IDODownloadInternal** é usada para obter ou definir propriedades de download estendido.</span><span class="sxs-lookup"><span data-stu-id="adfdb-107">The **IDODownloadInternal** interface is used to get or set extended download properties.</span></span>

## <a name="methods"></a><span data-ttu-id="adfdb-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="adfdb-108">Methods</span></span>

<span data-ttu-id="adfdb-109">A interface **IDODownloadInternal** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="adfdb-109">The **IDODownloadInternal** interface has these methods.</span></span>

| <span data-ttu-id="adfdb-110">Método</span><span class="sxs-lookup"><span data-stu-id="adfdb-110">Method</span></span> | <span data-ttu-id="adfdb-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="adfdb-111">Description</span></span> |
| ---- |:---- |
| [<span data-ttu-id="adfdb-112">IDODownloadInternal::GetPropertyEx</span><span class="sxs-lookup"><span data-stu-id="adfdb-112">IDODownloadInternal::GetPropertyEx</span></span>](./nf-dodownloadinternal-idodownloadinternal-getpropertyex.md) | <span data-ttu-id="adfdb-113">Recupera um ponteiro para uma **variante** que contém um valor de propriedade de download estendido específico.</span><span class="sxs-lookup"><span data-stu-id="adfdb-113">Retrieves a pointer to a **VARIANT** that contains a specific extended download property value.</span></span> |
| [<span data-ttu-id="adfdb-114">IDODownloadInternal::SetPropertyEx</span><span class="sxs-lookup"><span data-stu-id="adfdb-114">IDODownloadInternal::SetPropertyEx</span></span>](./nf-dodownloadinternal-idodownloadinternal-setpropertyex.md) | <span data-ttu-id="adfdb-115">Define uma propriedade de download estendido.</span><span class="sxs-lookup"><span data-stu-id="adfdb-115">Sets an extended download property.</span></span> <span data-ttu-id="adfdb-116">O método aceita um ponteiro para uma **variante** que contém um valor de propriedade específico a ser aplicado ao download.</span><span class="sxs-lookup"><span data-stu-id="adfdb-116">The method accepts a pointer to a **VARIANT** that contains a specific property value to apply to the download.</span></span> |

## <a name="requirements"></a><span data-ttu-id="adfdb-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="adfdb-117">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="adfdb-118">**Cliente mínimo com suporte**</span><span class="sxs-lookup"><span data-stu-id="adfdb-118">**Minimum supported client**</span></span> | <span data-ttu-id="adfdb-119">Somente aplicativos do Windows 10, versão 1809 \[ Win32\]</span><span class="sxs-lookup"><span data-stu-id="adfdb-119">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="adfdb-120">**Servidor mínimo com suporte**</span><span class="sxs-lookup"><span data-stu-id="adfdb-120">**Minimum supported server**</span></span> | <span data-ttu-id="adfdb-121">Somente aplicativos do Windows Server, versão 1809 \[ Win32\]</span><span class="sxs-lookup"><span data-stu-id="adfdb-121">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="adfdb-122">**Cabeçalho**</span><span class="sxs-lookup"><span data-stu-id="adfdb-122">**Header**</span></span> | <span data-ttu-id="adfdb-123">DODownloadInternal. h</span><span class="sxs-lookup"><span data-stu-id="adfdb-123">DODownloadInternal.h</span></span> |