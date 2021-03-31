---
title: Classe Win32_SessionBrokerTargetEvent
description: Representa uma alteração em um destino de agente de sessão.
ms.assetid: ee3ae0ed-eb8b-4777-9b9e-0e50722cf52a
ms.tgt_platform: multiple
keywords:
- Classe de Win32_SessionBrokerTargetEvent Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de Win32_SessionBrokerTargetEvent classe, descrita
topic_type:
- apiref
api_name:
- Win32_SessionBrokerTargetEvent
- Win32_SessionBrokerTargetEvent.SECURITY_DESCRIPTOR
- Win32_SessionBrokerTargetEvent.TIME_CREATED
- Win32_SessionBrokerTargetEvent.ChangeType
- Win32_SessionBrokerTargetEvent.PluginName
- Win32_SessionBrokerTargetEvent.TargetName
- Win32_SessionBrokerTargetEvent.FarmName
- Win32_SessionBrokerTargetEvent.Guid
- Win32_SessionBrokerTargetEvent.Environment
api_location:
- TssdWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d7f1cf6aab1c4497ce85cb93318c9ca79368853
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644450"
---
# <a name="win32_sessionbrokertargetevent-class"></a><span data-ttu-id="4ce83-105">\_Classe Win32 SessionBrokerTargetEvent</span><span class="sxs-lookup"><span data-stu-id="4ce83-105">Win32\_SessionBrokerTargetEvent class</span></span>

<span data-ttu-id="4ce83-106">Representa uma alteração em um destino de agente de sessão.</span><span class="sxs-lookup"><span data-stu-id="4ce83-106">Represents a change to a session broker target.</span></span>

<span data-ttu-id="4ce83-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="4ce83-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ce83-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4ce83-108">Syntax</span></span>

``` syntax
[AMENDMENT]
class Win32_SessionBrokerTargetEvent : __ExtrinsicEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  uint64 TIME_CREATED;
  uint32 ChangeType;
  string PluginName;
  string TargetName;
  string FarmName;
  string Guid;
  string Environment;
};
```

## <a name="members"></a><span data-ttu-id="4ce83-109">Membros</span><span class="sxs-lookup"><span data-stu-id="4ce83-109">Members</span></span>

<span data-ttu-id="4ce83-110">A classe **Win32 \_ SessionBrokerTargetEvent** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="4ce83-110">The **Win32\_SessionBrokerTargetEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="4ce83-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="4ce83-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4ce83-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="4ce83-112">Properties</span></span>

<span data-ttu-id="4ce83-113">A classe **Win32 \_ SessionBrokerTargetEvent** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="4ce83-113">The **Win32\_SessionBrokerTargetEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4ce83-114">**ChangeType**</span><span class="sxs-lookup"><span data-stu-id="4ce83-114">**ChangeType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ce83-115">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4ce83-115">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4ce83-116">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4ce83-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4ce83-117">Especifica a alteração que ocorreu.</span><span class="sxs-lookup"><span data-stu-id="4ce83-117">Specifies the change that occurred.</span></span> <span data-ttu-id="4ce83-118">Isso pode ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="4ce83-118">This can be one of the following values.</span></span>

<dt>

<span data-ttu-id="4ce83-119">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="4ce83-119">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="4ce83-120">O tipo de alteração não foi especificado.</span><span class="sxs-lookup"><span data-stu-id="4ce83-120">The type of change is not specified.</span></span>

</dd> <dt>

<span data-ttu-id="4ce83-121">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="4ce83-121">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="4ce83-122">O endereço IP externo foi alterado.</span><span class="sxs-lookup"><span data-stu-id="4ce83-122">The external IP address has changed.</span></span>

</dd> <dt>

<span data-ttu-id="4ce83-123">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="4ce83-123">4 (0x4)</span></span>
</dt> <dd>

<span data-ttu-id="4ce83-124">O endereço IP interno foi alterado.</span><span class="sxs-lookup"><span data-stu-id="4ce83-124">The internal IP address has changed.</span></span>

</dd> <dt>

<span data-ttu-id="4ce83-125">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="4ce83-125">8 (0x8)</span></span>
</dt> <dd>

<span data-ttu-id="4ce83-126">O destino foi Unido.</span><span class="sxs-lookup"><span data-stu-id="4ce83-126">The target was joined.</span></span>

</dd> <dt>

<span data-ttu-id="4ce83-127">16 (0x10)</span><span class="sxs-lookup"><span data-stu-id="4ce83-127">16 (0x10)</span></span>
</dt> <dd>

<span data-ttu-id="4ce83-128">O destino foi removido.</span><span class="sxs-lookup"><span data-stu-id="4ce83-128">The target was removed.</span></span>

</dd> <dt>

<span data-ttu-id="4ce83-129">32 (0x20)</span><span class="sxs-lookup"><span data-stu-id="4ce83-129">32 (0x20)</span></span>
</dt> <dd>

<span data-ttu-id="4ce83-130">O estado do destino foi alterado.</span><span class="sxs-lookup"><span data-stu-id="4ce83-130">The state of the target has changed.</span></span>

</dd> <dt>

<span data-ttu-id="4ce83-131">64 (0x40)</span><span class="sxs-lookup"><span data-stu-id="4ce83-131">64 (0x40)</span></span>
</dt> <dd>

<span data-ttu-id="4ce83-132">O destino está ocioso.</span><span class="sxs-lookup"><span data-stu-id="4ce83-132">The target is idle.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="4ce83-133">**Ambiente**</span><span class="sxs-lookup"><span data-stu-id="4ce83-133">**Environment**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ce83-134">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="4ce83-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4ce83-135">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4ce83-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4ce83-136">O nome do ambiente.</span><span class="sxs-lookup"><span data-stu-id="4ce83-136">The environment name.</span></span> <span data-ttu-id="4ce83-137">No caso de um destino de máquina virtual (VM), esse pode ser o nome do host da VM.</span><span class="sxs-lookup"><span data-stu-id="4ce83-137">In the case of a virtual machine (VM) target, this could be the VM host name.</span></span>

<span data-ttu-id="4ce83-138">**Windows Server 2008 R2:** Esta propriedade não está disponível antes do Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4ce83-138">**Windows Server 2008 R2:** This property is unavailable prior to Windows Server 2012</span></span>

</dd> <dt>

<span data-ttu-id="4ce83-139">**Farmname**</span><span class="sxs-lookup"><span data-stu-id="4ce83-139">**FarmName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ce83-140">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="4ce83-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4ce83-141">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4ce83-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4ce83-142">O nome do farm ao qual o destino pertence.</span><span class="sxs-lookup"><span data-stu-id="4ce83-142">The name of the farm the target belongs to.</span></span>

<span data-ttu-id="4ce83-143">**Windows Server 2008 R2:** Esta propriedade não está disponível antes do Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4ce83-143">**Windows Server 2008 R2:** This property is unavailable prior to Windows Server 2012</span></span>

</dd> <dt>

<span data-ttu-id="4ce83-144">**Volume**</span><span class="sxs-lookup"><span data-stu-id="4ce83-144">**Guid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ce83-145">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="4ce83-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4ce83-146">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4ce83-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4ce83-147">O GUID do destino.</span><span class="sxs-lookup"><span data-stu-id="4ce83-147">The GUID of the target.</span></span>

<span data-ttu-id="4ce83-148">**Windows Server 2008 R2:** Esta propriedade não está disponível antes do Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4ce83-148">**Windows Server 2008 R2:** This property is unavailable prior to Windows Server 2012</span></span>

</dd> <dt>

<span data-ttu-id="4ce83-149">**PluginName**</span><span class="sxs-lookup"><span data-stu-id="4ce83-149">**PluginName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ce83-150">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="4ce83-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4ce83-151">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4ce83-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4ce83-152">O nome do plug-in.</span><span class="sxs-lookup"><span data-stu-id="4ce83-152">The name of the plug-in.</span></span>

<span data-ttu-id="4ce83-153">**Windows Server 2008 R2:** Esta propriedade não está disponível antes do Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4ce83-153">**Windows Server 2008 R2:** This property is unavailable prior to Windows Server 2012</span></span>

</dd> <dt>

<span data-ttu-id="4ce83-154">**\_descritor de segurança**</span><span class="sxs-lookup"><span data-stu-id="4ce83-154">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ce83-155">Tipo de dados: matriz **uint8**</span><span class="sxs-lookup"><span data-stu-id="4ce83-155">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="4ce83-156">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4ce83-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4ce83-157">Descritor usado pelo provedor de eventos para determinar quais usuários podem receber o evento.</span><span class="sxs-lookup"><span data-stu-id="4ce83-157">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="4ce83-158">Esta propriedade é herdada do [**\_ \_ evento**](/windows/desktop/WmiSdk/--event).</span><span class="sxs-lookup"><span data-stu-id="4ce83-158">This property is inherited from [**\_\_Event**](/windows/desktop/WmiSdk/--event).</span></span> <span data-ttu-id="4ce83-159">Para obter mais informações sobre constantes usadas para definir esse descritor de segurança, consulte [constantes de segurança do WMI](/windows/desktop/WmiSdk/wmi-security-constants).</span><span class="sxs-lookup"><span data-stu-id="4ce83-159">For more information about constants used to set this security descriptor, see [WMI Security Constants](/windows/desktop/WmiSdk/wmi-security-constants).</span></span>

</dd> <dt>

<span data-ttu-id="4ce83-160">**TargetName**</span><span class="sxs-lookup"><span data-stu-id="4ce83-160">**TargetName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ce83-161">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="4ce83-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4ce83-162">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4ce83-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4ce83-163">O nome do destino.</span><span class="sxs-lookup"><span data-stu-id="4ce83-163">The name of the target.</span></span>

<span data-ttu-id="4ce83-164">**Windows Server 2008 R2:** Esta propriedade não está disponível antes do Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4ce83-164">**Windows Server 2008 R2:** This property is unavailable prior to Windows Server 2012</span></span>

</dd> <dt>

<span data-ttu-id="4ce83-165">**HORA da \_ criação**</span><span class="sxs-lookup"><span data-stu-id="4ce83-165">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4ce83-166">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="4ce83-166">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4ce83-167">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4ce83-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4ce83-168">Valor exclusivo que indica a hora em que o evento foi gerado.</span><span class="sxs-lookup"><span data-stu-id="4ce83-168">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="4ce83-169">Este é um valor de 64 bits que representa o número de intervalos de 100 nanossegundos após 1º de janeiro de 1601.</span><span class="sxs-lookup"><span data-stu-id="4ce83-169">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="4ce83-170">As informações estão no formato UTC (tempo Universal Coordenado).</span><span class="sxs-lookup"><span data-stu-id="4ce83-170">The information is in the Coordinated Universal Times (UTC) format.</span></span> <span data-ttu-id="4ce83-171">Esta propriedade é herdada do [**\_ \_ evento**](/windows/desktop/WmiSdk/--event).</span><span class="sxs-lookup"><span data-stu-id="4ce83-171">This property is inherited from [**\_\_Event**](/windows/desktop/WmiSdk/--event).</span></span>

<span data-ttu-id="4ce83-172">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="4ce83-172">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4ce83-173">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4ce83-173">Requirements</span></span>



| <span data-ttu-id="4ce83-174">Requisito</span><span class="sxs-lookup"><span data-stu-id="4ce83-174">Requirement</span></span> | <span data-ttu-id="4ce83-175">Valor</span><span class="sxs-lookup"><span data-stu-id="4ce83-175">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4ce83-176">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4ce83-176">Minimum supported client</span></span><br/> | <span data-ttu-id="4ce83-177">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="4ce83-177">None supported</span></span><br/>                                                              |
| <span data-ttu-id="4ce83-178">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4ce83-178">Minimum supported server</span></span><br/> | <span data-ttu-id="4ce83-179">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="4ce83-179">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="4ce83-180">Namespace</span><span class="sxs-lookup"><span data-stu-id="4ce83-180">Namespace</span></span><br/>                | <span data-ttu-id="4ce83-181">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="4ce83-181">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="4ce83-182">MOF</span><span class="sxs-lookup"><span data-stu-id="4ce83-182">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4ce83-183"><dt>TssdWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4ce83-183"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="4ce83-184">DLL</span><span class="sxs-lookup"><span data-stu-id="4ce83-184">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4ce83-185"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4ce83-185"><dt>TssdWmi.dll</dt></span></span> </dl> |



 

