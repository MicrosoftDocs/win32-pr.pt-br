---
description: A \_ classe CIM SettingContext associa objetos de configuração a objetos de configuração.
ms.assetid: 8ed7e150-b4e6-4fd4-809b-32e870b559c4
ms.tgt_platform: multiple
title: Classe CIM_SettingContext
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SettingContext
- CIM_SettingContext.Context
- CIM_SettingContext.Setting
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 867be99e1630f02c0163516ad7a86cf84c2fac13
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920250"
---
# <a name="cim_settingcontext-class"></a><span data-ttu-id="31df3-103">\_Classe CIM SettingContext</span><span class="sxs-lookup"><span data-stu-id="31df3-103">CIM\_SettingContext class</span></span>

<span data-ttu-id="31df3-104">A classe **CIM \_ SettingContext** associa objetos de configuração a objetos de configuração.</span><span class="sxs-lookup"><span data-stu-id="31df3-104">The **CIM\_SettingContext** class associates configuration objects with setting objects.</span></span> <span data-ttu-id="31df3-105">Por exemplo, as configurações de um adaptador de rede podem mudar com base no site ou na rede à qual seu sistema de computador de hospedagem está conectado.</span><span class="sxs-lookup"><span data-stu-id="31df3-105">For example, a network adapter's settings could change based on the site or network to which its hosting computer system is attached.</span></span> <span data-ttu-id="31df3-106">Nesse caso, o sistema de computador teria dois objetos de configuração diferentes, correspondentes às diferenças na configuração de rede para os dois segmentos de rede.</span><span class="sxs-lookup"><span data-stu-id="31df3-106">In which case, the computer system would have two different configuration objects, corresponding to the differences in network configuration for the two network segments.</span></span> <span data-ttu-id="31df3-107">Uma configuração agregaria um objeto de configuração para o adaptador de rede ao operar em um segmento; enquanto que a outra configuração agregaria um objeto de configuração de adaptador de rede diferente, específico a outro segmento.</span><span class="sxs-lookup"><span data-stu-id="31df3-107">One configuration would aggregate a setting object for the network adapter when operating on one segment; whereas, the other configuration would aggregate a different network adapter setting object, specific to another segment.</span></span> <span data-ttu-id="31df3-108">Observe que muitas configurações de computador são independentes da configuração de rede.</span><span class="sxs-lookup"><span data-stu-id="31df3-108">Note that many computer settings are independent of the network configuration.</span></span> <span data-ttu-id="31df3-109">Por exemplo, ambas as configurações agregariam o mesmo objeto de configuração para a resolução do monitor do sistema de computador.</span><span class="sxs-lookup"><span data-stu-id="31df3-109">For example, both configurations would aggregate the same setting object for the computer system's monitor resolution.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="31df3-110">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="31df3-110">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="31df3-111">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="31df3-111">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="31df3-112">A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="31df3-112">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="31df3-113">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="31df3-113">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="31df3-114">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="31df3-114">Syntax</span></span>

``` syntax
[Abstract, UUID("{F0B752E8-DB30-11d2-85FC-0000F8102E5F}"), Aggregation, Association, AMENDMENT]
class CIM_SettingContext
{
  CIM_Configuration REF Context;
  CIM_Setting       REF Setting;
};
```

## <a name="members"></a><span data-ttu-id="31df3-115">Membros</span><span class="sxs-lookup"><span data-stu-id="31df3-115">Members</span></span>

<span data-ttu-id="31df3-116">A classe **CIM \_ SettingContext** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="31df3-116">The **CIM\_SettingContext** class has these types of members:</span></span>

-   [<span data-ttu-id="31df3-117">Propriedades</span><span class="sxs-lookup"><span data-stu-id="31df3-117">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="31df3-118">Propriedades</span><span class="sxs-lookup"><span data-stu-id="31df3-118">Properties</span></span>

<span data-ttu-id="31df3-119">A classe **CIM \_ SettingContext** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="31df3-119">The **CIM\_SettingContext** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="31df3-120">**Contexto**</span><span class="sxs-lookup"><span data-stu-id="31df3-120">**Context**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31df3-121">Tipo de dados **: \_ configuração de CIM**</span><span class="sxs-lookup"><span data-stu-id="31df3-121">Data type: **CIM\_Configuration**</span></span>
</dt> <dt>

<span data-ttu-id="31df3-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="31df3-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31df3-123">Qualificadores: [ **agregação**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="31df3-123">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="31df3-124">Referência ao objeto de configuração que agrega a configuração.</span><span class="sxs-lookup"><span data-stu-id="31df3-124">Reference to the configuration object that aggregates the setting.</span></span>

</dd> <dt>

<span data-ttu-id="31df3-125">**Configuração**</span><span class="sxs-lookup"><span data-stu-id="31df3-125">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31df3-126">Tipo de dados **: \_ configuração de CIM**</span><span class="sxs-lookup"><span data-stu-id="31df3-126">Data type: **CIM\_Setting**</span></span>
</dt> <dt>

<span data-ttu-id="31df3-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="31df3-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="31df3-128">Referência a uma configuração agregada.</span><span class="sxs-lookup"><span data-stu-id="31df3-128">Reference to an aggregated setting.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="31df3-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="31df3-129">Remarks</span></span>

<span data-ttu-id="31df3-130">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="31df3-130">WMI does not implement this class.</span></span>

<span data-ttu-id="31df3-131">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="31df3-131">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="31df3-132">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="31df3-132">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="31df3-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="31df3-133">Requirements</span></span>



| <span data-ttu-id="31df3-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="31df3-134">Requirement</span></span> | <span data-ttu-id="31df3-135">Valor</span><span class="sxs-lookup"><span data-stu-id="31df3-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="31df3-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="31df3-136">Minimum supported client</span></span><br/> | <span data-ttu-id="31df3-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="31df3-137">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="31df3-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="31df3-138">Minimum supported server</span></span><br/> | <span data-ttu-id="31df3-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="31df3-139">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="31df3-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="31df3-140">Namespace</span></span><br/>                | <span data-ttu-id="31df3-141">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="31df3-141">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="31df3-142">MOF</span><span class="sxs-lookup"><span data-stu-id="31df3-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="31df3-143"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="31df3-143"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="31df3-144">DLL</span><span class="sxs-lookup"><span data-stu-id="31df3-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="31df3-145"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="31df3-145"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

