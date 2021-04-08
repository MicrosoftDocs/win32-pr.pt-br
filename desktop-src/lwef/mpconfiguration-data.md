---
title: Estrutura de MPCONFIGURATION_DATA (MpClient. h)
description: Contém dados sobre alterações de configuração, incluindo os valores novos e antigos.
ms.assetid: AB70B1C0-C148-44BC-8C0E-CC5D2A66BCA5
keywords:
- Recursos do ambiente Windows herdado da estrutura de MPCONFIGURATION_DATA
- Ponteiro de estrutura de PMPCONFIGURATION_DATA recursos de ambiente herdados do Windows
topic_type:
- apiref
api_name:
- MPCONFIGURATION_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7bb54ae4e323f2144dd25c52005d8484b0a207e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009219"
---
# <a name="mpconfiguration_data-structure"></a><span data-ttu-id="facfc-105">\_Estrutura de dados MPCONFIGURATION</span><span class="sxs-lookup"><span data-stu-id="facfc-105">MPCONFIGURATION\_DATA structure</span></span>

<span data-ttu-id="facfc-106">Contém dados sobre alterações de configuração, incluindo os valores novos e antigos.</span><span class="sxs-lookup"><span data-stu-id="facfc-106">Contains data about configuration changes, including the old and new values.</span></span>

## <a name="syntax"></a><span data-ttu-id="facfc-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="facfc-107">Syntax</span></span>


```C++
typedef struct tagMPCONFIGURATION_DATA {
  MP_MIDL_STRING LPWSTR ConfigurationName;
  DWORD                 DataType;
  DWORD                 PreviousDataSize;
  BYTE                  *pPreviousData;
  DWORD                 CurrentDataSize;
  BYTE                  *pCurrentData;
} MPCONFIGURATION_DATA, *PMPCONFIGURATION_DATA;
```



## <a name="members"></a><span data-ttu-id="facfc-108">Membros</span><span class="sxs-lookup"><span data-stu-id="facfc-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="facfc-109">**ConfigurationName**</span><span class="sxs-lookup"><span data-stu-id="facfc-109">**ConfigurationName**</span></span>
</dt> <dd>

<span data-ttu-id="facfc-110">Tipo: **PG \_ MIDL \_ String LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="facfc-110">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="facfc-111">Nome da configuração que foi alterada.</span><span class="sxs-lookup"><span data-stu-id="facfc-111">Name of the configuration that changed.</span></span>

</dd> <dt>

<span data-ttu-id="facfc-112">**DataType**</span><span class="sxs-lookup"><span data-stu-id="facfc-112">**DataType**</span></span>
</dt> <dd>

<span data-ttu-id="facfc-113">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="facfc-113">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="facfc-114">O tipo de dados usados.</span><span class="sxs-lookup"><span data-stu-id="facfc-114">The type of data used.</span></span>

</dd> <dt>

<span data-ttu-id="facfc-115">**PreviousDataSize**</span><span class="sxs-lookup"><span data-stu-id="facfc-115">**PreviousDataSize**</span></span>
</dt> <dd>

<span data-ttu-id="facfc-116">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="facfc-116">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="facfc-117">Tamanho dos dados anteriores, em bytes.</span><span class="sxs-lookup"><span data-stu-id="facfc-117">Size of previous data, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="facfc-118">**pPreviousData**</span><span class="sxs-lookup"><span data-stu-id="facfc-118">**pPreviousData**</span></span>
</dt> <dd>

<span data-ttu-id="facfc-119">Tipo: \**byte \** _</span><span class="sxs-lookup"><span data-stu-id="facfc-119">Type: \**BYTE\** _</span></span>

</dd> <dd>

<span data-ttu-id="facfc-120">Ponteiro para dados anteriores.</span><span class="sxs-lookup"><span data-stu-id="facfc-120">Pointer to previous data.</span></span>

</dd> <dt>

<span data-ttu-id="facfc-121">_ *CurrentDataSize*\*</span><span class="sxs-lookup"><span data-stu-id="facfc-121">_ *CurrentDataSize*\*</span></span>
</dt> <dd>

<span data-ttu-id="facfc-122">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="facfc-122">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="facfc-123">Tamanho dos novos dados, em bytes.</span><span class="sxs-lookup"><span data-stu-id="facfc-123">Size of new data, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="facfc-124">**pCurrentData**</span><span class="sxs-lookup"><span data-stu-id="facfc-124">**pCurrentData**</span></span>
</dt> <dd>

<span data-ttu-id="facfc-125">Tipo: **byte \***</span><span class="sxs-lookup"><span data-stu-id="facfc-125">Type: **BYTE\***</span></span>

</dd> <dd>

<span data-ttu-id="facfc-126">Ponteiro para novos dados.</span><span class="sxs-lookup"><span data-stu-id="facfc-126">Pointer to new data.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="facfc-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="facfc-127">Requirements</span></span>



| <span data-ttu-id="facfc-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="facfc-128">Requirement</span></span> | <span data-ttu-id="facfc-129">Valor</span><span class="sxs-lookup"><span data-stu-id="facfc-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="facfc-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="facfc-130">Minimum supported client</span></span><br/> | <span data-ttu-id="facfc-131">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="facfc-131">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="facfc-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="facfc-132">Minimum supported server</span></span><br/> | <span data-ttu-id="facfc-133">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="facfc-133">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="facfc-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="facfc-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="facfc-135"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="facfc-135"><dt>MpClient.h</dt></span></span> </dl> |



 

 





