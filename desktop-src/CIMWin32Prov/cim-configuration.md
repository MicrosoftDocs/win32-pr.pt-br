---
description: O \_ objeto de configuração CIM permite o agrupamento de conjuntos de parâmetros (definidos em \_ objetos de configuração CIM) e dependências para um ou mais elementos do sistema gerenciado.
ms.assetid: f597fe78-be50-4d31-b1eb-d219acaf1751
ms.tgt_platform: multiple
title: Classe CIM_Configuration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Configuration
- CIM_Configuration.Caption
- CIM_Configuration.Description
- CIM_Configuration.Name
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: c069f5c7186d08f01b54fe02c0568dbb4ff43d26
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646425"
---
# <a name="cim_configuration-class"></a><span data-ttu-id="b0510-103">\_Classe de configuração CIM</span><span class="sxs-lookup"><span data-stu-id="b0510-103">CIM\_Configuration class</span></span>

<span data-ttu-id="b0510-104">O objeto de **\_ configuração CIM** permite o agrupamento de conjuntos de parâmetros (definidos em objetos de [**\_ configuração CIM**](cim-setting.md) ) e dependências para um ou mais elementos do sistema gerenciado.</span><span class="sxs-lookup"><span data-stu-id="b0510-104">The **CIM\_Configuration** object allows the grouping of parameter sets (defined in [**CIM\_Setting**](cim-setting.md) objects) and dependencies for one or more managed system elements.</span></span> <span data-ttu-id="b0510-105">Esse objeto representa um determinado comportamento ou um estado funcional desejado para os elementos do sistema gerenciado.</span><span class="sxs-lookup"><span data-stu-id="b0510-105">This object represents a certain behavior, or a desired functional state for the managed system elements.</span></span> <span data-ttu-id="b0510-106">O estado funcional desejado geralmente é controlado por requisitos externos, como hora ou local.</span><span class="sxs-lookup"><span data-stu-id="b0510-106">The desired functional state is typically driven by external requirements, such as time or location.</span></span> <span data-ttu-id="b0510-107">Por exemplo, para se conectar a um sistema de email de casa, existe uma dependência em um modem; enquanto que uma dependência em um adaptador de rede existe no trabalho.</span><span class="sxs-lookup"><span data-stu-id="b0510-107">For example, to connect to a mail system from home, a dependency on a modem exists; whereas, a dependency on a network adapter exists at work.</span></span> <span data-ttu-id="b0510-108">As configurações para os dispositivos lógicos pertinentes (neste exemplo, o adaptador de rede e o modem POTS) podem ser definidas e agregadas pela **\_ configuração de CIM**.</span><span class="sxs-lookup"><span data-stu-id="b0510-108">Settings for the pertinent logical devices (in this example, POTS modem and network adapter) can be defined and aggregated by **CIM\_Configuration**.</span></span> <span data-ttu-id="b0510-109">Portanto, duas configurações de "conexão com o email" podem ser definidas agrupando as dependências relevantes e os objetos de [**\_ configuração CIM**](cim-setting.md) .</span><span class="sxs-lookup"><span data-stu-id="b0510-109">Therefore, two "Connect to Mail" configurations can be defined by grouping the relevant dependencies and [**CIM\_Setting**](cim-setting.md) objects.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b0510-110">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="b0510-110">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="b0510-111">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="b0510-111">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="b0510-112">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="b0510-112">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="b0510-113">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="b0510-113">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0510-114">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b0510-114">Syntax</span></span>

``` syntax
[Abstract, UUID("{4C51D7AE-DB22-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_Configuration
{
  string Caption;
  string Description;
  string Name;
};
```

## <a name="members"></a><span data-ttu-id="b0510-115">Membros</span><span class="sxs-lookup"><span data-stu-id="b0510-115">Members</span></span>

<span data-ttu-id="b0510-116">A classe de **\_ configuração CIM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="b0510-116">The **CIM\_Configuration** class has these types of members:</span></span>

-   [<span data-ttu-id="b0510-117">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b0510-117">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b0510-118">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b0510-118">Properties</span></span>

<span data-ttu-id="b0510-119">A classe de **\_ configuração CIM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="b0510-119">The **CIM\_Configuration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b0510-120">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="b0510-120">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0510-121">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b0510-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b0510-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b0510-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b0510-123">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="b0510-123">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="b0510-124">Breve descrição textual do objeto **de \_ configuração CIM** .</span><span class="sxs-lookup"><span data-stu-id="b0510-124">Short textual description of the **CIM\_Configuration** object.</span></span>

</dd> <dt>

<span data-ttu-id="b0510-125">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="b0510-125">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0510-126">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b0510-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b0510-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b0510-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0510-128">Descrição textual do objeto **de \_ configuração CIM** .</span><span class="sxs-lookup"><span data-stu-id="b0510-128">Textual description of the **CIM\_Configuration** object.</span></span>

</dd> <dt>

<span data-ttu-id="b0510-129">**Nome**</span><span class="sxs-lookup"><span data-stu-id="b0510-129">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0510-130">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b0510-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b0510-131">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b0510-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b0510-132">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="b0510-132">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="b0510-133">Rótulo pelo qual o objeto de **\_ configuração CIM** é conhecido.</span><span class="sxs-lookup"><span data-stu-id="b0510-133">Label by which the **CIM\_Configuration** object is known.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b0510-134">Comentários</span><span class="sxs-lookup"><span data-stu-id="b0510-134">Remarks</span></span>

<span data-ttu-id="b0510-135">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="b0510-135">WMI does not implement this class.</span></span>

<span data-ttu-id="b0510-136">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="b0510-136">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="b0510-137">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="b0510-137">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0510-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b0510-138">Requirements</span></span>



| <span data-ttu-id="b0510-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="b0510-139">Requirement</span></span> | <span data-ttu-id="b0510-140">Valor</span><span class="sxs-lookup"><span data-stu-id="b0510-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b0510-141">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b0510-141">Minimum supported client</span></span><br/> | <span data-ttu-id="b0510-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b0510-142">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b0510-143">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b0510-143">Minimum supported server</span></span><br/> | <span data-ttu-id="b0510-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b0510-144">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b0510-145">Namespace</span><span class="sxs-lookup"><span data-stu-id="b0510-145">Namespace</span></span><br/>                | <span data-ttu-id="b0510-146">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="b0510-146">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b0510-147">MOF</span><span class="sxs-lookup"><span data-stu-id="b0510-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b0510-148"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b0510-148"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b0510-149">DLL</span><span class="sxs-lookup"><span data-stu-id="b0510-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b0510-150"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b0510-150"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

