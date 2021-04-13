---
title: Obtendo propriedades de contabilidade
description: O objeto de contabilidade é um dos objetos na coleção de manipuladores de solicitação.
ms.assetid: eb5c8606-d3f0-4c33-9035-7b7b1369cb0d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9911397c1de3521ccb5a275405416d8b88c1fa6f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366293"
---
# <a name="obtaining-accounting-properties"></a><span data-ttu-id="3bc00-103">Obtendo propriedades de contabilidade</span><span class="sxs-lookup"><span data-stu-id="3bc00-103">Obtaining Accounting Properties</span></span>

> [!Note]  
> <span data-ttu-id="3bc00-104">O IAS (serviço de autenticação da Internet) foi renomeado como NPS (servidor de políticas de rede) a partir do Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="3bc00-104">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.</span></span> <span data-ttu-id="3bc00-105">O conteúdo deste tópico aplica-se ao IAS e ao NPS.</span><span class="sxs-lookup"><span data-stu-id="3bc00-105">The content of this topic applies to both IAS and NPS.</span></span> <span data-ttu-id="3bc00-106">Em todo o texto, o NPS é usado para fazer referência a todas as versões do serviço, incluindo as versões originalmente chamadas de IAS.</span><span class="sxs-lookup"><span data-stu-id="3bc00-106">Throughout the text, NPS is used to refer to all versions of the service, including the versions originally referred to as IAS.</span></span>

 

<span data-ttu-id="3bc00-107">O objeto de contabilidade é um dos objetos na coleção de manipuladores de solicitação.</span><span class="sxs-lookup"><span data-stu-id="3bc00-107">The accounting object is one of the objects in the Request Handlers collection.</span></span> <span data-ttu-id="3bc00-108">O valor de enumeração para a coleção de manipuladores de solicitação é a **propriedade \_ REQUESTHANDLERS do IAS \_ \_**.</span><span class="sxs-lookup"><span data-stu-id="3bc00-108">The enumeration value for the request handlers collection is **PROPERTY\_IAS\_REQUESTHANDLERS\_COLLECTION**.</span></span> <span data-ttu-id="3bc00-109">O nome do manipulador para o objeto de contabilidade é "Microsoft Accounting".</span><span class="sxs-lookup"><span data-stu-id="3bc00-109">The name of the handler for the accounting object is "Microsoft Accounting".</span></span>

<span data-ttu-id="3bc00-110">O código de Visual Basic a seguir acessa as propriedades disponíveis do manipulador de objeto de contabilidade.</span><span class="sxs-lookup"><span data-stu-id="3bc00-110">The following Visual Basic code accesses the properties available from the accounting object handler.</span></span>


```VB
Set sdoRequestHandler = sdoCollRequestHandlers.Item("Microsoft Accounting")
vtTemp = sdoRequestHandler.GetProperty(PROPERTY_ACCOUNTING_LOG_ACCOUNTING)
vtTemp = sdoRequestHandler.GetProperty(PROPERTY_ACCOUNTING_LOG_ACCOUNTING_INTERIM)
vtTemp = sdoRequestHandler.GetProperty(PROPERTY_ACCOUNTING_LOG_AUTHENTICATION)
vtTemp = sdoRequestHandler.GetProperty(PROPERTY_ACCOUNTING_LOG_FILE_DIRECTORY)
vtTemp = sdoRequestHandler.GetProperty(PROPERTY_ACCOUNTING_LOG_IAS1_FORMAT)
vtTemp = sdoRequestHandler.GetProperty(PROPERTY_ACCOUNTING_LOG_OPEN_NEW_FREQUENCY)
vtTemp = sdoRequestHandler.GetProperty(PROPERTY_ACCOUNTING_LOG_OPEN_NEW_SIZE)
```



<span data-ttu-id="3bc00-111">Para acessar as propriedades de contabilidade usando C++, primeiro obtenha a coleção de manipuladores de solicitação.</span><span class="sxs-lookup"><span data-stu-id="3bc00-111">To access the accounting properties using C++, first obtain the request handlers collection.</span></span> <span data-ttu-id="3bc00-112">A [recuperação de uma coleção contém um](/windows/desktop/Nps/sdo-retrieving-a-collection) código C++ que demonstra como obter uma coleção.</span><span class="sxs-lookup"><span data-stu-id="3bc00-112">The [Retrieving a Collection](/windows/desktop/Nps/sdo-retrieving-a-collection) contains C++ code that demonstrates how to obtain a collection.</span></span> <span data-ttu-id="3bc00-113">O valor de enumeração para a coleção de manipuladores de solicitação é a **propriedade \_ REQUESTHANDLERS do IAS \_ \_**.</span><span class="sxs-lookup"><span data-stu-id="3bc00-113">The enumeration value for the request handlers collection is **PROPERTY\_IAS\_REQUESTHANDLERS\_COLLECTION**.</span></span> <span data-ttu-id="3bc00-114">(Os valores correspondentes às várias coleções de NPS são enumerados pelo tipo de enumeração [**IASPROPERTIES**](/windows/desktop/api/sdoias/ne-sdoias-iasproperties) .)</span><span class="sxs-lookup"><span data-stu-id="3bc00-114">(The values corresponding to the various NPS collections are enumerated by the [**IASPROPERTIES**](/windows/desktop/api/sdoias/ne-sdoias-iasproperties) enumeration type.)</span></span>

<span data-ttu-id="3bc00-115">A coleção de manipuladores de solicitação contém um objeto chamado "Microsoft Accounting".</span><span class="sxs-lookup"><span data-stu-id="3bc00-115">The request handlers collection contains an object named "Microsoft Accounting".</span></span> <span data-ttu-id="3bc00-116">Recupere este objeto da coleção.</span><span class="sxs-lookup"><span data-stu-id="3bc00-116">Retrieve this object from the collection.</span></span> <span data-ttu-id="3bc00-117">A seção [recuperando um objeto de uma coleção](/windows/desktop/Nps/sdo-retrieving-an-object-from-a-collection) contém um código C++ que demonstra como obter um objeto de uma coleção.</span><span class="sxs-lookup"><span data-stu-id="3bc00-117">The section [Retrieving an Object from a Collection](/windows/desktop/Nps/sdo-retrieving-an-object-from-a-collection) contains C++ code that demonstrates how to obtain an object from a collection.</span></span>

<span data-ttu-id="3bc00-118">Depois que você tiver o objeto Microsoft Accounting, obtenha uma interface [**ISdo**](/windows/desktop/api/sdoias/nn-sdoias-isdo) para o objeto usando [**IUnknown:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)).</span><span class="sxs-lookup"><span data-stu-id="3bc00-118">Once you have the Microsoft Accounting object, obtain an [**ISdo**](/windows/desktop/api/sdoias/nn-sdoias-isdo) interface for the object using [**IUnknown::QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)).</span></span> <span data-ttu-id="3bc00-119">A seção [recuperando um usuário SDO](/windows/desktop/Nps/sdo-retrieving-a-user-sdo) contém um código C++ que demonstra como obter uma interface **ISdo** para um objeto.</span><span class="sxs-lookup"><span data-stu-id="3bc00-119">The section [Retrieving a User SDO](/windows/desktop/Nps/sdo-retrieving-a-user-sdo) contains C++ code that demonstrates how obtain an **ISdo** interface for an object.</span></span> <span data-ttu-id="3bc00-120">Em seguida, você pode usar o método [**ISdo:: GetProperty**](/windows/desktop/api/sdoias/nf-sdoias-isdo-getproperty) para obter valores de propriedade para o objeto Microsoft Accounting.</span><span class="sxs-lookup"><span data-stu-id="3bc00-120">You can then use the [**ISdo::GetProperty**](/windows/desktop/api/sdoias/nf-sdoias-isdo-getproperty) method to obtain property values for the Microsoft Accounting object.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3bc00-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3bc00-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3bc00-122">Recuperando uma coleção</span><span class="sxs-lookup"><span data-stu-id="3bc00-122">Retrieving a Collection</span></span>](/windows/desktop/Nps/sdo-retrieving-a-collection)
</dt> <dt>

[<span data-ttu-id="3bc00-123">Recuperando um objeto de uma coleção</span><span class="sxs-lookup"><span data-stu-id="3bc00-123">Retrieving an Object from a Collection</span></span>](/windows/desktop/Nps/sdo-retrieving-an-object-from-a-collection)
</dt> <dt>

[<span data-ttu-id="3bc00-124">Recuperando um SDO de usuário</span><span class="sxs-lookup"><span data-stu-id="3bc00-124">Retrieving a User SDO</span></span>](/windows/desktop/Nps/sdo-retrieving-a-user-sdo)
</dt> <dt>

[<span data-ttu-id="3bc00-125">**ISdo**</span><span class="sxs-lookup"><span data-stu-id="3bc00-125">**ISdo**</span></span>](/windows/desktop/api/sdoias/nn-sdoias-isdo)
</dt> <dt>

<span data-ttu-id="3bc00-126">[**IUnknown:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span><span class="sxs-lookup"><span data-stu-id="3bc00-126">[**IUnknown::QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span></span>
</dt> <dt>

[<span data-ttu-id="3bc00-127">**IASPROPERTIES**</span><span class="sxs-lookup"><span data-stu-id="3bc00-127">**IASPROPERTIES**</span></span>](/windows/desktop/api/sdoias/ne-sdoias-iasproperties)
</dt> </dl>

 

 