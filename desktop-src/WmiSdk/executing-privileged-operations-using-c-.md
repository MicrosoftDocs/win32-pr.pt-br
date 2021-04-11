---
description: Aplicativos cliente especiais podem invocar operações privilegiadas.
ms.assetid: e09fcadc-282f-4f07-b69c-b15bfdb07a7d
ms.tgt_platform: multiple
title: Executando operações privilegiadas usando C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fbc0468fef7531586020f55032bff94c977c4ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296632"
---
# <a name="executing-privileged-operations-using-c"></a><span data-ttu-id="2956e-103">Executando operações privilegiadas usando C++</span><span class="sxs-lookup"><span data-stu-id="2956e-103">Executing Privileged Operations Using C++</span></span>

<span data-ttu-id="2956e-104">Aplicativos cliente especiais podem invocar operações privilegiadas.</span><span class="sxs-lookup"><span data-stu-id="2956e-104">Special client applications might invoke privileged operations.</span></span> <span data-ttu-id="2956e-105">Por exemplo, um aplicativo pode permitir que um gerente reinicie um computador do Office sem resposta.</span><span class="sxs-lookup"><span data-stu-id="2956e-105">For example, an application could allow a manager to reboot an unresponsive office computer.</span></span> <span data-ttu-id="2956e-106">Usando o Instrumentação de Gerenciamento do Windows (WMI), você pode executar uma operação privilegiada chamando o provedor WMI para a operação privilegiada.</span><span class="sxs-lookup"><span data-stu-id="2956e-106">By using Windows Management Instrumentation (WMI), you can execute a privileged operation by calling the WMI provider for the privileged operation.</span></span>

<span data-ttu-id="2956e-107">O procedimento a seguir descreve como chamar um provedor para uma operação privilegiada.</span><span class="sxs-lookup"><span data-stu-id="2956e-107">The following procedure describes how to call a provider for a privileged operation.</span></span>

<span data-ttu-id="2956e-108">**Para chamar um provedor para uma operação privilegiada**</span><span class="sxs-lookup"><span data-stu-id="2956e-108">**To call a provider for a privileged operation**</span></span>

1.  <span data-ttu-id="2956e-109">Obtenha permissões para o processo do cliente para executar a operação privilegiada.</span><span class="sxs-lookup"><span data-stu-id="2956e-109">Obtain permissions for the client process to execute the privileged operation.</span></span>

    <span data-ttu-id="2956e-110">Normalmente, um administrador define as permissões usando as ferramentas administrativas do sistema — antes de executar o processo.</span><span class="sxs-lookup"><span data-stu-id="2956e-110">Typically, an administrator sets the permissions using system administrative tools—prior to running the process.</span></span>

2.  <span data-ttu-id="2956e-111">Obtenha a permissão para o processo do provedor para habilitar a operação privilegiada.</span><span class="sxs-lookup"><span data-stu-id="2956e-111">Obtain permission for the provider process to enable the privileged operation.</span></span>

    <span data-ttu-id="2956e-112">Normalmente, você pode definir permissões de provedor com uma chamada para a função [**AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) .</span><span class="sxs-lookup"><span data-stu-id="2956e-112">Typically, you can set provider permissions with a call to the [**AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) function.</span></span>

3.  <span data-ttu-id="2956e-113">Obtenha a permissão para o processo do cliente para habilitar a operação privilegiada.</span><span class="sxs-lookup"><span data-stu-id="2956e-113">Obtain permission for the client process to enable the privileged operation.</span></span>

    <span data-ttu-id="2956e-114">Essa etapa será necessária apenas se o provedor for local para o cliente.</span><span class="sxs-lookup"><span data-stu-id="2956e-114">This step is necessary only if the provider is local to the client.</span></span> <span data-ttu-id="2956e-115">Se o cliente e o provedor existirem no mesmo computador, o cliente deverá habilitar especificamente a operação privilegiada usando uma das seguintes técnicas:</span><span class="sxs-lookup"><span data-stu-id="2956e-115">If the client and provider exist on the same computer, the client must specifically enable the privileged operation by using one of the following techniques:</span></span>

    -   <span data-ttu-id="2956e-116">Se o cliente possuir o processo, o cliente poderá usar [**AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) para ajustar o token de processo antes de chamar o WMI.</span><span class="sxs-lookup"><span data-stu-id="2956e-116">If the client owns the process, the client can use [**AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) to adjust the process token before calling WMI.</span></span> <span data-ttu-id="2956e-117">Nesse caso, você não precisa mais codificar.</span><span class="sxs-lookup"><span data-stu-id="2956e-117">In this case, you do not need to code any further.</span></span>
    -   <span data-ttu-id="2956e-118">Se o cliente não puder acessar o token do cliente, o cliente poderá usar o procedimento a seguir para criar um token de thread e usar [**AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) nesse token.</span><span class="sxs-lookup"><span data-stu-id="2956e-118">If the client cannot access the client token, the client can use the following procedure to create a thread token and use [**AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) on that token.</span></span>

<span data-ttu-id="2956e-119">O procedimento a seguir descreve como criar um token de thread e usar [**AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) nesse token.</span><span class="sxs-lookup"><span data-stu-id="2956e-119">The following procedure describes how to create a thread token and use [**AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) on that token.</span></span>

<span data-ttu-id="2956e-120">**Para criar um token de thread e usar AdjustTokenPrivileges nesse token**</span><span class="sxs-lookup"><span data-stu-id="2956e-120">**To create a thread token and use AdjustTokenPrivileges on that token**</span></span>

1.  <span data-ttu-id="2956e-121">Crie uma cópia do token de processo chamando [**ImpersonateSelf**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-impersonateself).</span><span class="sxs-lookup"><span data-stu-id="2956e-121">Create a copy of the process token by calling [**ImpersonateSelf**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-impersonateself).</span></span>
2.  <span data-ttu-id="2956e-122">Recupere o token de thread recém-criado chamando [**GetTokenInformation**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-gettokeninformation).</span><span class="sxs-lookup"><span data-stu-id="2956e-122">Retrieve the newly created thread token by calling [**GetTokenInformation**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-gettokeninformation).</span></span>
3.  <span data-ttu-id="2956e-123">Habilite a operação privilegiada com uma chamada para [**AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) no novo token.</span><span class="sxs-lookup"><span data-stu-id="2956e-123">Enable the privileged operation with a call to [**AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) on the new token.</span></span>
4.  <span data-ttu-id="2956e-124">Obtenha um ponteiro para [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices).</span><span class="sxs-lookup"><span data-stu-id="2956e-124">Obtain a pointer to [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices).</span></span>
5.  <span data-ttu-id="2956e-125">Encobrir o ponteiro para [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) com uma chamada para [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span><span class="sxs-lookup"><span data-stu-id="2956e-125">Cloak the pointer to [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) with a call to [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span></span>
6.  <span data-ttu-id="2956e-126">Repita as etapas 1 a 5 em cada chamada para o WMI.</span><span class="sxs-lookup"><span data-stu-id="2956e-126">Repeat steps 1 through 5 on each call to WMI.</span></span>

    > [!Note]  
    > <span data-ttu-id="2956e-127">Você deve repetir as etapas porque o COM armazena os tokens em cache incorretamente.</span><span class="sxs-lookup"><span data-stu-id="2956e-127">You must repeat the steps because COM caches tokens incorrectly.</span></span>

     

<span data-ttu-id="2956e-128">O exemplo de código neste tópico requer a seguinte \# instrução include para compilação correta.</span><span class="sxs-lookup"><span data-stu-id="2956e-128">The code example in this topic requires the following \#include statement to correctly compile.</span></span>


```C++
#include <wbemidl.h>
```



<span data-ttu-id="2956e-129">O exemplo de código a seguir mostra como habilitar privilégios em um computador local.</span><span class="sxs-lookup"><span data-stu-id="2956e-129">The following code example shows how to enable privileges on a local machine.</span></span>


```C++
// Get the privileges 
// The token has been obtained outside the scope of this code sample
// ================== 
DWORD dwLen;
bool bRes;
HANDLE hToken;

// obtain dwLen
bRes = GetTokenInformation(
  hToken, 
  TokenPrivileges, 
  NULL, 
  0,
  &dwLen
); 

BYTE* pBuffer = new BYTE[dwLen];
if(pBuffer == NULL)
{
  CloseHandle(hToken);
  return WBEM_E_OUT_OF_MEMORY;
} 

bRes = GetTokenInformation(
  hToken, 
  TokenPrivileges, 
  pBuffer,     
  dwLen,        
  &dwLen
);

if (!bRes)
{
  CloseHandle(hToken);
  delete [] pBuffer;
  return WBEM_E_ACCESS_DENIED;
} 

// Iterate through all the privileges and enable them all
// ====================================================== 
TOKEN_PRIVILEGES* pPrivs = (TOKEN_PRIVILEGES*)pBuffer;
for (DWORD i = 0; i < pPrivs->PrivilegeCount; i++)
{
  pPrivs->Privileges[i].Attributes |= SE_PRIVILEGE_ENABLED;
} 
// Store the information back in the token
// ========================================= 
bRes = AdjustTokenPrivileges(
  hToken, 
  FALSE, 
  pPrivs, 
  0, NULL, NULL
);

delete [] pBuffer;
CloseHandle(hToken); 

if (!bRes)
  return WBEM_E_ACCESS_DENIED;
else
  return WBEM_S_NO_ERROR;
```



 

 
