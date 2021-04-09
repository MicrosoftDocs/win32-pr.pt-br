---
description: O serviço de autenticação Kerberos especifica o nome principal do servidor para garantir a identidade do computador ao qual ele está se conectando.
ms.assetid: 3d58db28-2e69-4e27-9f27-61529abbf750
ms.tgt_platform: multiple
title: Especificando o nome principal do servidor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a2f5aa4053b5ae7452e5f5e9c0ddcac15630ae5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091298"
---
# <a name="specifying-the-server-principal-name"></a><span data-ttu-id="7d801-103">Especificando o nome principal do servidor</span><span class="sxs-lookup"><span data-stu-id="7d801-103">Specifying the Server Principal Name</span></span>

<span data-ttu-id="7d801-104">O serviço de autenticação Kerberos especifica o nome principal do servidor para garantir a identidade do computador ao qual ele está se conectando.</span><span class="sxs-lookup"><span data-stu-id="7d801-104">The Kerberos authentication service specifies the server principal name to ensure the identity of the computer to which it is connecting.</span></span> <span data-ttu-id="7d801-105">Especifique o nome principal do servidor na chamada para o método de script [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md) fornecendo o nome do computador remoto.</span><span class="sxs-lookup"><span data-stu-id="7d801-105">Specify the server principal name in the call to the scripting method [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md) by giving the name of the remote computer.</span></span> <span data-ttu-id="7d801-106">Em C++, especifique o nome principal do servidor no parâmetro *pServerPrincName* ao chamar [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) para o proxy.</span><span class="sxs-lookup"><span data-stu-id="7d801-106">In C++, specify the server principal name in the *pServerPrincName* parameter when calling [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) for the proxy.</span></span> <span data-ttu-id="7d801-107">Para obter mais informações, consulte [conectando-se ao WMI em um computador remoto](connecting-to-wmi-on-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="7d801-107">For more information, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>

<span data-ttu-id="7d801-108">Esse parâmetro é necessário para que o Kerberos dê suporte à autenticação mútua.</span><span class="sxs-lookup"><span data-stu-id="7d801-108">This parameter is required for Kerberos to support mutual authentication.</span></span> <span data-ttu-id="7d801-109">No entanto, o uso do nome principal do servidor padrão não permite a autenticação mútua.</span><span class="sxs-lookup"><span data-stu-id="7d801-109">However, using the default server principal name does not allow mutual authentication.</span></span> <span data-ttu-id="7d801-110">Os clientes para os quais a autenticação mútua é crítica devem especificar um nome principal de servidor que corresponda à identidade do servidor que o serviço WMI está usando.</span><span class="sxs-lookup"><span data-stu-id="7d801-110">Clients for which mutual authentication is critical, must specify a server principal name that matches the server identity that the WMI service is using.</span></span> <span data-ttu-id="7d801-111">Para obter mais informações sobre como configurar a segurança de proxy e um exemplo de C++ mostrando como definir o nome principal do servidor, consulte [definindo a segurança em IWbemServices e em outros proxies](setting-the-security-on-iwbemservices-and-other-proxies.md).</span><span class="sxs-lookup"><span data-stu-id="7d801-111">For more information about setting proxy security and a C++ example showing how to set the server principal name, see [Setting the Security on IWbemServices and Other Proxies](setting-the-security-on-iwbemservices-and-other-proxies.md).</span></span>

<span data-ttu-id="7d801-112">Para obter mais informações sobre como definir o nome principal do servidor em script e Visual Basic, consulte [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md) e [conectando-se ao WMI em um computador remoto](connecting-to-wmi-on-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="7d801-112">For more information about setting the server principal name in script and Visual Basic, see [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md) and [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>

<span data-ttu-id="7d801-113">Ao contrário da maioria dos protocolos de segurança para Instrumentação de Gerenciamento do Windows (WMI) e Component Object Model (COM), você não pode definir a entidade do servidor em uma chamada para [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="7d801-113">Unlike most security protocols for Windows Management Instrumentation (WMI) and Component Object Model (COM), you cannot set the server principal in a call to [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span> <span data-ttu-id="7d801-114">No entanto, você pode definir a entidade de segurança do servidor com o parâmetro *bstrAuthority* para [**IWbemLocator:: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver)ou o parâmetro *pServerPrincName* para [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span><span class="sxs-lookup"><span data-stu-id="7d801-114">However, you can set the server principal with the *bstrAuthority* parameter for [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver), or the *pServerPrincName* parameter for [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span></span>

<span data-ttu-id="7d801-115">O exemplo de código neste tópico requer a seguinte \# instrução include para compilação correta.</span><span class="sxs-lookup"><span data-stu-id="7d801-115">The code example in this topic requires the following \#include statement to correctly compile.</span></span>


```C++
#include <wbemidl.h>
```



<span data-ttu-id="7d801-116">O exemplo de código a seguir mostra como definir o nome principal do servidor com [**ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver).</span><span class="sxs-lookup"><span data-stu-id="7d801-116">The following code example shows how to set the server principal name with [**ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver).</span></span>


```C++
IWbemServices* g_pNameSpace = NULL;

// Namespace to which to connect
BSTR  bstrNameSpace = 
SysAllocString( L"\\\\MyMachine\\root\default" );

// The bstrAuthority string contains the server
// principal name MyDomain\\MyMachine
// and the authentication service, which is Kerberos.
BSTR  bstrAuthority = 
SysAllocString( L"kerberos:MyDomain\\MyMachine"  );

HRESULT hr = NULL;
IWbemLocator* pWbemLocator = 0;

  hr = pWbemLocator->ConnectServer(
          bstrNameSpace,  // NameSpace name
          NULL,           // User name
          NULL,           // Password
          NULL,           // Locale
          0L,             // Security flags
          bstrAuthority,  // Authority, server principal name
          NULL,           // WBEM context
          &g_pNameSpace   // Namespace
          );

  // Free memory resources.
  g_pNameSpace->Release();
  SysFreeString(bstrNameSpace);
  SysFreeString(bstrAuthority);
```



## <a name="related-topics"></a><span data-ttu-id="7d801-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7d801-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7d801-118">Configurando o serviço de autenticação usando o VBScript</span><span class="sxs-lookup"><span data-stu-id="7d801-118">Setting the Authentication Service Using VBScript</span></span>](setting-the-authentication-service-using-vbscript.md)
</dt> <dt>

[<span data-ttu-id="7d801-119">Configurando a autenticação usando C++</span><span class="sxs-lookup"><span data-stu-id="7d801-119">Setting Authentication Using C++</span></span>](setting-authentication-using-c-.md)
</dt> <dt>

[<span data-ttu-id="7d801-120">Definindo a segurança em IWbemServices e em outros proxies</span><span class="sxs-lookup"><span data-stu-id="7d801-120">Setting the Security on IWbemServices and Other Proxies</span></span>](setting-the-security-on-iwbemservices-and-other-proxies.md)
</dt> </dl>

 

 
