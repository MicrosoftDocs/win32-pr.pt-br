---
title: Estrutura de MPCOMPONENT_STATUS (MpClient. h)
description: Informações de status do componente.
ms.assetid: 0E589E52-A204-425C-880B-CF13C16893F3
keywords:
- Recursos do ambiente Windows herdado da estrutura de MPCOMPONENT_STATUS
- Ponteiro de estrutura de PMPCOMPONENT_STATUS recursos de ambiente herdados do Windows
topic_type:
- apiref
api_name:
- MPCOMPONENT_STATUS
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2923136d2599440bc6ccfe863af9795f7d7ff96
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644530"
---
# <a name="mpcomponent_status-structure"></a><span data-ttu-id="618ee-105">Estrutura de status do MPCOMPONENT \_</span><span class="sxs-lookup"><span data-stu-id="618ee-105">MPCOMPONENT\_STATUS structure</span></span>

<span data-ttu-id="618ee-106">Informações de status do componente.</span><span class="sxs-lookup"><span data-stu-id="618ee-106">Component status information.</span></span>

## <a name="syntax"></a><span data-ttu-id="618ee-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="618ee-107">Syntax</span></span>


```C++
typedef struct tagMPCOMPONENT_STATUS {
  BOOL    fEnable;
  HRESULT hResult;
} MPCOMPONENT_STATUS, *PMPCOMPONENT_STATUS;
```



## <a name="members"></a><span data-ttu-id="618ee-108">Membros</span><span class="sxs-lookup"><span data-stu-id="618ee-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="618ee-109">**fEnable**</span><span class="sxs-lookup"><span data-stu-id="618ee-109">**fEnable**</span></span>
</dt> <dd>

<span data-ttu-id="618ee-110">Tipo: **bool**</span><span class="sxs-lookup"><span data-stu-id="618ee-110">Type: **BOOL**</span></span>

</dd> <dd>

<span data-ttu-id="618ee-111">Status do componente.</span><span class="sxs-lookup"><span data-stu-id="618ee-111">Status for the component.</span></span>

</dd> <dt>

<span data-ttu-id="618ee-112">**Resultado**</span><span class="sxs-lookup"><span data-stu-id="618ee-112">**hResult**</span></span>
</dt> <dd>

<span data-ttu-id="618ee-113">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="618ee-113">Type: **HRESULT**</span></span>

</dd> <dd>

<span data-ttu-id="618ee-114">Código de êxito ou de falha associado ao status.</span><span class="sxs-lookup"><span data-stu-id="618ee-114">Success or failure code associated with the status.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="618ee-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="618ee-115">Requirements</span></span>



| <span data-ttu-id="618ee-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="618ee-116">Requirement</span></span> | <span data-ttu-id="618ee-117">Valor</span><span class="sxs-lookup"><span data-stu-id="618ee-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="618ee-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="618ee-118">Minimum supported client</span></span><br/> | <span data-ttu-id="618ee-119">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="618ee-119">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="618ee-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="618ee-120">Minimum supported server</span></span><br/> | <span data-ttu-id="618ee-121">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="618ee-121">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="618ee-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="618ee-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="618ee-123"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="618ee-123"><dt>MpClient.h</dt></span></span> </dl> |



 

 





