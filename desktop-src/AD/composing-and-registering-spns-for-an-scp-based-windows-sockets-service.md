---
title: Compondo e registrando SPNs para o serviço Windows Sockets baseado em SCP
description: O exemplo de código a seguir mostra como compor e registrar os SPNs para um serviço. Chame esse código do seu instalador de serviço depois de chamar CreateService e criar o SCP (ponto de conexão de serviço) do serviço.
ms.assetid: 3957af10-974a-415f-b8fb-d9b52ac5a82d
ms.tgt_platform: multiple
keywords:
- nomes de entidade de serviço anúncio, composição e registro de SPNs para um serviço Windows Sockets baseado em SCP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d754d51c0ad34b1623bdc84fc8178b04d33515ed
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103640429"
---
# <a name="composing-and-registering-spns-for-scp-based-windows-sockets-service"></a><span data-ttu-id="5c594-105">Compondo e registrando SPNs para o serviço Windows Sockets baseado em SCP</span><span class="sxs-lookup"><span data-stu-id="5c594-105">Composing and registering SPNs for SCP-based Windows Sockets Service</span></span>

<span data-ttu-id="5c594-106">O exemplo de código a seguir mostra como compor e registrar os SPNs para um serviço.</span><span class="sxs-lookup"><span data-stu-id="5c594-106">The following code example shows how to compose and register the SPNs for a service.</span></span> <span data-ttu-id="5c594-107">Chame esse código do seu instalador de serviço depois de chamar [**CreateService**](/windows/desktop/api/winsvc/nf-winsvc-createservicea) e criar o SCP (ponto de conexão de serviço) do serviço.</span><span class="sxs-lookup"><span data-stu-id="5c594-107">Call this code from your service installer after calling [**CreateService**](/windows/desktop/api/winsvc/nf-winsvc-createservicea) and creating the service's service connection point (SCP).</span></span>

<span data-ttu-id="5c594-108">O exemplo de código a seguir chama as funções de exemplo **SpnCompose** e **SpnRegister** que compõem e registram o SPN.</span><span class="sxs-lookup"><span data-stu-id="5c594-108">The following code example calls the **SpnCompose** and **SpnRegister** example functions that compose and register the SPN.</span></span> <span data-ttu-id="5c594-109">Para obter mais informações e o código-fonte **SpnCompose** , consulte [composição dos SPNs de um serviço com um SCP](composing-the-spns-for-a-service-with-an-scp.md).</span><span class="sxs-lookup"><span data-stu-id="5c594-109">For more information and the **SpnCompose** source code, see [Composing the SPNs for a Service with an SCP](composing-the-spns-for-a-service-with-an-scp.md).</span></span> <span data-ttu-id="5c594-110">Para obter mais informações e o código-fonte **SpnRegister** , consulte [registrando os SPNs para um serviço](registering-the-spns-for-a-service.md).</span><span class="sxs-lookup"><span data-stu-id="5c594-110">For more information and the **SpnRegister** source code, see [Registering the SPNs for a Service](registering-the-spns-for-a-service.md).</span></span>

<span data-ttu-id="5c594-111">Este exemplo usa o nome da classe de serviço e o nome distinto de seu SCP para criar seu nome da entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="5c594-111">This example uses the service class name and the distinguished name of its SCP to create its service principal name.</span></span> <span data-ttu-id="5c594-112">Para obter mais informações e um exemplo de código que mostra como o cliente é associado ao SCP de serviço para recuperar essas cadeias de caracteres de nome, consulte [como os clientes encontram e usam um ponto de conexão de serviço](how-clients-find-and-use-a-service-connection-point.md).</span><span class="sxs-lookup"><span data-stu-id="5c594-112">For more information and a code example that shows how the client binds to the service SCP to retrieve these name strings, see [How Clients Find and Use a Service Connection Point](how-clients-find-and-use-a-service-connection-point.md).</span></span> <span data-ttu-id="5c594-113">Lembre-se de que o código para compor um SPN varia dependendo do tipo de serviço e dos mecanismos usados para publicar o serviço.</span><span class="sxs-lookup"><span data-stu-id="5c594-113">Be aware that the code for composing an SPN varies depending on the type of service and the mechanisms used to publish the service.</span></span>

<span data-ttu-id="5c594-114">O serviço registra seu SPN armazenando-o no atributo **servicePrincipalName** do objeto de conta do serviço no diretório.</span><span class="sxs-lookup"><span data-stu-id="5c594-114">The service registers its SPN by storing it in the **servicePrincipalName** attribute of the service's account object in the directory.</span></span> <span data-ttu-id="5c594-115">Se o serviço for executado na conta LocalSystem em vez de em uma conta de serviço, ele registrará seu SPN no objeto da conta do computador local no diretório.</span><span class="sxs-lookup"><span data-stu-id="5c594-115">If the service runs under the LocalSystem account instead of under a service account, it registers its SPN under the local computer account's object in the directory.</span></span>


```C++
TCHAR szDNofSCP[MAX_PATH]; // DN of SCP. Initialize by querying SCP.
TCHAR szServiceClass[]=TEXT("ADSockAuth");
LPCTSTR szServiceAccountDN;   // DN of a service logon account. 
 
DWORD dwStatus;
TCHAR **pspn = NULL;
ULONG ulSpn = 1;
 
// Compose the SPNs.
dwStatus = SpnCompose(
        &pspn,              // Receives pointer to the SPN array.
        &ulSpn,             // Receives number of SPNs returned.
        szDNofSCP,          // Input: DN of the SCP.
        szServiceClass);    // Input: the service class string.
 
// Register the SPNs
if (dwStatus == NO_ERROR) 
    dwStatus = SpnRegister(
       szServiceAccountDN,  // Logon account to register SPNs on
       pspn,                // Array of SPNs
       ulSpn,               // Number of SPNs in array
       DS_SPN_ADD_SPN_OP);  // Add SPNs to the account
 
// Free the array of SPNs returned by SpnCompose.
DsFreeSpnArray(ulSpn, pspn); 
```



<span data-ttu-id="5c594-116">Você pode usar um código semelhante para cancelar o registro de seus SPNs quando seu serviço for desinstalado.</span><span class="sxs-lookup"><span data-stu-id="5c594-116">You can use similar code to unregister your SPNs when your service is uninstalled.</span></span> <span data-ttu-id="5c594-117">Especifique o SPN de DS operação de **\_ \_ exclusão \_ \_** de SPN em vez de **DS \_ SPN \_ Adicionar \_ SPN \_ op**.</span><span class="sxs-lookup"><span data-stu-id="5c594-117">Specify the **DS\_SPN\_DELETE\_SPN\_OP** operation instead of **DS\_SPN\_ADD\_SPN\_OP**.</span></span>

 

 