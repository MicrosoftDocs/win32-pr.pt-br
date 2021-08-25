---
description: Recuperando um identificador de objeto de um identificador exclusivo persistente
ms.assetid: 146f8943-d4e1-4b87-a812-e534082a4f14
title: Recuperando uma ID de objeto de uma ID exclusiva persistente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6d4f08d496c7c03101602c945e6c27e7a2624fe84957eda932ead806f964d3f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120054766"
---
# <a name="retrieving-an-object-id-from-a-persistent-unique-id"></a>Recuperando uma ID de objeto de uma ID exclusiva persistente

Identificadores de objeto só têm a garantia de serem exclusivos para uma determinada sessão de dispositivo; Se o usuário estabelecer uma nova conexão, os identificadores de uma sessão anterior poderão não corresponder a identificadores da sessão atual. Para resolver esse problema, a API WPD dá suporte a PUIDs (identificadores exclusivos persistentes), que persistem entre sessões de dispositivo.

Alguns dispositivos armazenam seus PUIDs nativamente com um determinado objeto. Outros podem gerar o PUID com base em um hash dos dados do objeto selecionado. Outros podem tratar identificadores de objeto como PUIDs (porque eles podem garantir que esses identificadores nunca sejam alterados).

A função GetObjectIdentifierFromPersistentUniqueIdentifier no módulo Contentproperties. cpp demonstra a recuperação de um identificador de objeto para um determinado PUID.

Seu aplicativo pode recuperar um identificador de objeto para um PUID correspondente usando as interfaces descritas na tabela a seguir.



| Interface                                                                                      | Descrição                                                                                         |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [**Interface IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)                             | Fornece acesso ao método de recuperação.                                                            |
| [**Interface IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) | Usado para armazenar o identificador de objeto e o identificador exclusivo persistente (PUID) correspondente. |



 

A primeira tarefa que o aplicativo de exemplo realiza é obter um PUID do usuário.


```C++
// Prompt user to enter an unique identifier to convert to an object idenifier.
printf("Enter the Persistant Unique Identifier of the object you wish to convert into an object identifier.\n>");
hr = StringCbGetsW(szSelection,sizeof(szSelection));
if (FAILED(hr))
{
    printf("An invalid persistent object identifier was specified, aborting the query operation\n");
}
```



Depois disso, o aplicativo de exemplo recupera um objeto [**IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent) , que será usado para invocar o método [**GetObjectIDsFromPersistentUniqueIDs**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-getobjectidsfrompersistentuniqueids) .


```C++
if (SUCCEEDED(hr))
{
    hr = pDevice->Content(&pContent);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceContent from IPortableDevice, hr = 0x%lx\n",hr);
    }
}
```



Em seguida, ele cria um objeto [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) que irá conter o PUID fornecido pelo usuário.


```C++
hr = CoCreateInstance(CLSID_PortableDevicePropVariantCollection,
                      NULL,
                      CLSCTX_INPROC_SERVER,
                      IID_PPV_ARGS(&pPersistentUniqueIDs));
```



Depois que as três etapas anteriores forem executadas, o exemplo estará pronto para recuperar o identificador de objeto que corresponde ao PUID fornecido pelo usuário. Isso é feito chamando o método [**IPortableDeviceContent:: GetObjectIDsFromPersistentUniqueIDs**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-getobjectidsfrompersistentuniqueids) . Antes de chamar esse método, o exemplo Inicializa uma estrutura PROPVARIANT, grava o PUID fornecido pelo usuário para essa estrutura e o adiciona ao objeto IPortableDevicePropVariantCollection no qual pPersistentUniqueIDs aponta. Esse ponteiro é passado como o primeiro argumento para o método GetObjectIDsFromPersistentUniqueIDs. O segundo argumento de GetObjectIDsFromPersistentUniqueIDs é um objeto IPortableDevicePropVariantCollection que recebe o identificador de objeto correspondente.


```C++
if (SUCCEEDED(hr))
{
    if (pPersistentUniqueIDs != NULL)
    {
        PROPVARIANT pv = {0};
        PropVariantInit(&pv);

        // Initialize a PROPVARIANT structure with the object identifier string
        // that the user selected above. Notice we are allocating memory for the
        // PWSTR value.  This memory will be freed when PropVariantClear() is
        // called below.
        pv.vt      = VT_LPWSTR;
        pv.pwszVal = AtlAllocTaskWideString(szSelection);
        if (pv.pwszVal != NULL)
        {
            // Add the object identifier to the objects-to-delete list
            // (We are only deleting 1 in this example)
            hr = pPersistentUniqueIDs->Add(&pv);
            if (SUCCEEDED(hr))
            {
                // 3) Attempt to get the unique idenifier for the object from the device
                hr = pContent->GetObjectIDsFromPersistentUniqueIDs(pPersistentUniqueIDs,
                                                                   &pObjectIDs);
                if (SUCCEEDED(hr))
                {
                    PROPVARIANT pvId = {0};
                    hr = pObjectIDs->GetAt(0, &pvId);
                    if (SUCCEEDED(hr))
                    {
                        printf("The persistent unique identifier '%ws' relates to object identifier '%ws' on the device.\n", szSelection, pvId.pwszVal);
                    }
                    else
                    {
                        printf("! Failed to get the object identifier for '%ws' from the IPortableDevicePropVariantCollection, hr = 0x%lx\n",szSelection, hr);
                    }

                    // Free the returned allocated string from the GetAt() call
                    PropVariantClear(&pvId);
                }
                else
                {
                    printf("! Failed to get the object identifier from persistent object idenifier '%ws', hr = 0x%lx\n",szSelection, hr);
                }
            }
            else
            {
                printf("! Failed to get the object identifier from persistent object idenifier because we could no add the persistent object identifier string to the IPortableDevicePropVariantCollection, hr = 0x%lx\n",hr);
            }
        }
        else
        {
            hr = E_OUTOFMEMORY;
            printf("! Failed to get the object identifier because we could no allocate memory for the persistent object identifier string, hr = 0x%lx\n",hr);
        }

        // Free any allocated values in the PROPVARIANT before exiting
        PropVariantClear(&pv);
    }
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Interface IPortableDevice**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[**Interface IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[**Interface IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md)
</dt> <dt>

[**Guia de programação**](programming-guide.md)
</dt> </dl>

 

 



