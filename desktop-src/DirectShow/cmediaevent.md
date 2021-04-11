---
description: A classe CMediaEvent fornece implementação de classe base dos métodos IDispatch da IMediaEvent de interface dupla. Ele deixa como virtual pura as propriedades e métodos da interface IMediaEvent.
ms.assetid: 849e08ac-8d1b-4c86-94eb-ab5c4f10d68a
title: Classe CMediaEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaEvent
api_type:
- COM
api_location: ''
ms.openlocfilehash: 927e561fa557ac33b1669ca7353377f7814ca448
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104172512"
---
# <a name="cmediaevent-class"></a><span data-ttu-id="9a73b-104">Classe CMediaEvent</span><span class="sxs-lookup"><span data-stu-id="9a73b-104">CMediaEvent class</span></span>

![hierarquia de classe CMediaEvent](images/cutil03.png)

<span data-ttu-id="9a73b-106">A `CMediaEvent` classe fornece a implementação de classe base dos métodos **IDispatch** do [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent)de interface dual.</span><span class="sxs-lookup"><span data-stu-id="9a73b-106">The `CMediaEvent` class provides base class implementation of the **IDispatch** methods of the dual-interface [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent).</span></span> <span data-ttu-id="9a73b-107">Ele deixa como virtual pura as propriedades e métodos da interface **IMediaEvent** .</span><span class="sxs-lookup"><span data-stu-id="9a73b-107">It leaves as pure virtual the properties and methods of the **IMediaEvent** interface.</span></span>

<span data-ttu-id="9a73b-108">A `CMediaEvent` classe também fornece a implementação de classe base da interface [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) que deriva de [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent).</span><span class="sxs-lookup"><span data-stu-id="9a73b-108">The `CMediaEvent` class also provides base class implementation of the [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) interface which derives from [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent).</span></span>

<span data-ttu-id="9a73b-109">As funções de membro [**CMediaEvent:: GetIDsOfNames**](cmediaevent-getidsofnames.md), [**CMediaEvent:: GetTypeInfo**](cmediaevent-gettypeinfo.md), [**CMediaEvent:: GetTypeInfoCount**](cmediaevent-gettypeinfocount.md)e [**CMediaEvent:: Invoke**](cmediaevent-invoke.md) são implementações padrão da interface **IDispatch** usando a classe [**CBaseDispatch**](cbasedispatch.md) (e uma biblioteca de tipos) para analisar os comandos e passá-los para os métodos virtuais puros da interface [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent) .</span><span class="sxs-lookup"><span data-stu-id="9a73b-109">The [**CMediaEvent::GetIDsOfNames**](cmediaevent-getidsofnames.md), [**CMediaEvent::GetTypeInfo**](cmediaevent-gettypeinfo.md), [**CMediaEvent::GetTypeInfoCount**](cmediaevent-gettypeinfocount.md), and [**CMediaEvent::Invoke**](cmediaevent-invoke.md) member functions are standard implementations of the **IDispatch** interface using the [**CBaseDispatch**](cbasedispatch.md) class (and a type library) to parse the commands and pass them to the pure virtual methods of the [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent) interface.</span></span>



| <span data-ttu-id="9a73b-110">Funções de membro</span><span class="sxs-lookup"><span data-stu-id="9a73b-110">Member Functions</span></span>                                         | <span data-ttu-id="9a73b-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="9a73b-111">Description</span></span>                                                                                                                                                                                   |
|----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9a73b-112">**CMediaEvent**</span><span class="sxs-lookup"><span data-stu-id="9a73b-112">**CMediaEvent**</span></span>](cmediaevent-cmediaevent.md)           | <span data-ttu-id="9a73b-113">Constrói um objeto **CMediaEvent** .</span><span class="sxs-lookup"><span data-stu-id="9a73b-113">Constructs a **CMediaEvent** object.</span></span>                                                                                                                                                          |
| <span data-ttu-id="9a73b-114">Métodos IDispatch</span><span class="sxs-lookup"><span data-stu-id="9a73b-114">IDispatch Methods</span></span>                                        | <span data-ttu-id="9a73b-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="9a73b-115">Description</span></span>                                                                                                                                                                                   |
| [<span data-ttu-id="9a73b-116">**GetIDsOfNames**</span><span class="sxs-lookup"><span data-stu-id="9a73b-116">**GetIDsOfNames**</span></span>](cmediaevent-getidsofnames.md)       | <span data-ttu-id="9a73b-117">Mapeia um único membro e um conjunto opcional de parâmetros para um conjunto correspondente de identificadores de expedição de inteiro, que podem ser usados durante as chamadas subsequentes para o método **IDispatch:: Invoke** .</span><span class="sxs-lookup"><span data-stu-id="9a73b-117">Maps a single member and an optional set of parameters to a corresponding set of integer dispatch identifiers, which can be used during subsequent calls to the **IDispatch::Invoke** method.</span></span> |
| [<span data-ttu-id="9a73b-118">**GetTypeInfo**</span><span class="sxs-lookup"><span data-stu-id="9a73b-118">**GetTypeInfo**</span></span>](cmediaevent-gettypeinfo.md)           | <span data-ttu-id="9a73b-119">Recupera um objeto Type-informations, que recupera as informações de tipo de uma interface.</span><span class="sxs-lookup"><span data-stu-id="9a73b-119">Retrieves a type-information object, which retrieves the type information for an interface.</span></span>                                                                                                   |
| [<span data-ttu-id="9a73b-120">**GetTypeInfoCount**</span><span class="sxs-lookup"><span data-stu-id="9a73b-120">**GetTypeInfoCount**</span></span>](cmediaevent-gettypeinfocount.md) | <span data-ttu-id="9a73b-121">Recupera o número de interfaces de informações de tipo fornecidas por um objeto.</span><span class="sxs-lookup"><span data-stu-id="9a73b-121">Retrieves the number of type-information interfaces provided by an object.</span></span>                                                                                                                    |
| [<span data-ttu-id="9a73b-122">**Chame**</span><span class="sxs-lookup"><span data-stu-id="9a73b-122">**Invoke**</span></span>](cmediaevent-invoke.md)                     | <span data-ttu-id="9a73b-123">Fornece acesso a propriedades e métodos expostos por um objeto.</span><span class="sxs-lookup"><span data-stu-id="9a73b-123">Provides access to properties and methods exposed by an object.</span></span>                                                                                                                               |



 

 

 



