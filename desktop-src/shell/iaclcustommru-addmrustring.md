---
description: Adiciona uma entrada à lista de MRU (usados mais recentemente).
title: Método IACLCustomMRU::AddMRUString
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IACLCustomMRU.AddMRUString
api_type:
- COM
api_location: ''
ms.assetid: d8fb8fa5-452b-45fd-b015-d9bf3d0c642e
ms.openlocfilehash: 300474dde82274c668e52d9fe9910634d0ac904c
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841997"
---
# <a name="iaclcustommruaddmrustring-method"></a><span data-ttu-id="d97c1-103">Método IACLCustomMRU::AddMRUString</span><span class="sxs-lookup"><span data-stu-id="d97c1-103">IACLCustomMRU::AddMRUString method</span></span>

<span data-ttu-id="d97c1-104">Adiciona uma entrada à lista de MRU (usados mais recentemente).</span><span class="sxs-lookup"><span data-stu-id="d97c1-104">Adds an entry to the most recently used (MRU) list.</span></span>

## <a name="syntax"></a><span data-ttu-id="d97c1-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d97c1-105">Syntax</span></span>


```C++
HRESULT AddMRUString(
  [in] LPCWSTR pwszEntry
);
```



## <a name="parameters"></a><span data-ttu-id="d97c1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d97c1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d97c1-107">*pwszEntry* \[ Em\]</span><span class="sxs-lookup"><span data-stu-id="d97c1-107">*pwszEntry* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d97c1-108">Tipo: **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="d97c1-108">Type: **LPCWSTR**</span></span>

<span data-ttu-id="d97c1-109">Um ponteiro para um buffer que contém a nova entrada.</span><span class="sxs-lookup"><span data-stu-id="d97c1-109">A pointer to a buffer containing the new entry.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d97c1-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d97c1-110">Return value</span></span>

<span data-ttu-id="d97c1-111">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="d97c1-111">Type: **HRESULT**</span></span>

<span data-ttu-id="d97c1-112">Se esse método for bem-sucedido, ele **retornará S \_ OK.**</span><span class="sxs-lookup"><span data-stu-id="d97c1-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d97c1-113">Caso contrário, ele retornará um **código de erro HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="d97c1-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="d97c1-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d97c1-114">Requirements</span></span>



| <span data-ttu-id="d97c1-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="d97c1-115">Requirement</span></span> | <span data-ttu-id="d97c1-116">Valor</span><span class="sxs-lookup"><span data-stu-id="d97c1-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d97c1-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d97c1-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d97c1-118">Somente \[ aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="d97c1-118">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="d97c1-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d97c1-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d97c1-120">Somente aplicativos da área de trabalho do Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="d97c1-120">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



 

 




