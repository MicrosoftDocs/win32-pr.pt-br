---
title: Compondo SPNs para um serviço RpcNs
description: O exemplo de código a seguir compõe os SPNs (nomes da entidade de serviço) para um serviço RPC que tem uma entrada no contêiner RpcServices no diretório. Um serviço RPC usa a função RpcNsBindingExport para criar sua entrada RpcServices.
ms.assetid: 4fd585b3-3f9b-4f7f-bc1b-22879587a590
ms.tgt_platform: multiple
keywords:
- Compondo SPNs para um serviço de RpcNs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb65b377b5bdd041c5a34b05262f7e62f43801c5
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104453948"
---
# <a name="composing-spns-for-an-rpcns-service"></a>Compondo SPNs para um serviço RpcNs

O exemplo de código a seguir compõe os SPNs (nomes da entidade de serviço) para um serviço RPC que tem uma entrada no contêiner RpcServices no diretório. Um serviço RPC usa a função [**RpcNsBindingExport**](/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindingexporta) para criar sua entrada RpcServices.

Um serviço RPC usa este exemplo de código para criar o SPN ou SPNs que identificam uma instância do serviço. O serviço usa essa rotina para executar as seguintes tarefas:

-   Para registrar ou cancelar o registro dos SPNs no diretório, quando o serviço é instalado ou removido. Para obter mais informações e um exemplo de código, consulte [registrando os SPNs de um serviço](registering-the-spns-for-a-service.md).
-   Registre-se com o serviço de autenticação RPC quando o serviço for iniciado. Para obter mais informações, consulte [autenticação mútua em aplicativos RPC](mutual-authentication-in-rpc-applications.md).

Este exemplo de código usa o nome distinto da entrada RpcServices do serviço para compor o SPN. Antes de chamar esse código, chame a função [**RpcNsBindingExport**](/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindingexporta) para criar a entrada RpcServices do serviço.

Este exemplo de código chama a função [**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) para criar um SPN. O SPN é composto pelo nome da classe de serviço e pelo nome distinto da entrada RpcServices do serviço.


```C++
/**********

    SpnCompose()

    Composes a service principal name from a service name and class.

    Parameters:

    pszServiceName - Contains a null-terminated string that contains 
    the name of the service.

    pszServiceClass - Contains a null-terminated string that contains 
    the name of the service class.

    pspn - Pointer to an LPTSTR array that receives the array of 
    SPNs. This array must freed with the DsFreeSpnArray function when 
    it is no longer required.

    pulSpn - Pointer to a unsigned long that receives the number of 
    elements in the pspn array.

***********/

HRESULT SpnCompose(LPTSTR pszServiceName, 
                   LPTSTR pszServiceClass, 
                   LPTSTR **pspn, 
                   unsigned long *pulSpn) 
{
    HRESULT hr;
    CComPtr<IADs> spRoot;

    // Get the defaultNamingContext for the local domain.
    hr = ADsGetObject(L"LDAP://RootDSE",
                      IID_IADs,
                      (void**)&spRoot);
    if(FAILED(hr))
    {
        return hr;
    }

    // Get the distinguished name of the current domain.
    CComVariant svarDSRoot;
    hr = spRoot->Get(CComBSTR("defaultNamingContext"), &svarDSRoot);
     
    /*
    Compose the DN of the service's entry in the RpcServices 
    container, created by a call to RpcNsBindingExport. The entry 
    for an RPC service is in the System/RpcServices container in the 
    defaultNamingContext of the local domain.
    */
    
    CComBSTR sbstrDsEntryName = "CN=";
    sbstrDsEntryName += pszServiceName;
    sbstrDsEntryName += ",CN=RpcServices,CN=System,";
    sbstrDsEntryName += svarDSRoot.bstrVal;

    USES_CONVERSION;  // Required for the W2T() macro.
    DWORD status;

    /*
    Build the SPN for this service using the DN and the service 
    class.
    */
    status = DsGetSpn(
        DS_SPN_SERVICE, // Type of SPN to create.
        pszServiceClass, // Service class - a name in this case.
        W2T(sbstrDsEntryName), // DN of the RpcServices for 
                               // this RPC service.
        0, // Use the default instance port.
        0, // Number of additional instance names.
        NULL, // No additional instance names.
        NULL, // No additional instance ports.
        pulSpn, // Size of SPN array.
        pspn // Returned SPN(s).
        );
     
    return HRESULT_FROM_WIN32(status);
}
```



 

 