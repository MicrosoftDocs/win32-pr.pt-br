---
description: Os provedores podem chamar métodos implementados pelo WMI de dentro de suas implementações de método.
ms.assetid: 5bfd9d9b-ffe5-4def-a97d-85c4c01223f0
ms.tgt_platform: multiple
title: Fazendo chamadas para o WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 534e478336cdd9675e382ef9b089f2d7bc595b03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011065"
---
# <a name="making-calls-to-wmi"></a><span data-ttu-id="77525-103">Fazendo chamadas para o WMI</span><span class="sxs-lookup"><span data-stu-id="77525-103">Making Calls to WMI</span></span>

<span data-ttu-id="77525-104">Os provedores podem chamar métodos implementados pelo WMI de dentro de suas implementações de método.</span><span class="sxs-lookup"><span data-stu-id="77525-104">Providers can call methods implemented by WMI from within their method implementations.</span></span> <span data-ttu-id="77525-105">No entanto, há considerações especiais quando um provedor chama a implementação de WMI de um método [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) de dentro de sua própria implementação do mesmo método.</span><span class="sxs-lookup"><span data-stu-id="77525-105">However, there are special considerations when a provider calls the WMI implementation of an [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) method from within its own implementation of the same method.</span></span> <span data-ttu-id="77525-106">Essas considerações são importantes, independentemente de o provedor chamar a versão síncrona ou assíncrona do método.</span><span class="sxs-lookup"><span data-stu-id="77525-106">These considerations are important regardless of whether the provider calls the synchronous or asynchronous version of the method.</span></span>

<span data-ttu-id="77525-107">Cada método de [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) que um provedor pode implementar tem um parâmetro *pCtx* , um ponteiro para uma implementação de interface [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) .</span><span class="sxs-lookup"><span data-stu-id="77525-107">Each [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) method that a provider can implement has a *pCtx* parameter, a pointer to an [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) interface implementation.</span></span> <span data-ttu-id="77525-108">Quando o WMI chama o provedor, o WMI passa um ponteiro válido nesse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="77525-108">When WMI calls the provider, WMI passes a valid pointer in this parameter.</span></span> <span data-ttu-id="77525-109">Um provedor sempre deve passar esse mesmo ponteiro em todas as chamadas para o WMI que eles fazem durante a manutenção de solicitações.</span><span class="sxs-lookup"><span data-stu-id="77525-109">A provider must always pass this same pointer in any calls to WMI that they make while servicing requests.</span></span> <span data-ttu-id="77525-110">O inativo para definir *pCtx* adequadamente pode fazer com que o WMI inicie um loop infinito.</span><span class="sxs-lookup"><span data-stu-id="77525-110">Neglecting to set *pCtx* appropriately can cause WMI to start an infinite loop.</span></span>

<span data-ttu-id="77525-111">O exemplo de código a seguir mostra a maneira correta de chamar a implementação de WMI de [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) de dentro de uma implementação de [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span><span class="sxs-lookup"><span data-stu-id="77525-111">The following code example shows the correct way to call the WMI implementation of [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) from within an implementation of [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span></span>


```C++
STDMETHODIMP CClassProv::GetObjectAsync (BSTR ObjectPath,
    long lFlags, IWbemContext *pCtx,
    IWbemObjectSink *pHandler)
{
  IWbemClassObject *pclObj = NULL;
  IWbemServices* m_pNamespace;
  HRESULT hr = m_pNamespace->GetObject(
      _bstr_t(L"AClass"), 0, pCtx, &pclObj, 
      NULL );
  pclObj->Release();
  return pHandler->SetStatus(0, hr, NULL, NULL);
}
```



<span data-ttu-id="77525-112">O exemplo de código C++ neste tópico requer as referências a seguir e \# inclui instruções para compilar corretamente.</span><span class="sxs-lookup"><span data-stu-id="77525-112">The C++ code example in this topic requires the following references and \#include statements to compile correctly.</span></span>


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <comdef.h>
#include <Wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")
```



<span data-ttu-id="77525-113">Os provedores de instância, classe e propriedade não devem emitir nenhuma chamada para o WMI solicitando a modificação de dados durante a manutenção de uma solicitação de leitura.</span><span class="sxs-lookup"><span data-stu-id="77525-113">Instance, class, and property providers must not issue any calls to WMI requesting the modification of data while servicing a read request.</span></span> <span data-ttu-id="77525-114">Os únicos provedores que são exceções a essa regra são os provedores de push.</span><span class="sxs-lookup"><span data-stu-id="77525-114">The only providers that are exceptions to this rule are push providers.</span></span> <span data-ttu-id="77525-115">Um provedor de Push é um provedor de classe que armazena dados no repositório do WMI e se baseia no WMI para lidar com solicitações de clientes.</span><span class="sxs-lookup"><span data-stu-id="77525-115">A push provider is a class provider that stores data in the WMI repository and relies on WMI to handle requests from clients.</span></span> <span data-ttu-id="77525-116">Durante a manutenção de uma solicitação de leitura, um provedor de push pode atualizar o repositório WMI, mas deve definir o parâmetro *lFlags* para a **atualização do proprietário do \_ sinalizador \_ \_ WBEM** na chamada [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) apropriada.</span><span class="sxs-lookup"><span data-stu-id="77525-116">While servicing a read request, a push provider can update the WMI repository, but must set the *lFlags* parameter to **WBEM\_FLAG\_OWNER\_UPDATE** in the appropriate [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) call.</span></span>

<span data-ttu-id="77525-117">Os provedores de eventos não devem fazer nenhuma alteração de classe durante a manutenção de uma chamada.</span><span class="sxs-lookup"><span data-stu-id="77525-117">Event providers must not make any class changes while servicing a call.</span></span> <span data-ttu-id="77525-118">Eles também não podem emitir chamadas relacionadas a eventos, como modificar um filtro de eventos.</span><span class="sxs-lookup"><span data-stu-id="77525-118">They also cannot issue any event-related calls, such as modifying an event filter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="77525-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="77525-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="77525-120">Desenvolvendo um provedor WMI</span><span class="sxs-lookup"><span data-stu-id="77525-120">Developing a WMI Provider</span></span>](developing-a-wmi-provider.md)
</dt> <dt>

[<span data-ttu-id="77525-121">Configurando descritores de segurança namepace</span><span class="sxs-lookup"><span data-stu-id="77525-121">Setting Namepace Security Descriptors</span></span>](setting-namespace-security-descriptors.md)
</dt> <dt>

[<span data-ttu-id="77525-122">Protegendo seu provedor</span><span class="sxs-lookup"><span data-stu-id="77525-122">Securing Your Provider</span></span>](securing-your-provider.md)
</dt> </dl>

 

 



