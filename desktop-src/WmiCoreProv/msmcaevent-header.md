---
description: Representa o cabeçalho comum que todas as classes MSMCAEvent usam. Essa classe está disponível somente em sistemas Windows de 64 bits.
ms.assetid: ff20522c-f805-47dc-bef2-4176211de698
title: Classe MSMCAEvent_Header
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAEvent_Header
- MSMCAEvent_Header.AdditionalErrors
- MSMCAEvent_Header.Cpu
- MSMCAEvent_Header.ErrorSeverity
- MSMCAEvent_Header.RecordId
- MSMCAEvent_Header.Type
- MSMCAEvent_Header.LogToEventlog
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: 426f943014f3b6cfbdba5a25d331c0ea621048cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105784956"
---
# <a name="msmcaevent_header-class"></a><span data-ttu-id="74613-104">\_Classe de cabeçalho MSMCAEvent</span><span class="sxs-lookup"><span data-stu-id="74613-104">MSMCAEvent\_Header class</span></span>

<span data-ttu-id="74613-105">A classe de **\_ cabeçalho MSMCAEvent** representa o cabeçalho comum que todas as [classes MSMCA](msmca-classes.md) usam.</span><span class="sxs-lookup"><span data-stu-id="74613-105">The **MSMCAEvent\_Header** class represents the common header that all [MSMCA classes](msmca-classes.md) use.</span></span> <span data-ttu-id="74613-106">Os arquivos de cabeçalho são usados para que o código C e C++ possa ter uma estrutura de dados que descreva o cabeçalho comum para todos os eventos.</span><span class="sxs-lookup"><span data-stu-id="74613-106">The header files are used so that C and C++ code can have a data structure that describes the common header for all events.</span></span> <span data-ttu-id="74613-107">Essa classe é reservada para uso interno.</span><span class="sxs-lookup"><span data-stu-id="74613-107">This class is reserved for internal use.</span></span> <span data-ttu-id="74613-108">Essa classe está disponível somente em sistemas Windows de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="74613-108">This class is available only in 64-bit Windows systems.</span></span>

<span data-ttu-id="74613-109">A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="74613-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="74613-110">As propriedades e os métodos estão em ordem alfabética, não em ordem de MOF.</span><span class="sxs-lookup"><span data-stu-id="74613-110">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="74613-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="74613-111">Syntax</span></span>

``` syntax
class MSMCAEvent_Header
{
  uint32 AdditionalErrors;
  uint32 Cpu;
  uint8  ErrorSeverity;
  uint64 RecordId;
  uint32 Type;
  uint32 LogToEventlog;
};
```

## <a name="members"></a><span data-ttu-id="74613-112">Membros</span><span class="sxs-lookup"><span data-stu-id="74613-112">Members</span></span>

<span data-ttu-id="74613-113">A classe de **\_ cabeçalho MSMCAEvent** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="74613-113">The **MSMCAEvent\_Header** class has these types of members:</span></span>

-   [<span data-ttu-id="74613-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="74613-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="74613-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="74613-115">Properties</span></span>

<span data-ttu-id="74613-116">A classe de **\_ cabeçalho MSMCAEvent** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="74613-116">The **MSMCAEvent\_Header** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="74613-117">**AdditionalErrors**</span><span class="sxs-lookup"><span data-stu-id="74613-117">**AdditionalErrors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74613-118">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="74613-118">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="74613-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="74613-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74613-120">Número de erros adicionais no registro MCA.</span><span class="sxs-lookup"><span data-stu-id="74613-120">Number of additional errors in the MCA record.</span></span>

</dd> <dt>

<span data-ttu-id="74613-121">**CPUs**</span><span class="sxs-lookup"><span data-stu-id="74613-121">**Cpu**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74613-122">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="74613-122">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="74613-123">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="74613-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74613-124">CPU que relata o erro.</span><span class="sxs-lookup"><span data-stu-id="74613-124">CPU that reports the error.</span></span> <span data-ttu-id="74613-125">Essa propriedade se aplica somente a um sistema multiprocessador no qual o primeiro processador recebe o número 0, o segundo processador recebe o número 1 e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="74613-125">This property only applies to a multiprocessor system in which the first processor is assigned the number 0, the second processor is assigned the number 1, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="74613-126">**ErrorSeverity**</span><span class="sxs-lookup"><span data-stu-id="74613-126">**ErrorSeverity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74613-127">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="74613-127">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="74613-128">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="74613-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74613-129">Nível de severidade do erro relatado.</span><span class="sxs-lookup"><span data-stu-id="74613-129">Severity level of the error reported.</span></span>



| <span data-ttu-id="74613-130">Valor</span><span class="sxs-lookup"><span data-stu-id="74613-130">Value</span></span>                                                                                                | <span data-ttu-id="74613-131">Significado</span><span class="sxs-lookup"><span data-stu-id="74613-131">Meaning</span></span>                |
|------------------------------------------------------------------------------------------------------|------------------------|
| <span id="0"></span><dl> <span data-ttu-id="74613-132"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="74613-132"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="74613-133">Recuperado</span><span class="sxs-lookup"><span data-stu-id="74613-133">Recoverable</span></span><br/> |
| <span id="1"></span><dl> <span data-ttu-id="74613-134"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="74613-134"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="74613-135">Fatais</span><span class="sxs-lookup"><span data-stu-id="74613-135">Fatal</span></span><br/>       |
| <span id="2"></span><dl> <span data-ttu-id="74613-136"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="74613-136"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="74613-137">Corrigível</span><span class="sxs-lookup"><span data-stu-id="74613-137">Correctable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="74613-138">**LogToEventlog**</span><span class="sxs-lookup"><span data-stu-id="74613-138">**LogToEventlog**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74613-139">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="74613-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="74613-140">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="74613-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74613-141">Se for 0 (zero), esse evento não será registrado no log de eventos do sistema.</span><span class="sxs-lookup"><span data-stu-id="74613-141">If 0 (zero) then this event is not logged to the system event log.</span></span>

</dd> <dt>

<span data-ttu-id="74613-142">**RecordId**</span><span class="sxs-lookup"><span data-stu-id="74613-142">**RecordId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74613-143">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="74613-143">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="74613-144">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="74613-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74613-145">Identificador de registro do registro de erro para este erro.</span><span class="sxs-lookup"><span data-stu-id="74613-145">Record identifier of the error record for this error.</span></span>

<span data-ttu-id="74613-146">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="74613-146">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="74613-147">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="74613-147">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74613-148">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="74613-148">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="74613-149">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="74613-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74613-150">Tipo de mensagem de log de eventos.</span><span class="sxs-lookup"><span data-stu-id="74613-150">Type of event log message.</span></span> <span data-ttu-id="74613-151">Essas mensagens correspondem aos códigos de mensagem de log de eventos usados para inserir mensagens de log de eventos pelo provedor de consumidor do log de eventos do Windows quando ele recebe um dos eventos.</span><span class="sxs-lookup"><span data-stu-id="74613-151">These messages correspond to the event log message codes used to insert event log messages by the Windows event log consumer provider when it receives one of the events.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="74613-152">Requisitos</span><span class="sxs-lookup"><span data-stu-id="74613-152">Requirements</span></span>



| <span data-ttu-id="74613-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="74613-153">Requirement</span></span> | <span data-ttu-id="74613-154">Valor</span><span class="sxs-lookup"><span data-stu-id="74613-154">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="74613-155">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="74613-155">Minimum supported client</span></span><br/> | <span data-ttu-id="74613-156">Windows XP</span><span class="sxs-lookup"><span data-stu-id="74613-156">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="74613-157">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="74613-157">Minimum supported server</span></span><br/> | <span data-ttu-id="74613-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="74613-158">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="74613-159">Namespace</span><span class="sxs-lookup"><span data-stu-id="74613-159">Namespace</span></span><br/>                | <span data-ttu-id="74613-160">\\WMI raiz</span><span class="sxs-lookup"><span data-stu-id="74613-160">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="74613-161">MOF</span><span class="sxs-lookup"><span data-stu-id="74613-161">MOF</span></span><br/>                      | <dl> <span data-ttu-id="74613-162"><dt>Wmicore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="74613-162"><dt>Wmicore.mof</dt></span></span> </dl> |
| <span data-ttu-id="74613-163">DLL</span><span class="sxs-lookup"><span data-stu-id="74613-163">DLL</span></span><br/>                      | <dl> <span data-ttu-id="74613-164"><dt>Wmiprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="74613-164"><dt>Wmiprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="74613-165">Confira também</span><span class="sxs-lookup"><span data-stu-id="74613-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74613-166">Classes MSMCA</span><span class="sxs-lookup"><span data-stu-id="74613-166">MSMCA Classes</span></span>](msmca-classes.md)
</dt> <dt>

[<span data-ttu-id="74613-167">Classes WMI C++</span><span class="sxs-lookup"><span data-stu-id="74613-167">WMI C++ Classes</span></span>](/windows/desktop/WmiSdk/wmi-c-classes)
</dt> </dl>

 

