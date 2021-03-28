---
description: Adiciona uma entrada à lista MRU (usada mais recentemente).
title: 'Método IACLCustomMRU:: AddMRUString'
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
ms.openlocfilehash: d2f444041f466b367f3d4532f65029bcc69c3683
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988972"
---
# <a name="iaclcustommruaddmrustring-method"></a><span data-ttu-id="068fe-103">Método IACLCustomMRU:: AddMRUString</span><span class="sxs-lookup"><span data-stu-id="068fe-103">IACLCustomMRU::AddMRUString method</span></span>

<span data-ttu-id="068fe-104">Adiciona uma entrada à lista MRU (usada mais recentemente).</span><span class="sxs-lookup"><span data-stu-id="068fe-104">Adds an entry to the most recently used (MRU) list.</span></span>

## <a name="syntax"></a><span data-ttu-id="068fe-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="068fe-105">Syntax</span></span>


```C++
HRESULT AddMRUString(
  [in] LPCWSTR pwszEntry
);
```



## <a name="parameters"></a><span data-ttu-id="068fe-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="068fe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="068fe-107">*pwszEntry* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="068fe-107">*pwszEntry* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="068fe-108">Tipo: **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="068fe-108">Type: **LPCWSTR**</span></span>

<span data-ttu-id="068fe-109">Um ponteiro para um buffer que contém a nova entrada.</span><span class="sxs-lookup"><span data-stu-id="068fe-109">A pointer to a buffer containing the new entry.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="068fe-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="068fe-110">Return value</span></span>

<span data-ttu-id="068fe-111">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="068fe-111">Type: **HRESULT**</span></span>

<span data-ttu-id="068fe-112">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="068fe-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="068fe-113">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="068fe-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="068fe-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="068fe-114">Requirements</span></span>



| <span data-ttu-id="068fe-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="068fe-115">Requirement</span></span> | <span data-ttu-id="068fe-116">Valor</span><span class="sxs-lookup"><span data-stu-id="068fe-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="068fe-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="068fe-117">Minimum supported client</span></span><br/> | <span data-ttu-id="068fe-118">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="068fe-118">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="068fe-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="068fe-119">Minimum supported server</span></span><br/> | <span data-ttu-id="068fe-120">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="068fe-120">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



 

 




