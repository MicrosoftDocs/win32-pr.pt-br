---
description: Representa a manipulação de verificação de máquina (CMC) corrigida a ser alternada do driver de interrupção para sondagem. Essa classe está disponível somente em sistemas Windows de 64 bits.
ms.assetid: c5e99e13-0f65-40bc-8863-b2ca7ea221df
title: Classe MSMCAEvent_SwitchToCMCPolling
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAEvent_SwitchToCMCPolling
- MSMCAEvent_SwitchToCMCPolling.Active
- MSMCAEvent_SwitchToCMCPolling.InstanceName
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: f7d0d543dc36054550d4ddf6cc1a77ce80cf1647
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296338"
---
# <a name="msmcaevent_switchtocmcpolling-class"></a><span data-ttu-id="2fda2-104">\_Classe MSMCAEvent SwitchToCMCPolling</span><span class="sxs-lookup"><span data-stu-id="2fda2-104">MSMCAEvent\_SwitchToCMCPolling class</span></span>

<span data-ttu-id="2fda2-105">A classe **MSMCAEvent \_ SwitchToCMCPolling** representa a manipulação de verificação de máquina corrigida (CMC) a ser alternada do driver de interrupção para sondagem.</span><span class="sxs-lookup"><span data-stu-id="2fda2-105">The **MSMCAEvent\_SwitchToCMCPolling** class represents the corrected machine check (CMC) handling to be switched from the interrupt driver to polling.</span></span> <span data-ttu-id="2fda2-106">Em alguns casos, o kernel sonda a camada de abstração do sistema (SAL) para qualquer erro de plataforma CMC ou correção (CPE) que ocorreu dentro do intervalo de sondagem anterior.</span><span class="sxs-lookup"><span data-stu-id="2fda2-106">In some cases, the kernel polls the system abstraction layer (SAL) for any CMC or corrected platform error (CPE) that occurred within the previous polling interval.</span></span> <span data-ttu-id="2fda2-107">Essa classe está disponível somente em sistemas Windows de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="2fda2-107">This class is available only in 64-bit Windows systems.</span></span>

<span data-ttu-id="2fda2-108">A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="2fda2-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="2fda2-109">As propriedades e os métodos estão em ordem alfabética, não em ordem de MOF.</span><span class="sxs-lookup"><span data-stu-id="2fda2-109">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="2fda2-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2fda2-110">Syntax</span></span>

``` syntax
class MSMCAEvent_SwitchToCMCPolling : WMIEvent
{
  boolean Active;
  string  InstanceName;
};
```

## <a name="members"></a><span data-ttu-id="2fda2-111">Membros</span><span class="sxs-lookup"><span data-stu-id="2fda2-111">Members</span></span>

<span data-ttu-id="2fda2-112">A classe **MSMCAEvent \_ SwitchToCMCPolling** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="2fda2-112">The **MSMCAEvent\_SwitchToCMCPolling** class has these types of members:</span></span>

-   [<span data-ttu-id="2fda2-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="2fda2-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2fda2-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="2fda2-114">Properties</span></span>

<span data-ttu-id="2fda2-115">A classe **MSMCAEvent \_ SwitchToCMCPolling** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="2fda2-115">The **MSMCAEvent\_SwitchToCMCPolling** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2fda2-116">**Ativo**</span><span class="sxs-lookup"><span data-stu-id="2fda2-116">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2fda2-117">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="2fda2-117">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2fda2-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2fda2-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2fda2-119">**True**, se esta instância da classe estiver ativa; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="2fda2-119">**TRUE**, if this instance of the class is active; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="2fda2-120">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="2fda2-120">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2fda2-121">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2fda2-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2fda2-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2fda2-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2fda2-123">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="2fda2-123">Qualifiers: [**Key**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="2fda2-124">Identificador exclusivo desta instância da classe.</span><span class="sxs-lookup"><span data-stu-id="2fda2-124">Unique identifier of this instance of the class.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2fda2-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="2fda2-125">Remarks</span></span>

<span data-ttu-id="2fda2-126">A classe **MSMCAEvent \_ SwitchToCMCPolling** é derivada de [**WmiEvent**](wmievent.md).</span><span class="sxs-lookup"><span data-stu-id="2fda2-126">The **MSMCAEvent\_SwitchToCMCPolling** class is derived from [**WMIEvent**](wmievent.md).</span></span>

<span data-ttu-id="2fda2-127">A camada de abstração do sistema (SAL) é o código gravado na ROM que o sistema operacional chama para executar operações dependentes da plataforma.</span><span class="sxs-lookup"><span data-stu-id="2fda2-127">The system abstraction layer (SAL) is code burned onto ROM that the operating system calls to perform platform-dependent operations.</span></span> <span data-ttu-id="2fda2-128">É semelhante ao BIOS em uma plataforma x86.</span><span class="sxs-lookup"><span data-stu-id="2fda2-128">It is similar to the BIOS on an x86 platform.</span></span> <span data-ttu-id="2fda2-129">Nos casos em que a plataforma não dá suporte a interrupções para sondagem de CMC ou CPE, o sistema operacional é sondado a cada minuto, verificando se ocorreu um erro anteriormente.</span><span class="sxs-lookup"><span data-stu-id="2fda2-129">In cases where the platform does not support interrupts for CMC or CPE polling, the operating system polls every minute, checking if an error occurred previously.</span></span> <span data-ttu-id="2fda2-130">Se a plataforma der suporte a interrupções e o sistema operacional receber uma quantidade definida pelo usuário de pesquisas CMC ou CPE dentro de um minuto, ele desabilitará a interrupção e a sondagem.</span><span class="sxs-lookup"><span data-stu-id="2fda2-130">If the platform does support interrupts and the operating system receives a user defined amount of CMC or CPE polls within one minute, then it disables the interrupt and poll.</span></span> <span data-ttu-id="2fda2-131">Se o usuário não definir o número de pesquisas em um minuto, o sistema definirá um padrão para 10 pesquisas por minuto.</span><span class="sxs-lookup"><span data-stu-id="2fda2-131">If the user does not define the number of polls within one minute, the system sets a default to 10 polls per minute.</span></span>

## <a name="requirements"></a><span data-ttu-id="2fda2-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2fda2-132">Requirements</span></span>



| <span data-ttu-id="2fda2-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="2fda2-133">Requirement</span></span> | <span data-ttu-id="2fda2-134">Valor</span><span class="sxs-lookup"><span data-stu-id="2fda2-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2fda2-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2fda2-135">Minimum supported client</span></span><br/> | <span data-ttu-id="2fda2-136">Windows XP</span><span class="sxs-lookup"><span data-stu-id="2fda2-136">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="2fda2-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2fda2-137">Minimum supported server</span></span><br/> | <span data-ttu-id="2fda2-138">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2fda2-138">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="2fda2-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="2fda2-139">Namespace</span></span><br/>                | <span data-ttu-id="2fda2-140">\\WMI raiz</span><span class="sxs-lookup"><span data-stu-id="2fda2-140">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="2fda2-141">MOF</span><span class="sxs-lookup"><span data-stu-id="2fda2-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2fda2-142"><dt>Wmicore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2fda2-142"><dt>Wmicore.mof</dt></span></span> </dl> |
| <span data-ttu-id="2fda2-143">DLL</span><span class="sxs-lookup"><span data-stu-id="2fda2-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2fda2-144"><dt>Wmiprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2fda2-144"><dt>Wmiprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2fda2-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="2fda2-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2fda2-146">Classes MSMCA</span><span class="sxs-lookup"><span data-stu-id="2fda2-146">MSMCA Classes</span></span>](msmca-classes.md)
</dt> <dt>

[<span data-ttu-id="2fda2-147">**WMIEvent**</span><span class="sxs-lookup"><span data-stu-id="2fda2-147">**WMIEvent**</span></span>](wmievent.md)
</dt> </dl>

 

