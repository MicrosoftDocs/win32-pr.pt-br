---
description: Essa classe é a classe de tipo de evento para eventos de espera de término ALPC. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: 89a357dd-c217-4b55-994a-4252fa3cae1c
title: Classe ALPC_Unwait
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ALPC_Unwait
- ALPC_Unwait.Status
api_type:
- NA
api_location: ''
ms.openlocfilehash: f0846eae1ebb88e8892f1fe9b8dd07fd1be9d146
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501990"
---
# <a name="alpc_unwait-class"></a><span data-ttu-id="cdcc5-104">\_Classe de desesperação ALPC</span><span class="sxs-lookup"><span data-stu-id="cdcc5-104">ALPC\_Unwait class</span></span>

<span data-ttu-id="cdcc5-105">Essa classe é a classe de tipo de evento para eventos de espera de término ALPC.</span><span class="sxs-lookup"><span data-stu-id="cdcc5-105">This class is the event type class for ALPC end wait events.</span></span>

<span data-ttu-id="cdcc5-106">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="cdcc5-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="cdcc5-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cdcc5-107">Syntax</span></span>

``` syntax
[EventType(37), EventTypeName("ALPC-Unwait")]
class ALPC_Unwait : ALPC
{
  uint32 Status;
};
```

## <a name="members"></a><span data-ttu-id="cdcc5-108">Membros</span><span class="sxs-lookup"><span data-stu-id="cdcc5-108">Members</span></span>

<span data-ttu-id="cdcc5-109">A classe de **\_ desesperação ALPC** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="cdcc5-109">The **ALPC\_Unwait** class has these types of members:</span></span>

-   [<span data-ttu-id="cdcc5-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="cdcc5-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cdcc5-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="cdcc5-111">Properties</span></span>

<span data-ttu-id="cdcc5-112">A classe de **\_ desesperação ALPC** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="cdcc5-112">The **ALPC\_Unwait** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cdcc5-113">**Status**</span><span class="sxs-lookup"><span data-stu-id="cdcc5-113">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdcc5-114">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cdcc5-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cdcc5-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cdcc5-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cdcc5-116">Status da operação de espera.</span><span class="sxs-lookup"><span data-stu-id="cdcc5-116">Status from wait operation.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cdcc5-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cdcc5-117">Requirements</span></span>



| <span data-ttu-id="cdcc5-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="cdcc5-118">Requirement</span></span> | <span data-ttu-id="cdcc5-119">Valor</span><span class="sxs-lookup"><span data-stu-id="cdcc5-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="cdcc5-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cdcc5-120">Minimum supported client</span></span><br/> | <span data-ttu-id="cdcc5-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cdcc5-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="cdcc5-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cdcc5-122">Minimum supported server</span></span><br/> | <span data-ttu-id="cdcc5-123">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="cdcc5-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




