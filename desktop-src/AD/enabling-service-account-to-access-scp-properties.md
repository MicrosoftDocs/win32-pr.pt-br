---
title: Habilitando a conta de serviço para acessar as propriedades do SCP
description: O exemplo de código a seguir define um par de ACEs (entradas de controle de acesso) em um objeto SCP (ponto de conexão de serviço).
ms.assetid: 663dcf55-5f0d-49af-8b51-4c1e35b79ef1
ms.tgt_platform: multiple
keywords:
- Habilitando a conta de serviço para acessar as propriedades do SCP AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b49adcd1b4747b1c13a64a5af54c6cc6a42e6afe
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103823659"
---
# <a name="enabling-service-account-to-access-scp-properties"></a><span data-ttu-id="f29ed-104">Habilitando a conta de serviço para acessar as propriedades do SCP</span><span class="sxs-lookup"><span data-stu-id="f29ed-104">Enabling Service Account to Access SCP Properties</span></span>

<span data-ttu-id="f29ed-105">O exemplo de código a seguir define um par de ACEs (entradas de controle de acesso) em um objeto SCP (ponto de conexão de serviço).</span><span class="sxs-lookup"><span data-stu-id="f29ed-105">The following code example sets a pair of Access Control Entries (ACEs) on a service connection point (SCP) object.</span></span> <span data-ttu-id="f29ed-106">As ACEs concedem acesso de leitura/gravação à conta de usuário ou computador sob a qual a instância de serviço será executada.</span><span class="sxs-lookup"><span data-stu-id="f29ed-106">The ACEs grant read/write access to the user or computer account under which the service instance will be running.</span></span> <span data-ttu-id="f29ed-107">O instalador do serviço usa um código semelhante ao seguinte para garantir que o serviço possa atualizar suas propriedades em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="f29ed-107">The service installer uses code similar to the following to ensure that the service can update its properties at run time.</span></span> <span data-ttu-id="f29ed-108">Se as ACEs semelhantes a essas não estiverem definidas, o serviço não terá acesso às propriedades do SCP.</span><span class="sxs-lookup"><span data-stu-id="f29ed-108">If ACEs similar to these these are not set, the service will not have access to the properties of the SCP.</span></span>

<span data-ttu-id="f29ed-109">Normalmente, um instalador de serviço definirá essas ACEs depois de criar o objeto SCP.</span><span class="sxs-lookup"><span data-stu-id="f29ed-109">Typically, a service installer will set these ACEs after creating the SCP object.</span></span> <span data-ttu-id="f29ed-110">Para obter mais informações e um exemplo de código que cria um SCP e chama essa função, consulte [como os clientes encontram e usam um ponto de conexão de serviço](how-clients-find-and-use-a-service-connection-point.md).</span><span class="sxs-lookup"><span data-stu-id="f29ed-110">For more information, and a code example that creates an SCP and calls this function, see [How Clients Find and Use a Service Connection Point](how-clients-find-and-use-a-service-connection-point.md).</span></span> <span data-ttu-id="f29ed-111">Se o serviço for reconfigurado para ser executado em uma conta diferente, as ACEs deverão ser atualizadas.</span><span class="sxs-lookup"><span data-stu-id="f29ed-111">If the service is reconfigured to run under a different account, the ACEs must be updated.</span></span> <span data-ttu-id="f29ed-112">Para ser executado com êxito, este exemplo de código deve ser executado no contexto de segurança de um administrador de domínio.</span><span class="sxs-lookup"><span data-stu-id="f29ed-112">To run successfully, this code example must be run in the security context of a domain administrator.</span></span>

<span data-ttu-id="f29ed-113">O primeiro parâmetro da função de exemplo especifica o nome da conta de usuário a ser concedida ao acesso.</span><span class="sxs-lookup"><span data-stu-id="f29ed-113">The first parameter of the sample function specifies the name of the user account to be granted access.</span></span> <span data-ttu-id="f29ed-114">A função assume que o nome está no formato de \*\*\*\*\\*\*\* nome de usuário do domínio\* .</span><span class="sxs-lookup"><span data-stu-id="f29ed-114">The function assumes the name is in *Domain ***\\*** UserName* format.</span></span> <span data-ttu-id="f29ed-115">Se nenhuma conta for especificada, a função assumirá que o serviço usa a conta LocalSystem.</span><span class="sxs-lookup"><span data-stu-id="f29ed-115">If no account is specified, the function assumes the service uses the LocalSystem account.</span></span> <span data-ttu-id="f29ed-116">Isso significa que a função deve conceder acesso à conta de computador do servidor host no qual o serviço está em execução.</span><span class="sxs-lookup"><span data-stu-id="f29ed-116">This means the function must grant access to the computer account of the host server on which the service is running.</span></span> <span data-ttu-id="f29ed-117">Para fazer isso, o exemplo de código chama a função [**GetComputerObjectName**](/windows/desktop/api/secext/nf-secext-getcomputerobjectnamea) para obter o domínio e o nome de usuário do computador local.</span><span class="sxs-lookup"><span data-stu-id="f29ed-117">To do this, the code example calls the [**GetComputerObjectName**](/windows/desktop/api/secext/nf-secext-getcomputerobjectnamea) function to obtain the domain and user name of the local computer.</span></span>

<span data-ttu-id="f29ed-118">O exemplo de código a seguir pode ser modificado para conceder ao serviço acesso completo ao objeto SCP, mas a prática recomendada é conceder apenas os direitos de acesso específicos que o serviço requer em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="f29ed-118">The following code example can be modified to grant the service full access to the SCP object, but the best practice is to grant only the specific access rights that the service requires at run time.</span></span> <span data-ttu-id="f29ed-119">Nesse caso, a função concede acesso a duas propriedades.</span><span class="sxs-lookup"><span data-stu-id="f29ed-119">In this case, the function grants access to two properties.</span></span>



| <span data-ttu-id="f29ed-120">Propriedade</span><span class="sxs-lookup"><span data-stu-id="f29ed-120">Property</span></span>                                                              | <span data-ttu-id="f29ed-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="f29ed-121">Description</span></span>                                                          |
|-----------------------------------------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="f29ed-122">**serviceDNSName**</span><span class="sxs-lookup"><span data-stu-id="f29ed-122">**serviceDNSName**</span></span>](/windows/desktop/ADSchema/a-servicednsname)                       | <span data-ttu-id="f29ed-123">O nome do servidor host no qual o serviço está em execução.</span><span class="sxs-lookup"><span data-stu-id="f29ed-123">The name of the host server on which the service is running.</span></span>         |
| [<span data-ttu-id="f29ed-124">**serviceBindingInformation**</span><span class="sxs-lookup"><span data-stu-id="f29ed-124">**serviceBindingInformation**</span></span>](/windows/desktop/ADSchema/a-servicebindinginformation) | <span data-ttu-id="f29ed-125">Informações de associação privada que o serviço atualiza quando é iniciado.</span><span class="sxs-lookup"><span data-stu-id="f29ed-125">Private binding information that the service updates when it starts.</span></span> |



 

<span data-ttu-id="f29ed-126">Cada propriedade é identificada pelo **schemaIDGUID** da classe **attributeSchema** da propriedade.</span><span class="sxs-lookup"><span data-stu-id="f29ed-126">Each property is identified by the **schemaIDGUID** of the property's **attributeSchema** class.</span></span> <span data-ttu-id="f29ed-127">Cada propriedade no esquema tem seu próprio **schemaIDGUID** exclusivo.</span><span class="sxs-lookup"><span data-stu-id="f29ed-127">Every property in the schema has its own unique **schemaIDGUID**.</span></span> <span data-ttu-id="f29ed-128">O exemplo de código a seguir usa cadeias de caracteres para especificar os GUIDs.</span><span class="sxs-lookup"><span data-stu-id="f29ed-128">The following code example uses strings to specify the GUIDs.</span></span> <span data-ttu-id="f29ed-129">As cadeias de caracteres GUID têm o seguinte formato em que cada "X" é substituído por um dígito hexadecimal: {XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX}.</span><span class="sxs-lookup"><span data-stu-id="f29ed-129">The GUID strings have the following format where each "X" is replaced by a hexadecimal digit: {XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX}.</span></span>

<span data-ttu-id="f29ed-130">Consulte as páginas de referência do esquema de Active Directory para os valores de **schemaIDGUID** atribuídos às propriedades para conceder ou negar acesso ao.</span><span class="sxs-lookup"><span data-stu-id="f29ed-130">Refer to the Active Directory Schema reference pages for the **schemaIDGUID** values assigned to the properties to grant or deny access to.</span></span>

<span data-ttu-id="f29ed-131">O exemplo de código a seguir usa as interfaces [**IADsSecurityDescriptor**](/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor), [**IADsAccessControlList**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrollist)e [**IADsAccessControlEntry**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrolentry) para executar as seguintes operações.</span><span class="sxs-lookup"><span data-stu-id="f29ed-131">The following code example uses the [**IADsSecurityDescriptor**](/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor), [**IADsAccessControlList**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrollist), and [**IADsAccessControlEntry**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrolentry) interfaces to perform the following operations.</span></span>

1.  <span data-ttu-id="f29ed-132">Obtenha o descritor de segurança do objeto SCP.</span><span class="sxs-lookup"><span data-stu-id="f29ed-132">Obtain the security descriptor of the SCP object.</span></span>
2.  <span data-ttu-id="f29ed-133">Defina as ACEs apropriadas na DACL (lista de controle de acesso discricionário) do descritor de segurança.</span><span class="sxs-lookup"><span data-stu-id="f29ed-133">Set the appropriate ACEs in the discretionary access control list (DACL) of the security descriptor.</span></span>
3.  <span data-ttu-id="f29ed-134">Modifique o descritor de segurança do objeto SCP.</span><span class="sxs-lookup"><span data-stu-id="f29ed-134">Modify the security descriptor of the SCP object.</span></span>


```C++
#include <atlbase.h>

//******************************
//
//  AllowAccessToScpProperties()
//
//******************************

HRESULT AllowAccessToScpProperties(
    LPWSTR wszAccountSAM,   // Service account to allow access.
    IADs *pSCPObject)       // IADs pointer to the SCP object.
{
    HRESULT hr = E_FAIL;
    IADsAccessControlList *pACL = NULL;
    IADsSecurityDescriptor *pSD = NULL;
    IDispatch *pDisp = NULL;
    IADsAccessControlEntry *pACE1 = NULL;
    IADsAccessControlEntry *pACE2 = NULL;
    IDispatch *pDispACE = NULL;
    long lFlags = 0L;
    CComBSTR sbstrTrustee;
    CComBSTR sbstrSecurityDescriptor = L"nTSecurityDescriptor";
    VARIANT varSD;

    if(NULL == pSCPObject)
    {
        return E_INVALIDARG;
    }
    
    VariantInit(&varSD);
     
    /*
    If no service account is specified, service runs under 
    LocalSystem. Allow access to the computer account of the 
    service's host.
    */
    if (wszAccountSAM) 
    {
        sbstrTrustee = wszAccountSAM;
    }
    else
    {
        LPWSTR pwszComputerName;
        DWORD dwLen;
        
        // Get the size required for the SAM account name.
        dwLen = 0;
        GetComputerObjectNameW(NameSamCompatible, 
            NULL, &dwLen);
        
        pwszComputerName = new WCHAR[dwLen + 1];
        if(NULL == pwszComputerName)
        {
            hr = E_OUTOFMEMORY;
            goto cleanup;
        }

        /*
        Get the SAM account name of the computer object for 
        the server.
        */
        if(!GetComputerObjectNameW(NameSamCompatible,
            pwszComputerName, &dwLen))
        {
            delete pwszComputerName;
            
            hr = HRESULT_FROM_WIN32(GetLastError());
            goto cleanup;
        }

        sbstrTrustee = pwszComputerName;
        wprintf(L"GetComputerObjectName: %s\n", pwszComputerName);
        delete pwszComputerName;
    } 

    // Get the nTSecurityDescriptor.
    hr = pSCPObject->Get(sbstrSecurityDescriptor, &varSD);
    if (FAILED(hr) || (varSD.vt != VT_DISPATCH)) 
    {
        _tprintf(TEXT("Get nTSecurityDescriptor failed: 0x%x\n"), hr);
        goto cleanup;
    } 
     
    /*
    Use the V_DISPATCH macro to get the IDispatch pointer from 
    VARIANT structure and QueryInterface for an 
    IADsSecurityDescriptor pointer.
    */
    hr = V_DISPATCH( &varSD )->QueryInterface(
        IID_IADsSecurityDescriptor,
        (void**)&pSD);
    if (FAILED(hr)) 
    {
        _tprintf(
            TEXT("Cannot get IADsSecurityDescriptor: 0x%x\n"), 
            hr);
        goto cleanup;
    } 
     
    /*
    Get an IADsAccessControlList pointer to the security 
    descriptor's DACL.
    */
    hr = pSD->get_DiscretionaryAcl(&pDisp);
    if (SUCCEEDED(hr))
    {
        hr = pDisp->QueryInterface(
            IID_IADsAccessControlList,
            (void**)&pACL);
    }
    if (FAILED(hr)) 
    {
        _tprintf(TEXT("Cannot get DACL: 0x%x\n"), hr);
        goto cleanup;
    } 
     
    // Create the COM object for the first ACE.
    hr = CoCreateInstance(CLSID_AccessControlEntry,
                        NULL,
                        CLSCTX_INPROC_SERVER,
                        IID_IADsAccessControlEntry,
                        (void **)&pACE1);
     
    // Create the COM object for the second ACE.
    if (SUCCEEDED(hr))
    {
        hr = CoCreateInstance(CLSID_AccessControlEntry,
                        NULL,
                        CLSCTX_INPROC_SERVER,
                        IID_IADsAccessControlEntry,
                        (void **)&pACE2);
    }
    if (FAILED(hr)) 
    {
        _tprintf(TEXT("Cannot create ACEs: 0x%x\n"), hr);
        goto cleanup;
    } 
     
    // Set the properties of the two ACEs.
                                
    // Allow read and write access to the property.
    hr = pACE1->put_AccessMask(
        ADS_RIGHT_DS_READ_PROP | ADS_RIGHT_DS_WRITE_PROP);
    hr = pACE2->put_AccessMask( 
        ADS_RIGHT_DS_READ_PROP | ADS_RIGHT_DS_WRITE_PROP);
                                
    // Set the trustee, which is either the service account or the 
    // host computer account.
    hr = pACE1->put_Trustee( sbstrTrustee );
    hr = pACE2->put_Trustee( sbstrTrustee );
                                
    // Set the ACE type.
    hr = pACE1->put_AceType( ADS_ACETYPE_ACCESS_ALLOWED_OBJECT );
    hr = pACE2->put_AceType( ADS_ACETYPE_ACCESS_ALLOWED_OBJECT );
                                
    // Set AceFlags to zero because ACE is not inheritable.
    hr = pACE1->put_AceFlags( 0 );
    hr = pACE2->put_AceFlags( 0 );
     
    // Set Flags to indicate an ACE that protects a specified object.
    hr = pACE1->put_Flags( ADS_FLAG_OBJECT_TYPE_PRESENT );
    hr = pACE2->put_Flags( ADS_FLAG_OBJECT_TYPE_PRESENT );
     
    // Set ObjectType to the schemaIDGUID of the attribute.
    // serviceDNSName
    hr = pACE1->put_ObjectType( 
        L"{28630eb8-41d5-11d1-a9c1-0000f80367c1}"); 
    // serviceBindingInformation
    hr = pACE2->put_ObjectType( 
        L"{b7b1311c-b82e-11d0-afee-0000f80367c1}"); 
     
    /*
    Add the ACEs to the DACL. Need an IDispatch pointer for 
    each ACE to pass to the AddAce method.
    */
    hr = pACE1->QueryInterface(IID_IDispatch,(void**)&pDispACE);
    if (SUCCEEDED(hr))
    {
        hr = pACL->AddAce(pDispACE);
    }
    if (FAILED(hr)) 
    {
        _tprintf(TEXT("Cannot add first ACE: 0x%x\n"), hr);
        goto cleanup;
    }
    else 
    {
        if (pDispACE)
            pDispACE->Release();
    
        pDispACE = NULL;
    }
     
    // Repeat for the second ACE.
    hr = pACE2->QueryInterface(IID_IDispatch, (void**)&pDispACE);
    if (SUCCEEDED(hr))
    {
        hr = pACL->AddAce(pDispACE);
    }
    if (FAILED(hr)) 
    {
        _tprintf(TEXT("Cannot add second ACE: 0x%x\n"), hr);
        goto cleanup;
    }
     
    // Write the modified DACL back to the security descriptor.
    hr = pSD->put_DiscretionaryAcl(pDisp);
    if (SUCCEEDED(hr))
    {
        /*
        Write the ntSecurityDescriptor property to the 
        property cache.
        */
        hr = pSCPObject->Put(sbstrSecurityDescriptor, varSD);
        if (SUCCEEDED(hr))
        {
            // SetInfo updates the SCP object in the directory.
            hr = pSCPObject->SetInfo();
        }
    }
                                    
    cleanup:
    if (pDispACE)
        pDispACE->Release();
                        
    if (pACE1)
        pACE1->Release();
                    
    if (pACE2)
        pACE2->Release();
                    
    if (pACL)
        pACL->Release();
               
    if (pDisp)
        pDisp->Release();
            
    if (pSD)
        pSD->Release();
 
    VariantClear(&varSD);
 
    return hr;
}
```



 

 