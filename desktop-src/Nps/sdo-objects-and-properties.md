---
title: Objetos e propriedades
description: As características de um objeto no SDO são determinadas pelas propriedades do objeto e os valores associados a essas propriedades.
ms.assetid: 9faa7759-cad5-4429-94b0-6cba145cfadb
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efed7720388e61b9d6131acafd4b9bda17694d29
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105789627"
---
# <a name="objects-and-properties"></a><span data-ttu-id="e0796-103">Objetos e propriedades</span><span class="sxs-lookup"><span data-stu-id="e0796-103">Objects and Properties</span></span>

<span data-ttu-id="e0796-104">As características de um objeto no SDO são determinadas pelas propriedades do objeto e os valores associados a essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="e0796-104">The characteristics of an object in SDO are determined by the object's properties, and the values associated with those properties.</span></span> <span data-ttu-id="e0796-105">Ao contrário de alguns outros modelos de objeto, os objetos SDO em si não têm métodos.</span><span class="sxs-lookup"><span data-stu-id="e0796-105">Unlike some other object models, SDO objects themselves do not have methods.</span></span> <span data-ttu-id="e0796-106">No entanto, os objetos SDO expõem interfaces COM que fornecem métodos.</span><span class="sxs-lookup"><span data-stu-id="e0796-106">However, SDO objects do expose COM interfaces that provide methods.</span></span>

<span data-ttu-id="e0796-107">Os objetos em SDO expõem a interface [**ISdo**](/windows/desktop/api/sdoias/nn-sdoias-isdo) que fornece métodos para manipular as propriedades de objetos.</span><span class="sxs-lookup"><span data-stu-id="e0796-107">Objects in SDO expose the [**ISdo**](/windows/desktop/api/sdoias/nn-sdoias-isdo) interface that provides methods for manipulating the objects properties.</span></span> <span data-ttu-id="e0796-108">Para acessar as propriedades do objeto, obtenha uma interface **ISdo** para o objeto e use os métodos de interface [**GetProperty**](/windows/desktop/api/sdoias/nf-sdoias-isdo-getproperty) e [**putProperty**](/windows/desktop/api/sdoias/nf-sdoias-isdo-putproperty) para recuperar e definir valores para as propriedades.</span><span class="sxs-lookup"><span data-stu-id="e0796-108">To access the object's properties, obtain an **ISdo** interface for the object, and use the [**GetProperty**](/windows/desktop/api/sdoias/nf-sdoias-isdo-getproperty) and [**PutProperty**](/windows/desktop/api/sdoias/nf-sdoias-isdo-putproperty) interface methods to retrieve and set values for the properties.</span></span> <span data-ttu-id="e0796-109">O tópico [recuperando um usuário SDO contém um](/windows/desktop/Nps/sdo-retrieving-a-user-sdo) código de exemplo que demonstra a obtenção da interface **ISdo** para um objeto de usuário.</span><span class="sxs-lookup"><span data-stu-id="e0796-109">The topic [Retrieving a User SDO](/windows/desktop/Nps/sdo-retrieving-a-user-sdo) contains sample code that demonstrates obtaining the **ISdo** interface for a User object.</span></span>

<span data-ttu-id="e0796-110">Depois de fazer alterações nas propriedades de um objeto, use o método [**ISdo:: apply**](/windows/desktop/api/sdoias/nf-sdoias-isdo-apply) para gravar as alterações no armazenamento persistente do objeto.</span><span class="sxs-lookup"><span data-stu-id="e0796-110">After making changes to the properties of an object, use the [**ISdo::Apply**](/windows/desktop/api/sdoias/nf-sdoias-isdo-apply) method to write the changes to persistent storage for the object.</span></span> <span data-ttu-id="e0796-111">Você pode cancelar as alterações feitas nas propriedades de um objeto antes de chamar **ISdo:: apply** chamando o método [**ISdo:: Restore**](/windows/desktop/api/sdoias/nf-sdoias-isdo-restore) .</span><span class="sxs-lookup"><span data-stu-id="e0796-111">You can cancel changes made to an object's properties before you call **ISdo::Apply** by calling the [**ISdo::Restore**](/windows/desktop/api/sdoias/nf-sdoias-isdo-restore) method.</span></span> <span data-ttu-id="e0796-112">Esse método restaura os valores das propriedades de um objeto do armazenamento persistente.</span><span class="sxs-lookup"><span data-stu-id="e0796-112">This method restores the values of an object's properties from persistent storage.</span></span>

<span data-ttu-id="e0796-113">A tabela a seguir mostra os tipos de enumeração que enumeram as propriedades de alguns dos objetos em SDO.</span><span class="sxs-lookup"><span data-stu-id="e0796-113">The following table shows the enumeration types that enumerate the properties of some of the objects in SDO.</span></span>



| <span data-ttu-id="e0796-114">Objeto</span><span class="sxs-lookup"><span data-stu-id="e0796-114">Object</span></span>                                 | <span data-ttu-id="e0796-115">Tipo de enumeração</span><span class="sxs-lookup"><span data-stu-id="e0796-115">Enumeration type</span></span>                                       |
|----------------------------------------|--------------------------------------------------------|
| <span data-ttu-id="e0796-116">Todos os objetos SDO</span><span class="sxs-lookup"><span data-stu-id="e0796-116">All SDO objects</span></span>                        | [<span data-ttu-id="e0796-117">**IASCOMMONPROPERTIES**</span><span class="sxs-lookup"><span data-stu-id="e0796-117">**IASCOMMONPROPERTIES**</span></span>](/windows/desktop/api/sdoias/ne-sdoias-iascommonproperties) |
| <span data-ttu-id="e0796-118">Objeto de usuário</span><span class="sxs-lookup"><span data-stu-id="e0796-118">User Object</span></span>                            | [<span data-ttu-id="e0796-119">**USERproperties**</span><span class="sxs-lookup"><span data-stu-id="e0796-119">**USERPROPERTIES**</span></span>](/windows/desktop/api/sdoias/ne-sdoias-userproperties)           |
| <span data-ttu-id="e0796-120">Objeto de serviço (servidor de políticas de rede)</span><span class="sxs-lookup"><span data-stu-id="e0796-120">Service Object (Network Policy Server)</span></span> | [<span data-ttu-id="e0796-121">**IASPROPERTIES**</span><span class="sxs-lookup"><span data-stu-id="e0796-121">**IASPROPERTIES**</span></span>](/windows/desktop/api/sdoias/ne-sdoias-iasproperties)             |
| <span data-ttu-id="e0796-122">Objeto de protocolo RADIUS da Microsoft</span><span class="sxs-lookup"><span data-stu-id="e0796-122">Microsoft RADIUS Protocol Object</span></span>       | [<span data-ttu-id="e0796-123">**RADIUSproperties**</span><span class="sxs-lookup"><span data-stu-id="e0796-123">**RADIUSPROPERTIES**</span></span>](/windows/desktop/api/sdoias/ne-sdoias-radiusproperties)       |



 

> [!Note]  
> <span data-ttu-id="e0796-124">O IAS (serviço de autenticação da Internet) foi renomeado como NPS (servidor de políticas de rede) a partir do Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="e0796-124">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.</span></span>

 

## <a name="collections"></a><span data-ttu-id="e0796-125">Coleções</span><span class="sxs-lookup"><span data-stu-id="e0796-125">Collections</span></span>

<span data-ttu-id="e0796-126">Os objetos geralmente são agrupados em coleções.</span><span class="sxs-lookup"><span data-stu-id="e0796-126">Objects are often grouped into collections.</span></span> <span data-ttu-id="e0796-127">A API de SDO fornece funcionalidade, por meio da interface de [**coleção ISdo**](/windows/desktop/api/sdoias/nn-sdoias-isdocollection) , para enumerar os objetos em uma coleção e para adicionar e excluir objetos de uma coleção.</span><span class="sxs-lookup"><span data-stu-id="e0796-127">The SDO API provides functionality, through the [**ISdo Collection**](/windows/desktop/api/sdoias/nn-sdoias-isdocollection) interface, to enumerate the objects in a collection and to add and delete objects from a collection.</span></span>

<span data-ttu-id="e0796-128">O acesso a uma coleção é obtido pela recuperação de uma propriedade de coleção no objeto que contém a coleção.</span><span class="sxs-lookup"><span data-stu-id="e0796-128">Access to a collection is obtained by retrieving a collection property on the object that contains the collection.</span></span> <span data-ttu-id="e0796-129">Para obter mais informações, consulte a seção [hierarquia de modelo de objeto](/windows/desktop/Nps/sdo-object-model-hierarchy).</span><span class="sxs-lookup"><span data-stu-id="e0796-129">For more information, see the section [Object Model Hierarchy](/windows/desktop/Nps/sdo-object-model-hierarchy).</span></span>

<span data-ttu-id="e0796-130">O tipo de dados para todas as propriedades que correspondem às coleções é expedição de VT \_ .</span><span class="sxs-lookup"><span data-stu-id="e0796-130">The data type for all properties that correspond to collections is VT\_DISPATCH.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e0796-131">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e0796-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e0796-132">Hierarquia de modelo de objeto SDO</span><span class="sxs-lookup"><span data-stu-id="e0796-132">SDO Object Model Hierarchy</span></span>](/windows/desktop/Nps/sdo-object-model-hierarchy)
</dt> <dt>

[<span data-ttu-id="e0796-133">Atributos com suporte a SDO</span><span class="sxs-lookup"><span data-stu-id="e0796-133">SDO Supported Attributes</span></span>](/windows/desktop/Nps/sdo-sdo-supported-attributes)
</dt> </dl>

 

 