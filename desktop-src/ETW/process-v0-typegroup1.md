---
description: Essa classe é a classe de tipo de evento para eventos de processo. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: fcf2897d-32b4-42b9-892c-f0106687d3c2
title: Classe Process_V0_TypeGroup1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Process_V0_TypeGroup1
- Process_V0_TypeGroup1.ProcessId
- Process_V0_TypeGroup1.ParentId
- Process_V0_TypeGroup1.UserSID
- Process_V0_TypeGroup1.ImageFileName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 2889feb05bfc396f2c2018ca59d2cf46fba8ec13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967438"
---
# <a name="process_v0_typegroup1-class"></a><span data-ttu-id="9decc-104">\_Classe Process V0 \_ TypeGroup1</span><span class="sxs-lookup"><span data-stu-id="9decc-104">Process\_V0\_TypeGroup1 class</span></span>

<span data-ttu-id="9decc-105">Essa classe é a classe de tipo de evento para eventos de processo.</span><span class="sxs-lookup"><span data-stu-id="9decc-105">This class is the event type class for process events.</span></span>

<span data-ttu-id="9decc-106">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="9decc-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="9decc-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9decc-107">Syntax</span></span>

``` syntax
[EventType{1, 2, 3, 4}, EventTypeName{"Start", "End", "DCStart", "DCEnd"}]
class Process_V0_TypeGroup1 : Process_V0
{
  uint32 ProcessId;
  uint32 ParentId;
  object UserSID;
  string ImageFileName;
};
```

## <a name="members"></a><span data-ttu-id="9decc-108">Membros</span><span class="sxs-lookup"><span data-stu-id="9decc-108">Members</span></span>

<span data-ttu-id="9decc-109">A classe **process \_ V0 \_ TypeGroup1** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="9decc-109">The **Process\_V0\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="9decc-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="9decc-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9decc-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="9decc-111">Properties</span></span>

<span data-ttu-id="9decc-112">A classe **process \_ V0 \_ TypeGroup1** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="9decc-112">The **Process\_V0\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9decc-113">ImageFileName</span><span class="sxs-lookup"><span data-stu-id="9decc-113">ImageFileName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9decc-114">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9decc-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9decc-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9decc-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9decc-116">Qualificadores: WmiDataId (4), StringTermination ("NullTerminated")</span><span class="sxs-lookup"><span data-stu-id="9decc-116">Qualifiers: WmiDataId(4), StringTermination("NullTerminated")</span></span>
</dt> </dl>

<span data-ttu-id="9decc-117">Caminho para o arquivo executável do processo.</span><span class="sxs-lookup"><span data-stu-id="9decc-117">Path to the executable file of the process.</span></span>

</dd> <dt>

<span data-ttu-id="9decc-118">ParentId</span><span class="sxs-lookup"><span data-stu-id="9decc-118">ParentId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9decc-119">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9decc-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9decc-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9decc-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9decc-121">Qualificadores: WmiDataId (2), ponteiro</span><span class="sxs-lookup"><span data-stu-id="9decc-121">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="9decc-122">Identificador exclusivo do processo que cria um processo.</span><span class="sxs-lookup"><span data-stu-id="9decc-122">Unique identifier of the process that creates a process.</span></span> <span data-ttu-id="9decc-123">Os números de identificador de processo são reutilizados, portanto, eles identificam apenas um processo durante o tempo de vida desse processo.</span><span class="sxs-lookup"><span data-stu-id="9decc-123">Process identifier numbers are reused, so they only identify a process for the lifetime of that process.</span></span> <span data-ttu-id="9decc-124">É possível que o processo identificado pelo ParentProcessId seja encerrado; portanto, ParentProcessId pode não se referir a um processo em execução.</span><span class="sxs-lookup"><span data-stu-id="9decc-124">It is possible that the process identified by ParentProcessId is terminated, so ParentProcessId may not refer to a running process.</span></span> <span data-ttu-id="9decc-125">Também é possível que o ParentProcessId incorretamente faça referência a um processo que reutiliza um identificador de processo.</span><span class="sxs-lookup"><span data-stu-id="9decc-125">It is also possible that ParentProcessId incorrectly refers to a process that reuses a process identifier.</span></span>

</dd> <dt>

<span data-ttu-id="9decc-126">ProcessId</span><span class="sxs-lookup"><span data-stu-id="9decc-126">ProcessId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9decc-127">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9decc-127">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9decc-128">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9decc-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9decc-129">Qualificadores: WmiDataId (1), ponteiro</span><span class="sxs-lookup"><span data-stu-id="9decc-129">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="9decc-130">Identificador de processo global que você pode usar para identificar um processo.</span><span class="sxs-lookup"><span data-stu-id="9decc-130">Global process identifier that you can use to identify a process.</span></span> <span data-ttu-id="9decc-131">O valor é válido a partir do momento em que um processo é criado até ser encerrado.</span><span class="sxs-lookup"><span data-stu-id="9decc-131">The value is valid from the time a process is created until it is terminated.</span></span>

</dd> <dt>

<span data-ttu-id="9decc-132">UserSID</span><span class="sxs-lookup"><span data-stu-id="9decc-132">UserSID</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9decc-133">Tipo de dados: **objeto**</span><span class="sxs-lookup"><span data-stu-id="9decc-133">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="9decc-134">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9decc-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9decc-135">Qualificadores: WmiDataId (3), extensão ("Sid")</span><span class="sxs-lookup"><span data-stu-id="9decc-135">Qualifiers: WmiDataId(3), Extension("Sid")</span></span>
</dt> </dl>

<span data-ttu-id="9decc-136">SID (identificador de segurança) para o contexto do usuário no qual o evento ocorre.</span><span class="sxs-lookup"><span data-stu-id="9decc-136">Security identifier (SID) for the user context under which the event happens.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9decc-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9decc-137">Requirements</span></span>



| <span data-ttu-id="9decc-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="9decc-138">Requirement</span></span> | <span data-ttu-id="9decc-139">Valor</span><span class="sxs-lookup"><span data-stu-id="9decc-139">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="9decc-140">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9decc-140">Minimum supported client</span></span><br/> | <span data-ttu-id="9decc-141">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="9decc-141">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="9decc-142">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9decc-142">Minimum supported server</span></span><br/> | <span data-ttu-id="9decc-143">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9decc-143">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9decc-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="9decc-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9decc-145">**V0 de processo \_**</span><span class="sxs-lookup"><span data-stu-id="9decc-145">**Process\_V0**</span></span>](process-v0.md)
</dt> </dl>

 

 




