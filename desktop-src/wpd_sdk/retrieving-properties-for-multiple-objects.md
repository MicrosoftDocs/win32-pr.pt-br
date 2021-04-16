---
description: Recuperando propriedades de vários objetos
ms.assetid: 0d0c6b3d-23bc-4628-a684-14bb9e18967f
title: Recuperando propriedades de vários objetos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56c069f6a28b923339f66f8423f211eff4704ef6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105765096"
---
# <a name="retrieving-properties-for-multiple-objects"></a>Recuperando propriedades de vários objetos

Alguns drivers de dispositivo dão suporte à recuperação de propriedades para vários objetos em uma única chamada de função; Isso é conhecido como uma recuperação em massa. Há dois tipos de operações de recuperação em massa: o primeiro tipo recupera propriedades para uma lista de objetos e o segundo tipo recupera propriedades para todos os objetos de um determinado formato. O exemplo descrito nesta seção demonstra o primeiro.

Seu aplicativo pode executar uma recuperação em massa usando as interfaces descritas na tabela a seguir.



| Interface                                                                                      | Descrição                                                        |
|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [**Interface IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)                             | Fornece acesso aos métodos específicos de conteúdo.                   |
| [**Interface IPortableDeviceKeyCollection**](iportabledevicekeycollection.md)                 | Usado para identificar as propriedades a serem recuperadas.                   |
| [**Interface IPortableDeviceProperties**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)                       | Usado para determinar se um determinado driver dá suporte a operações em massa. |
| [**Interface IPortableDevicePropertiesBulk**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk)               | Dá suporte à operação de recuperação em massa.                             |
| [**Interface IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) | Usado para armazenar os identificadores de objeto para a operação em massa.       |



 

A função ReadContentPropertiesBulk no módulo Contentproperties. cpp do aplicativo de exemplo demonstra uma operação de recuperação em massa.

A primeira tarefa realizada neste exemplo é determinar se o driver fornecido oferece suporte a operações em massa. Isso é feito chamando QueryInterface na interface IPortableDeviceProperties e verificando a existência de IPortableDevicePropertiesBulk.


```C++
HRESULT                                       hr                = S_OK;
GUID                                          guidContext       = GUID_NULL;
CGetBulkValuesCallback*                       pCallback         = NULL;
CComPtr<IPortableDeviceProperties>            pProperties;
CComPtr<IPortableDevicePropertiesBulk>        pPropertiesBulk;
CComPtr<IPortableDeviceValues>                pObjectProperties;
CComPtr<IPortableDeviceContent>               pContent;
CComPtr<IPortableDeviceKeyCollection>         pPropertiesToRead;
CComPtr<IPortableDevicePropVariantCollection> pObjectIDs;


if (SUCCEEDED(hr))
{
    hr = pDevice->Content(&pContent);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceContent from IPortableDevice, hr = 0x%lx\n",hr);
    }
}



if (SUCCEEDED(hr))
{
    hr = pContent->Properties(&pProperties);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceProperties from IPortableDevice, hr = 0x%lx\n",hr);
    }
}



if (SUCCEEDED(hr))
{
    hr = pProperties->QueryInterface(IID_PPV_ARGS(&pPropertiesBulk));
    if (FAILED(hr))
    {
        printf("This driver does not support BULK property operations.\n");
    }
}
```



Se o driver oferecer suporte a operações em massa, a próxima etapa será criar uma instância da [**interface IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) e especificar as chaves que correspondem às propriedades que o aplicativo irá recuperar. Para obter uma descrição desse processo, consulte o tópico [Recuperando propriedades de um único objeto](retrieving-properties-for-a-single-object.md) .

Depois que as chaves apropriadas forem especificadas, o aplicativo de exemplo criará uma instância da [**interface IPortableDevicePropertiesBulkCallback**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk). O aplicativo usará os métodos nesta interface para acompanhar o progresso da operação de recuperação em massa assíncrona.


```C++
if (SUCCEEDED(hr))
{
    pCallback = new CGetBulkValuesCallback();
    if (pCallback == NULL)
    {
        hr = E_OUTOFMEMORY;
        printf("! Failed to allocate CGetBulkValuesCallback, hr = 0x%lx\n", hr);
    }
}
```



A próxima função que o aplicativo de exemplo chama é a função auxiliar CreateIPortableDevicePropVariantCollectionWithAllObjectIDs. Essa função cria uma lista de todos os identificadores de objeto disponíveis para fins de exemplo. (Um aplicativo do mundo real limitaria a lista de identificadores a um determinado conjunto de objetos. Por exemplo, um aplicativo pode criar uma lista de identificadores para todos os objetos no momento em uma determinada exibição de pasta.)

Conforme observado acima, a função auxiliar enumera recursivamente todos os objetos em um determinado dispositivo. Ele retorna essa lista em uma [**interface IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) que contém um identificador para cada objeto encontrado. A função auxiliar é definida no módulo ContentEnumeration. cpp.


```C++
// 7) Call our helper function CreateIPortableDevicePropVariantCollectionWithAllObjectIDs
// to enumerate and create an IPortableDevicePropVariantCollection with the object
// identifiers needed to perform the bulk operation on.
if (SUCCEEDED(hr))
{
    hr = CreateIPortableDevicePropVariantCollectionWithAllObjectIDs(pDevice,
                                                                    pContent,
                                                                    &pObjectIDs);
}
```



Depois que as etapas anteriores forem realizadas, o aplicativo de exemplo iniciará a recuperação de propriedade assíncrona. Isso é feito fazendo o seguinte:

1.  Chamando IPortableDevicePropertiesBulk:: QueueGetValuesByObjectList, que enfileira uma solicitação para a recuperação de propriedade em massa. (Observe que, embora a solicitação seja enfileirada, ela não é iniciada.)
2.  Chamando IPortableDevicePropertiesBulk:: Start para iniciar a solicitação em fila.

Essas etapas são demonstradas no trecho de código a seguir do aplicativo de exemplo.


```C++
   if (SUCCEEDED(hr))
   {
       hr = pPropertiesBulk->QueueGetValuesByObjectList(pObjectIDs,
                                                        pPropertiesToRead,
                                                        pCallback,
                                                        &guidContext);


       if(SUCCEEDED(hr))
       {
           // Cleanup any previously created global event handles.
           if (g_hBulkPropertyOperationEvent != NULL)
           {
               CloseHandle(g_hBulkPropertyOperationEvent);
               g_hBulkPropertyOperationEvent = NULL;
           }

           // In order to create a simpler to follow example we create and wait infinitly
           // for the bulk property operation to complete and ignore any errors.
           // Production code should be written in a more robust manner.
           // Create the global event handle to wait on for the bulk operation
           // to complete.
           g_hBulkPropertyOperationEvent = CreateEvent(NULL, FALSE, FALSE, NULL);
           if (g_hBulkPropertyOperationEvent != NULL)
           {
               // Call Start() to actually being the Asynchronous bulk operation.
               hr = pPropertiesBulk->Start(guidContext);
               if(FAILED(hr))
               {
                   printf("! Failed to start property operation, hr = 0x%lx\n", hr);
               }
           }
           else
           {
               printf("! Failed to create the global event handle to wait on for the bulk operation. Aborting operation.\n");
           }
       }
       else
       {
           printf("! QueueGetValuesByObjectList Failed, hr = 0x%lx\n", hr);
       }
   }
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Interface IPortableDevice**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[**Interface IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[**Interface IPortableDeviceKeyCollection**](iportabledevicekeycollection.md)
</dt> <dt>

[**Interface IPortableDeviceProperties**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)
</dt> <dt>

[**Interface IPortableDevicePropertiesBulk**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk)
</dt> <dt>

[**Interface IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md)
</dt> <dt>

[**Guia de programação**](programming-guide.md)
</dt> </dl>

 

 



