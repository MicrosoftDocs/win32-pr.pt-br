---
title: Invocando assistentes de criação do seu aplicativo
description: Um aplicativo ou componente pode usar os mesmos assistentes de criação de objeto de serviço de diretório usados pelos snap-ins administrativos do MMC Active Directory. Isso é feito com a interface IDsAdminCreateObj.
ms.assetid: be4b6101-f795-403b-b93e-960759ac4f14
ms.tgt_platform: multiple
keywords:
- Invocando assistentes de criação do AD do aplicativo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa523d3b861d1d4a7588455b04c1a9633734253a
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104453916"
---
# <a name="invoking-creation-wizards-from-your-application"></a><span data-ttu-id="759aa-104">Invocando assistentes de criação do seu aplicativo</span><span class="sxs-lookup"><span data-stu-id="759aa-104">Invoking Creation Wizards from Your Application</span></span>

<span data-ttu-id="759aa-105">Um aplicativo ou componente pode usar os mesmos assistentes de criação de objeto de serviço de diretório usados pelos snap-ins administrativos do MMC Active Directory. Isso é feito com a interface [**IDsAdminCreateObj**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadmincreateobj) .</span><span class="sxs-lookup"><span data-stu-id="759aa-105">An application or component can use the same directory service object creation wizards used by the Active Directory administrative MMC snap-ins. This is accomplished with the [**IDsAdminCreateObj**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadmincreateobj) interface.</span></span>

## <a name="using-the-idsadmincreateobj-interface"></a><span data-ttu-id="759aa-106">Usando a interface IDsAdminCreateObj</span><span class="sxs-lookup"><span data-stu-id="759aa-106">Using the IDsAdminCreateObj Interface</span></span>

<span data-ttu-id="759aa-107">Um aplicativo ou componente (cliente) cria uma instância da interface [**IDsAdminCreateObj**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadmincreateobj) chamando [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) com o identificador de **classe \_ DsAdminCreateObj do CLSID** .</span><span class="sxs-lookup"><span data-stu-id="759aa-107">An application or component (client) creates an instance of the [**IDsAdminCreateObj**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadmincreateobj) interface by calling [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) with the **CLSID\_DsAdminCreateObj** class identifier.</span></span> <span data-ttu-id="759aa-108">COM deve ser inicializado chamando [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) antes de **CoCreateInstance** ser chamado.</span><span class="sxs-lookup"><span data-stu-id="759aa-108">COM must be initialized by calling [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) before **CoCreateInstance** is called.</span></span>

<span data-ttu-id="759aa-109">Em seguida, o cliente chama [**IDsAdminCreateObj:: Initialize**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadmincreateobj-initialize) para inicializar o objeto [**IDsAdminCreateObj**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadmincreateobj) .</span><span class="sxs-lookup"><span data-stu-id="759aa-109">The client then calls [**IDsAdminCreateObj::Initialize**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadmincreateobj-initialize) to initialize the [**IDsAdminCreateObj**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadmincreateobj) object.</span></span> <span data-ttu-id="759aa-110">**IDsAdminCreateObj:: Initialize** aceita um ponteiro de interface [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) que representa o contêiner no qual o objeto deve ser criado e o nome da classe do objeto a ser criado.</span><span class="sxs-lookup"><span data-stu-id="759aa-110">**IDsAdminCreateObj::Initialize** accepts an [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) interface pointer that represents the container that the object should be created in, and the class name of the object to be created.</span></span> <span data-ttu-id="759aa-111">Ao criar objetos de usuário, também é possível especificar um objeto existente que será copiado para o novo objeto.</span><span class="sxs-lookup"><span data-stu-id="759aa-111">When creating user objects, it is also possible to specify an existing object that will be copied to the new object.</span></span>

<span data-ttu-id="759aa-112">Quando o objeto [**IDsAdminCreateObj**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadmincreateobj) tiver sido inicializado, o cliente chamará [**IDsAdminCreateObj:: createjanelarestrita**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadmincreateobj-createmodal) para exibir o assistente de criação de objeto.</span><span class="sxs-lookup"><span data-stu-id="759aa-112">When the [**IDsAdminCreateObj**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadmincreateobj) object has been initialized, the client calls [**IDsAdminCreateObj::CreateModal**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadmincreateobj-createmodal) to display the object creation wizard.</span></span>

<span data-ttu-id="759aa-113">Ao contrário da maioria dos identificadores de classe e de interface, **CLSID \_ DsAdminCreateObj** e **IID \_ ADsAdminCreateObj** não são definidos em um arquivo de biblioteca.</span><span class="sxs-lookup"><span data-stu-id="759aa-113">Unlike most class and interface identifiers, **CLSID\_DsAdminCreateObj** and **IID\_ADsAdminCreateObj** are not defined in a library file.</span></span> <span data-ttu-id="759aa-114">Isso significa que você deve definir o armazenamento para esses identificadores em seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="759aa-114">This means you must define the storage for these identifiers within your application.</span></span> <span data-ttu-id="759aa-115">Para fazer isso, você deve incluir o arquivo Initguid. h imediatamente antes de incluir o DSAdmin. h.</span><span class="sxs-lookup"><span data-stu-id="759aa-115">To do this, you must include the file initguid.h immediately before including dsadmin.h.</span></span> <span data-ttu-id="759aa-116">O arquivo Initguid. h deve ser incluído apenas uma vez em um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="759aa-116">The initguid.h file must only be included once in an application.</span></span> <span data-ttu-id="759aa-117">O exemplo de código a seguir mostra como incluir esses arquivos.</span><span class="sxs-lookup"><span data-stu-id="759aa-117">The following code example shows how to include these files.</span></span>


```C++
#include <initguid.h>
#include <dsadmin.h>
```



<span data-ttu-id="759aa-118">O exemplo de código a seguir mostra como a interface [**IDsAdminCreateObj**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadmincreateobj) pode ser criada e usada para iniciar o assistente de criação de objeto para um objeto de usuário.</span><span class="sxs-lookup"><span data-stu-id="759aa-118">The following code example shows how the [**IDsAdminCreateObj**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadmincreateobj) interface can be created and used to start the object creation wizard for a user object.</span></span>


```C++
//  Add activeds.lib to your project
//  Add adsiid.lib to your project

#include "stdafx.h"
#include <atlbase.h>
#include <atlstr.h>
#include "activeds.h"
#include <initguid.h> // Only include this in one source file
#include <dsadmin.h>

//  GetUserContainer() function binds to the user container
IADsContainer* GetUserContainer(void)
{
    IADsContainer *pUsers = NULL;
    HRESULT hr;
    IADs *pRoot;

    //  Bind to the rootDSE.
    hr = ADsGetObject(L"LDAP://rootDSE", IID_IADs, (LPVOID*)&pRoot);

    if(SUCCEEDED(hr))
    {
        VARIANT var;
        VariantInit(&var);
        CComBSTR sbstr(L"defaultNamingContext");

        //  Get the default naming context (domain) DN.
        hr = pRoot->Get(sbstr, &var);
        if(SUCCEEDED(hr) && (VT_BSTR == var.vt))
        {
            CStringW sstr(L"LDAP://CN=Users,");
            sstr += var.bstrVal;

            //  Bind to the User container.
            hr = ADsGetObject(sstr, IID_IADsContainer, (LPVOID*)&pUsers);

            VariantClear(&var);
        }
    }

    return pUsers;
}


//  The LaunchNewUserWizard() function launches the user wizard.
HRESULT LaunchNewUserWizard(IADs** ppAdsOut)
{
    if(NULL == ppAdsOut)
    {
        return E_INVALIDARG;
    }

    HRESULT hr;
    IDsAdminCreateObj* pCreateObj = NULL;

    hr = ::CoCreateInstance(CLSID_DsAdminCreateObj,
                            NULL, 
                            CLSCTX_INPROC_SERVER,
                            IID_IDsAdminCreateObj,
                            (void**)&pCreateObj);

    if(SUCCEEDED(hr))
    {
        IADsContainer *pContainer;

        pContainer = GetUserContainer();

        if(pContainer)
        {
            hr = pCreateObj->Initialize(pContainer, NULL, L"user");
            if(SUCCEEDED(hr))
            {
                HWND    hwndParent;

                hwndParent = GetDesktopWindow();

                hr = pCreateObj->CreateModal(hwndParent, ppAdsOut);
            }

            pContainer->Release();
        }

        pCreateObj->Release();
    }

    return hr;    
}

//  Entry point to the application
int main(void)
{
    HRESULT hr;
    IADs *pAds = NULL;

    CoInitialize(NULL);

    hr = LaunchNewUserWizard(&pAds);
    if((S_OK == hr) && (NULL != pAds))
    {
        pAds->Release();
    }

    CoUninitialize();

    return 0;
}
```



 

 