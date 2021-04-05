---
title: Estrutura de MPSAMPLE_DATA (MpClient. h)
description: Dados de notificação passados para a função de retorno de chamada de envio de exemplo.
ms.assetid: 58F348C6-411D-4545-9D4D-A80095FD139B
keywords:
- Recursos do ambiente Windows herdado da estrutura de MPSAMPLE_DATA
- Ponteiro de estrutura de PMPSAMPLE_DATA recursos de ambiente herdados do Windows
topic_type:
- apiref
api_name:
- MPSAMPLE_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24a894638465c0362069b8fdcbacddf98bfdd2c1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086428"
---
# <a name="mpsample_data-structure"></a><span data-ttu-id="e7330-105">\_Estrutura de dados MPSAMPLE</span><span class="sxs-lookup"><span data-stu-id="e7330-105">MPSAMPLE\_DATA structure</span></span>

<span data-ttu-id="e7330-106">Dados de notificação passados para a função de retorno de chamada de envio de exemplo.</span><span class="sxs-lookup"><span data-stu-id="e7330-106">Notification data passed to the sample submission callback function.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7330-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e7330-107">Syntax</span></span>


```C++
typedef struct tagMPSAMPLE_DATA {
  DWORD dwSampleIndex;
} MPSAMPLE_DATA, *PMPSAMPLE_DATA;
```



## <a name="members"></a><span data-ttu-id="e7330-108">Membros</span><span class="sxs-lookup"><span data-stu-id="e7330-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="e7330-109">**dwSampleIndex**</span><span class="sxs-lookup"><span data-stu-id="e7330-109">**dwSampleIndex**</span></span>
</dt> <dd>

<span data-ttu-id="e7330-110">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="e7330-110">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="e7330-111">Índice do item de exemplo para o qual o status de envio é relatado.</span><span class="sxs-lookup"><span data-stu-id="e7330-111">Index of the sample item for which the submission status is reported.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e7330-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e7330-112">Requirements</span></span>



| <span data-ttu-id="e7330-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="e7330-113">Requirement</span></span> | <span data-ttu-id="e7330-114">Valor</span><span class="sxs-lookup"><span data-stu-id="e7330-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e7330-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e7330-115">Minimum supported client</span></span><br/> | <span data-ttu-id="e7330-116">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="e7330-116">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="e7330-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e7330-117">Minimum supported server</span></span><br/> | <span data-ttu-id="e7330-118">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="e7330-118">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e7330-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e7330-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="e7330-120"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="e7330-120"><dt>MpClient.h</dt></span></span> </dl> |



 

 





