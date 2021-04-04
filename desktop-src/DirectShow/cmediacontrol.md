---
description: A classe CMediaControl fornece a manipulação de classe base dos métodos IDispatch da IMediaControl de interface dupla. Ele deixa como virtual pura as propriedades e métodos da Interface IMediaControl.
ms.assetid: 033a2de6-8046-408c-995f-ec2de6654c41
title: Classe CMediaControl
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaControl
api_type:
- COM
api_location: ''
ms.openlocfilehash: ae3a528263af4bd2fe5e4eccbe28793799c373a0
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "103837677"
---
# <a name="cmediacontrol-class"></a><span data-ttu-id="f8d65-104">Classe CMediaControl</span><span class="sxs-lookup"><span data-stu-id="f8d65-104">CMediaControl class</span></span>

![hierarquia de classe CMediaControl](images/cutil02.png)

<span data-ttu-id="f8d65-106">A `CMediaControl` classe fornece a manipulação de classe base dos métodos [**IDispatch**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) do [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol)de interface dupla.</span><span class="sxs-lookup"><span data-stu-id="f8d65-106">The `CMediaControl` class provides base class handling of the [**IDispatch**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) methods of the dual-interface [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol).</span></span> <span data-ttu-id="f8d65-107">Ele deixa como virtual pura as propriedades e métodos da interface **IMediaControl** .</span><span class="sxs-lookup"><span data-stu-id="f8d65-107">It leaves as pure virtual the properties and methods of the **IMediaControl** interface.</span></span>

<span data-ttu-id="f8d65-108">Normalmente, o Gerenciador do grafo de filtro é o único objeto que implementa a interface [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) .</span><span class="sxs-lookup"><span data-stu-id="f8d65-108">Typically, the filter graph manager is the only object that implements the [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) interface.</span></span> <span data-ttu-id="f8d65-109">(os filtros implementam a interface [**IMediaFilter**](/windows/desktop/api/Strmif/nn-strmif-imediafilter) , herdada por [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), para receber comandos de controle do Gerenciador de gráfico de filtro.) Portanto, essa biblioteca de classes é de uso limitado para filtrar os desenvolvedores.</span><span class="sxs-lookup"><span data-stu-id="f8d65-109">(filters implement the [**IMediaFilter**](/windows/desktop/api/Strmif/nn-strmif-imediafilter) interface, inherited by [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), to receive control commands from the filter graph manager.) Therefore, this class library is of limited use to filter developers.</span></span>

<span data-ttu-id="f8d65-110">As funções de membro [**CMediaControl:: GetIDsOfNames**](cmediacontrol-getidsofnames.md), [**CMediaControl:: GetTypeInfo**](cmediacontrol-gettypeinfo.md), [**CMediaControl:: GetTypeInfoCount**](cmediacontrol-gettypeinfocount.md)e [**CMediaControl:: Invoke**](cmediacontrol-invoke.md) são implementações padrão dos métodos [**IDispatch**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) usando a classe [**CBaseDispatch**](cbasedispatch.md) (e uma biblioteca de tipos) para analisar os comandos e passá-los para os métodos virtuais puros da interface [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) .</span><span class="sxs-lookup"><span data-stu-id="f8d65-110">The [**CMediaControl::GetIDsOfNames**](cmediacontrol-getidsofnames.md), [**CMediaControl::GetTypeInfo**](cmediacontrol-gettypeinfo.md), [**CMediaControl::GetTypeInfoCount**](cmediacontrol-gettypeinfocount.md), and [**CMediaControl::Invoke**](cmediacontrol-invoke.md) member functions are standard implementations of the [**IDispatch**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) methods using the [**CBaseDispatch**](cbasedispatch.md) class (and a type library) to parse the commands and pass them to the pure virtual methods of the [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) interface.</span></span>

<span data-ttu-id="f8d65-111">Os métodos [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) , definidos em Control. ODL, são deixados como virtuais puros.</span><span class="sxs-lookup"><span data-stu-id="f8d65-111">The [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) methods, defined in control.odl, are left as pure virtual.</span></span>



| <span data-ttu-id="f8d65-112">Funções de membro</span><span class="sxs-lookup"><span data-stu-id="f8d65-112">Member Functions</span></span>                                           | <span data-ttu-id="f8d65-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="f8d65-113">Description</span></span>                                                                                                                                                                                                                             |
|------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f8d65-114">**CMediaControl**</span><span class="sxs-lookup"><span data-stu-id="f8d65-114">**CMediaControl**</span></span>](cmediacontrol-cmediacontrol.md)       | <span data-ttu-id="f8d65-115">Constrói um objeto **CMediaControl** .</span><span class="sxs-lookup"><span data-stu-id="f8d65-115">Constructs a **CMediaControl** object.</span></span>                                                                                                                                                                                                  |
| <span data-ttu-id="f8d65-116">Métodos IDispatch</span><span class="sxs-lookup"><span data-stu-id="f8d65-116">IDispatch Methods</span></span>                                          | <span data-ttu-id="f8d65-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="f8d65-117">Description</span></span>                                                                                                                                                                                                                             |
| [<span data-ttu-id="f8d65-118">**GetIDsOfNames**</span><span class="sxs-lookup"><span data-stu-id="f8d65-118">**GetIDsOfNames**</span></span>](cmediacontrol-getidsofnames.md)       | <span data-ttu-id="f8d65-119">Mapeia um único membro e um conjunto opcional de parâmetros para um conjunto correspondente de identificadores de expedição de inteiro (DISPIDs), que podem ser usados durante as chamadas subsequentes para o método [**CMediaControl:: Invoke**](cmediacontrol-invoke.md) .</span><span class="sxs-lookup"><span data-stu-id="f8d65-119">Maps a single member and an optional set of parameters to a corresponding set of integer dispatch identifiers (DISPIDs), which can be used during subsequent calls to the [**CMediaControl::Invoke**](cmediacontrol-invoke.md) method.</span></span> |
| [<span data-ttu-id="f8d65-120">**GetTypeInfo**</span><span class="sxs-lookup"><span data-stu-id="f8d65-120">**GetTypeInfo**</span></span>](cmediacontrol-gettypeinfo.md)           | <span data-ttu-id="f8d65-121">Recupera um objeto Type-informations, que pode recuperar as informações de tipo de uma interface.</span><span class="sxs-lookup"><span data-stu-id="f8d65-121">Retrieves a type-information object, which can retrieve the type information for an interface.</span></span>                                                                                                                                          |
| [<span data-ttu-id="f8d65-122">**GetTypeInfoCount**</span><span class="sxs-lookup"><span data-stu-id="f8d65-122">**GetTypeInfoCount**</span></span>](cmediacontrol-gettypeinfocount.md) | <span data-ttu-id="f8d65-123">Recupera o número de interfaces de informações de tipo fornecidas por um objeto.</span><span class="sxs-lookup"><span data-stu-id="f8d65-123">Retrieves the number of type-information interfaces provided by an object.</span></span>                                                                                                                                                              |
| [<span data-ttu-id="f8d65-124">**Chame**</span><span class="sxs-lookup"><span data-stu-id="f8d65-124">**Invoke**</span></span>](cmediacontrol-invoke.md)                     | <span data-ttu-id="f8d65-125">Fornece acesso a propriedades e métodos expostos por um objeto.</span><span class="sxs-lookup"><span data-stu-id="f8d65-125">Provides access to properties and methods exposed by an object.</span></span>                                                                                                                                                                         |



 

 

 
