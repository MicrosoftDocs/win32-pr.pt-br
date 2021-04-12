---
title: Classe Win32_CentralPublishingChangeEvent
description: Um evento que representa uma alteração nas configurações do RDV central.
ms.assetid: 95be015e-a185-4548-a7f7-a22b351a34c8
ms.tgt_platform: multiple
keywords:
- Classe de Win32_CentralPublishingChangeEvent Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de Win32_CentralPublishingChangeEvent classe, descrita
topic_type:
- apiref
api_name:
- Win32_CentralPublishingChangeEvent
- Win32_CentralPublishingChangeEvent.SECURITY_DESCRIPTOR
- Win32_CentralPublishingChangeEvent.TIME_CREATED
- Win32_CentralPublishingChangeEvent.TargetInstance
- Win32_CentralPublishingChangeEvent.OperationType
api_location:
- TscPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4695479eb33301bda51b558375a18186fa08161e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455381"
---
# <a name="win32_centralpublishingchangeevent-class"></a><span data-ttu-id="5d205-105">\_Classe Win32 CentralPublishingChangeEvent</span><span class="sxs-lookup"><span data-stu-id="5d205-105">Win32\_CentralPublishingChangeEvent class</span></span>

<span data-ttu-id="5d205-106">Um evento que representa uma alteração nas configurações do RDV central.</span><span class="sxs-lookup"><span data-stu-id="5d205-106">An event that represents a change to the central RDV settings.</span></span>

<span data-ttu-id="5d205-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="5d205-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d205-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5d205-108">Syntax</span></span>

``` syntax
class Win32_CentralPublishingChangeEvent : __ExtrinsicEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  uint64 TIME_CREATED;
  object TargetInstance;
  uint32 OperationType;
};
```

## <a name="members"></a><span data-ttu-id="5d205-109">Membros</span><span class="sxs-lookup"><span data-stu-id="5d205-109">Members</span></span>

<span data-ttu-id="5d205-110">A classe **Win32 \_ CentralPublishingChangeEvent** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="5d205-110">The **Win32\_CentralPublishingChangeEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="5d205-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5d205-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5d205-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5d205-112">Properties</span></span>

<span data-ttu-id="5d205-113">A classe **Win32 \_ CentralPublishingChangeEvent** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="5d205-113">The **Win32\_CentralPublishingChangeEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5d205-114">**OperationType**</span><span class="sxs-lookup"><span data-stu-id="5d205-114">**OperationType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d205-115">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5d205-115">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5d205-116">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5d205-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5d205-117">O tipo de operação correspondente ao evento.</span><span class="sxs-lookup"><span data-stu-id="5d205-117">The type of operation corresponding to the event.</span></span>

<dt>

<span id="Create"></span><span id="create"></span><span id="CREATE"></span>

<span data-ttu-id="5d205-118">**Criar** (0)</span><span class="sxs-lookup"><span data-stu-id="5d205-118">**Create** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Modify"></span><span id="modify"></span><span id="MODIFY"></span>

<span data-ttu-id="5d205-119">**Modificar** (1)</span><span class="sxs-lookup"><span data-stu-id="5d205-119">**Modify** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Delete"></span><span id="delete"></span><span id="DELETE"></span>

<span data-ttu-id="5d205-120">**Excluir** (2)</span><span class="sxs-lookup"><span data-stu-id="5d205-120">**Delete** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5d205-121">**\_descritor de segurança**</span><span class="sxs-lookup"><span data-stu-id="5d205-121">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d205-122">Tipo de dados: matriz **uint8**</span><span class="sxs-lookup"><span data-stu-id="5d205-122">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="5d205-123">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5d205-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5d205-124">Descritor usado pelo provedor de eventos para determinar quais usuários podem receber o evento.</span><span class="sxs-lookup"><span data-stu-id="5d205-124">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="5d205-125">Esta propriedade é herdada do [**\_ \_ evento**](/windows/desktop/WmiSdk/--event).</span><span class="sxs-lookup"><span data-stu-id="5d205-125">This property is inherited from [**\_\_Event**](/windows/desktop/WmiSdk/--event).</span></span> <span data-ttu-id="5d205-126">Para obter mais informações sobre constantes usadas para definir esse descritor de segurança, consulte [constantes de segurança do WMI](/windows/desktop/WmiSdk/wmi-security-constants).</span><span class="sxs-lookup"><span data-stu-id="5d205-126">For more information about constants used to set this security descriptor, see [WMI Security Constants](/windows/desktop/WmiSdk/wmi-security-constants).</span></span>

</dd> <dt>

<span data-ttu-id="5d205-127">**TargetInstance**</span><span class="sxs-lookup"><span data-stu-id="5d205-127">**TargetInstance**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d205-128">Tipo de dados: **objeto**</span><span class="sxs-lookup"><span data-stu-id="5d205-128">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="5d205-129">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5d205-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5d205-130">Objeto alterado pela operação correspondente ao evento.</span><span class="sxs-lookup"><span data-stu-id="5d205-130">Object changed by the operation corresponding to the event.</span></span>

</dd> <dt>

<span data-ttu-id="5d205-131">**HORA da \_ criação**</span><span class="sxs-lookup"><span data-stu-id="5d205-131">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d205-132">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="5d205-132">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5d205-133">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5d205-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5d205-134">Valor exclusivo que indica a hora em que o evento foi gerado.</span><span class="sxs-lookup"><span data-stu-id="5d205-134">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="5d205-135">Este é um valor de 64 bits que representa o número de intervalos de 100 nanossegundos após 1º de janeiro de 1601.</span><span class="sxs-lookup"><span data-stu-id="5d205-135">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="5d205-136">As informações estão no formato UTC (tempo Universal Coordenado).</span><span class="sxs-lookup"><span data-stu-id="5d205-136">The information is in the Coordinated Universal Times (UTC) format.</span></span> <span data-ttu-id="5d205-137">Esta propriedade é herdada do [**\_ \_ evento**](/windows/desktop/WmiSdk/--event).</span><span class="sxs-lookup"><span data-stu-id="5d205-137">This property is inherited from [**\_\_Event**](/windows/desktop/WmiSdk/--event).</span></span>

<span data-ttu-id="5d205-138">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="5d205-138">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5d205-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5d205-139">Requirements</span></span>



| <span data-ttu-id="5d205-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="5d205-140">Requirement</span></span> | <span data-ttu-id="5d205-141">Valor</span><span class="sxs-lookup"><span data-stu-id="5d205-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5d205-142">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5d205-142">Minimum supported client</span></span><br/> | <span data-ttu-id="5d205-143">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="5d205-143">None supported</span></span><br/>                                                                |
| <span data-ttu-id="5d205-144">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5d205-144">Minimum supported server</span></span><br/> | <span data-ttu-id="5d205-145">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5d205-145">Windows Server 2012</span></span><br/>                                                           |
| <span data-ttu-id="5d205-146">Namespace</span><span class="sxs-lookup"><span data-stu-id="5d205-146">Namespace</span></span><br/>                | <span data-ttu-id="5d205-147">\\TerminalServices da cimv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="5d205-147">Root\\cimv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="5d205-148">MOF</span><span class="sxs-lookup"><span data-stu-id="5d205-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5d205-149"><dt>Tscpub. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5d205-149"><dt>Tscpub.mof</dt></span></span> </dl>    |
| <span data-ttu-id="5d205-150">DLL</span><span class="sxs-lookup"><span data-stu-id="5d205-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5d205-151"><dt>TscPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5d205-151"><dt>TscPubWmi.dll</dt></span></span> </dl> |



 

