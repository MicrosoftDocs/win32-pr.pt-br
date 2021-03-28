---
description: Essa classe é a classe de tipo de evento para eventos de perfil de amostra. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: 75ea1e5e-2554-40bb-aa9d-c6d4942c5801
title: Classe SampledProfile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SampledProfile
- SampledProfile.InstructionPointer
- SampledProfile.ThreadId
- SampledProfile.Count
api_type:
- NA
api_location: ''
ms.openlocfilehash: 3d7a69eef1a2a7988569ffcd930b73a559e18d90
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968151"
---
# <a name="sampledprofile-class"></a><span data-ttu-id="2321f-104">Classe SampledProfile</span><span class="sxs-lookup"><span data-stu-id="2321f-104">SampledProfile class</span></span>

<span data-ttu-id="2321f-105">Essa classe é a classe de tipo de evento para eventos de perfil de amostra.</span><span class="sxs-lookup"><span data-stu-id="2321f-105">This class is the event type class for sampled profile events.</span></span>

<span data-ttu-id="2321f-106">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="2321f-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="2321f-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2321f-107">Syntax</span></span>

``` syntax
[EventType{46}, EventTypeName{"SampleProfile"}]
class SampledProfile : PerfInfo
{
  uint32 InstructionPointer;
  uint32 ThreadId;
  uint32 Count;
};
```

## <a name="members"></a><span data-ttu-id="2321f-108">Membros</span><span class="sxs-lookup"><span data-stu-id="2321f-108">Members</span></span>

<span data-ttu-id="2321f-109">A classe **SampledProfile** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="2321f-109">The **SampledProfile** class has these types of members:</span></span>

-   [<span data-ttu-id="2321f-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="2321f-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2321f-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="2321f-111">Properties</span></span>

<span data-ttu-id="2321f-112">A classe **SampledProfile** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="2321f-112">The **SampledProfile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2321f-113">**Count**</span><span class="sxs-lookup"><span data-stu-id="2321f-113">**Count**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2321f-114">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2321f-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2321f-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2321f-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2321f-116">Qualificadores: WmiDataId (3)</span><span class="sxs-lookup"><span data-stu-id="2321f-116">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="2321f-117">Não usado.</span><span class="sxs-lookup"><span data-stu-id="2321f-117">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="2321f-118">**InstructionPointer**</span><span class="sxs-lookup"><span data-stu-id="2321f-118">**InstructionPointer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2321f-119">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2321f-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2321f-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2321f-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2321f-121">Qualificadores: WmiDataId (1), ponteiro</span><span class="sxs-lookup"><span data-stu-id="2321f-121">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="2321f-122">Endereço da imagem que estava sendo executada no momento em que o processador foi amostrado.</span><span class="sxs-lookup"><span data-stu-id="2321f-122">Address of the image that was running at the time the processor was sampled.</span></span>

</dd> <dt>

<span data-ttu-id="2321f-123">**ThreadId**</span><span class="sxs-lookup"><span data-stu-id="2321f-123">**ThreadId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2321f-124">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2321f-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2321f-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2321f-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2321f-126">Qualificadores: WmiDataId (2)</span><span class="sxs-lookup"><span data-stu-id="2321f-126">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="2321f-127">Identificador de thread do thread que estava sendo executado no momento em que o processador foi amostrado.</span><span class="sxs-lookup"><span data-stu-id="2321f-127">Thread identifier of the thread that was running at the time the processor was sampled.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2321f-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="2321f-128">Remarks</span></span>

<span data-ttu-id="2321f-129">Esses eventos fornecem um perfil de execução de amostra.</span><span class="sxs-lookup"><span data-stu-id="2321f-129">These events provide a sampled execution profile.</span></span> <span data-ttu-id="2321f-130">O evento registra o que estava sendo executado no processador.</span><span class="sxs-lookup"><span data-stu-id="2321f-130">The event records what was being executed on the processor.</span></span> <span data-ttu-id="2321f-131">Você pode usar os eventos de imagem para identificar o módulo binário que contém essa instrução.</span><span class="sxs-lookup"><span data-stu-id="2321f-131">You can use the Image events to identify the binary module containing that instruction.</span></span> <span data-ttu-id="2321f-132">Você pode usar essas informações para produzir um perfil de execução para a duração do rastreamento.</span><span class="sxs-lookup"><span data-stu-id="2321f-132">You can then use this information to produce an execution profile for the duration of the trace.</span></span>

## <a name="requirements"></a><span data-ttu-id="2321f-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2321f-133">Requirements</span></span>



| <span data-ttu-id="2321f-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="2321f-134">Requirement</span></span> | <span data-ttu-id="2321f-135">Valor</span><span class="sxs-lookup"><span data-stu-id="2321f-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="2321f-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2321f-136">Minimum supported client</span></span><br/> | <span data-ttu-id="2321f-137">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2321f-137">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="2321f-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2321f-138">Minimum supported server</span></span><br/> | <span data-ttu-id="2321f-139">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2321f-139">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




