---
description: Carrega uma lista de cadeias de caracteres na lista MRU (usada mais recentemente) do registro.
title: 'Método IACLCustomMRU:: Initialize'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IACLCustomMRU.Initialize
api_type:
- COM
api_location: ''
ms.assetid: 358921b0-46c4-4428-b0b5-57a44fc3247b
ms.openlocfilehash: 768df625cb66c888ddccc85f72de5b8676c20b10
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988971"
---
# <a name="iaclcustommruinitialize-method"></a><span data-ttu-id="2f881-103">Método IACLCustomMRU:: Initialize</span><span class="sxs-lookup"><span data-stu-id="2f881-103">IACLCustomMRU::Initialize method</span></span>

<span data-ttu-id="2f881-104">Carrega uma lista de cadeias de caracteres na lista MRU (usada mais recentemente) do registro.</span><span class="sxs-lookup"><span data-stu-id="2f881-104">Loads a list of strings into the most recently used (MRU) list from the registry.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f881-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2f881-105">Syntax</span></span>


```C++
HRESULT Initialize(
  [in] LPCWSTR pwszMRURegKey,
  [in] DWORD   dwMax
);
```



## <a name="parameters"></a><span data-ttu-id="2f881-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2f881-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f881-107">*pwszMRURegKey* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2f881-107">*pwszMRURegKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f881-108">Tipo: **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="2f881-108">Type: **LPCWSTR**</span></span>

<span data-ttu-id="2f881-109">Um ponteiro para um buffer contendo a chave do registro que contém as cadeias de caracteres da lista MRU.</span><span class="sxs-lookup"><span data-stu-id="2f881-109">A pointer to a buffer containing the registry key holding the strings for the MRU list.</span></span>

</dd> <dt>

<span data-ttu-id="2f881-110">*dwMax* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2f881-110">*dwMax* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f881-111">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="2f881-111">Type: **DWORD**</span></span>

<span data-ttu-id="2f881-112">O número máximo de entradas que podem ser obtidas de *pwszMRURegKey*.</span><span class="sxs-lookup"><span data-stu-id="2f881-112">The maximum number of entries that can be taken from *pwszMRURegKey*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f881-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2f881-113">Return value</span></span>

<span data-ttu-id="2f881-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="2f881-114">Type: **HRESULT**</span></span>

<span data-ttu-id="2f881-115">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="2f881-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="2f881-116">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="2f881-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f881-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2f881-117">Requirements</span></span>



| <span data-ttu-id="2f881-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="2f881-118">Requirement</span></span> | <span data-ttu-id="2f881-119">Valor</span><span class="sxs-lookup"><span data-stu-id="2f881-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="2f881-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2f881-120">Minimum supported client</span></span><br/> | <span data-ttu-id="2f881-121">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="2f881-121">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="2f881-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2f881-122">Minimum supported server</span></span><br/> | <span data-ttu-id="2f881-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2f881-123">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



 

 




