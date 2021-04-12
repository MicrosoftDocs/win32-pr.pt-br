---
title: Ligação tardia do que está acontecendo nos bastidores
description: Este tópico descreve como a associação tardia funciona no ADSI.
ms.assetid: f4ff19fc-d69e-4528-a6e2-2544d9149e8c
ms.tgt_platform: multiple
keywords:
- ADSI de extensões, associação tardia, o que está acontecendo nos bastidores
- Associação de anúncio, associação tardia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5299b715325e4eda88a0eeaca2b22b4bdaa15a96
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104454342"
---
# <a name="late-binding-whats-happening-under-the-hood"></a><span data-ttu-id="08987-105">Associação tardia: o que está acontecendo nos bastidores?</span><span class="sxs-lookup"><span data-stu-id="08987-105">Late Binding: What's Happening Under the Hood?</span></span>

<span data-ttu-id="08987-106">A lista a seguir descreve o processo geral para executar uma ligação tardia:</span><span class="sxs-lookup"><span data-stu-id="08987-106">The following list outlines the general process for performing a late bind:</span></span>

-   <span data-ttu-id="08987-107">Algo é associado a um objeto de diretório ADSI.</span><span class="sxs-lookup"><span data-stu-id="08987-107">Something binds to an ADSI directory object.</span></span> <span data-ttu-id="08987-108">Por exemplo, "LDAP:Binding = Jeffsmith, OU = Sales, DC = Fabrikam, DC = COM" é associado usando associação tardia COM.</span><span class="sxs-lookup"><span data-stu-id="08987-108">For example, "LDAP://CN=Jeffsmith,OU=Sales,DC=Fabrikam,DC=COM" binds using COM late binding.</span></span> <span data-ttu-id="08987-109">Isso faz com que o ADSI chame o método [**QueryInterface**](/windows/win32/api/oaidl/nn-oaidl-idispatch) na interface **IDispatch** .</span><span class="sxs-lookup"><span data-stu-id="08987-109">This causes ADSI to call the [**QueryInterface**](/windows/win32/api/oaidl/nn-oaidl-idispatch) method on the **IDispatch** interface.</span></span>
-   <span data-ttu-id="08987-110">A ADSI localiza um objeto na classe User e cria um objeto que dá suporte às interfaces apropriadas, como [**IADs**](/windows/desktop/api/Iads/nn-iads-iads), [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser).</span><span class="sxs-lookup"><span data-stu-id="08987-110">ADSI finds an object in the user class and creates an object that supports the appropriate interfaces, such as [**IADs**](/windows/desktop/api/Iads/nn-iads-iads), [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser).</span></span>
-   <span data-ttu-id="08987-111">O ADSI executa uma pesquisa no registro e localiza CLSIDs de extensão para o usuário.</span><span class="sxs-lookup"><span data-stu-id="08987-111">ADSI performs a lookup in the registry and finds extension CLSIDs for user.</span></span> <span data-ttu-id="08987-112">Lembre-se de que o ADSI armazena esses dados em cache.</span><span class="sxs-lookup"><span data-stu-id="08987-112">Be aware that ADSI caches this data.</span></span>
-   <span data-ttu-id="08987-113">Algo faz uma chamada para o método **MyNewMethod** .</span><span class="sxs-lookup"><span data-stu-id="08987-113">Something makes a call to the **MyNewMethod** method.</span></span> <span data-ttu-id="08987-114">A ADSI pesquisa sua ID de expedição e as IDs de expedição para outras extensões ADSI.</span><span class="sxs-lookup"><span data-stu-id="08987-114">ADSI looks up its dispatch ID and the dispatch IDs for other ADSI extensions.</span></span> <span data-ttu-id="08987-115">Em seguida, o ADSI localiza a extensão que atende a essa chamada e chama a interface [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension) para essa extensão.</span><span class="sxs-lookup"><span data-stu-id="08987-115">ADSI then finds the extension that serves this call, and calls the [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension) interface for that extension.</span></span>
-   <span data-ttu-id="08987-116">A extensão executa a função.</span><span class="sxs-lookup"><span data-stu-id="08987-116">The extension executes the function.</span></span>
-   <span data-ttu-id="08987-117">Agora, o gravador do cliente invoca o método **YourNewMethod** usando a interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) para a extensão atual.</span><span class="sxs-lookup"><span data-stu-id="08987-117">Now, the client writer invokes the **YourNewMethod** method using the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface for the current extension.</span></span> <span data-ttu-id="08987-118">A implementação de **IDispatch** da extensão é delegada de volta para o **IDispatch** para ADSI.</span><span class="sxs-lookup"><span data-stu-id="08987-118">The extension's **IDispatch** implementation delegates back to the **IDispatch** for ADSI.</span></span>
-   <span data-ttu-id="08987-119">O [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) para ADSI procura novamente a extensão apropriada ou, em seguida, chama a extensão apropriada usando a interface [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension) para essa extensão.</span><span class="sxs-lookup"><span data-stu-id="08987-119">The [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) for ADSI again searches for the appropriate extension, or itself, then it calls the appropriate extension using the [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension) interface for that extension.</span></span>

 

 