---
title: Fornecendo informações de classe
description: Fornecendo informações de classe
ms.assetid: 808d9a39-4511-4aba-a23f-3c929970503b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc4505a12d4a7f50a605cbd04cae33805db2b19b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104084072"
---
# <a name="providing-class-information"></a><span data-ttu-id="d3f13-103">Fornecendo informações de classe</span><span class="sxs-lookup"><span data-stu-id="d3f13-103">Providing Class Information</span></span>

<span data-ttu-id="d3f13-104">Geralmente, é útil para um cliente de um objeto examinar as informações de tipo do objeto.</span><span class="sxs-lookup"><span data-stu-id="d3f13-104">It is often useful for a client of an object to examine the object's type information.</span></span> <span data-ttu-id="d3f13-105">Dado o CLSID do objeto, um cliente pode localizar a biblioteca de tipos do objeto usando entradas do registro e, em seguida, pode verificar a biblioteca de tipos para a entrada coclasse na biblioteca que corresponde ao CLSID.</span><span class="sxs-lookup"><span data-stu-id="d3f13-105">Given the object's CLSID, a client can locate the object's type library using registry entries and then can scan the type library for the coclass entry in the library matching the CLSID.</span></span>

<span data-ttu-id="d3f13-106">No entanto, nem todos os objetos têm um CLSID, embora ainda precisem fornecer informações de tipo.</span><span class="sxs-lookup"><span data-stu-id="d3f13-106">However, not all objects have a CLSID, although they still need to provide type information.</span></span> <span data-ttu-id="d3f13-107">Além disso, é conveniente que um cliente tenha uma maneira de simplesmente pedir a um objeto suas informações de tipo em vez de passar por todos os tédio para extrair as mesmas informações das entradas do registro.</span><span class="sxs-lookup"><span data-stu-id="d3f13-107">In addition, it is convenient for a client to have a way to simply ask an object for its type information instead of going through all the tedium to extract the same information from registry entries.</span></span> <span data-ttu-id="d3f13-108">Esse recurso é importante ao lidar com interfaces de saída em objetos conectáveis.</span><span class="sxs-lookup"><span data-stu-id="d3f13-108">This capability is important when dealing with outgoing interfaces on connectable objects.</span></span> <span data-ttu-id="d3f13-109">(Consulte [usando o IProvideClassInfo](using-iprovideclassinfo.md) para obter mais informações sobre como os objetos conectáveis fornecem esse recurso.)</span><span class="sxs-lookup"><span data-stu-id="d3f13-109">(See [Using IProvideClassInfo](using-iprovideclassinfo.md) for more information on how connectable objects provide this capability.)</span></span>

<span data-ttu-id="d3f13-110">Nesses casos, um cliente pode consultar o objeto para [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) ou [**IProvideClassInfo2**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo2).</span><span class="sxs-lookup"><span data-stu-id="d3f13-110">In these cases, a client can query the object for [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) or [**IProvideClassInfo2**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo2).</span></span> <span data-ttu-id="d3f13-111">Se essas interfaces existirem, o cliente chamará o método [**GetClassInfo**](/windows/desktop/api/OCIdl/nf-ocidl-iprovideclassinfo-getclassinfo) para obter as informações de tipo da interface.</span><span class="sxs-lookup"><span data-stu-id="d3f13-111">If these interfaces exist, the client calls the [**GetClassInfo**](/windows/desktop/api/OCIdl/nf-ocidl-iprovideclassinfo-getclassinfo) method to get the type information for the interface.</span></span>

<span data-ttu-id="d3f13-112">Ao implementar [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) ou [**IProvideClassInfo2**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo2), um objeto especifica que ele pode fornecer informações de tipo para sua classe inteira; ou seja, o que descreveria em sua seção coclass de sua biblioteca de tipos, se ela tiver uma.</span><span class="sxs-lookup"><span data-stu-id="d3f13-112">By implementing [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) or [**IProvideClassInfo2**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo2), an object specifies that it can provide type information for its entire class; that is, what it would describe in its coclass section of its type library, if it has one.</span></span> <span data-ttu-id="d3f13-113">[**GetClassInfo**](/windows/desktop/api/OCIdl/nf-ocidl-iprovideclassinfo-getclassinfo) retorna um ponteiro **ITypeInfo** correspondente às informações de coclasse do objeto.</span><span class="sxs-lookup"><span data-stu-id="d3f13-113">[**GetClassInfo**](/windows/desktop/api/OCIdl/nf-ocidl-iprovideclassinfo-getclassinfo) returns an **ITypeInfo** pointer corresponding to the object's coclass information.</span></span> <span data-ttu-id="d3f13-114">Por meio desse ponteiro **ITypeInfo** , o cliente pode examinar todas as definições de interface de entrada e saída do objeto.</span><span class="sxs-lookup"><span data-stu-id="d3f13-114">Through this **ITypeInfo** pointer, the client can examine all the object's incoming and outgoing interface definitions.</span></span>

<span data-ttu-id="d3f13-115">O objeto também pode fornecer [**IProvideClassInfo2**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo2).</span><span class="sxs-lookup"><span data-stu-id="d3f13-115">The object can also provide [**IProvideClassInfo2**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo2).</span></span> <span data-ttu-id="d3f13-116">A interface **IProvideClassInfo2** é uma extensão simples para [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) que torna rápido e fácil recuperar os identificadores de interface de saída de um objeto para seu conjunto de eventos padrão.</span><span class="sxs-lookup"><span data-stu-id="d3f13-116">The **IProvideClassInfo2** interface is a simple extension to [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) that makes it quick and easy to retrieve an object's outgoing interface identifiers for its default event set.</span></span> <span data-ttu-id="d3f13-117">**IProvideClassInfo2** é derivado de **IProvideClassInfo**.</span><span class="sxs-lookup"><span data-stu-id="d3f13-117">**IProvideClassInfo2** is derived from **IProvideClassInfo**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d3f13-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d3f13-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d3f13-119">Clientes e servidores COM</span><span class="sxs-lookup"><span data-stu-id="d3f13-119">COM Clients and Servers</span></span>](com-clients-and-servers.md)
</dt> </dl>

 

 




