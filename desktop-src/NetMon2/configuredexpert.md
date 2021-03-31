---
description: A estrutura CONFIGUREDEXPERT associa um especialista aos seus dados de configuração.
ms.assetid: 96a6650b-6d6f-495e-83bb-385d44ff015d
title: Estrutura CONFIGUREDEXPERT (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CONFIGUREDEXPERT
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 3f3d40bf5d38c6b5151691a7d15bd93bef01eee5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104169707"
---
# <a name="configuredexpert-structure"></a><span data-ttu-id="113cb-103">Estrutura CONFIGUREDEXPERT</span><span class="sxs-lookup"><span data-stu-id="113cb-103">CONFIGUREDEXPERT structure</span></span>

<span data-ttu-id="113cb-104">A estrutura **CONFIGUREDEXPERT** associa um especialista aos seus dados de configuração.</span><span class="sxs-lookup"><span data-stu-id="113cb-104">The **CONFIGUREDEXPERT** structure associates an expert with its configuration data.</span></span>

## <a name="syntax"></a><span data-ttu-id="113cb-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="113cb-105">Syntax</span></span>


```C++
typedef struct {
  HEXPERT       hExpert;
  DWORD         StartupFlags;
  PEXPERTCONFIG pConfig;
} CONFIGUREDEXPERT, *PCONFIGUREDEXPERT;
```



## <a name="members"></a><span data-ttu-id="113cb-106">Membros</span><span class="sxs-lookup"><span data-stu-id="113cb-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="113cb-107">**hExpert**</span><span class="sxs-lookup"><span data-stu-id="113cb-107">**hExpert**</span></span>
</dt> <dd>

<span data-ttu-id="113cb-108">Lide com um especialista.</span><span class="sxs-lookup"><span data-stu-id="113cb-108">Handle to an expert.</span></span>

</dd> <dt>

<span data-ttu-id="113cb-109">**StartupFlags**</span><span class="sxs-lookup"><span data-stu-id="113cb-109">**StartupFlags**</span></span>
</dt> <dd>

<span data-ttu-id="113cb-110">Os valores do sinalizador de inicialização do especialista.</span><span class="sxs-lookup"><span data-stu-id="113cb-110">Startup flag values of the expert.</span></span>

</dd> <dt>

<span data-ttu-id="113cb-111">**pConfig**</span><span class="sxs-lookup"><span data-stu-id="113cb-111">**pConfig**</span></span>
</dt> <dd>

<span data-ttu-id="113cb-112">Ponteiro para uma estrutura [**EXPERTCONFIG**](expertconfig.md) .</span><span class="sxs-lookup"><span data-stu-id="113cb-112">Pointer to an [**EXPERTCONFIG**](expertconfig.md) structure.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="113cb-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="113cb-113">Requirements</span></span>



| <span data-ttu-id="113cb-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="113cb-114">Requirement</span></span> | <span data-ttu-id="113cb-115">Valor</span><span class="sxs-lookup"><span data-stu-id="113cb-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="113cb-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="113cb-116">Minimum supported client</span></span><br/> | <span data-ttu-id="113cb-117">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="113cb-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="113cb-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="113cb-118">Minimum supported server</span></span><br/> | <span data-ttu-id="113cb-119">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="113cb-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="113cb-120">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="113cb-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="113cb-121"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="113cb-121"><dt>Netmon.h</dt></span></span> </dl> |



 

 




