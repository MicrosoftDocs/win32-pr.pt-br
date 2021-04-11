---
title: Como a ADSI integra extensões
description: Diretrizes que descrevem como o ADSI interage com extensões.
ms.assetid: 00301551-ec56-4cb4-8e77-264c3ad48814
ms.tgt_platform: multiple
keywords:
- ADSI de extensões
- ADSI e extensões
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 956a76954851ea54b4eae99bfa45102a3b2fefa5
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104008361"
---
# <a name="how-adsi-integrates-extensions"></a><span data-ttu-id="3da0f-105">Como a ADSI integra extensões</span><span class="sxs-lookup"><span data-stu-id="3da0f-105">How ADSI Integrates Extensions</span></span>

<span data-ttu-id="3da0f-106">As diretrizes a seguir descrevem como o ADSI interage com extensões:</span><span class="sxs-lookup"><span data-stu-id="3da0f-106">The following guidelines describe how ADSI interacts with extensions:</span></span>

-   <span data-ttu-id="3da0f-107">Algo é associado a um objeto de diretório ADSI.</span><span class="sxs-lookup"><span data-stu-id="3da0f-107">Something binds to an ADSI directory object.</span></span> <span data-ttu-id="3da0f-108">Por exemplo, "LDAP:Binding = JeffSmith, OU = Sales, DC = Fabrikam, DC = COM".</span><span class="sxs-lookup"><span data-stu-id="3da0f-108">For example, "LDAP://CN=JeffSmith,OU=Sales,DC=Fabrikam,DC=COM".</span></span>
-   <span data-ttu-id="3da0f-109">A ADSI identifica que o objeto está na classe de **usuário** .</span><span class="sxs-lookup"><span data-stu-id="3da0f-109">ADSI identifies that the object is in the **user** class.</span></span>
-   <span data-ttu-id="3da0f-110">O ADSI executa uma pesquisa no registro e identifica os CLSIDs de extensão para o **usuário**.</span><span class="sxs-lookup"><span data-stu-id="3da0f-110">ADSI performs a lookup in the registry and identifies the extension CLSIDs for **user**.</span></span> <span data-ttu-id="3da0f-111">Lembre-se de que o ADSI armazena esses dados em cache.</span><span class="sxs-lookup"><span data-stu-id="3da0f-111">Be aware that ADSI caches this data.</span></span>
-   <span data-ttu-id="3da0f-112">Algo chama o método **QueryInterface** para IID \_ IMyExtension.</span><span class="sxs-lookup"><span data-stu-id="3da0f-112">Something calls the **QueryInterface** method for IID\_IMyExtension.</span></span> <span data-ttu-id="3da0f-113">A ADSI pesquisa as interfaces associadas ao objeto de **usuário** , começando com suas próprias interfaces e, em seguida, examinando as interfaces de extensão.</span><span class="sxs-lookup"><span data-stu-id="3da0f-113">ADSI searches the interfaces associated with the **user** object, starting with its own interfaces, then looking at extension interfaces.</span></span>
-   <span data-ttu-id="3da0f-114">Se uma correspondência for encontrada, a ADSI criará uma instância do componente que dá suporte a IMyExtension de IID \_ e chamará **QueryInterface** para a extensão.</span><span class="sxs-lookup"><span data-stu-id="3da0f-114">If a match is found, ADSI creates an instance of the component that supports IID\_IMyExtension, and calls **QueryInterface** for the extension.</span></span> <span data-ttu-id="3da0f-115">A interface resultante é retornada.</span><span class="sxs-lookup"><span data-stu-id="3da0f-115">The resulting interface is returned.</span></span>
-   <span data-ttu-id="3da0f-116">O usuário usa essa interface para chamar os métodos de interface.</span><span class="sxs-lookup"><span data-stu-id="3da0f-116">The user uses this interface to call the interface methods.</span></span>
-   <span data-ttu-id="3da0f-117">Em seguida, o cliente chama **QueryInterface** para IID \_ IYourExtension, que está em um componente diferente.</span><span class="sxs-lookup"><span data-stu-id="3da0f-117">Next, the client calls **QueryInterface** for IID\_IYourExtension, which is in a different component.</span></span> <span data-ttu-id="3da0f-118">Esse componente Delega essa chamada de **QueryInterface** para a interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) do agregador, que é a própria ADSI.</span><span class="sxs-lookup"><span data-stu-id="3da0f-118">This component delegates this **QueryInterface** call to the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface of the aggregator, which happens to be ADSI itself.</span></span>
-   <span data-ttu-id="3da0f-119">Novamente, a ADSI pesquisa as interfaces e cria a instância do componente.</span><span class="sxs-lookup"><span data-stu-id="3da0f-119">Again, ADSI searches the interfaces and creates the component instance.</span></span>

 

 