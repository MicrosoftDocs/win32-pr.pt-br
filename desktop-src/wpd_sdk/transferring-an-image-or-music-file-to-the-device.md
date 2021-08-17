---
description: Transferindo uma imagem ou arquivo de música para o dispositivo
ms.assetid: bace274c-512a-46da-80a7-84734ee880b7
title: Transferindo uma imagem ou arquivo de música para o dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44cf16c4c95080b5479825bbc4a0f8dcfd131fdb603821edab0a2e9df4d03c41
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119928056"
---
# <a name="transferring-an-image-or-music-file-to-the-device"></a>Transferindo uma imagem ou arquivo de música para o dispositivo

Uma das operações mais comuns realizadas por um aplicativo é a transferência de conteúdo para um dispositivo conectado.

As transferências de conteúdo são realizadas usando as interfaces descritas na tabela a seguir.



| Interface                                                                | Descrição                                                    |
|--------------------------------------------------------------------------|----------------------------------------------------------------|
| [**IPortableDeviceContent Interface**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)       | Fornece acesso aos métodos específicos do conteúdo.               |
| [**IPortableDeviceDataStream Interface**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicedatastream) | Usado ao escrever o conteúdo no dispositivo.                   |
| [**IPortableDeviceValues Interface**](iportabledevicevalues.md)         | Usado para recuperar propriedades que descrevem o conteúdo.         |
| IStream Interface                                                        | Usado para simplificar a leitura de conteúdo e a escrita no dispositivo. |



 

A `TransferContentToDevice` função no módulo ContentTransfer.cpp do aplicativo de exemplo demonstra como um aplicativo pode transferir conteúdo de um computador para um dispositivo conectado. Neste exemplo específico, o conteúdo transferido pode ser um arquivo que contém uma imagem, música ou informações de contato.

A primeira tarefa realizada pela função é solicitar que o usuário insira um identificador de objeto, que identifica o objeto a `TransferContentToDevice` ser transferido.


```C++
HRESULT                             hr = S_OK;
WCHAR                               szSelection[81]        = {0};
WCHAR                               szFilePath[MAX_PATH]   = {0};
DWORD                               cbOptimalTransferSize   = 0;
CComPtr<IStream>                    pFileStream;
CComPtr<IPortableDeviceDataStream>  pFinalObjectDataStream;
CComPtr<IPortableDeviceValues>      pFinalObjectProperties;
CComPtr<IPortableDeviceContent>     pContent;
CComPtr<IStream>                    pTempStream;  // Temporary IStream which we use to QI for IPortableDeviceDataStream

// Prompt user to enter an object identifier for the parent object on the device to transfer.
printf("Enter the identifer of the parent object which the file will be transferred under.\n>");
hr = StringCbGetsW(szSelection,sizeof(szSelection));
if (FAILED(hr))
{
    printf("An invalid object identifier was specified, aborting content transfer\n");
}
```



A segunda tarefa realizada pela função é criar um objeto `TransferContentToDevice` [**IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent) chamando o [**método IPortableDevice::Content.**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-content)


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



A próxima tarefa realizada pela função é a criação de uma caixa de diálogo FileOpen com a qual o usuário pode especificar o local e o nome do arquivo `TransferContentToDevice` a ser transferido. 


```C++
if (SUCCEEDED(hr))
{
    OPENFILENAME OpenFileNameInfo   = {0};

    OpenFileNameInfo.lStructSize    = sizeof(OPENFILENAME);
    OpenFileNameInfo.hwndOwner      = NULL;
    OpenFileNameInfo.lpstrFile      = szFilePath;
    OpenFileNameInfo.nMaxFile       = ARRAYSIZE(szFilePath);
    OpenFileNameInfo.lpstrFilter    = pszFileTypeFilter;
    OpenFileNameInfo.nFilterIndex   = 1;
    OpenFileNameInfo.Flags          = OFN_PATHMUSTEXIST | OFN_FILEMUSTEXIST;
    OpenFileNameInfo.lpstrDefExt    = pszDefaultFileExtension;

    if (GetOpenFileName(&OpenFileNameInfo) == FALSE)
    {
        printf("The transfer operation was canceled.\n");
        hr = E_ABORT;
    }
}
```



A função passa uma cadeia de caracteres de filtro ( ) para o `TransferContentToDevice` método GetOpenFileName, que determina o tipo de `wszFileTypeFilter` arquivos que o usuário pode escolher. Consulte a `DoMenu` função no módulo WpdApiSample.cpp para ver exemplos dos três filtros diferentes permitidos pelo exemplo.

Depois que o usuário identifica um arquivo específico para transferência para o dispositivo, a função abre esse arquivo como um objeto IStream e recupera as propriedades necessárias para concluir a `TransferContentToDevice` transferência.


```C++
if (SUCCEEDED(hr))
{
    // Open the selected file as an IStream.  This will simplify reading the
    // data and writing to the device.
    hr = SHCreateStreamOnFile(szFilePath, STGM_READ, &pFileStream);
    if (SUCCEEDED(hr))
    {
        // Get the required properties needed to properly describe the data being
        // transferred to the device.
        hr = GetRequiredPropertiesForContentType(guidContentType,           // Content type of the data
                                                 szSelection,              // Parent to transfer the data under
                                                 szFilePath,               // Full file path to the data file
                                                 pFileStream,               // Open IStream that contains the data
                                                 &pFinalObjectProperties);  // Returned properties describing the data
        if (FAILED(hr))
        {
            printf("! Failed to get required properties needed to transfer a file to the device, hr = 0x%lx\n", hr);
        }
    }

    if (FAILED(hr))
    {
        printf("! Failed to open file named (%ws) to transfer to device, hr = 0x%lx\n",szFilePath, hr);
    }
}
```



As propriedades necessárias são recuperadas chamando `GetRequiredPropertiesForContentType` a função auxiliar, que opera no objeto IStream. A função auxiliar cria um objeto `GetRequiredPropertiesForContentType` [**IPortableDeviceValues,**](iportabledevicevalues.md) recupera as propriedades na lista a seguir e as adiciona a esse objeto.

-   Identificador de objeto pai
-   Tamanho do fluxo em bytes
-   Nome do arquivo de conteúdo
-   Nome do conteúdo (o nome do arquivo sem a extensão)
-   Tipo de conteúdo (imagem, áudio ou contato)
-   Formato de conteúdo (JFIF, WMA ou vCard2)

O aplicativo de exemplo usa as propriedades recuperadas para criar o novo conteúdo no dispositivo. Isso é feito em três fases:

1.  O aplicativo chama o método [**IPortableDeviceContent::CreateObjectWithPropertiesAndData**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata) para criar um novo objeto IStream no dispositivo.
2.  O aplicativo usa esse objeto para obter um [**objeto IPortableDeviceDataStream**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicedatastream) do driver WPD.
3.  O aplicativo usa o novo **objeto IPortableDeviceDataStream** para gravar o conteúdo no dispositivo (por meio da função auxiliar StreamCopy). A função auxiliar grava os dados do arquivo de origem no fluxo retornado por [**IPortableDeviceContent::CreateObjectWithPropertiesAndData**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata).
4.  O aplicativo conclui a operação chamando o método Commit no fluxo de destino.


```C++
// 4) Transfer for the content to the device
if (SUCCEEDED(hr))
{
    hr = pContent->CreateObjectWithPropertiesAndData(pFinalObjectProperties,    // Properties describing the object data
                                                     &pTempStream,              // Returned object data stream (to transfer the data to)
                                                     &cbOptimalTransferSize,    // Returned optimal buffer size to use during transfer
                                                     NULL);

    // Once we have a the IStream returned from CreateObjectWithPropertiesAndData,
    // QI for IPortableDeviceDataStream so we can use the additional methods
    // to get more information about the object (i.e. The newly created object
    // identifier on the device)
    if (SUCCEEDED(hr))
    {
        hr = pTempStream->QueryInterface(IID_PPV_ARGS(&pFinalObjectDataStream));
        if (FAILED(hr))
        {
            printf("! Failed to QueryInterface for IPortableDeviceDataStream, hr = 0x%lx\n",hr);
        }
    }

    // Since we have IStream-compatible interfaces, call our helper function
    // that copies the contents of a source stream into a destination stream.
    if (SUCCEEDED(hr))
    {
        DWORD cbTotalBytesWritten = 0;

        hr = StreamCopy(pFinalObjectDataStream, // Destination (The Object to transfer to)
                        pFileStream,            // Source (The File data to transfer from)
                        cbOptimalTransferSize,  // The driver specified optimal transfer buffer size
                        &cbTotalBytesWritten);  // The total number of bytes transferred from file to the device
        if (FAILED(hr))
        {
            printf("! Failed to transfer object to device, hr = 0x%lx\n",hr);
        }
    }
    else
    {
        printf("! Failed to get IStream (representing destination object data on the device) from IPortableDeviceContent, hr = 0x%lx\n",hr);
    }

    // After transferring content to the device, the client is responsible for letting the
    // driver know that the transfer is complete by calling the Commit() method
    // on the IPortableDeviceDataStream interface.
    if (SUCCEEDED(hr))
    {
        hr = pFinalObjectDataStream->Commit(0);
        if (FAILED(hr))
        {
            printf("! Failed to commit object to device, hr = 0x%lx\n",hr);
        }
    }

    // Some clients may want to know the object identifier of the newly created
    // object.  This is done by calling GetObjectID() method on the
    // IPortableDeviceDataStream interface.
    if (SUCCEEDED(hr))
    {
        PWSTR pszNewlyCreatedObject = NULL;
        hr = pFinalObjectDataStream->GetObjectID(&pszNewlyCreatedObject);
        if (SUCCEEDED(hr))
        {
            printf("The file '%ws' was transferred to the device.\nThe newly created object's ID is '%ws'\n",szFilePath ,pszNewlyCreatedObject);
        }

        if (FAILED(hr))
        {
            printf("! Failed to get the newly transferred object's identifier from the device, hr = 0x%lx\n",hr);
        }

        // Free the object identifier string returned from the GetObjectID() method.
        CoTaskMemFree(pszNewlyCreatedObject);
        pszNewlyCreatedObject = NULL;
    }
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IPortableDevice Interface**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[**IPortableDeviceContent Interface**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[**IPortableDeviceDataStream Interface**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicedatastream)
</dt> <dt>

[**IPortableDeviceValues Interface**](iportabledevicevalues.md)
</dt> <dt>

[**Guia de programação**](programming-guide.md)
</dt> </dl>

 

 



