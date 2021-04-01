---
title: Registrando o objeto COM da página de propriedades em um especificador de exibição
description: Este tópico mostra como registrar uma DLL de extensão que contém uma folha de propriedades Active Directory com o registro do Windows e Active Directory.
ms.assetid: e2d6142b-c2fe-4435-b4af-83f7cd45218b
ms.tgt_platform: multiple
keywords:
- Registrando o objeto COM da página de propriedades em um especificador de exibição Active Directory
- Active Directory de objeto COM de página de propriedades, registrando em um especificador de exibição
- Active Directory de especificadores de exibição, registrando o objeto COM da página de propriedades em
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c5b08ac0ea6329026a6d367e71064bde917b1a6
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104084437"
---
# <a name="registering-the-property-page-com-object-in-a-display-specifier"></a>Registrando o objeto COM da página de propriedades em um especificador de exibição

Ao usar COM para criar uma DLL de extensão de folha de propriedades para Active Directory Domain Services, você também deve registrar a extensão com o registro do Windows e Active Directory Domain Services. O registro da extensão permite que os snap-ins administrativos do MMC Active Directory e o Shell do Windows reconheçam a extensão.

## <a name="registering-in-the-windows-registry"></a>Registrando no registro do Windows

Como todos os servidores COM, uma extensão de folha de propriedades deve ser registrada no registro do Windows. A extensão é registrada sob a chave a seguir.

```
HKEY_CLASSES_ROOT
   CLSID
      <clsid>
```

*<clsid>* é a representação de cadeia de caracteres do CLSID, conforme produzido pela função [**StringFromCLSID**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) . Sob a *<clsid>* chave, há uma chave **InprocServer32** que identifica o objeto como um servidor no processo de 32 bits. Na chave **InprocServer32** , o local da dll é especificado no valor padrão e o modelo de threading é especificado no valor de **ThreadingModel** . Todas as extensões de folha de propriedades devem usar o modelo de Threading "Apartment".

## <a name="registering-with-active-directory-domain-services"></a>Registrando com Active Directory Domain Services

O registro da extensão da folha de propriedades é específico de uma localidade. Se a extensão da folha de propriedades se aplicar a todas as localidades, ela deverá ser registrada no objeto [**displaySpecifier**](/windows/desktop/ADSchema/c-displayspecifier) da classe Object em todos os subcontêineres de localidade no contêiner exibir especificadores. Se a extensão da folha de Propriedades for localizada para uma determinada localidade, registre-a no objeto **displaySpecifier** nesse subcontêiner de localidade. Para obter mais informações sobre o contêiner e as localidades dos especificadores de exibição, consulte [Exibir especificadores de exibição](display-specifiers.md) e [contêiner DisplaySpecifiers](displayspecifiers-container.md).

Há três atributos de especificador de exibição para os quais uma extensão de folha de propriedades pode ser registrada. São [**adminPropertyPages**](/windows/desktop/ADSchema/a-adminpropertypages), [**shellPropertyPages**](/windows/desktop/ADSchema/a-shellpropertypages)e [**adminMultiselectPropertyPages**](/windows/desktop/ADSchema/a-adminmultiselectpropertypages).

O atributo [**adminPropertyPages**](/windows/desktop/ADSchema/a-adminpropertypages) identifica as páginas de propriedades administrativas a serem exibidas em Active Directory snap-ins administrativos. A página de propriedades é exibida quando o usuário exibe as propriedades de objetos da classe apropriada em um dos snap-ins administrativos do MMC Active Directory.

O atributo [**shellPropertyPages**](/windows/desktop/ADSchema/a-shellpropertypages) identifica as páginas de propriedades do usuário final a serem exibidas no Shell do Windows. A página de propriedades é exibida quando o usuário exibe as propriedades dos objetos da classe apropriada no Windows Explorer. A partir dos sistemas operacionais Windows Server 2003, o Shell do Windows não exibe mais objetos do Active Directory Domain Services.

O [**adminMultiselectPropertyPages**](/windows/desktop/ADSchema/a-adminmultiselectpropertypages) só está disponível nos sistemas operacionais Windows Server 2003. A página de propriedades é exibida quando o usuário exibe as propriedades de mais de um objeto da classe apropriada em um dos snap-ins administrativos do MMC Active Directory.

Todos esses atributos têm valores múltiplos.

Os valores para os atributos [**adminPropertyPages**](/windows/desktop/ADSchema/a-adminpropertypages) e [**shellPropertyPages**](/windows/desktop/ADSchema/a-shellpropertypages) exigem o formato a seguir.


```C++
<order number>,<clsid>,<optional data>
```



Os valores para o atributo [**adminMultiselectPropertyPages**](/windows/desktop/ADSchema/a-adminmultiselectpropertypages) exigem o formato a seguir.


```C++
<order number>,<clsid>
```



O " &lt; número do pedido &gt; " é um número sem sinal que representa a posição da página na planilha. Quando uma folha de propriedades é exibida, os valores são classificados usando uma comparação de "número de &lt; ordem" de cada valor &gt; . Se mais de um valor tiver o mesmo " &lt; número do pedido &gt; ", esses objetos com da página de propriedades serão carregados na ordem em que são lidos do servidor de Active Directory. Se possível, você deve usar um " &lt; número de pedido" não existente &gt; ; ou seja, um não é usado por outros valores na propriedade. Não há uma posição de início prescrita e as lacunas são permitidas na &lt; sequência "número do pedido &gt; ".

O " &lt; CLSID &gt; " é a representação de cadeia de caracteres do CLSID, conforme produzido pela função [**StringFromCLSID**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) .

O " &lt; dados opcionais &gt; " é um valor de cadeia de caracteres que não é necessário. Esse valor pode ser recuperado pelo objeto COM da página de propriedades usando o ponteiro [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) passado para o método [**IShellExtInit:: Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) . O objeto COM da página de propriedades Obtém esses dados chamando [**IDataObject:: GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) com o formato de área de transferência [**CFSTR \_ DSPROPERTYPAGEINFO**](cfstr-dspropertypageinfo.md) . Isso fornece um **HGLOBAL** que contém uma estrutura [**DSPROPERTYPAGEINFO**](/windows/desktop/api/Dsclient/ns-dsclient-dspropertypageinfo) a estrutura **DSPROPERTYPAGEINFO** contém uma cadeia de caracteres Unicode que contém os " &lt; dados opcionais &gt; ". Os " &lt; dados opcionais &gt; " não são permitidos com o atributo [**adminMultiselectPropertyPages**](/windows/desktop/ADSchema/a-adminmultiselectpropertypages) . O exemplo de código C/C++ a seguir mostra como recuperar os " &lt; dados opcionais &gt; ".


```C++
fe.cfFormat = RegisterClipboardFormat(CFSTR_DSPROPERTYPAGEINFO);
fe.ptd = NULL;
fe.dwAspect = DVASPECT_CONTENT;
fe.lindex = -1;
fe.tymed = TYMED_HGLOBAL;
hr = pDataObj->GetData(&fe, &stm);
if(SUCCEEDED(hr))
{
    DSPROPERTYPAGEINFO *pPageInfo;
    
    pPageInfo = (DSPROPERTYPAGEINFO*)GlobalLock(stm.hGlobal);
    if(pPageInfo)
    {
        LPWSTR  pwszData;

        pwszData = (LPWSTR)((LPBYTE)pPageInfo + pPageInfo->offsetString);
        pwszData = NULL;
        
        GlobalUnlock(stm.hGlobal);
    }

    ReleaseStgMedium(&stm);
}
```



Uma extensão de folha de propriedades pode implementar mais de uma página de propriedades; um possível uso dos " &lt; dados opcionais &gt; " é nomear as páginas a serem exibidas. Isso fornece a flexibilidade de escolher a implementação de vários objetos COM, um para cada página ou um único objeto COM para lidar com várias páginas.

O exemplo de código a seguir é um valor de exemplo que pode ser usado para os atributos [**adminPropertyPages**](/windows/desktop/ADSchema/a-adminpropertypages), [**shellPropertyPages**](/windows/desktop/ADSchema/a-shellpropertypages)ou [**adminMultiselectPropertyPages**](/windows/desktop/ADSchema/a-adminmultiselectpropertypages) .


```C++
1,{6dfe6485-a212-11d0-bcd5-00c04fd8d5b6}
```



> [!IMPORTANT]
> Para o Shell do Windows, os dados do especificador de exibição são recuperados no logon do usuário e armazenados em cache para a sessão do usuário. Para snap-ins administrativos, os dados do especificador de exibição são recuperados quando o snap-in é carregado e armazenado em cache durante o tempo de vida do processo. Para o Shell do Windows, isso indica que as alterações nos especificadores de exibição entram em vigor depois que um usuário faz logoff e, em seguida, faz logon novamente. Para os snap-ins administrativos, as alterações entram em vigor quando o snap-in ou o arquivo de console é carregado.

 

## <a name="adding-a-value-to-the-property-sheet-extension-attributes"></a>Adicionando um valor aos atributos de extensão da folha de propriedades

O procedimento a seguir descreve como registrar uma extensão de folha de propriedades em um dos atributos de extensão da folha de propriedades.

**Registrando uma extensão de folha de propriedades em um dos atributos de extensão da folha de propriedades**

1.  Verifique se a extensão ainda não existe nos valores de atributo.
2.  Adicione o novo valor ao final da lista de ordenação de páginas de propriedades. Isso define a parte " &lt; número &gt; do pedido" do valor do atributo para o próximo valor após o número de ordem mais alto existente.
3.  O método [**IADs::P utex**](/windows/desktop/api/iads/nf-iads-iads-putex) é usado para adicionar o novo valor ao atributo. O parâmetro *lnControlCode* deve ser definido como **Propriedade do ADS \_ \_ Append** para que o novo valor seja anexado aos valores existentes e não, portanto, substitua os valores existentes. O método [**IADs:: setinfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) deve ser chamado posteriormente para confirmar a alteração no diretório.

Lembre-se de que a mesma extensão de folha de propriedades pode ser registrada para mais de uma classe de objeto.

O método [**IADs::P utex**](/windows/desktop/api/iads/nf-iads-iads-putex) é usado para adicionar o novo valor ao atributo. O parâmetro *lnControlCode* deve ser definido como **Propriedade do ADS \_ \_ Append**, para que o novo valor seja anexado aos valores existentes e não, portanto, substitua os valores existentes. O método [**IADs:: setinfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) deve ser chamado depois de confirmar a alteração no diretório.

O exemplo de código a seguir adiciona uma extensão de folha de propriedades à classe Group na localidade padrão do computador. Lembre-se de que a função **AddPropertyPageToDisplaySpecifier** verifica o CLSID da extensão da folha de propriedades nos valores existentes, obtém o número de ordem mais alto e adiciona o valor para a página de propriedades usando [**IADs::P utex**](/windows/desktop/api/iads/nf-iads-iads-putex) com o código de controle **\_ \_ Append da propriedade ADS** .


```C++
//  Add msvcrt.dll to the project.
//  Add activeds.lib to the project.
//  Add adsiid.lib to the project.

#include "stdafx.h"
#include <wchar.h>
#include <objbase.h>
#include <activeds.h>
#include "atlbase.h"

HRESULT AddPropertyPageToDisplaySpecifier(LPOLESTR szClassName, //  ldapDisplayName of the class.
                                          CLSID *pPropPageCLSID //  CLSID of property page COM object.
                                         );

HRESULT BindToDisplaySpecifiersContainerByLocale(LCID *locale,
                                                 IADsContainer **ppDispSpecCont
                                                 );

HRESULT GetDisplaySpecifier(IADsContainer *pContainer, LPOLESTR szDispSpec, IADs **ppObject);

//  Entry point for the application.
void wmain(int argc, wchar_t *argv[ ])
{

    wprintf(L"This program adds a sample property page to the display specifier for group class in the local computer's default locale.\n");

    // Initialize COM.
    CoInitialize(NULL);
    HRESULT hr = S_OK;

    //  Class ID for the sample property page.
    LPOLESTR szCLSID = L"{D9FCE809-8A10-11d2-A7E7-00C04F79DC0F}";
    LPOLESTR szClass = L"group";
    CLSID clsid;
    //  Convert to GUID.
    hr = CLSIDFromString(
        szCLSID,  //  Pointer to the string representation of the CLSID.
        &clsid    //  Pointer to the CLSID.
        );

    hr = AddPropertyPageToDisplaySpecifier(szClass, //  ldapDisplayName of the class.
                                           &clsid //  CLSID of property page COM object.
                                          );
    if (S_OK == hr)
        wprintf(L"Property page registered successfully\n");
    else if (S_FALSE == hr)
        wprintf(L"Property page was not added because it was already registered.\n");
    else
        wprintf(L"Property page was not added. HR: %x.\n");

    //  Uninitialize COM.
    CoUninitialize();
    return;
}

//  Adds a property page to Active Directory admin snap-ins.
HRESULT AddPropertyPageToDisplaySpecifier(LPOLESTR szClassName, //  ldapDisplayName of class.
                                          CLSID *pPropPageCLSID //  CLSID of property page COM object.
                                         )
{
    HRESULT hr = E_FAIL;
    IADsContainer *pContainer = NULL;
    LPOLESTR szDispSpec = new OLECHAR[MAX_PATH];
    IADs *pObject = NULL;
    VARIANT var;
    CComBSTR sbstrProperty = L"adminPropertyPages";
    LCID locale = NULL;
    //  Get the display specifier container using default system locale.
    //  When adding a property page COM object, specify the locale
    //  because the registration is locale-specific.
    //  This means if you created a property page
    //  for German, explicitly add it to the 407 container,
    //  so that it will be used when a computer is running with locale
    //  set to German and not the locale set on the
    //  computer where this application is running.
    hr = BindToDisplaySpecifiersContainerByLocale(&locale,
                                                  &pContainer
                                                 );
    //  Handle fail case where dispspec object
    //  is not found and give option to create one.

    if (SUCCEEDED(hr))
    {
        //  Bind to display specifier object for the specified class.
        //  Build the display specifier name.
#ifdef _MBCS
        wcscpy_s(szDispSpec, szClassName);
        wcscat_s(szDispSpec, L"-Display");
        hr = GetDisplaySpecifier(pContainer, szDispSpec, &pObject);
#endif _MBCS#endif _MBCS
        if (SUCCEEDED(hr))
        {
            //  Convert GUID to string.
            LPOLESTR szDSGUID = new WCHAR [39];
            ::StringFromGUID2(*pPropPageCLSID, szDSGUID, 39); 

            //  Get the adminPropertyPages property.
            hr = pObject->GetEx(sbstrProperty, &var);
            if (SUCCEEDED(hr))
            {
                LONG lstart, lend;
                SAFEARRAY *sa = V_ARRAY(&var);
                VARIANT varItem;
                //  Get the lower and upper bound.
                hr = SafeArrayGetLBound(sa, 1, &lstart);
                if (SUCCEEDED(hr))
                {
                    hr = SafeArrayGetUBound(sa, 1, &lend);
                }
                if (SUCCEEDED(hr))
                {
                    //  Iterate the values to verify if the prop page CLSID
                    //  is already registered.
                    VariantInit(&varItem);
                    BOOL bExists = FALSE;
                    UINT uiLastItem = 0;
                    UINT uiTemp = 0;
                    INT iOffset = 0;
                    LPOLESTR szMainStr = new OLECHAR[MAX_PATH];
                    LPOLESTR szItem = new OLECHAR[MAX_PATH];
                    LPOLESTR szStr = NULL;
                    for (long idx=lstart; idx <= lend; idx++)
                    {
                        hr = SafeArrayGetElement(sa, &idx, &varItem);
                        if (SUCCEEDED(hr))
                        {
#ifdef _MBCS
                            //  Verify that the specified CLSID is already registered.
                            wcscpy_s(szMainStr,varItem.bstrVal);
                            if (wcsstr(szMainStr,szDSGUID))
                                bExists = TRUE;
                            //  Get the index which is the number before the first comma.
                            szStr = wcschr(szMainStr, ',');
                            iOffset = (int)(szStr - szMainStr);
                            wcsncpy_s(szItem, szMainStr, iOffset);
                            szItem[iOffset]=0L;
                            uiTemp = _wtoi(szItem);
                            if (uiTemp > uiLastItem)
                                uiLastItem = uiTemp;
                            VariantClear(&varItem);
#endif _MBCS
                        }
                    }
                    //  If the CLSID is not registered, add it.
                    if (!bExists)
                    {
                        //  Build the value to add.
                        LPOLESTR szValue = new OLECHAR[MAX_PATH];
                        //  Next index to add at end of list.
#ifdef _MBCS
                        uiLastItem++;
                        _itow_s(uiLastItem, szValue, 10);   
                        wcscat_s(szValue,L",");
                        //  Add the class ID for the property page.
                        wcscat_s(szValue,szDSGUID);
                        wprintf(L"Value to add: %s\n", szValue);
#endif _MBCS

                        VARIANT varAdd;
                        //  Only one value to add
                        LPOLESTR pszAddStr[1];
                        pszAddStr[0]=szValue;
                        ADsBuildVarArrayStr(pszAddStr, 1, &varAdd);

                        hr = pObject->PutEx(ADS_PROPERTY_APPEND, sbstrProperty, varAdd);
                        if (SUCCEEDED(hr))
                        {
                            //  Commit the change.
                            hr = pObject->SetInfo();
                        }
                    }
                    else
                        hr = S_FALSE;
                }
            }
            VariantClear(&var);
        }
        if (pObject)
            pObject->Release();
    }

    return hr;
}

//  This function returns a pointer to the display specifier container 
//  for the specified locale.
//  If locale is NULL, use the default system locale and then return the locale in the locale param.
HRESULT BindToDisplaySpecifiersContainerByLocale(LCID *locale,
                                                 IADsContainer **ppDispSpecCont
                                                )
{
    HRESULT hr = E_FAIL;

    if ((!ppDispSpecCont)||(!locale))
        return E_POINTER;

    //  If no locale is specified, use the default system locale.
    if (!(*locale))
    {
        *locale = GetSystemDefaultLCID();
        if (!(*locale))
            return E_FAIL;
    }

    //  Verify that it is a valid locale.
    if (!IsValidLocale(*locale, LCID_SUPPORTED))
        return E_INVALIDARG;

    LPOLESTR szPath = new OLECHAR[MAX_PATH*2];
    IADs *pObj = NULL;
    VARIANT var;

    hr = ADsOpenObject(L"LDAP://rootDSE",
                       NULL,
                       NULL,
                       ADS_SECURE_AUTHENTICATION, // Use Secure Authentication.
                       IID_IADs,
                       (void**)&pObj);

    if (SUCCEEDED(hr))
    {
        //  Get the DN to the config container.
        hr = pObj->Get(CComBSTR("configurationNamingContext"), &var);
        if (SUCCEEDED(hr))
        {
#ifdef _MBCS
            //  Build the string to bind to the DisplaySpecifiers container.
            swprintf_s(szPath,L"LDAP://cn=%x,cn=DisplaySpecifiers,%s", *locale, var.bstrVal);
            //  Bind to the DisplaySpecifiers container.
            *ppDispSpecCont = NULL;
            hr = ADsOpenObject(szPath,
                               NULL,
                               NULL,
                               ADS_SECURE_AUTHENTICATION, // Use Secure Authentication.
                               IID_IADsContainer,
                               (void**)ppDispSpecCont);
#endif _MBCS

            if(FAILED(hr))
            {
                if (*ppDispSpecCont)
                {
                    (*ppDispSpecCont)->Release();
                    (*ppDispSpecCont) = NULL;
                }
            }
        }
    }
    //   Cleanup.
    VariantClear(&var);
    if (pObj)
        pObj->Release();

    return hr;
}

HRESULT GetDisplaySpecifier(IADsContainer *pContainer, LPOLESTR szDispSpec, IADs **ppObject)
{
    HRESULT hr = E_FAIL;
    CComBSTR sbstrDSPath;
    IDispatch *pDisp = NULL;

    if (!pContainer)
    {
        hr = E_POINTER;
        return hr;
    }

    //  Verify other pointers.
    //  Initialize the output pointer.
    (*ppObject) = NULL;

    //  Build relative path to the display specifier object.
    sbstrDSPath = "CN=";
    sbstrDSPath += szDispSpec;

    //  Use child object binding with IADsContainer::GetObject.
    hr = pContainer->GetObject(CComBSTR("displaySpecifier"),
        sbstrDSPath,
        &pDisp);
    if (SUCCEEDED(hr))
    {
        hr = pDisp->QueryInterface(IID_IADs, (void**)ppObject);
        if (FAILED(hr))
        {
            //  Clean up.
            if (*ppObject)
                (*ppObject)->Release();
        }
    }

    if (pDisp)
        pDisp->Release();

    return hr;

}
```



 

 