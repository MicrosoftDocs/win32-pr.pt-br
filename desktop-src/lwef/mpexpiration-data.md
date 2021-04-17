---
title: Estrutura de MPEXPIRATION_DATA (MpClient. h)
description: Notificação de status de expiração do produto.
ms.assetid: BF464FFD-16AE-4F46-83CD-E0355478180C
keywords:
- Recursos do ambiente Windows herdado da estrutura de MPEXPIRATION_DATA
- Ponteiro de estrutura de PMPEXPIRATION_DATA recursos de ambiente herdados do Windows
topic_type:
- apiref
api_name:
- MPEXPIRATION_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df5e417b1ce6b1d1f4c15d646b44b0ea6c1fade2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105751391"
---
# <a name="mpexpiration_data-structure"></a><span data-ttu-id="61413-105">\_Estrutura de dados MPEXPIRATION</span><span class="sxs-lookup"><span data-stu-id="61413-105">MPEXPIRATION\_DATA structure</span></span>

<span data-ttu-id="61413-106">Notificação de status de expiração do produto.</span><span class="sxs-lookup"><span data-stu-id="61413-106">Product expiration status notification.</span></span>

## <a name="syntax"></a><span data-ttu-id="61413-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="61413-107">Syntax</span></span>


```C++
typedef struct tagMPEXPIRATION_DATA {
  MP_EXPIRE_REASON       Reason;
  MP_EXPIRE_STATE_REPORT State;
} MPEXPIRATION_DATA, *PMPEXPIRATION_DATA;
```



## <a name="members"></a><span data-ttu-id="61413-108">Membros</span><span class="sxs-lookup"><span data-stu-id="61413-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="61413-109">**Motivo**</span><span class="sxs-lookup"><span data-stu-id="61413-109">**Reason**</span></span>
</dt> <dd>

<span data-ttu-id="61413-110">Tipo: **\_ \_ motivo de expiração do MP**</span><span class="sxs-lookup"><span data-stu-id="61413-110">Type: **MP\_EXPIRE\_REASON**</span></span>

</dd> <dd>

<span data-ttu-id="61413-111">Motivo da expiração.</span><span class="sxs-lookup"><span data-stu-id="61413-111">Expiration reason.</span></span> <span data-ttu-id="61413-112">Esse é um dos seguintes valores possíveis:</span><span class="sxs-lookup"><span data-stu-id="61413-112">This is one of the following possible values:</span></span>



| <span data-ttu-id="61413-113">Valor</span><span class="sxs-lookup"><span data-stu-id="61413-113">Value</span></span>                                                                                                                                                                                                                                | <span data-ttu-id="61413-114">Significado</span><span class="sxs-lookup"><span data-stu-id="61413-114">Meaning</span></span>                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------|
| <span id="MP_EXPIRED_UNKNOWN"></span><span id="mp_expired_unknown"></span><dl> <span data-ttu-id="61413-115"><dt>**MP \_ 0 de \_ desconhecido expirado**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="61413-115"><dt>**MP\_EXPIRED\_UNKNOWN**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="61413-116">Desconhecido.</span><span class="sxs-lookup"><span data-stu-id="61413-116">Unknown.</span></span><br/>    |
| <span id="MP_EXPIRED_EVAL"></span><span id="mp_expired_eval"></span><dl> <span data-ttu-id="61413-117"><dt>**MP \_ \_Avaliação expirada**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="61413-117"><dt>**MP\_EXPIRED\_EVAL**</dt> <dt>1</dt></span></span> </dl>          | <span data-ttu-id="61413-118">Período.</span><span class="sxs-lookup"><span data-stu-id="61413-118">Evaluation.</span></span><br/> |
| <span id="MP_EXPIRED_WAT"></span><span id="mp_expired_wat"></span><dl> <span data-ttu-id="61413-119"><dt>**MP \_ \_Wat 2 expirado**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="61413-119"><dt>**MP\_EXPIRED\_WAT**</dt> <dt>2</dt></span></span> </dl>             | <span data-ttu-id="61413-120">Wat.</span><span class="sxs-lookup"><span data-stu-id="61413-120">WAT.</span></span><br/>        |



 

</dd> <dt>

<span data-ttu-id="61413-121">**State**</span><span class="sxs-lookup"><span data-stu-id="61413-121">**State**</span></span>
</dt> <dd>

<span data-ttu-id="61413-122">Tipo: **\_ \_ \_ relatório de estado de expiração do PG**</span><span class="sxs-lookup"><span data-stu-id="61413-122">Type: **MP\_EXPIRE\_STATE\_REPORT**</span></span>

</dd> <dd>

<span data-ttu-id="61413-123">Estado de expiração.</span><span class="sxs-lookup"><span data-stu-id="61413-123">Expiration state.</span></span> <span data-ttu-id="61413-124">Esse é um dos seguintes valores possíveis:</span><span class="sxs-lookup"><span data-stu-id="61413-124">This is one of the following possible values:</span></span>



| <span data-ttu-id="61413-125">Valor</span><span class="sxs-lookup"><span data-stu-id="61413-125">Value</span></span>                                                                                                                                                                                                                                                                      | <span data-ttu-id="61413-126">Significado</span><span class="sxs-lookup"><span data-stu-id="61413-126">Meaning</span></span>                   |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------|
| <span id="MP_EXPIRE_STATE_REPORT_UNKNOWN"></span><span id="mp_expire_state_report_unknown"></span><dl> <span data-ttu-id="61413-127"><dt>**MP \_ Relatório de estado de EXPIRAção \_ \_ \_ desconhecido**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="61413-127"><dt>**MP\_EXPIRE\_STATE\_REPORT\_UNKNOWN**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="61413-128">Estado desconhecido.</span><span class="sxs-lookup"><span data-stu-id="61413-128">State unknown.</span></span><br/> |
| <span id="MP_EXPIRE_STATE_REPORT_VALID"></span><span id="mp_expire_state_report_valid"></span><dl> <span data-ttu-id="61413-129"><dt>**MP \_ Relatório de \_ estado expirado \_ \_ válido**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="61413-129"><dt>**MP\_EXPIRE\_STATE\_REPORT\_VALID**</dt> <dt>1</dt></span></span> </dl>       | <span data-ttu-id="61413-130">Sem expiração.</span><span class="sxs-lookup"><span data-stu-id="61413-130">No expiration.</span></span><br/> |
| <span id="MP_EXPIRE_STATE_REPORT_WARNING"></span><span id="mp_expire_state_report_warning"></span><dl> <span data-ttu-id="61413-131"><dt>**MP \_ \_ \_ \_ Aviso de expiração do relatório de estado**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="61413-131"><dt>**MP\_EXPIRE\_STATE\_REPORT\_WARNING**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="61413-132">Quase vencido.</span><span class="sxs-lookup"><span data-stu-id="61413-132">Near expired.</span></span><br/>  |
| <span id="MP_EXPIRE_STATE_REPORT_EXPIRED"></span><span id="mp_expire_state_report_expired"></span><dl> <span data-ttu-id="61413-133"><dt>**MP \_ EXPIRAr \_ \_ relatório de \_ estado**</dt> expirado <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="61413-133"><dt>**MP\_EXPIRE\_STATE\_REPORT\_EXPIRED**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="61413-134">Vencer.</span><span class="sxs-lookup"><span data-stu-id="61413-134">Expired.</span></span><br/>       |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="61413-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="61413-135">Requirements</span></span>



| <span data-ttu-id="61413-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="61413-136">Requirement</span></span> | <span data-ttu-id="61413-137">Valor</span><span class="sxs-lookup"><span data-stu-id="61413-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="61413-138">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="61413-138">Minimum supported client</span></span><br/> | <span data-ttu-id="61413-139">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="61413-139">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="61413-140">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="61413-140">Minimum supported server</span></span><br/> | <span data-ttu-id="61413-141">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="61413-141">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="61413-142">parâmetro</span><span class="sxs-lookup"><span data-stu-id="61413-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="61413-143"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="61413-143"><dt>MpClient.h</dt></span></span> </dl> |



 

 





