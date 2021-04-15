---
title: Implementando CSearch
description: Implementando CSearch
ms.assetid: 3041807a-e7e0-4022-ab90-a8b846bafc0e
keywords:
- Plug-ins do Windows Media Player, classe CSearch
- plug-ins, classe CSearch
- plug-ins de interface do usuário, classe CSearch
- Plug-ins de interface do usuário, classe CSearch
- Classe CSearch
- Guia de programação, plug-ins de interface do usuário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f36c6446ca0eb6b1cc9dfb5f45044493c2a8fd6b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104498652"
---
# <a name="implementing-csearch"></a><span data-ttu-id="aff59-109">Implementando CSearch</span><span class="sxs-lookup"><span data-stu-id="aff59-109">Implementing CSearch</span></span>

<span data-ttu-id="aff59-110">A interface **IWMPPluginUI** tem vários métodos que são chamados pelo Windows Media Player em momentos diferentes durante o ciclo de vida de uma instância de plug-in.</span><span class="sxs-lookup"><span data-stu-id="aff59-110">The **IWMPPluginUI** interface has several methods that are called by Windows Media Player at different times during the life cycle of a plug-in instance.</span></span> <span data-ttu-id="aff59-111">O assistente fornece implementações básicas desses métodos, bem como o construtor de classes e o destruidor e outros métodos de classe.</span><span class="sxs-lookup"><span data-stu-id="aff59-111">The wizard provides basic implementations of these methods as well as the class constructor and destructor and other class methods.</span></span> <span data-ttu-id="aff59-112">O arquivo Search. h deve ser modificado para que o Windows Media Player possa se comunicar com a interface do usuário, que é descrita na próxima seção.</span><span class="sxs-lookup"><span data-stu-id="aff59-112">The Search.h file must be modified so that Windows Media Player can communicate with the UI, which is described in the next section.</span></span>

<span data-ttu-id="aff59-113">Para que a classe CPluginWindow tenha acesso à variável m de membro privado \_ , uma declaração de classe Friend deve ser feita dentro da definição de classe CSearch, conforme mostrado no seguinte trecho de código:</span><span class="sxs-lookup"><span data-stu-id="aff59-113">For the CPluginWindow class to have access to the private member variable m\_spCore, a friend class declaration must be made inside the CSearch class definition as shown in the following code snippet:</span></span>


```C++
class ATL_NO_VTABLE CSearch : 
    public CComObjectRootEx<CComSingleThreadModel>,
    public CComCoClass<CSearch, &CLSID_Search>,
    public IWMPPluginUI
{

friend class CPluginWindow;

// Rest of class definition...

}

```



## <a name="related-topics"></a><span data-ttu-id="aff59-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="aff59-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aff59-115">**Guia de programação de plug-ins de interface do usuário**</span><span class="sxs-lookup"><span data-stu-id="aff59-115">**User Interface Plug-ins Programming Guide**</span></span>](user-interface-plug-ins-programming-guide.md)
</dt> </dl>

 

 




