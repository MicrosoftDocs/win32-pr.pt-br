---
title: Estrutura de MPCLEAN_DATA (MpClient. h)
description: Dados de notificação passados para a função de retorno de chamada limpa.
ms.assetid: 475A6525-5BD8-4B29-A684-53EE2758C790
keywords:
- Recursos do ambiente Windows herdado da estrutura de MPCLEAN_DATA
- Ponteiro de estrutura de PMPCLEAN_DATA recursos de ambiente herdados do Windows
topic_type:
- apiref
api_name:
- MPCLEAN_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89f0c7e867918b6567279be7c41ce72e7e396576
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644531"
---
# <a name="mpclean_data-structure"></a><span data-ttu-id="f5aef-105">\_Estrutura de dados MPCLEAN</span><span class="sxs-lookup"><span data-stu-id="f5aef-105">MPCLEAN\_DATA structure</span></span>

<span data-ttu-id="f5aef-106">Dados de notificação passados para a função de retorno de chamada limpa.</span><span class="sxs-lookup"><span data-stu-id="f5aef-106">Notification data passed to clean callback function.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5aef-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f5aef-107">Syntax</span></span>


```C++
typedef struct tagMPCLEAN_DATA {
  MPTHREAT_ID      ThreatID;
  MPTHREAT_ACTION  ThreatAction;
  DWORD            dwStatus;
  PMPRESOURCE_INFO ResourceInfo;
} MPCLEAN_DATA, *PMPCLEAN_DATA;
```



## <a name="members"></a><span data-ttu-id="f5aef-108">Membros</span><span class="sxs-lookup"><span data-stu-id="f5aef-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="f5aef-109">**Threatid**</span><span class="sxs-lookup"><span data-stu-id="f5aef-109">**ThreatID**</span></span>
</dt> <dd>

<span data-ttu-id="f5aef-110">Tipo: **\_ ID de MPTHREAT**</span><span class="sxs-lookup"><span data-stu-id="f5aef-110">Type: **MPTHREAT\_ID**</span></span>

</dd> <dd>

<span data-ttu-id="f5aef-111">Identificador de ameaça para o **mpnotify \_ limpar \_ ameaça \_ Iniciar** / **mpnotify limpeza de ameaça \_ \_ \_ bem-sucedida** / **mpnotify eventos \_ \_ \_ com falha de limpeza de ameaça** .</span><span class="sxs-lookup"><span data-stu-id="f5aef-111">Threat identifier for the **MPNOTIFY\_CLEAN\_THREAT\_START**/**MPNOTIFY\_CLEAN\_THREAT\_SUCCEEDED**/**MPNOTIFY\_CLEAN\_THREAT\_FAILED** events.</span></span> <span data-ttu-id="f5aef-112">O bit superior é definido para identificar ameaças relacionadas ao antivírus.</span><span class="sxs-lookup"><span data-stu-id="f5aef-112">Upper bit is set to identify antivirus-related threats.</span></span>

</dd> <dt>

<span data-ttu-id="f5aef-113">**Threataction**</span><span class="sxs-lookup"><span data-stu-id="f5aef-113">**ThreatAction**</span></span>
</dt> <dd>

<span data-ttu-id="f5aef-114">Tipo: **[ **\_ ação MPTHREAT**](mpthreat-action.md)**</span><span class="sxs-lookup"><span data-stu-id="f5aef-114">Type: **[**MPTHREAT\_ACTION**](mpthreat-action.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f5aef-115">Ação de ameaça para o **mpnotify \_ limpar \_ ameaça \_ Iniciar** / **mpnotify limpeza de ameaça \_ \_ \_ bem-sucedida** / **mpnotify eventos \_ \_ \_ com falha de limpeza de ameaça** .</span><span class="sxs-lookup"><span data-stu-id="f5aef-115">Threat action for the **MPNOTIFY\_CLEAN\_THREAT\_START**/**MPNOTIFY\_CLEAN\_THREAT\_SUCCEEDED**/**MPNOTIFY\_CLEAN\_THREAT\_FAILED** events.</span></span> <span data-ttu-id="f5aef-116">Consulte [**a \_ ação MPTHREAT**](mpthreat-action.md).</span><span class="sxs-lookup"><span data-stu-id="f5aef-116">See [**MPTHREAT\_ACTION**](mpthreat-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="f5aef-117">**dwStatus**</span><span class="sxs-lookup"><span data-stu-id="f5aef-117">**dwStatus**</span></span>
</dt> <dd>

<span data-ttu-id="f5aef-118">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="f5aef-118">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="f5aef-119">Status ou ações adicionais associadas à ação executada.</span><span class="sxs-lookup"><span data-stu-id="f5aef-119">Additional status or actions associated with the action taken.</span></span> <span data-ttu-id="f5aef-120">Essa é uma combinação de sinalizadores de bit [**do \_ sinalizador MPSTATUS**](mpstatus-flag.md).</span><span class="sxs-lookup"><span data-stu-id="f5aef-120">This is a combination of bit flags from [**MPSTATUS\_FLAG**](mpstatus-flag.md).</span></span>

</dd> <dt>

<span data-ttu-id="f5aef-121">**ResourceInfo**</span><span class="sxs-lookup"><span data-stu-id="f5aef-121">**ResourceInfo**</span></span>
</dt> <dd>

<span data-ttu-id="f5aef-122">Tipo: **\_ informações de PMPRESOURCE**</span><span class="sxs-lookup"><span data-stu-id="f5aef-122">Type: **PMPRESOURCE\_INFO**</span></span>

</dd> <dd>

<span data-ttu-id="f5aef-123">Informações de recurso para a **mpnotify \_ limpeza de \_ ameaça \_ Iniciar** / **mpnotify limpeza de ameaça \_ \_ \_ bem-sucedida** / **mpnotify eventos \_ \_ \_ com falha de limpeza de ameaça** .</span><span class="sxs-lookup"><span data-stu-id="f5aef-123">Resource information for the **MPNOTIFY\_CLEAN\_THREAT\_START**/**MPNOTIFY\_CLEAN\_THREAT\_SUCCEEDED**/**MPNOTIFY\_CLEAN\_THREAT\_FAILED** events.</span></span> <span data-ttu-id="f5aef-124">Consulte [**MPRESOURCE \_ info**](mpresource-info.md).</span><span class="sxs-lookup"><span data-stu-id="f5aef-124">See [**MPRESOURCE\_INFO**](mpresource-info.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f5aef-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f5aef-125">Requirements</span></span>



| <span data-ttu-id="f5aef-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5aef-126">Requirement</span></span> | <span data-ttu-id="f5aef-127">Valor</span><span class="sxs-lookup"><span data-stu-id="f5aef-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f5aef-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f5aef-128">Minimum supported client</span></span><br/> | <span data-ttu-id="f5aef-129">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="f5aef-129">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="f5aef-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f5aef-130">Minimum supported server</span></span><br/> | <span data-ttu-id="f5aef-131">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="f5aef-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f5aef-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f5aef-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="f5aef-133"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="f5aef-133"><dt>MpClient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5aef-134">Consulte também</span><span class="sxs-lookup"><span data-stu-id="f5aef-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5aef-135">**informações de MPRESOURCE \_**</span><span class="sxs-lookup"><span data-stu-id="f5aef-135">**MPRESOURCE\_INFO**</span></span>](mpresource-info.md)
</dt> <dt>

[<span data-ttu-id="f5aef-136">**\_sinalizador MPSTATUS**</span><span class="sxs-lookup"><span data-stu-id="f5aef-136">**MPSTATUS\_FLAG**</span></span>](mpstatus-flag.md)
</dt> <dt>

[<span data-ttu-id="f5aef-137">**\_ação MPTHREAT**</span><span class="sxs-lookup"><span data-stu-id="f5aef-137">**MPTHREAT\_ACTION**</span></span>](mpthreat-action.md)
</dt> </dl>

 

 





