---
title: Localizando um objeto remoto
description: Localizando um objeto remoto
ms.assetid: b329de53-646b-42a2-afa3-06473c3483d6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d0ce1b2280faaed7be3b5afb25a48438ff1a2b7
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103824024"
---
# <a name="locating-a-remote-object"></a><span data-ttu-id="1c32e-103">Localizando um objeto remoto</span><span class="sxs-lookup"><span data-stu-id="1c32e-103">Locating a Remote Object</span></span>

<span data-ttu-id="1c32e-104">Com o advento do COM para sistemas distribuídos, o COM usa o modelo básico para a criação de objetos descritos em [objetos de classe com e CLSIDs](com-class-objects-and-clsids.md) e adiciona mais de uma maneira de localizar um objeto que pode residir em outro sistema em uma rede, sem sobrecarregar o aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="1c32e-104">With the advent of COM for distributed systems, COM uses the basic model for object creation described in [COM Class Objects and CLSIDs](com-class-objects-and-clsids.md) and adds more than one way to locate an object that might reside on another system in a network, without overburdening the client application.</span></span>

<span data-ttu-id="1c32e-105">COM adicionou chaves do registro que permitem que um servidor Registre o nome do computador no qual ele reside ou o computador onde um armazenamento existente está localizado.</span><span class="sxs-lookup"><span data-stu-id="1c32e-105">COM has added registry keys that permit a server to register the name of the machine on which it resides or the machine where an existing storage is located.</span></span> <span data-ttu-id="1c32e-106">Portanto, os aplicativos cliente precisam saber apenas o CLSID do servidor.</span><span class="sxs-lookup"><span data-stu-id="1c32e-106">Therefore, client applications need know only the CLSID of the server.</span></span>

<span data-ttu-id="1c32e-107">No entanto, para casos em que é desejado, o COM substituiu um parâmetro anteriormente reservado de [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) por uma estrutura [**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo) , que permite que um cliente especifique o local de um servidor.</span><span class="sxs-lookup"><span data-stu-id="1c32e-107">However, for cases where it is desired, COM has replaced a previously reserved parameter of [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) with a [**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo) structure, which allows a client to specify the location of a server.</span></span> <span data-ttu-id="1c32e-108">Outro valor importante na função **CoGetClassObject** é a enumeração [**CLSCTX**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx) , que especifica se o objeto esperado deve ser executado no processo, fora do processo local ou remoto fora do processo de execução.</span><span class="sxs-lookup"><span data-stu-id="1c32e-108">Another important value in the **CoGetClassObject** function is the [**CLSCTX**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx) enumeration, which specifies whether the expected object is to be run in-process, out-of-process local, or out-of-process remote.</span></span> <span data-ttu-id="1c32e-109">Juntos, esses dois valores e os valores no registro determinam como e onde o objeto deve ser executado.</span><span class="sxs-lookup"><span data-stu-id="1c32e-109">Taken together, these two values and the values in the registry determine how and where the object is to be run.</span></span>

> [!Note]  
> <span data-ttu-id="1c32e-110">As chamadas de criação de instância, quando especificam um local do servidor, podem substituir uma configuração do registro.</span><span class="sxs-lookup"><span data-stu-id="1c32e-110">Instance creation calls, when they specify a server location, can override a registry setting.</span></span> <span data-ttu-id="1c32e-111">O algoritmo COM usado para fazer isso é descrito na referência para a enumeração [**CLSCTX**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx) .</span><span class="sxs-lookup"><span data-stu-id="1c32e-111">The algorithm COM uses for doing this is described in the reference for the [**CLSCTX**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx) enumeration.</span></span>

 

<span data-ttu-id="1c32e-112">A ativação remota depende da relação de segurança entre o cliente e o servidor.</span><span class="sxs-lookup"><span data-stu-id="1c32e-112">Remote activation depends on the security relationship between client and server.</span></span> <span data-ttu-id="1c32e-113">Para obter mais informações, consulte [segurança em com](security-in-com.md).</span><span class="sxs-lookup"><span data-stu-id="1c32e-113">For more information, see [Security in COM](security-in-com.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="1c32e-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1c32e-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1c32e-115">Objetos de classe COM e CLSIDs</span><span class="sxs-lookup"><span data-stu-id="1c32e-115">COM Class Objects and CLSIDs</span></span>](com-class-objects-and-clsids.md)
</dt> <dt>

[<span data-ttu-id="1c32e-116">Criando um objeto por meio de um objeto de classe</span><span class="sxs-lookup"><span data-stu-id="1c32e-116">Creating an Object Through a Class Object</span></span>](creating-an-object-through-a-class-object.md)
</dt> </dl>

 

 