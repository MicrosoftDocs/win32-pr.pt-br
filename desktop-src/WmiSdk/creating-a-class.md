---
description: No WMI, uma classe é um objeto que descreve algum aspecto de uma empresa, como um tipo especial de unidade de disco.
ms.assetid: 06b75910-f126-48b6-8e43-4a9ed4661732
ms.tgt_platform: multiple
title: Criando uma classe WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2274252715ce44b9d2b79e398c945ca723fe3f7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105758664"
---
# <a name="creating-a-wmi-class"></a><span data-ttu-id="67181-103">Criando uma classe WMI</span><span class="sxs-lookup"><span data-stu-id="67181-103">Creating a WMI Class</span></span>

<span data-ttu-id="67181-104">No WMI, uma classe é um objeto que descreve algum aspecto de uma empresa, como um tipo especial de unidade de disco.</span><span class="sxs-lookup"><span data-stu-id="67181-104">In WMI, a class is an object that describes some aspect of an enterprise, such as a special type of disk drive.</span></span> <span data-ttu-id="67181-105">Depois de criar uma definição de classe, grave seu provedor DLL para fornecer instâncias da classe, dados de propriedade e métodos de execução definidos para a classe.</span><span class="sxs-lookup"><span data-stu-id="67181-105">After you have created a class definition, write your provider DLL to supply instances of the class, property data, and execute methods defined for the class.</span></span> <span data-ttu-id="67181-106">Scripts e aplicativos podem então obter dados ou controlar o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="67181-106">Scripts and applications can then obtain data or control the device.</span></span> <span data-ttu-id="67181-107">Para obter mais informações, consulte [desenvolvendo um provedor WMI](developing-a-wmi-provider.md).</span><span class="sxs-lookup"><span data-stu-id="67181-107">For more information, see [Developing a WMI Provider](developing-a-wmi-provider.md).</span></span>

> [!Note]  
> <span data-ttu-id="67181-108">Para garantir que todas as suas definições de classe WMI para objetos gerenciados sejam restauradas no [*repositório do WMI*](gloss-w.md) se o WMI tiver uma falha e for reiniciado, use a instrução de pré-processador de instrução de [**\# AutoRecuperação pragma**](pragma-autorecover.md) em seu arquivo MOF.</span><span class="sxs-lookup"><span data-stu-id="67181-108">To ensure that all your WMI class definitions for managed objects are restored to the [*WMI repository*](gloss-w.md) if WMI has a failure and restarts, use the [**\#pragma autorecover**](pragma-autorecover.md) statement preprocessor instruction in your MOF file.</span></span>

 

## <a name="base-class"></a><span data-ttu-id="67181-109">Classe base</span><span class="sxs-lookup"><span data-stu-id="67181-109">Base Class</span></span>

<span data-ttu-id="67181-110">Uma classe base representa algum conceito geral.</span><span class="sxs-lookup"><span data-stu-id="67181-110">A base class represents some general concept.</span></span> <span data-ttu-id="67181-111">Por exemplo, a classe [**CIM \_ CDROMDrive**](/windows/desktop/CIMWin32Prov/cim-cdromdrive) representa todos os tipos de unidades de CD-ROM no WMI e contém propriedades gerais que descrevem todos os tipos de unidades de CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="67181-111">For example, the [**CIM\_CDROMDrive**](/windows/desktop/CIMWin32Prov/cim-cdromdrive) class represents all types of CD-ROM drives in WMI, and contains general properties that describe all kinds of CD-ROM drives.</span></span> <span data-ttu-id="67181-112">Para obter mais informações, consulte [criando uma classe base](creating-a-base-class.md).</span><span class="sxs-lookup"><span data-stu-id="67181-112">For more information, see [Creating a Base Class](creating-a-base-class.md).</span></span>

<span data-ttu-id="67181-113">Uma classe derivada herda propriedades e métodos de outra classe.</span><span class="sxs-lookup"><span data-stu-id="67181-113">A derived class inherits properties and methods from another class.</span></span> <span data-ttu-id="67181-114">Uma classe derivada geralmente representa um caso específico de uma classe base.</span><span class="sxs-lookup"><span data-stu-id="67181-114">A derived class usually represents a specific case of a base class.</span></span> <span data-ttu-id="67181-115">Por exemplo, a classe [**Win32 \_ CDROMDrive**](/windows/desktop/CIMWin32Prov/win32-cdromdrive) representa uma unidade de CD-ROM em um sistema Windows.</span><span class="sxs-lookup"><span data-stu-id="67181-115">For example, the [**Win32\_CDROMDrive**](/windows/desktop/CIMWin32Prov/win32-cdromdrive) class represents a CD-ROM drive on a Windows system.</span></span> <span data-ttu-id="67181-116">A classe **Win32 \_ CDROMDrive** baseia-se em e herda muitas propriedades de [**CIM \_ CDROMDrive**](/windows/desktop/CIMWin32Prov/cim-cdromdrive).</span><span class="sxs-lookup"><span data-stu-id="67181-116">The **Win32\_CDROMDrive** class is based on and inherits many of properties from [**CIM\_CDROMDrive**](/windows/desktop/CIMWin32Prov/cim-cdromdrive).</span></span> <span data-ttu-id="67181-117">No entanto, o **Win32 \_ CDROMDrive**, como outras classes derivadas, pode ter propriedades adicionais que tornam a classe derivada exclusiva.</span><span class="sxs-lookup"><span data-stu-id="67181-117">However, **Win32\_CDROMDrive**, like other derived classes, can have additional properties that make the derived class unique.</span></span> <span data-ttu-id="67181-118">Para obter mais informações, consulte [criando uma classe derivada](creating-a-derived-class.md).</span><span class="sxs-lookup"><span data-stu-id="67181-118">For more information, see [Creating a Derived Class](creating-a-derived-class.md).</span></span>

## <a name="properties-and-methods"></a><span data-ttu-id="67181-119">Propriedades e métodos</span><span class="sxs-lookup"><span data-stu-id="67181-119">Properties and Methods</span></span>

<span data-ttu-id="67181-120">Criar uma classe significa definir as propriedades que descrevem essa classe.</span><span class="sxs-lookup"><span data-stu-id="67181-120">Creating a class means defining the properties that describe that class.</span></span> <span data-ttu-id="67181-121">Você também pode definir métodos que manipulam o objeto representado pela classe.</span><span class="sxs-lookup"><span data-stu-id="67181-121">You can also define methods that manipulate the object represented by the class.</span></span>

<span data-ttu-id="67181-122">Geralmente, uma propriedade representa um aspecto do objeto, como um número de série para um dispositivo ou um tamanho em bytes para um processo, enquanto um método representa uma ação que altera o estado ou o comportamento do dispositivo ou da entidade lógica.</span><span class="sxs-lookup"><span data-stu-id="67181-122">Generally, a property represents an aspect of the object, such as a serial number for a device or a size in bytes for a process, while a method represents an action that changes the state or behavior of the device or logical entity.</span></span>

<span data-ttu-id="67181-123">Cada classe deve ter pelo menos uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="67181-123">Each class must have at least one key property.</span></span> <span data-ttu-id="67181-124">Embora uma classe possa ter várias chaves, você não pode criar uma instância de uma classe com mais de 256 chaves.</span><span class="sxs-lookup"><span data-stu-id="67181-124">While a class may have multiple keys, you cannot create an instance of a class with more than 256 keys.</span></span>

## <a name="related-topics"></a><span data-ttu-id="67181-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="67181-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="67181-126">Criando classes formato MOF (MOF)</span><span class="sxs-lookup"><span data-stu-id="67181-126">Designing Managed Object Format (MOF) Classes</span></span>](designing-managed-object-format--mof--classes.md)
</dt> </dl>

 

 
