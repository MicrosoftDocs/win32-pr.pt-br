---
title: Coleções e grupos
description: A ADSI usa objetos de coleção para representar qualquer conjunto arbitrário de itens em um serviço de diretório que pode ser representado usando o mesmo tipo de dados.
ms.assetid: 03257cc9-f354-4e1c-8880-936a7acac3ef
ms.tgt_platform: multiple
keywords:
- ADSI ADSI, usando, coleções e grupos
- ADSI de coleções
- ADSI de grupos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9f0f4d699d8dde0c3d70c7449dfe146212b2b30
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103917664"
---
# <a name="collections-and-groups"></a><span data-ttu-id="766a4-106">Coleções e grupos</span><span class="sxs-lookup"><span data-stu-id="766a4-106">Collections and Groups</span></span>

<span data-ttu-id="766a4-107">A ADSI usa objetos de coleção para representar qualquer conjunto arbitrário de itens em um serviço de diretório que pode ser representado usando o mesmo tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="766a4-107">ADSI uses collection objects to represent any arbitrary set of items in a directory service that can be represented using the same data type.</span></span> <span data-ttu-id="766a4-108">Os objetos de coleção são definidos como um conjunto de valores **variantes** , representando qualquer um dos tipos de dados de automação válidos.</span><span class="sxs-lookup"><span data-stu-id="766a4-108">Collection objects are defined as a set of **VARIANT** values, representing any of the valid Automation data types.</span></span> <span data-ttu-id="766a4-109">Os objetos de coleção podem representar informações persistentes, como listas de controle de acesso e informações voláteis, como trabalhos de impressão em uma fila de impressão.</span><span class="sxs-lookup"><span data-stu-id="766a4-109">Collection objects can represent both persistent information such as access-control lists and volatile information such as print jobs in a print queue.</span></span>

<span data-ttu-id="766a4-110">A Convenção COM padrão para listar o conteúdo de um objeto de coleção (ou contêiner) é criar um objeto enumerador que dê suporte a [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant), que tem métodos para percorrer a lista de objetos de coleção.</span><span class="sxs-lookup"><span data-stu-id="766a4-110">The standard COM convention for listing the contents of a collection (or container) object is to create an enumerator object that supports [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant), which has methods to step through the list of collection objects.</span></span> <span data-ttu-id="766a4-111">As interfaces na ADSI que fornecem o método **Get \_ \_ NewEnum** (Observe os dois sublinhados) são [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer), [**IADsMembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers) e [**iadscollection**](/windows/desktop/api/Iads/nn-iads-iadscollection).</span><span class="sxs-lookup"><span data-stu-id="766a4-111">The interfaces in ADSI that supply the **get\_\_NewEnum** method (note the two underscores) are [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer), [**IADsMembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers) and [**IADsCollection**](/windows/desktop/api/Iads/nn-iads-iadscollection).</span></span> <span data-ttu-id="766a4-112">A ADSI também fornece às funções auxiliares [**ADsBuildEnumerator**](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildenumerator) e [**ADsEnumerateNext**](/windows/desktop/api/Adshlp/nf-adshlp-adsenumeratenext) para programas C e C++ para simplificar a enumeração.</span><span class="sxs-lookup"><span data-stu-id="766a4-112">ADSI also supplies the helper functions [**ADsBuildEnumerator**](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildenumerator) and [**ADsEnumerateNext**](/windows/desktop/api/Adshlp/nf-adshlp-adsenumeratenext) for C and C++ programs to simplify enumeration.</span></span> <span data-ttu-id="766a4-113">Os clientes de automação usam a enumeração implicitamente quando chamam o **próximo** em um loop **for** .</span><span class="sxs-lookup"><span data-stu-id="766a4-113">Automation clients use enumeration implicitly when they call **Next** in a **For** loop.</span></span>

<span data-ttu-id="766a4-114">Os grupos são apenas coleções de objetos que dão suporte à interface [**IADsMembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers) .</span><span class="sxs-lookup"><span data-stu-id="766a4-114">Groups are simply collections of objects supporting the [**IADsMembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers) interface.</span></span>

 

 