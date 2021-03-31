---
title: Enumeração de MPSCAN_TYPE (MpClient. h)
description: Tipo de verificação executada.
ms.assetid: 980A80FD-FF02-4338-B7FB-DAA141F65E89
keywords:
- Recursos do ambiente Windows herdado de enumeração de MPSCAN_TYPE
- PMPSCAN_TYPE recursos de ambiente herdados do ponteiro de enumeração do Windows
topic_type:
- apiref
api_name:
- MPSCAN_TYPE
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9eb89137dc9cfe5b8a4ff1f44a7a101239aa3a22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644308"
---
# <a name="mpscan_type-enumeration"></a><span data-ttu-id="d1ea5-105">\_Enumeração de tipo MPSCAN</span><span class="sxs-lookup"><span data-stu-id="d1ea5-105">MPSCAN\_TYPE enumeration</span></span>

<span data-ttu-id="d1ea5-106">Tipo de verificação executada.</span><span class="sxs-lookup"><span data-stu-id="d1ea5-106">Type of scan performed.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1ea5-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="d1ea5-107">Syntax</span></span>


```C++
typedef enum tagMPSCAN_TYPE { 
  MPSCAN_TYPE_UNKNOWN   = 0,
  MPSCAN_TYPE_QUICK     = 1,
  MPSCAN_TYPE_FULL      = 2,
  MPSCAN_TYPE_RESOURCE  = 3,
  MPSCAN_TYPE_MAXVALUE  = 3
} MPSCAN_TYPE, *PMPSCAN_TYPE;
```



## <a name="constants"></a><span data-ttu-id="d1ea5-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="d1ea5-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="d1ea5-109"><span id="MPSCAN_TYPE_UNKNOWN"></span><span id="mpscan_type_unknown"></span>**tipo de MPSCAN \_ \_ desconhecido**</span><span class="sxs-lookup"><span data-stu-id="d1ea5-109"><span id="MPSCAN_TYPE_UNKNOWN"></span><span id="mpscan_type_unknown"></span>**MPSCAN\_TYPE\_UNKNOWN**</span></span>
</dt> <dd>

<span data-ttu-id="d1ea5-110">Somente para uso interno.</span><span class="sxs-lookup"><span data-stu-id="d1ea5-110">Internal use only.</span></span>

</dd> <dt>

<span data-ttu-id="d1ea5-111"><span id="MPSCAN_TYPE_QUICK"></span><span id="mpscan_type_quick"></span>**MPSCAN \_ tipo \_ rápido**</span><span class="sxs-lookup"><span data-stu-id="d1ea5-111"><span id="MPSCAN_TYPE_QUICK"></span><span id="mpscan_type_quick"></span>**MPSCAN\_TYPE\_QUICK**</span></span>
</dt> <dd>

<span data-ttu-id="d1ea5-112">Verifica os processos em execução e vários pontos de ASEP no sistema em que o malware normalmente se oculta.</span><span class="sxs-lookup"><span data-stu-id="d1ea5-112">Scans running processes and various ASEP points in the system where malware typically hides.</span></span>

</dd> <dt>

<span data-ttu-id="d1ea5-113"><span id="MPSCAN_TYPE_FULL"></span><span id="mpscan_type_full"></span>**MPSCAN \_ tipo \_ completo**</span><span class="sxs-lookup"><span data-stu-id="d1ea5-113"><span id="MPSCAN_TYPE_FULL"></span><span id="mpscan_type_full"></span>**MPSCAN\_TYPE\_FULL**</span></span>
</dt> <dd>

<span data-ttu-id="d1ea5-114">Executa uma verificação rápida seguida da verificação de todas as unidades fixas do sistema.</span><span class="sxs-lookup"><span data-stu-id="d1ea5-114">Performs a quick scan followed by scan of all fixed drives of the system.</span></span>

</dd> <dt>

<span data-ttu-id="d1ea5-115"><span id="MPSCAN_TYPE_RESOURCE"></span><span id="mpscan_type_resource"></span>**\_recurso de tipo MPSCAN \_**</span><span class="sxs-lookup"><span data-stu-id="d1ea5-115"><span id="MPSCAN_TYPE_RESOURCE"></span><span id="mpscan_type_resource"></span>**MPSCAN\_TYPE\_RESOURCE**</span></span>
</dt> <dd>

<span data-ttu-id="d1ea5-116">Examina recursos específicos, como arquivos ou pastas.</span><span class="sxs-lookup"><span data-stu-id="d1ea5-116">Scans specific resources, such as files or folders.</span></span>

</dd> <dt>

<span data-ttu-id="d1ea5-117"><span id="MPSCAN_TYPE_MAXVALUE"></span><span id="mpscan_type_maxvalue"></span>**tipo de MPSCAN \_ \_ MaxValue**</span><span class="sxs-lookup"><span data-stu-id="d1ea5-117"><span id="MPSCAN_TYPE_MAXVALUE"></span><span id="mpscan_type_maxvalue"></span>**MPSCAN\_TYPE\_MAXVALUE**</span></span>
</dt> <dd>

<span data-ttu-id="d1ea5-118">Valor máximo possível.</span><span class="sxs-lookup"><span data-stu-id="d1ea5-118">Maximum value possible.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d1ea5-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d1ea5-119">Requirements</span></span>



| <span data-ttu-id="d1ea5-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="d1ea5-120">Requirement</span></span> | <span data-ttu-id="d1ea5-121">Valor</span><span class="sxs-lookup"><span data-stu-id="d1ea5-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d1ea5-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d1ea5-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d1ea5-123">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="d1ea5-123">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="d1ea5-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d1ea5-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d1ea5-125">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="d1ea5-125">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d1ea5-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d1ea5-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="d1ea5-127"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="d1ea5-127"><dt>MpClient.h</dt></span></span> </dl> |



 

 





