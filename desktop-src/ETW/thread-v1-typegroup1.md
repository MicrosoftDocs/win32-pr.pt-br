---
description: Essa classe é a classe de tipo de evento para eventos de início de thread. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: 412de56f-4f54-46e8-ab60-d47371247e79
title: Classe Thread_V1_TypeGroup1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Thread_V1_TypeGroup1
- Thread_V1_TypeGroup1.ProcessId
- Thread_V1_TypeGroup1.TThreadId
- Thread_V1_TypeGroup1.StackBase
- Thread_V1_TypeGroup1.StackLimit
- Thread_V1_TypeGroup1.UserStackBase
- Thread_V1_TypeGroup1.UserStackLimit
- Thread_V1_TypeGroup1.StartAddr
- Thread_V1_TypeGroup1.Win32StartAddr
- Thread_V1_TypeGroup1.WaitMode
api_type:
- NA
api_location: ''
ms.openlocfilehash: 13c419b417b614eb9022d1cb7c09a84ca705b3dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103921970"
---
# <a name="thread_v1_typegroup1-class"></a><span data-ttu-id="6fb8f-104">\_ \_ Classe TypeGroup1 de thread v1</span><span class="sxs-lookup"><span data-stu-id="6fb8f-104">Thread\_V1\_TypeGroup1 class</span></span>

<span data-ttu-id="6fb8f-105">Essa classe é a classe de tipo de evento para eventos de início de thread.</span><span class="sxs-lookup"><span data-stu-id="6fb8f-105">This class is the event type class for thread start events.</span></span>

<span data-ttu-id="6fb8f-106">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="6fb8f-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="6fb8f-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6fb8f-107">Syntax</span></span>

``` syntax
[EventType{1, 3}, EventTypeName{"Start", "DCStart"}]
class Thread_V1_TypeGroup1 : Thread_V1
{
  uint32 ProcessId;
  uint32 TThreadId;
  uint32 StackBase;
  uint32 StackLimit;
  uint32 UserStackBase;
  uint32 UserStackLimit;
  uint32 StartAddr;
  uint32 Win32StartAddr;
  sint8  WaitMode;
};
```

## <a name="members"></a><span data-ttu-id="6fb8f-108">Membros</span><span class="sxs-lookup"><span data-stu-id="6fb8f-108">Members</span></span>

<span data-ttu-id="6fb8f-109">A classe **thread \_ v1 \_ TypeGroup1** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="6fb8f-109">The **Thread\_V1\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="6fb8f-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="6fb8f-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6fb8f-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="6fb8f-111">Properties</span></span>

<span data-ttu-id="6fb8f-112">A classe **thread \_ v1 \_ TypeGroup1** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="6fb8f-112">The **Thread\_V1\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6fb8f-113">ProcessId</span><span class="sxs-lookup"><span data-stu-id="6fb8f-113">ProcessId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6fb8f-114">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6fb8f-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6fb8f-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6fb8f-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6fb8f-116">Qualificadores: WmiDataId (1)</span><span class="sxs-lookup"><span data-stu-id="6fb8f-116">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="6fb8f-117">Identificador de processo do thread envolvido no evento.</span><span class="sxs-lookup"><span data-stu-id="6fb8f-117">Process identifier of the thread involved in the event.</span></span>

<span data-ttu-id="6fb8f-118">**Windows Server 2003:** Contém o qualificador de formato ("x").</span><span class="sxs-lookup"><span data-stu-id="6fb8f-118">**Windows Server 2003:** Contains the Format("x") qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="6fb8f-119">StackBase</span><span class="sxs-lookup"><span data-stu-id="6fb8f-119">StackBase</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6fb8f-120">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6fb8f-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6fb8f-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6fb8f-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6fb8f-122">Qualificadores: WmiDataId (3), ponteiro</span><span class="sxs-lookup"><span data-stu-id="6fb8f-122">Qualifiers: WmiDataId(3), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="6fb8f-123">Endereço base da pilha do thread.</span><span class="sxs-lookup"><span data-stu-id="6fb8f-123">Base address of the thread's stack.</span></span>

</dd> <dt>

<span data-ttu-id="6fb8f-124">StackLimit</span><span class="sxs-lookup"><span data-stu-id="6fb8f-124">StackLimit</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6fb8f-125">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6fb8f-125">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6fb8f-126">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6fb8f-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6fb8f-127">Qualificadores: WmiDataId (4), ponteiro</span><span class="sxs-lookup"><span data-stu-id="6fb8f-127">Qualifiers: WmiDataId(4), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="6fb8f-128">Limite da pilha do thread.</span><span class="sxs-lookup"><span data-stu-id="6fb8f-128">Limit of the thread's stack.</span></span>

</dd> <dt>

<span data-ttu-id="6fb8f-129">StartAddr</span><span class="sxs-lookup"><span data-stu-id="6fb8f-129">StartAddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6fb8f-130">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6fb8f-130">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6fb8f-131">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6fb8f-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6fb8f-132">Qualificadores: WmiDataId (7), ponteiro</span><span class="sxs-lookup"><span data-stu-id="6fb8f-132">Qualifiers: WmiDataId(7), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="6fb8f-133">Endereço de memória no qual o rastreamento é iniciado.</span><span class="sxs-lookup"><span data-stu-id="6fb8f-133">Memory address at which the trace starts.</span></span>

</dd> <dt>

<span data-ttu-id="6fb8f-134">TThreadId</span><span class="sxs-lookup"><span data-stu-id="6fb8f-134">TThreadId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6fb8f-135">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6fb8f-135">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6fb8f-136">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6fb8f-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6fb8f-137">Qualificadores: WmiDataId (2)</span><span class="sxs-lookup"><span data-stu-id="6fb8f-137">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="6fb8f-138">Identificador de thread do thread envolvido no evento.</span><span class="sxs-lookup"><span data-stu-id="6fb8f-138">Thread identifier of the thread involved in the event.</span></span>

<span data-ttu-id="6fb8f-139">**Windows Server 2003:** Contém o qualificador de formato ("x").</span><span class="sxs-lookup"><span data-stu-id="6fb8f-139">**Windows Server 2003:** Contains the Format("x") qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="6fb8f-140">UserStackBase</span><span class="sxs-lookup"><span data-stu-id="6fb8f-140">UserStackBase</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6fb8f-141">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6fb8f-141">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6fb8f-142">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6fb8f-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6fb8f-143">Qualificadores: WmiDataId (5), ponteiro</span><span class="sxs-lookup"><span data-stu-id="6fb8f-143">Qualifiers: WmiDataId(5), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="6fb8f-144">Endereço base da pilha do modo de usuário do thread.</span><span class="sxs-lookup"><span data-stu-id="6fb8f-144">Base address of the thread's user-mode stack.</span></span>

</dd> <dt>

<span data-ttu-id="6fb8f-145">UserStackLimit</span><span class="sxs-lookup"><span data-stu-id="6fb8f-145">UserStackLimit</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6fb8f-146">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6fb8f-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6fb8f-147">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6fb8f-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6fb8f-148">Qualificadores: WmiDataId (6), ponteiro</span><span class="sxs-lookup"><span data-stu-id="6fb8f-148">Qualifiers: WmiDataId(6), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="6fb8f-149">Limite da pilha do modo de usuário do thread.</span><span class="sxs-lookup"><span data-stu-id="6fb8f-149">Limit of the thread's user-mode stack.</span></span>

</dd> <dt>

<span data-ttu-id="6fb8f-150">Waitmode</span><span class="sxs-lookup"><span data-stu-id="6fb8f-150">WaitMode</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6fb8f-151">Tipo de dados: **sint8**</span><span class="sxs-lookup"><span data-stu-id="6fb8f-151">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="6fb8f-152">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6fb8f-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6fb8f-153">Qualificadores: WmiDataId (9), formato ("c")</span><span class="sxs-lookup"><span data-stu-id="6fb8f-153">Qualifiers: WmiDataId(9), Format("c")</span></span>
</dt> </dl>

<span data-ttu-id="6fb8f-154">Não usado.</span><span class="sxs-lookup"><span data-stu-id="6fb8f-154">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="6fb8f-155">Win32StartAddr</span><span class="sxs-lookup"><span data-stu-id="6fb8f-155">Win32StartAddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6fb8f-156">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6fb8f-156">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6fb8f-157">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6fb8f-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6fb8f-158">Qualificadores: WmiDataId (8), ponteiro</span><span class="sxs-lookup"><span data-stu-id="6fb8f-158">Qualifiers: WmiDataId(8), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="6fb8f-159">Endereço inicial da função a ser executada por este thread.</span><span class="sxs-lookup"><span data-stu-id="6fb8f-159">Starting address of the function to be executed by this thread.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6fb8f-160">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6fb8f-160">Requirements</span></span>



| <span data-ttu-id="6fb8f-161">Requisito</span><span class="sxs-lookup"><span data-stu-id="6fb8f-161">Requirement</span></span> | <span data-ttu-id="6fb8f-162">Valor</span><span class="sxs-lookup"><span data-stu-id="6fb8f-162">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="6fb8f-163">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6fb8f-163">Minimum supported client</span></span><br/> | <span data-ttu-id="6fb8f-164">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6fb8f-164">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="6fb8f-165">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6fb8f-165">Minimum supported server</span></span><br/> | <span data-ttu-id="6fb8f-166">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6fb8f-166">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="6fb8f-167">Confira também</span><span class="sxs-lookup"><span data-stu-id="6fb8f-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6fb8f-168">**Thread \_ v1**</span><span class="sxs-lookup"><span data-stu-id="6fb8f-168">**Thread\_V1**</span></span>](thread-v1.md)
</dt> </dl>

 

 




