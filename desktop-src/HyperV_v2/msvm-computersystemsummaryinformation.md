---
description: Contém um resumo de informações sobre o sistema de computador virtual especificado.
ms.assetid: ab31d5db-a8d3-47bc-a024-0f4c4b93a34b
title: Classe Msvm_ComputerSystemSummaryInformation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ComputerSystemSummaryInformation
- Msvm_ComputerSystemSummaryInformation.Antecedent
- Msvm_ComputerSystemSummaryInformation.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 35248bcfa14609e8db25b148088b6feb8d161116
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827156"
---
# <a name="msvm_computersystemsummaryinformation-class"></a><span data-ttu-id="3cbfa-103">\_Classe Msvm ComputerSystemSummaryInformation</span><span class="sxs-lookup"><span data-stu-id="3cbfa-103">Msvm\_ComputerSystemSummaryInformation class</span></span>

<span data-ttu-id="3cbfa-104">Contém um resumo de informações sobre o sistema de computador virtual especificado.</span><span class="sxs-lookup"><span data-stu-id="3cbfa-104">Contains an information summary about the specified virtual computer system.</span></span>

<span data-ttu-id="3cbfa-105">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="3cbfa-105">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3cbfa-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3cbfa-106">Syntax</span></span>

``` syntax
[Dynamic, Association, Provider("VmmsWmiInstanceAndMethodProvider")]
class Msvm_ComputerSystemSummaryInformation : CIM_ElementView
{
  CIM_ComputerSystem          REF Antecedent;
  Msvm_SummaryInformationBase REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="3cbfa-107">Membros</span><span class="sxs-lookup"><span data-stu-id="3cbfa-107">Members</span></span>

<span data-ttu-id="3cbfa-108">A classe **Msvm \_ ComputerSystemSummaryInformation** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="3cbfa-108">The **Msvm\_ComputerSystemSummaryInformation** class has these types of members:</span></span>

-   [<span data-ttu-id="3cbfa-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="3cbfa-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3cbfa-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="3cbfa-110">Properties</span></span>

<span data-ttu-id="3cbfa-111">A classe **Msvm \_ ComputerSystemSummaryInformation** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="3cbfa-111">The **Msvm\_ComputerSystemSummaryInformation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3cbfa-112">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="3cbfa-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3cbfa-113">Tipo de dados **: \_ sistema de ComputerSystem CIM**</span><span class="sxs-lookup"><span data-stu-id="3cbfa-113">Data type: **CIM\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="3cbfa-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3cbfa-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3cbfa-115">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**substituição**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecessor")</span><span class="sxs-lookup"><span data-stu-id="3cbfa-115">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="3cbfa-116">Um objeto de [**\_ sistema**](cim-computersystem.md) de recursos CIM que é uma instância na representação normalizada do recurso gerenciado.</span><span class="sxs-lookup"><span data-stu-id="3cbfa-116">A [**CIM\_ComputerSystem**](cim-computersystem.md) object that is an instance in the normalized representation of the managed resource.</span></span>

> [!Note]
>
> <span data-ttu-id="3cbfa-117">Tipo de dados atualizado do [**Msvm \_ ComputerSystem**](msvm-computersystem.md) no Windows 10, versão 1703.</span><span class="sxs-lookup"><span data-stu-id="3cbfa-117">Datatype upgraded from [**Msvm\_ComputerSystem**](msvm-computersystem.md) in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="3cbfa-118">**Depende**</span><span class="sxs-lookup"><span data-stu-id="3cbfa-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3cbfa-119">Tipo de dados: **Msvm \_ SummaryInformationBase**</span><span class="sxs-lookup"><span data-stu-id="3cbfa-119">Data type: **Msvm\_SummaryInformationBase**</span></span>
</dt> <dt>

<span data-ttu-id="3cbfa-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3cbfa-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3cbfa-121">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**substituição**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente")</span><span class="sxs-lookup"><span data-stu-id="3cbfa-121">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="3cbfa-122">Uma instância de [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md) que representa uma exibição desnormalizada ou agregada do recurso gerenciado que é representado pelo [**Msvm \_ ComputerSystem**](msvm-computersystem.md) referenciado pela propriedade Antecedent.</span><span class="sxs-lookup"><span data-stu-id="3cbfa-122">An instance of [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) that represents a de-normalized or aggregate view of the managed resource that is represented by the [**Msvm\_ComputerSystem**](msvm-computersystem.md) referenced by the Antecedent property.</span></span>

> [!Note]
>
> <span data-ttu-id="3cbfa-123">Tipo de dados atualizado de [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md) no Windows 10, versão 1703.</span><span class="sxs-lookup"><span data-stu-id="3cbfa-123">Datatype updated from [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) in Windows 10, version 1703.</span></span>

 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3cbfa-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3cbfa-124">Requirements</span></span>



| <span data-ttu-id="3cbfa-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="3cbfa-125">Requirement</span></span> | <span data-ttu-id="3cbfa-126">Valor</span><span class="sxs-lookup"><span data-stu-id="3cbfa-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3cbfa-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3cbfa-127">Minimum supported client</span></span><br/> | <span data-ttu-id="3cbfa-128">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="3cbfa-128">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="3cbfa-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3cbfa-129">Minimum supported server</span></span><br/> | <span data-ttu-id="3cbfa-130">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="3cbfa-130">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="3cbfa-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="3cbfa-131">Namespace</span></span><br/>                | <span data-ttu-id="3cbfa-132">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="3cbfa-132">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="3cbfa-133">MOF</span><span class="sxs-lookup"><span data-stu-id="3cbfa-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3cbfa-134"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3cbfa-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3cbfa-135">DLL</span><span class="sxs-lookup"><span data-stu-id="3cbfa-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3cbfa-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3cbfa-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="3cbfa-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="3cbfa-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3cbfa-138">**\_ELEMENTVIEW CIM**</span><span class="sxs-lookup"><span data-stu-id="3cbfa-138">**CIM\_ElementView**</span></span>](cim-elementview.md)
</dt> </dl>

 

