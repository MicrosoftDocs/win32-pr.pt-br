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
# <a name="composing-and-registering-spns-for-scp-based-windows-sockets-service"></a>Compondo e registrando SPNs para o serviço Windows Sockets baseado em SCP

O exemplo de código a seguir mostra como compor e registrar os SPNs para um serviço. Chame esse código do seu instalador de serviço depois de chamar [**CreateService**](/windows/desktop/api/winsvc/nf-winsvc-createservicea) e criar o SCP (ponto de conexão de serviço) do serviço.

O exemplo de código a seguir chama as funções de exemplo **SpnCompose** e **SpnRegister** que compõem e registram o SPN. Para obter mais informações e o código-fonte **SpnCompose** , consulte [composição dos SPNs de um serviço com um SCP](composing-the-spns-for-a-service-with-an-scp.md). Para obter mais informações e o código-fonte **SpnRegister** , consulte [registrando os SPNs para um serviço](registering-the-spns-for-a-service.md).

Este exemplo usa o nome da classe de serviço e o nome distinto de seu SCP para criar seu nome da entidade de serviço. Para obter mais informações e um exemplo de código que mostra como o cliente é associado ao SCP de serviço para recuperar essas cadeias de caracteres de nome, consulte [como os clientes encontram e usam um ponto de conexão de serviço](how-clients-find-and-use-a-service-connection-point.md). Lembre-se de que o código para compor um SPN varia dependendo do tipo de serviço e dos mecanismos usados para publicar o serviço.

O serviço registra seu SPN armazenando-o no atributo **servicePrincipalName** do objeto de conta do serviço no diretório. Se o serviço for executado na conta LocalSystem em vez de em uma conta de serviço, ele registrará seu SPN no objeto da conta do computador local no diretório.


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



Você pode usar um código semelhante para cancelar o registro de seus SPNs quando seu serviço for desinstalado. Especifique o SPN de DS operação de **\_ \_ exclusão \_ \_** de SPN em vez de **DS \_ SPN \_ Adicionar \_ SPN \_ op**.

 

 