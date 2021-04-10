---
title: Estrutura de MPENDOFLIFE_DATA (MpClient. h)
description: '\ 0034; Fim da vida útil \ 0034; dados de notificação.'
ms.assetid: 00C2E707-9034-4BBC-99CF-3DFA4B8C08D9
keywords:
- Recursos do ambiente Windows herdado da estrutura de MPENDOFLIFE_DATA
- Ponteiro de estrutura de PMPENDOFLIFE_DATA recursos de ambiente herdados do Windows
topic_type:
- apiref
api_name:
- MPENDOFLIFE_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e209b9b35a089523815c353e8a750152bf4af75
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085946"
---
# <a name="mpendoflife_data-structure"></a><span data-ttu-id="79662-105">\_Estrutura de dados MPENDOFLIFE</span><span class="sxs-lookup"><span data-stu-id="79662-105">MPENDOFLIFE\_DATA structure</span></span>

<span data-ttu-id="79662-106">Dados de notificação "fim da vida útil".</span><span class="sxs-lookup"><span data-stu-id="79662-106">"End of life" notification data.</span></span>

## <a name="syntax"></a><span data-ttu-id="79662-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="79662-107">Syntax</span></span>


```C++
typedef struct tagMPENDOFLIFE_DATA {
  FILETIME ftSignatureExpiry;
  FILETIME ftPlatformExpiry;
  BOOL     fAdminControlled;
  BOOL     fEndOfLifeImpendingOrPast;
} MPENDOFLIFE_DATA, *PMPENDOFLIFE_DATA;
```



## <a name="members"></a><span data-ttu-id="79662-108">Membros</span><span class="sxs-lookup"><span data-stu-id="79662-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="79662-109">**ftSignatureExpiry**</span><span class="sxs-lookup"><span data-stu-id="79662-109">**ftSignatureExpiry**</span></span>
</dt> <dd>

<span data-ttu-id="79662-110">Tipo: **FILETIME**</span><span class="sxs-lookup"><span data-stu-id="79662-110">Type: **FILETIME**</span></span>

</dd> <dd>

<span data-ttu-id="79662-111">Hora em que a assinatura expira.</span><span class="sxs-lookup"><span data-stu-id="79662-111">Time when the signature expires.</span></span>

</dd> <dt>

<span data-ttu-id="79662-112">**ftPlatformExpiry**</span><span class="sxs-lookup"><span data-stu-id="79662-112">**ftPlatformExpiry**</span></span>
</dt> <dd>

<span data-ttu-id="79662-113">Tipo: **FILETIME**</span><span class="sxs-lookup"><span data-stu-id="79662-113">Type: **FILETIME**</span></span>

</dd> <dd>

<span data-ttu-id="79662-114">Hora em que a plataforma expira.</span><span class="sxs-lookup"><span data-stu-id="79662-114">Time when the platform expires.</span></span>

</dd> <dt>

<span data-ttu-id="79662-115">**fAdminControlled**</span><span class="sxs-lookup"><span data-stu-id="79662-115">**fAdminControlled**</span></span>
</dt> <dd>

<span data-ttu-id="79662-116">Tipo: **bool**</span><span class="sxs-lookup"><span data-stu-id="79662-116">Type: **BOOL**</span></span>

</dd> <dd>

<span data-ttu-id="79662-117">True se o administrador que controla a política para mostrar a notificação.</span><span class="sxs-lookup"><span data-stu-id="79662-117">True if the administrator controlling the policy for showing the notification.</span></span> <span data-ttu-id="79662-118">Se definido, isso informa a interface do usuário para não mostrar a notificação de EOL.</span><span class="sxs-lookup"><span data-stu-id="79662-118">If set, this tells the UI to not show the EOL notification.</span></span>

</dd> <dt>

<span data-ttu-id="79662-119">**fEndOfLifeImpendingOrPast**</span><span class="sxs-lookup"><span data-stu-id="79662-119">**fEndOfLifeImpendingOrPast**</span></span>
</dt> <dd>

<span data-ttu-id="79662-120">Tipo: **bool**</span><span class="sxs-lookup"><span data-stu-id="79662-120">Type: **BOOL**</span></span>

</dd> <dd>

<span data-ttu-id="79662-121">True se "End of Life" estiver pendente ou passado.</span><span class="sxs-lookup"><span data-stu-id="79662-121">True if "End of Life" is pending or past.</span></span> <span data-ttu-id="79662-122">Se false, a interface do usuário e os clientes podem limpar quaisquer Estados relacionados a EOL.</span><span class="sxs-lookup"><span data-stu-id="79662-122">If false, UI and clients can clear any EOL related states.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="79662-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="79662-123">Requirements</span></span>



| <span data-ttu-id="79662-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="79662-124">Requirement</span></span> | <span data-ttu-id="79662-125">Valor</span><span class="sxs-lookup"><span data-stu-id="79662-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="79662-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="79662-126">Minimum supported client</span></span><br/> | <span data-ttu-id="79662-127">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="79662-127">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="79662-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="79662-128">Minimum supported server</span></span><br/> | <span data-ttu-id="79662-129">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="79662-129">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="79662-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="79662-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="79662-131"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="79662-131"><dt>MpClient.h</dt></span></span> </dl> |



 

 





