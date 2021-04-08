---
description: Um aplicativo de gerenciamento que usa o provedor de registro do sistema pode definir classes com propriedades que representam dados de registro para chaves específicas e, em seguida, armazena as classes no repositório do WMI.
ms.assetid: e8707a3d-a393-4be0-9e86-297f0af15d99
ms.tgt_platform: multiple
title: Definindo classes para o provedor de registro do sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ebce4867559398722182b7b77ae02bc31c070b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922283"
---
# <a name="defining-classes-for-the-system-registry-provider"></a><span data-ttu-id="2d8fd-103">Definindo classes para o provedor de registro do sistema</span><span class="sxs-lookup"><span data-stu-id="2d8fd-103">Defining Classes for the System Registry Provider</span></span>

<span data-ttu-id="2d8fd-104">Um aplicativo de gerenciamento que usa o provedor de registro do sistema pode definir classes com propriedades que representam dados de registro para chaves específicas e, em seguida, armazena as classes no repositório do WMI.</span><span class="sxs-lookup"><span data-stu-id="2d8fd-104">A management application using the System Registry provider can define classes with properties that represent registry data for particular keys and then stores the classes in the WMI repository.</span></span> <span data-ttu-id="2d8fd-105">A maioria dos processos para definir uma classe para o registro do sistema é idêntica à definição de qualquer outra classe.</span><span class="sxs-lookup"><span data-stu-id="2d8fd-105">Most of the processes for defining a class for the system registry is identical to defining any other class.</span></span> <span data-ttu-id="2d8fd-106">No entanto, o provedor de registro do sistema requer que você use tipos de dados e qualificadores específicos.</span><span class="sxs-lookup"><span data-stu-id="2d8fd-106">However, the System Registry provider requires that you use specific data types and qualifiers.</span></span>

<span data-ttu-id="2d8fd-107">O procedimento a seguir descreve como definir uma classe para o provedor de registro do sistema.</span><span class="sxs-lookup"><span data-stu-id="2d8fd-107">The following procedure describes how to define a class for the System Registry provider.</span></span>

<span data-ttu-id="2d8fd-108">**Para definir uma classe para o provedor de registro do sistema**</span><span class="sxs-lookup"><span data-stu-id="2d8fd-108">**To define a class for the System Registry provider**</span></span>

1.  <span data-ttu-id="2d8fd-109">Crie a classe como você faria com qualquer outra classe.</span><span class="sxs-lookup"><span data-stu-id="2d8fd-109">Create the class as you would any other class.</span></span>

    <span data-ttu-id="2d8fd-110">Para obter mais informações, consulte [criando uma classe](creating-a-class.md).</span><span class="sxs-lookup"><span data-stu-id="2d8fd-110">For more information, see [Creating a Class](creating-a-class.md).</span></span>

2.  <span data-ttu-id="2d8fd-111">Mapeie os tipos de dados do registro apropriados para os tipos apropriados do WMI.</span><span class="sxs-lookup"><span data-stu-id="2d8fd-111">Map the appropriate registry data types to the appropriate WMI types.</span></span>

    <span data-ttu-id="2d8fd-112">O provedor de registro do sistema mapeia os tipos de dados do registro para tipos de dados específicos do WMI.</span><span class="sxs-lookup"><span data-stu-id="2d8fd-112">The System Registry provider maps the registry data types to specific WMI data types.</span></span> <span data-ttu-id="2d8fd-113">Para obter mais informações, consulte [mapeando um tipo de dados do registro para um tipo de dados do WMI](mapping-a-registry-data-type-to-a-wmi-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="2d8fd-113">For more information, see [Mapping a Registry Data Type to a WMI Data Type](mapping-a-registry-data-type-to-a-wmi-data-type.md).</span></span>

3.  <span data-ttu-id="2d8fd-114">Use os qualificadores necessários para definir o local do provedor de registro e o local da chave do registro apropriada.</span><span class="sxs-lookup"><span data-stu-id="2d8fd-114">Use the required qualifiers to define the location of the Registry provider and the location of the appropriate registry key.</span></span>

    <span data-ttu-id="2d8fd-115">O provedor de registro do sistema usa três qualificadores para definir o local de várias classes, provedores e entradas de registro.</span><span class="sxs-lookup"><span data-stu-id="2d8fd-115">The System Registry provider uses three qualifiers to define the location of various classes, providers, and registry entries.</span></span> <span data-ttu-id="2d8fd-116">Para obter mais informações, consulte [definindo uma classe de registro com qualificadores](defining-a-registry-class-with-qualifiers.md).</span><span class="sxs-lookup"><span data-stu-id="2d8fd-116">For more information, see [Defining a Registry Class With Qualifiers](defining-a-registry-class-with-qualifiers.md).</span></span>

 

 



