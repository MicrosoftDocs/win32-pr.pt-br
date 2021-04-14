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
# <a name="invoking-creation-wizards-from-your-application"></a>Invocando assistentes de criação do seu aplicativo

Um aplicativo ou componente pode usar os mesmos assistentes de criação de objeto de serviço de diretório usados pelos snap-ins administrativos do MMC Active Directory. Isso é feito com a interface [**IDsAdminCreateObj**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadmincreateobj) .

## <a name="using-the-idsadmincreateobj-interface"></a>Usando a interface IDsAdminCreateObj

Um aplicativo ou componente (cliente) cria uma instância da interface [**IDsAdminCreateObj**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadmincreateobj) chamando [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) com o identificador de **classe \_ DsAdminCreateObj do CLSID** . COM deve ser inicializado chamando [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) antes de **CoCreateInstance** ser chamado.

Em seguida, o cliente chama [**IDsAdminCreateObj:: Initialize**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadmincreateobj-initialize) para inicializar o objeto [**IDsAdminCreateObj**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadmincreateobj) . **IDsAdminCreateObj:: Initialize** aceita um ponteiro de interface [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) que representa o contêiner no qual o objeto deve ser criado e o nome da classe do objeto a ser criado. Ao criar objetos de usuário, também é possível especificar um objeto existente que será copiado para o novo objeto.

Quando o objeto [**IDsAdminCreateObj**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadmincreateobj) tiver sido inicializado, o cliente chamará [**IDsAdminCreateObj:: createjanelarestrita**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadmincreateobj-createmodal) para exibir o assistente de criação de objeto.

Ao contrário da maioria dos identificadores de classe e de interface, **CLSID \_ DsAdminCreateObj** e **IID \_ ADsAdminCreateObj** não são definidos em um arquivo de biblioteca. Isso significa que você deve definir o armazenamento para esses identificadores em seu aplicativo. Para fazer isso, você deve incluir o arquivo Initguid. h imediatamente antes de incluir o DSAdmin. h. O arquivo Initguid. h deve ser incluído apenas uma vez em um aplicativo. O exemplo de código a seguir mostra como incluir esses arquivos.


```C++
#include <initguid.h>
#include <dsadmin.h>
```



O exemplo de código a seguir mostra como a interface [**IDsAdminCreateObj**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadmincreateobj) pode ser criada e usada para iniciar o assistente de criação de objeto para um objeto de usuário.


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



 

 