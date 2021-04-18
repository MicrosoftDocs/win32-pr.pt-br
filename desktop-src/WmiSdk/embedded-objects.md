---
description: Um objeto incorporado é um objeto de uma classe que existe dentro de uma declaração de classe ou instância de outra classe.
ms.assetid: 11a4556b-f682-4850-aedc-793602c5745b
ms.tgt_platform: multiple
title: Inserindo objetos em uma classe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39b94296a6869dddca7fd3df08739615a4a0c501
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105787782"
---
# <a name="embedding-objects-in-a-class"></a><span data-ttu-id="6e78b-103">Inserindo objetos em uma classe</span><span class="sxs-lookup"><span data-stu-id="6e78b-103">Embedding Objects in a Class</span></span>

<span data-ttu-id="6e78b-104">Um objeto incorporado é um objeto de uma classe que existe dentro de uma declaração de classe ou instância de outra classe.</span><span class="sxs-lookup"><span data-stu-id="6e78b-104">An embedded object is an object of a class that exists within a class or instance declaration of another class.</span></span> <span data-ttu-id="6e78b-105">Por exemplo, a classe [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) contém objetos inseridos do [**Win32 com \_ confiança**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) .</span><span class="sxs-lookup"><span data-stu-id="6e78b-105">For example, the [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) class contains [**Win32\_Trustee**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) embedded objects.</span></span> <span data-ttu-id="6e78b-106">Cada um dos objetos de **\_ confiança do Win32** contém um objeto do [**Win32 \_ Ace**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) .</span><span class="sxs-lookup"><span data-stu-id="6e78b-106">Each of the **Win32\_Trustee** objects contains a [**Win32\_ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) object.</span></span> <span data-ttu-id="6e78b-107">O WMI não limita a profundidade para a qual uma classe pode ter objetos incorporados.</span><span class="sxs-lookup"><span data-stu-id="6e78b-107">WMI does not limit the depth to which a class can have embedded objects.</span></span> <span data-ttu-id="6e78b-108">No entanto, usar outro design, como a criação de uma classe de associação, pode tornar um esquema mais gerenciável.</span><span class="sxs-lookup"><span data-stu-id="6e78b-108">However, using another design, such as creating an association class, may make a more manageable schema.</span></span>

<span data-ttu-id="6e78b-109">Para obter mais informações sobre objetos inseridos, consulte os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="6e78b-109">For more information about embedded objects, see the following topics:</span></span>

-   [<span data-ttu-id="6e78b-110">Criando objetos inseridos</span><span class="sxs-lookup"><span data-stu-id="6e78b-110">Creating Embedded Objects</span></span>](creating-embedded-objects.md)
-   [<span data-ttu-id="6e78b-111">Consultando objetos inseridos</span><span class="sxs-lookup"><span data-stu-id="6e78b-111">Querying Embedded Objects</span></span>](querying-embedded-objects.md)

## <a name="related-topics"></a><span data-ttu-id="6e78b-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6e78b-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6e78b-113">Criando classes formato MOF (MOF)</span><span class="sxs-lookup"><span data-stu-id="6e78b-113">Designing Managed Object Format (MOF) Classes</span></span>](designing-managed-object-format--mof--classes.md)
</dt> </dl>

 

 
