---
description: Movendo o conteúdo no dispositivo
ms.assetid: 5072d308-d376-4141-96df-dbef23fb9f9b
title: Movendo o conteúdo no dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0830dab93b4ac0cd11f988c34edef24b1eb11b8869f63efdc4b0b518fc9380b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119928366"
---
# <a name="moving-content-on-the-device"></a>Movendo o conteúdo no dispositivo

Outra operação comum realizada por um aplicativo WPD é a transferência de conteúdo de um local no dispositivo para outro.

As operações de movimentação de conteúdo são realizadas usando as interfaces descritas na tabela a seguir.



| Interface                                                                                      | Descrição                                       |
|------------------------------------------------------------------------------------------------|---------------------------------------------------|
| [**IPortableDeviceContent Interface**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)                             | Fornece acesso aos métodos específicos do conteúdo.  |
| [**IPortableDevicePropVariantCollection Interface**](iportabledevicepropvariantcollection.md) | Fornece acesso aos métodos específicos da propriedade. |



 

A função MoveContentAlreadyOnDevice no módulo ContentTransfer.cpp do aplicativo de exemplo demonstra como um aplicativo pode mover o conteúdo de um local para outro.

A primeira tarefa realizada pela função MoveContentAlreadyOnDevice é consultar o driver de dispositivo para ver se ele dá suporte à movimentação de conteúdo. Isso é feito chamando a função auxiliar SupportsCommand e passando WPD \_ COMMAND OBJECT MANAGEMENT MOVE OBJECTS como o segundo \_ \_ \_ \_ argumento.


```C++
HRESULT                                       hr                               = S_OK;
WCHAR                                         wszSelection[81]                 = {0};
WCHAR                                         wszDestinationFolderObjectID[81] = {0};
CComPtr<IPortableDeviceContent>               pContent;
CComPtr<IPortableDevicePropVariantCollection> pObjectsToMove;
CComPtr<IPortableDevicePropVariantCollection> pObjectsFailedToMove;
if (SupportsCommand(pDevice, WPD_COMMAND_OBJECT_MANAGEMENT_MOVE_OBJECTS) == FALSE)
{
    printf("! This device does not support the move operation (i.e. The WPD_COMMAND_OBJECT_MANAGEMENT_MOVE_OBJECTS command)\n");
    return;
}
```



A próxima etapa envolve solicitar que o usuário insira dois identificadores de objeto. O primeiro é o identificador do conteúdo que será movido. O segundo é o identificador do local para o qual o aplicativo deve mover esse conteúdo.


```C++
HRESULT                                       hr                               = S_OK;
WCHAR                                         wszSelection[81]                 = {0};
WCHAR                                         wszDestinationFolderObjectID[81] = {0};
CComPtr<IPortableDeviceContent>               pContent;
CComPtr<IPortableDevicePropVariantCollection> pObjectsToMove;
CComPtr<IPortableDevicePropVariantCollection> pObjectsFailedToMove;
printf("Enter the identifer of the object you wish to move.\n>");
hr = StringCbGetsW(wszSelection,sizeof(wszSelection));
if (FAILED(hr))
{
    printf("An invalid object identifier was specified, aborting content moving\n");
}

// Prompt user to enter an object identifier on the device to move.
printf("Enter the identifer of the object you wish to move '%ws' to.\n>", wszSelection);
hr = StringCbGetsW(wszDestinationFolderObjectID,sizeof(wszDestinationFolderObjectID));
if (FAILED(hr))
{
    printf("An invalid object identifier was specified, aborting content moving\n");
}
```



Em seguida, o exemplo recupera um [**objeto IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent) usado para acessar o [**método IPortableDeviceContent::Move.**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-move)


```C++
HRESULT                                       hr                               = S_OK;
WCHAR                                         wszSelection[81]                 = {0};
WCHAR                                         wszDestinationFolderObjectID[81] = {0};
CComPtr<IPortableDeviceContent>               pContent;
CComPtr<IPortableDevicePropVariantCollection> pObjectsToMove;
CComPtr<IPortableDevicePropVariantCollection> pObjectsFailedToMove;
if (SUCCEEDED(hr))
{
    hr = pDevice->Content(&pContent);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceContent from IPortableDevice, hr = 0x%lx\n",hr);
    }
}
```



Por fim, o conteúdo é movido. Esse processo envolve o seguinte:

1.  Criando um [**objeto IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) que recebe uma estrutura PROPVARIANT para o objeto a ser movido.
2.  Adicionando o PROPVARIANT ao objeto IPortableDevicePropVariantCollection.
3.  Invocando o método IPortableDeviceContent::Move.


```C++
HRESULT                                       hr                               = S_OK;
WCHAR                                         wszSelection[81]                 = {0};
WCHAR                                         wszDestinationFolderObjectID[81] = {0};
CComPtr<IPortableDeviceContent>               pContent;
CComPtr<IPortableDevicePropVariantCollection> pObjectsToMove;
CComPtr<IPortableDevicePropVariantCollection> pObjectsFailedToMove;
if (SUCCEEDED(hr))
{
    hr = CoCreateInstance(CLSID_PortableDevicePropVariantCollection,
                          NULL,
                          CLSCTX_INPROC_SERVER,
                          IID_IPortableDevicePropVariantCollection,
                          (VOID**) &pObjectsToMove);
    if (SUCCEEDED(hr))
    {
        if (pObjectsToMove != NULL)
        {
            PROPVARIANT pv = {0};
            PropVariantInit(&pv);

            // Initialize a PROPVARIANT structure with the object identifier string
            // that the user selected above. Notice we are allocating memory for the
            // LPWSTR value.  This memory will be freed when PropVariantClear() is
            // called below.
            pv.vt      = VT_LPWSTR;
            pv.pwszVal = AtlAllocTaskWideString(wszSelection);
            if (pv.pwszVal != NULL)
            {
                // Add the object identifier to the objects-to-move list
                // (We are only moving 1 in this example)
                hr = pObjectsToMove->Add(&pv);
                if (SUCCEEDED(hr))
                {
                    // Attempt to move the object on the device
                    hr = pContent->Move(pObjectsToMove,               // Object(s) to move
                                        wszDestinationFolderObjectID, // Folder to move to
                                        NULL);                        // Object(s) that failed to delete (we are only moving 1, so we can pass NULL here)
                    if (SUCCEEDED(hr))
                    {
                        // An S_OK return lets the caller know that the deletion was successful
                        if (hr == S_OK)
                        {
                            printf("The object '%ws' was moved on the device.\n", wszSelection);
                        }

                        // An S_FALSE return lets the caller know that the move failed.
                        // The caller should check the returned IPortableDevicePropVariantCollection
                        // for a list of object identifiers that failed to be moved.
                        else
                        {
                            printf("The object '%ws' failed to be moved on the device.\n", wszSelection);
                        }
                    }
                    else
                    {
                        printf("! Failed to move an object on the device, hr = 0x%lx\n",hr);
                    }
                }
                else
                {
                    printf("! Failed to move an object on the device because we could no add the object identifier string to the IPortableDevicePropVariantCollection, hr = 0x%lx\n",hr);
                }
            }
            else
            {
                hr = E_OUTOFMEMORY;
                printf("! Failed to move an object on the device because we could no allocate memory for the object identifier string, hr = 0x%lx\n",hr);
            }

            // Free any allocated values in the PROPVARIANT before exiting
            PropVariantClear(&pv);
        }
        else
        {
            printf("! Failed to move an object from the device because we were returned a NULL IPortableDevicePropVariantCollection interface pointer, hr = 0x%lx\n",hr);
        }
    }
    else
    {
        printf("! Failed to CoCreateInstance CLSID_PortableDevicePropVariantCollection, hr = 0x%lx\n",hr);
    }
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IPortableDevice Interface**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[**IPortableDeviceContent Interface**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[**IPortableDevicePropVariantCollection Interface**](iportabledevicepropvariantcollection.md)
</dt> <dt>

[**Guia de programação**](programming-guide.md)
</dt> </dl>

 

 



