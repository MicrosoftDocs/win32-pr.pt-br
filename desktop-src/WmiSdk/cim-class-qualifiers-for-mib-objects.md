---
description: O provedor SNMP usa os seguintes qualificadores de classe CIM ao mapear definições de objeto MIB para definições de classe CIM.
ms.assetid: 458167dc-562e-47b8-8760-797ae13f9459
ms.tgt_platform: multiple
title: Qualificadores de classe CIM para objetos MIB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d60fe97debc7fd81b48a6daf0f5a955374546458
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171235"
---
# <a name="cim-class-qualifiers-for-mib-objects"></a><span data-ttu-id="15f28-103">Qualificadores de classe CIM para objetos MIB</span><span class="sxs-lookup"><span data-stu-id="15f28-103">CIM Class Qualifiers for MIB Objects</span></span>

<span data-ttu-id="15f28-104">O provedor SNMP usa os seguintes qualificadores de classe CIM ao mapear definições de objeto MIB para definições de classe CIM.</span><span class="sxs-lookup"><span data-stu-id="15f28-104">The SNMP Provider uses the following CIM class qualifiers when mapping MIB object definitions to CIM class definitions.</span></span> <span data-ttu-id="15f28-105">Um qualificador obrigatório deve estar presente para que o provedor SNMP resolva completamente um objeto de grupo.</span><span class="sxs-lookup"><span data-stu-id="15f28-105">A mandatory qualifier must be present for the SNMP Provider to fully resolve a group object.</span></span> <span data-ttu-id="15f28-106">Falha ao definir um qualificador obrigatório retorna um erro.</span><span class="sxs-lookup"><span data-stu-id="15f28-106">Failure to define a mandatory qualifier returns an error.</span></span> <span data-ttu-id="15f28-107">A especificação de um valor de qualificador inválido também retorna um erro.</span><span class="sxs-lookup"><span data-stu-id="15f28-107">Specifying an illegal qualifier value also returns an error.</span></span>

> [!Note]  
> <span data-ttu-id="15f28-108">Para obter mais informações sobre como instalar o provedor, consulte [Configurando o ambiente SNMP WMI](setting-up-the-wmi-snmp-environment.md).</span><span class="sxs-lookup"><span data-stu-id="15f28-108">For more information about installing the provider, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

 



| <span data-ttu-id="15f28-109">Qualificador</span><span class="sxs-lookup"><span data-stu-id="15f28-109">Qualifier</span></span>           | <span data-ttu-id="15f28-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="15f28-110">Description</span></span>                                                                                                                             |
|---------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="15f28-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="15f28-111">**Description**</span></span>     | <span data-ttu-id="15f28-112">**cadeia de caracteres** Adicional</span><span class="sxs-lookup"><span data-stu-id="15f28-112">**string** Optional</span></span><br/> <span data-ttu-id="15f28-113">Descrição da classe.</span><span class="sxs-lookup"><span data-stu-id="15f28-113">Description of the class.</span></span><br/>                                                                      |
| <span data-ttu-id="15f28-114">**ObjectID do grupo \_**</span><span class="sxs-lookup"><span data-stu-id="15f28-114">**Group\_Objectid**</span></span> | <span data-ttu-id="15f28-115">**cadeia de caracteres** Obrigatório, se a classe for para o provedor de classe SNMP.</span><span class="sxs-lookup"><span data-stu-id="15f28-115">**string** Mandatory, if the class is for the SNMP class provider.</span></span><br/> <span data-ttu-id="15f28-116">Identificador de objeto da coleção criei.</span><span class="sxs-lookup"><span data-stu-id="15f28-116">Object identifier of the fabricated collection.</span></span><br/> |
| <span data-ttu-id="15f28-117">**Importações de módulo \_**</span><span class="sxs-lookup"><span data-stu-id="15f28-117">**Module\_Imports**</span></span> | <span data-ttu-id="15f28-118">**cadeia de caracteres** Adicional</span><span class="sxs-lookup"><span data-stu-id="15f28-118">**string** Optional</span></span><br/> <span data-ttu-id="15f28-119">Lista separada por vírgulas de nomes de módulo MIB usados para resolver importações.</span><span class="sxs-lookup"><span data-stu-id="15f28-119">Comma-separated list of MIB module names used to resolve imports.</span></span><br/>                              |
| <span data-ttu-id="15f28-120">**Nome do módulo \_**</span><span class="sxs-lookup"><span data-stu-id="15f28-120">**Module\_Name**</span></span>    | <span data-ttu-id="15f28-121">**cadeia de caracteres** Adicional</span><span class="sxs-lookup"><span data-stu-id="15f28-121">**string** Optional</span></span><br/> <span data-ttu-id="15f28-122">Nome da identidade de um módulo MIB.</span><span class="sxs-lookup"><span data-stu-id="15f28-122">Identity name of a MIB module.</span></span><br/>                                                                 |
| <span data-ttu-id="15f28-123">**Referência**</span><span class="sxs-lookup"><span data-stu-id="15f28-123">**Reference**</span></span>       | <span data-ttu-id="15f28-124">**cadeia de caracteres** Adicional</span><span class="sxs-lookup"><span data-stu-id="15f28-124">**string** Optional</span></span><br/> <span data-ttu-id="15f28-125">Refere-se a outro documento que contém mais informações sobre a classe.</span><span class="sxs-lookup"><span data-stu-id="15f28-125">Refers to another document that contains more information about the class.</span></span><br/>                     |
| <span data-ttu-id="15f28-126">**Único**</span><span class="sxs-lookup"><span data-stu-id="15f28-126">**Singleton**</span></span>       | <span data-ttu-id="15f28-127">**Bool** Obrigatório para classes mapeadas de coleções escalares.</span><span class="sxs-lookup"><span data-stu-id="15f28-127">**Bool** Mandatory for classes mapped from scalar collections.</span></span><br/> <span data-ttu-id="15f28-128">Indica uma classe que só pode ter uma instância.</span><span class="sxs-lookup"><span data-stu-id="15f28-128">Indicates a class that can only have one instance.</span></span><br/>  |



 

 

 




