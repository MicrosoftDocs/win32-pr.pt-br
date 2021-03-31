---
description: Recuperando métodos de serviço com suporte
ms.assetid: 783a6552-9b22-4af4-9252-b443e2624687
title: Recuperando métodos de serviço com suporte
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6029af655a8835a4eee887d919c534856062ff13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829081"
---
# <a name="retrieving-supported-service-methods"></a>Recuperando métodos de serviço com suporte

Os métodos de serviço encapsulam a funcionalidade que cada serviço define e implementa. Eles são específicos de cada tipo de tipo de serviço e são representados por um GUID exclusivo.

Por exemplo, o serviço de contatos define um método **BeginSync** que os aplicativos chamam para preparar o dispositivo para sincronizar objetos de contato e um método **endsync** para notificar o dispositivo de que a sincronização foi concluída.

Os aplicativos podem consultar programaticamente os métodos com suporte e acessar esses métodos e seus atributos usando a interface [**IPortableDeviceServiceCapabilities**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) .

Os métodos de serviço não devem ser confundidos com comandos WPD. Os comandos WPD fazem parte da DDI (interface de driver de dispositivo) Standard WPD e são o mecanismo de comunicação entre um aplicativo WPD e o driver. Os comandos são predefinidos, agrupados por categorias, por exemplo, \_ a categoria de WPD \_ comum e são representados por uma estrutura PROPERTYKEY. Para obter mais informações, consulte o tópico [**comandos**](commands.md) .

O aplicativo WpdServicesApiSample inclui código que demonstra como um aplicativo pode recuperar os métodos com suporte de um determinado serviço Contacts usando as interfaces na tabela a seguir.



|                                                                                      |                                                                                                                |
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Interface                                                                            | Descrição                                                                                                    |
| [**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)                             | Usado para recuperar a interface **IPortableDeviceServiceCapabilities** para acessar os métodos de serviço com suporte. |
| [**IPortableDeviceServiceCapabilities**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities)     | Fornece acesso aos métodos, atributos de método e parâmetros de método com suporte.                             |
| [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) | Contém a lista de métodos com suporte.                                                                        |
| [**IPortableDeviceValues**](iportabledevicevalues.md)                               | Contém os atributos para um método e para os parâmetros de um determinado método.                                      |
| [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md)                 | Contém os parâmetros para um determinado método.                                                                    |



 

Quando o usuário escolhe a opção "5" na linha de comando, o aplicativo invoca o método **ListSupportedMethods** que é encontrado no módulo permethods. cpp.

Observe que, antes de recuperar a lista de eventos, o aplicativo de exemplo abre um serviço de contatos em um dispositivo conectado.

Em WPD, um método é descrito por seu nome, direitos de acesso, parâmetros e dados relacionados. O aplicativo de exemplo exibe um nome amigável, por exemplo, "CustomMethod" ou um GUID. O nome do método ou GUID é seguido pelos dados do Access ("leitura/gravação"), o nome de qualquer formato associado e os dados do parâmetro. Esses dados incluem o nome do parâmetro, uso, VARTYPE e Form.

Cinco métodos no módulo Service Methods. cpp dão suporte à recuperação de métodos (e dados relacionados) para o serviço de contatos fornecido: **ListSupportedMethods**, **DisplayMethod**, **DisplayMethodAccess**, **DisplayFormat** e **DisplayMethodParameters**. O método **ListSupportedMethods** recupera uma contagem de métodos com suporte e o identificador GUID para cada um; em seguida, ele chama o método **DisplayMethod** . O método **DisplayMethod** chama o método [**IPortableDeviceServiceCapapbilities:: getmethodattributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getmethodattributes) para recuperar as opções, os parâmetros e assim por diante do método fornecido. Depois que o **DisplayMethod** recupera os dados do método, ele renderiza o nome (ou GUID), as restrições de acesso, o formato associado (se houver) e as descrições de parâmetro. **DisplayMethodAccess**, **DisplayFormat** e **DisplayMethodParameters** são funções auxiliares que renderizam seus respectivos campos de dados.

O método **ListSupportedMethods** invoca o método [**IPortableDeviceService:: Capabilities**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-capabilities) para recuperar uma interface [**IPortableDeviceServiceCapabilities**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) . Usando essa interface, ele recupera os métodos com suporte chamando o método [**IPortableDeviceServiceCapabilities:: GetSupportedMethods**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getsupportedmethods) . O método **GetSupportedMethods** recupera os GUIDs de cada método suportado pelo serviço e copia esse GUID em um objeto [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) .

O código a seguir usa o método **ListSupportedMethods** .


```C++
// List all supported methods on the service
void ListSupportedMethods(IPortableDeviceService* pService)
{
    HRESULT hr              = S_OK;
    DWORD   dwNumMethods    = 0;
    CComPtr<IPortableDeviceServiceCapabilities>     pCapabilities;
    CComPtr<IPortableDevicePropVariantCollection>   pMethods;

    if (pService == NULL)
    {
        printf("! A NULL IPortableDeviceService interface pointer was received\n");
        return;
    }

    // Get an IPortableDeviceServiceCapabilities interface from the IPortableDeviceService interface to
    // access the service capabilities-specific methods.
    hr = pService->Capabilities(&pCapabilities);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceServiceCapabilities from IPortableDeviceService, hr = 0x%lx\n",hr);
    }

    // Get all methods supported by the service.
    if (SUCCEEDED(hr))
    {
        hr = pCapabilities->GetSupportedMethods(&pMethods);
        if (FAILED(hr))
        {
            printf("! Failed to get supported methods from the service, hr = 0x%lx\n",hr);
        }
    }

    // Get the number of supported methods found on the service.
    if (SUCCEEDED(hr))
    {
        hr = pMethods->GetCount(&dwNumMethods);
        if (FAILED(hr))
        {
            printf("! Failed to get number of supported methods, hr = 0x%lx\n",hr);
        }
    }

    printf("\n%d Supported Methods Found on the service\n\n", dwNumMethods);

    // Loop through each method and display it
    if (SUCCEEDED(hr))
    {
        for (DWORD dwIndex = 0; dwIndex < dwNumMethods; dwIndex++)
        {
            PROPVARIANT pv = {0};
            PropVariantInit(&pv);
            hr = pMethods->GetAt(dwIndex, &pv);

            if (SUCCEEDED(hr))
            {
                // We have a method.  It is assumed that
                // methods are returned as VT_CLSID VarTypes.
                if (pv.puuid != NULL)
                {
                    DisplayMethod(pCapabilities, *pv.puuid);
                    printf("\n");
                }
            }

            PropVariantClear(&pv);
        }
    }    
}
```



Depois que o método **ListSupportedMethods** recupera o GUID para cada evento suportado pelo serviço fornecido, ele invoca o método **DisplayMethod** para recuperar os atributos específicos do método. Esses atributos incluem: nome amigável de script do método, restrições de acesso necessárias, qualquer formato associado e lista de parâmetros.

O método **DisplayMethod** invoca o método [**IPortableDeviceServiceCapabilities:: getmethodattributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getmethodattributes) para recuperar uma coleção de atributos para o método fornecido. Em seguida, ele chama o método [**IPortableDeviceValues:: GetStringValue**](iportabledevicevalues-getstringvalue.md) para recuperar o nome do método. O **DisplayMethod** chama [**IPortableDeviceValues:: GetUnsignedIntegerValue**](iportabledevicevalues-getunsignedintegervalue.md) para recuperar o restrctions de acesso. Depois disso, ele chama [**IPortableDeviceValues:: Getguidvalue**](iportabledevicevalues-getguidvalue.md) para recuperar qualquer formato associado. E, finalmente, o **DisplayMethod** chama [**IPortableDeviceValues:: GetIPortableDeviceKeyCollectionValue**](iportabledevicevalues-getiportabledevicekeycollectionvalue.md) para recuperar os dados do parâmetro. Ele passa os dados retornados por esses métodos para as funções auxiliares **DisplayMethodAccess**, **DisplayFormat** e **DisplayMethodParameters** , que renderizam as informações para o método fornecido.

O código a seguir usa o método **DisplayMethod** .


```C++
// Display basic information about a method
void DisplayMethod(
    IPortableDeviceServiceCapabilities* pCapabilities,
    REFGUID                             Method)
{
    CComPtr<IPortableDeviceValues> pAttributes;

    // Get the method attributes which describe the method
    HRESULT hr = pCapabilities->GetMethodAttributes(Method, &pAttributes);
    if (FAILED(hr))
    {
        printf("! Failed to get the method attributes, hr = 0x%lx\n",hr);
    }

    if (SUCCEEDED(hr))
    {
        PWSTR   pszMethodName  = NULL;
        DWORD   dwMethodAccess = WPD_COMMAND_ACCESS_READ;
        GUID    guidFormat     = GUID_NULL;

        CComPtr<IPortableDeviceValues>          pOptions;
        CComPtr<IPortableDeviceKeyCollection>   pParameters;

        // Display the name of the method if available. Otherwise, fall back to displaying the GUID.
        hr = pAttributes->GetStringValue(WPD_METHOD_ATTRIBUTE_NAME, &pszMethodName);
        if (SUCCEEDED(hr))
        {
            printf("%ws", pszMethodName);
        }
        else
        {
            printf("%ws", (PWSTR)CGuidToString(Method));
        }       

        // Display the method access if available, otherwise default to WPD_COMMAND_ACCESS_READ access
        hr = pAttributes->GetUnsignedIntegerValue(WPD_METHOD_ATTRIBUTE_ACCESS, &dwMethodAccess);
        if (FAILED(hr))
        {
            dwMethodAccess = WPD_COMMAND_ACCESS_READ;
            hr = S_OK;
        }
        printf("\n\tAccess: ");
        DisplayMethodAccess(dwMethodAccess);

        // Display the associated format if specified.
        // Methods that have an associated format may only be supported for that format.
        // Methods that don't have associated formats generally apply to the entire service.
        hr = pAttributes->GetGuidValue(WPD_METHOD_ATTRIBUTE_ASSOCIATED_FORMAT, &guidFormat);
        if (SUCCEEDED(hr))
        {
            printf("\n\tAssociated Format: ");
            DisplayFormat(pCapabilities, guidFormat);
        }

        // Display the method parameters, if available
        hr = pAttributes->GetIPortableDeviceKeyCollectionValue(WPD_METHOD_ATTRIBUTE_PARAMETERS, &pParameters);
        if (SUCCEEDED(hr))
        {
            DisplayMethodParameters(pCapabilities, Method, pParameters);
        }
        
        CoTaskMemFree(pszMethodName);
        pszMethodName = NULL;

    }
}
```



A função auxiliar **DisplayMethodAccess** recebe um valor DWORD que contém as opções de acesso do método. Ele compara esse valor com o \_ comando WPD acesso de comando \_ \_ Read e WPD de \_ acesso a comandos de leitura \_ \_ para determinar o privilégio de acesso do método. Usando o resultado, ele renderiza uma cadeia de caracteres que indica a restrição de acesso para o método fornecido.

O código a seguir usa a função auxiliar **DisplayMethodAccess** .


```C++
void DisplayMethodAccess(
    DWORD   dwAccess)
{
    switch(static_cast<WPD_COMMAND_ACCESS_TYPES>(dwAccess))
    {
        case WPD_COMMAND_ACCESS_READ:
            printf("Read");
            break;
            
        case WPD_COMMAND_ACCESS_READWRITE:
            printf("Read/Write");
            break;

        default:
            printf("Unknown Access");
            break;
    }
}
```



A função auxiliar **DisplayMethod** recebe um objeto [**IPORTABLEDEVICESERVICECAPABILITIES**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) e o GUID do método como parâmetros. Usando o objeto **IPortableDeviceServiceCapabilities** , ele invoca o método [**IPortableDeviceServiceCapabilities:: getmethodattributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getformatattributes) para recuperar os atributos do método e renderizá-los na janela do console do aplicativo.

A função auxiliar **DisplayMethodParameters** recebe um objeto [**IPORTABLEDEVICESERVICECAPABILITIES**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities) , o GUID do método e um objeto IPortableDeviceKeyCollection que contém os parâmetros do método. Usando o objeto [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) , ele invoca o método [**IPortableDeviceServiceCapabilities:: GetMethodParameterAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getmethodparameterattributes) para recuperar o nome, o uso, o VarType e o formato do parâmetro. Ele renderiza essas informações na janela do console do aplicativo.

O código a seguir usa a função auxiliar **DisplayMethodParameters** .


```C++
// Display the method parameters.
void DisplayMethodParameters(
    IPortableDeviceServiceCapabilities* pCapabilities,
    REFGUID                             Method,
    IPortableDeviceKeyCollection*       pParameters)
{
    DWORD   dwNumParameters = 0;

    // Get the number of parameters for this event.
    HRESULT hr = pParameters->GetCount(&dwNumParameters);
    if (FAILED(hr))
    {
        printf("! Failed to get number of parameters, hr = 0x%lx\n",hr);
    }

    printf("\n\t%d Method Parameters:\n", dwNumParameters);

    // Loop through each parameter and display it
    if (SUCCEEDED(hr))
    {
        for (DWORD dwIndex = 0; dwIndex < dwNumParameters; dwIndex++)
        {
            PROPERTYKEY parameter;
            hr = pParameters->GetAt(dwIndex, &parameter);

            if (SUCCEEDED(hr))
            {
                CComPtr<IPortableDeviceValues> pAttributes;

                // Display the parameter's Name, Usage, Vartype, and Form
                hr = pCapabilities->GetMethodParameterAttributes(Method, parameter, &pAttributes);
                if (FAILED(hr))
                {
                    printf("! Failed to get the method parameter attributes, hr = 0x%lx\n",hr);
                }

                if (SUCCEEDED(hr))
                {
                    PWSTR   pszParameterName    = NULL;
                    DWORD   dwAttributeVarType  = 0;
                    DWORD   dwAttributeForm     = WPD_PARAMETER_ATTRIBUTE_FORM_UNSPECIFIED;
                    DWORD   dwAttributeUsage    = (DWORD)-1;

                    hr = pAttributes->GetStringValue(WPD_PARAMETER_ATTRIBUTE_NAME, &pszParameterName);
                    if (SUCCEEDED(hr))
                    {
                        printf("\t\tName: %ws\n", pszParameterName);
                    }
                    else
                    {
                        printf("! Failed to get the method parameter name, hr = 0x%lx\n",hr);
                    }

                    // Read the WPD_PARAMETER_ATTRIBUTE_USAGE value, if specified. 
                    hr = pAttributes->GetUnsignedIntegerValue(WPD_PARAMETER_ATTRIBUTE_USAGE, &dwAttributeUsage);
                    if (SUCCEEDED(hr))
                    {
                        printf("\t\tUsage: ");
                        DisplayParameterUsage(dwAttributeUsage);
                        printf("\n");
                    }
                    else
                    {
                        printf("! Failed to get the method parameter usage, hr = 0x%lx\n",hr);
                    }

                    hr = pAttributes->GetUnsignedIntegerValue(WPD_PARAMETER_ATTRIBUTE_VARTYPE, &dwAttributeVarType);
                    if (SUCCEEDED(hr))
                    {
                        printf("\t\tVARTYPE: ");
                        DisplayVarType(static_cast<VARTYPE>(dwAttributeVarType));
                        printf("\n");
                    }
                    else
                    {
                        printf("! Failed to get the method parameter VARTYPE, hr = 0x%lx\n",hr);
                    }

                    // Read the WPD_PARAMETER_ATTRIBUTE_FORM value.
                    hr = pAttributes->GetUnsignedIntegerValue(WPD_PARAMETER_ATTRIBUTE_FORM, &dwAttributeForm);
                    if (FAILED(hr))
                    {
                        // If the read fails, assume WPD_PARAMETER_ATTRIBUTE_FORM_UNSPECIFIED
                        dwAttributeForm = WPD_PARAMETER_ATTRIBUTE_FORM_UNSPECIFIED;
                        hr = S_OK;
                    }

                    printf("\t\tForm: ");
                    DisplayParameterForm(dwAttributeForm);
                    printf("\n");

                    CoTaskMemFree(pszParameterName);
                    pszParameterName = NULL;
                }
                
                printf("\n");
            }
        }
    }
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md)
</dt> <dt>

[**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)
</dt> <dt>

[**IPortableDeviceServiceCapabilities**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicecapabilities)
</dt> <dt>

[**IPortableDeviceValues**](iportabledevicevalues.md)
</dt> <dt>

[WpdServicesApiSample](wpdapisample-sample-service-application.md)
</dt> </dl>

 

 



