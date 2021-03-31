---
description: Transferindo um objeto Properties-Only para o dispositivo
ms.assetid: 6305cff9-c0ce-4ef5-a129-bc329b9c563f
title: Transferindo um objeto Properties-Only para o dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e20f9bcfecd46ea3047310ea5b946a366b35b9c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662805"
---
# <a name="transferring-a-properties-only-object-to-the-device"></a>Transferindo um objeto Properties-Only para o dispositivo

Embora o exemplo no tópico anterior tenha demonstrado a criação de conteúdo em um dispositivo que consiste em Propriedades e dados, este tópico se concentra na criação de um objeto somente de propriedades.

Transferências somente de propriedade são realizadas usando as interfaces descritas na tabela a seguir.



| Interface                                                          | Descrição                                            |
|--------------------------------------------------------------------|--------------------------------------------------------|
| [**Interface IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent) | Fornece acesso aos métodos específicos de conteúdo.       |
| [**Interface IPortableDeviceValues**](iportabledevicevalues.md)   | Usado para recuperar propriedades que descrevem o conteúdo. |



 

A `TransferContactToDevice` função no módulo ContentTransfer. cpp do aplicativo de exemplo demonstra como um aplicativo pode transferir informações de contato de um PC para um dispositivo conectado. Neste exemplo específico, o nome do contato transferido é um "John Kane" embutido em código e o número de telefone de contato transferido é sempre "425-555-0123".

A primeira tarefa realizada pela `TransferContactToDevice` função é solicitar que o usuário insira um identificador de objeto para o objeto pai no dispositivo (sob o qual o conteúdo será transferido).


```C++
HRESULT                             hr = S_OK;
WCHAR                               szSelection[81]        = {0};
CComPtr<IPortableDeviceValues>      pFinalObjectProperties;
CComPtr<IPortableDeviceContent>     pContent;

// Prompt user to enter an object identifier for the parent object on the device to transfer.
printf("Enter the identifer of the parent object which the contact will be transferred under.\n>");
hr = StringCbGetsW(szSelection,sizeof(szSelection));
if (FAILED(hr))
{
    printf("An invalid object identifier was specified, aborting content transfer\n");
}
```



A próxima etapa é a recuperação das propriedades de contato, que serão usadas quando o exemplo gravar o novo contato no dispositivo. A recuperação de propriedades de contato é executada pela `GetRequiredPropertiesForPropertiesOnlyContact` função auxiliar.


```C++
// 2) Get the properties that describe the object being created on the device

if (SUCCEEDED(hr))
{
    hr = GetRequiredPropertiesForPropertiesOnlyContact(szSelection,              // Parent to transfer the data under
                                                       &pFinalObjectProperties);  // Returned properties describing the data
    if (FAILED(hr))
    {
        printf("! Failed to get required properties needed to transfer an image file to the device, hr = 0x%lx\n", hr);
    }
}
```



Essa função grava os dados a seguir em um objeto **IPortableDeviceValues** .

-   O identificador de objeto para o pai do contato no dispositivo. (Esse é o destino onde o dispositivo armazenará o objeto.)
-   O tipo de objeto (um contato).
-   O nome do contato (uma cadeia de caracteres embutida em código de "John Kane").
-   O número de telefone de contato (uma cadeia de caracteres embutida em código de "425-555-0123").

A etapa final cria o objeto somente propriedades no dispositivo (usando as propriedades definidas pela `GetRequiredPropertiesForPropertiesOnlyContact` função auxiliar). Isso é feito chamando o método **IPortableDeviceContent:: CreateObjectWithPropertiesOnly** .


```C++
if (SUCCEEDED(hr))
{
    PWSTR pszNewlyCreatedObject = NULL;
    hr = pContent->CreateObjectWithPropertiesOnly(pFinalObjectProperties,    // Properties describing the object data
                                                  &pszNewlyCreatedObject);
    if (SUCCEEDED(hr))
    {
        printf("The contact was transferred to the device.\nThe newly created object's ID is '%ws'\n",pszNewlyCreatedObject);
    }

    if (FAILED(hr))
    {
        printf("! Failed to transfer contact object to the device, hr = 0x%lx\n",hr);
    }

    // Free the object identifier string returned from CreateObjectWithPropertiesOnly
    CoTaskMemFree(pszNewlyCreatedObject);
    pszNewlyCreatedObject = NULL;
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Interface IPortableDevice**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[**Interface IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[**Interface IPortableDeviceValues**](iportabledevicevalues.md)
</dt> <dt>

[**Guia de programação**](programming-guide.md)
</dt> </dl>

 

 



