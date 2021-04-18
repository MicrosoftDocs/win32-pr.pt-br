---
description: Uma coleção SNMP é mapeada para uma classe CIM e os elementos de uma coleção são mapeados para as propriedades de uma classe CIM. Todas as definições de classe CIM geradas devem ser derivadas da classe SnmpObjectType.
ms.assetid: e6f82fd6-e3d8-48c5-8c7b-a30a2d502f41
ms.tgt_platform: multiple
title: Coleções SNMP
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a85473a394ce715ff9759e974a47824e5621509f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105787609"
---
# <a name="snmp-collections"></a><span data-ttu-id="ceb4b-104">Coleções SNMP</span><span class="sxs-lookup"><span data-stu-id="ceb4b-104">SNMP Collections</span></span>

<span data-ttu-id="ceb4b-105">Uma coleção SNMP é mapeada para uma classe CIM e os elementos de uma coleção são mapeados para as propriedades de uma classe CIM.</span><span class="sxs-lookup"><span data-stu-id="ceb4b-105">An SNMP collection maps to a CIM class and the elements of a collection map to the properties of a CIM class.</span></span> <span data-ttu-id="ceb4b-106">Todas as definições de classe CIM geradas devem ser derivadas da classe **SnmpObjectType** .</span><span class="sxs-lookup"><span data-stu-id="ceb4b-106">All generated CIM class definitions must be derived from the **SnmpObjectType** class.</span></span>

> [!Note]  
> <span data-ttu-id="ceb4b-107">Para obter mais informações sobre como instalar o provedor, consulte [Configurando o ambiente SNMP WMI](setting-up-the-wmi-snmp-environment.md).</span><span class="sxs-lookup"><span data-stu-id="ceb4b-107">For more information about installing the provider, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

 

<span data-ttu-id="ceb4b-108">As seguintes definições de classe pai têm todas as definições de classe geradas:</span><span class="sxs-lookup"><span data-stu-id="ceb4b-108">The following class definitions parent all generated class definitions:</span></span>

``` syntax
[abstract]
class SnmpMacro
{
};

[abstract]
class SnmpObjectType:SnmpMacro
{
};
```

## <a name="remarks"></a><span data-ttu-id="ceb4b-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="ceb4b-109">Remarks</span></span>

<span data-ttu-id="ceb4b-110">As regras a seguir se aplicam ao mapear coleções SNMP para classes CIM.</span><span class="sxs-lookup"><span data-stu-id="ceb4b-110">The following rules apply when mapping SNMP collections to CIM classes.</span></span> <span data-ttu-id="ceb4b-111">A menos que especificado de outra forma, essas regras se aplicam a coleções escalares e de tabela:</span><span class="sxs-lookup"><span data-stu-id="ceb4b-111">Unless otherwise specified, these rules apply to both scalar and table collections:</span></span>

-   <span data-ttu-id="ceb4b-112">O processo de mapeamento gera nomes de classe CIM concatenando "SNMP \_ ", o nome de identidade do módulo MIB, " \_ " e o descritor de objeto da coleção.</span><span class="sxs-lookup"><span data-stu-id="ceb4b-112">The mapping process generates CIM class names by concatenating "SNMP\_", the MIB module identity name, "\_", and the collection's object descriptor.</span></span>

    <span data-ttu-id="ceb4b-113">Por exemplo: o **sistema** se traduz no **\_ \_ \_ sistema MIB RFC1213 SNMP**, enquanto o **iftable** se traduz em **SNMP \_ RFC1213 \_ MIB \_ iftable**.</span><span class="sxs-lookup"><span data-stu-id="ceb4b-113">For example: **system** translates to **SNMP\_RFC1213\_MIB\_system**, while **ifTable** translates to **SNMP\_RFC1213\_MIB\_ifTable**.</span></span>

-   <span data-ttu-id="ceb4b-114">Em todos os casos, hifens (-) em identificadores de MIB SNMP são mapeados para sublinhados ( \_ ) em nomes de classe CIM.</span><span class="sxs-lookup"><span data-stu-id="ceb4b-114">In all cases, hyphens (-) in SNMP MIB identifiers map to underscores (\_) in CIM class names.</span></span>
-   <span data-ttu-id="ceb4b-115">Conflitos de nomenclatura podem ocorrer devido a uma não diferenciação de maiúsculas e minúsculas de nome CIM.</span><span class="sxs-lookup"><span data-stu-id="ceb4b-115">Naming conflicts can occur due to CIM name case-insensitivity.</span></span> <span data-ttu-id="ceb4b-116">Se ocorrer um conflito de nomenclatura, o provedor escolherá uma das definições de Grupo conflitantes e ignorará as definições restantes.</span><span class="sxs-lookup"><span data-stu-id="ceb4b-116">If a naming conflict occurs, the provider chooses one of the conflicting group definitions and ignores the remaining definitions.</span></span>
-   <span data-ttu-id="ceb4b-117">O nome de identidade do módulo MIB que contém a coleção é mapeado para o nome do **módulo \_** qualificador de classe CIM.</span><span class="sxs-lookup"><span data-stu-id="ceb4b-117">The identity name of the MIB module that contains the collection maps to the CIM class qualifier **Module\_Name**.</span></span>
-   <span data-ttu-id="ceb4b-118">O identificador de objeto da coleção criei é mapeado para o ObjectID do **grupo \_** de qualificador de classe CIM.</span><span class="sxs-lookup"><span data-stu-id="ceb4b-118">The object identifier of the fabricated collection maps to the CIM class qualifier **Group\_Objectid**.</span></span>
-   <span data-ttu-id="ceb4b-119">A lista de importações do módulo MIB (obtida da definição de macro de **identidade de módulo** ) é mapeada para **as \_ importações do módulo** de qualificador de classe CIM.</span><span class="sxs-lookup"><span data-stu-id="ceb4b-119">The MIB module imports list (obtained from the **MODULE-IDENTITY** macro definition) maps to the CIM class qualifier **module\_imports**.</span></span> <span data-ttu-id="ceb4b-120">Esse qualificador contém uma lista separada por vírgulas de nomes de módulo.</span><span class="sxs-lookup"><span data-stu-id="ceb4b-120">This qualifier contains a comma-separated list of module names.</span></span>

 

 



