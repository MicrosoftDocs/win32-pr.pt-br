---
title: Lendo arquivos do dispositivo
description: Lendo arquivos do dispositivo
ms.assetid: adb87b53-39e2-4f83-ab6d-7e2f7c0bd5d3
keywords:
- Windows Mídia Gerenciador de Dispositivos, lendo arquivos de dispositivos
- Gerenciador de Dispositivos, lendo arquivos de dispositivos
- Guia de programação, lendo arquivos de dispositivos
- aplicativos de área de trabalho, lendo arquivos de dispositivos
- criando Windows mídia Gerenciador de Dispositivos aplicativos, lendo arquivos de dispositivos
- lendo arquivos de dispositivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4352be59a335461f46bfc722146e4c51d31f72c1559e9ad8631e80cb6752c241
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119903996"
---
# <a name="reading-files-from-the-device"></a>Lendo arquivos do dispositivo

Quando encontrar um arquivo que deseja copiar do dispositivo, você pode copiar o arquivo do dispositivo para o computador em uma única chamada ou usar um retorno de chamada para que os bytes de arquivo sejam lidos diretamente para seu aplicativo, o que pode processar ou armazenar os dados conforme eles se ajustam.

As etapas a seguir mostram a maneira básica de copiar um arquivo de um dispositivo em uma única chamada:

1.  Obtenha um identificador para o arquivo no dispositivo. Você pode obter o identificador usando uma pesquisa de arquivo recursiva ou, se souber a ID persistente do armazenamento, chamando [**IWMDMDevice3:: FindStorage**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-findstorage). Em ambos os casos, você precisa da interface [**IWMDMStorage**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage) do objeto.
2.  Determine se o armazenamento é um arquivo ou uma pasta. Somente os arquivos podem ser copiados do dispositivo. Chame [**IWMDMStorage:: GetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getattributes) para obter atributos de armazenamento, o que informará se o armazenamento é um arquivo ou uma pasta.
3.  Consulte **IWMDMStorage** para [**IWMDMStorageControl**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstoragecontrol)e chame [**IWMDMStorageControl:: Read**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-read) para ler o arquivo do dispositivo e salvá-lo em um local especificado.

Se, em vez disso, você quiser ler o bloco de arquivo por bloco do dispositivo, deverá implementar a interface de retorno de chamada [**IWMDMOperation**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation) . passe essa interface para a chamada **IWMDMStorageControl:: Read** e Windows Media Gerenciador de Dispositivos enviará partes de dados de arquivo sequencialmente para seu retorno de chamada. As etapas a seguir mostram como ler um bloco de arquivos do dispositivo por bloco:

1.  Obtenha a interface **IWMDMStorage** para o armazenamento e determine se ele é um arquivo, conforme descrito anteriormente.
2.  Prepare quaisquer identificadores de arquivo ou outros identificadores necessários para manter os dados recebidos.
3.  Consulta para a interface **IWMDMStorageControl** do armazenamento
4.  Chame **IWMDMStorageControl:: Read** para iniciar a operação de leitura, passando a interface **IWMDMOperation** que você implementou.
5.  Windows A mídia Gerenciador de Dispositivos enviará o bloco de dados por bloco para seu dispositivo, conforme descrito em [manipulando transferências de arquivo manualmente](handling-file-transfers-manually.md).

A seguinte função de exemplo C++ lê um objeto de armazenamento de um dispositivo. A função aceita um ponteiro de interface **IWMDMOperation** opcional; Se for enviado, a função criará um arquivo explicitamente e manipulará a gravação dos dados no arquivo em sua implementação de **IWMDMOperation:: TransferObjectData**; caso contrário, ele lerá o arquivo e salvará no destino especificado por *pwszDestName*.


```C++
HANDLE m_File = NULL;

HRESULT myFileRead(IWMDMStorage pStorage, LPWSTR pwszDestName, IWMDMOperation* pOperation)
{
    HRESULT hr = S_OK;
    if ((pStorage == NULL) || (pwszDestName == NULL)) 
    {
        return E_INVALIDPARAM;
    }

    // Check that the storage is readable.
    DWORD attributes = 0;
    UINT flags = 0;
    hr = pStorage->GetAttributes(&attributes, NULL); 
    if (FAILED(hr))
    {
        return hr;
    }

    // Check that content is readable.
    if ((attributes & WMDM_FILE_ATTR_CANREAD) == 0)
    {
        return E_FAIL;
    }
    // Check that it is not abstract (such as an abstract playlist).
    else if (attributes & WMDM_STORAGE_ATTR_VIRTUAL)
    {
        return E_FAIL;
    }

    // Set some flag values for the read operation.
    flags |= WMDM_MODE_BLOCK;
    if (attributes & WMDM_FILE_ATTR_FOLDER)
    {
        flags |= WMDM_CONTENT_FOLDER;
    }
    if (attributes & WMDM_FILE_ATTR_FILE)
    {
        flags |= WMDM_CONTENT_FILE;
    }

    // Get the IWMDMStorageControl interface.
    CComQIPtr<IWMDMStorageControl> pStgControl(pStorage);
    
    // Extra steps if we want to read the file ourselves using IWMDMOperation3.
    if (pOperation != NULL)
    {
        // Create a new file and get the handle. m_File is a global variable
        // that we will use in IWMDMOperation::TransferObjectData.
        // This can also be done when IWMDMOperation::BeginRead is called.
        m_File = CreateFile(
            pwszDestName,   // Destination file name.
            GENERIC_WRITE,  // Write and append writes
            NULL,           // File can't be shared while using, and must be closed.
            NULL,           // Handle can't be inherited.
            CREATE_ALWAYS,  // Overwrite existing files.
            FILE_ATTRIBUTE_NORMAL, // No special attributes.
            NULL            // No template file supplied.
           );
        if (m_File == INVALID_HANDLE_VALUE) return E_FAIL;
        // Modify the Read() method flag. WMDM_CONTENT_FILE and WMDM_CONTENT_FOLDER 
        // are not valid flags when pOperation != NULL.
        flags |= WMDM_CONTENT_OPERATIONINTERFACE;
    }

    // Read the file.
    hr = pStgControl->Read(
             flags,        // Synchronous call specified.
             pwszDestName, // Ignored if pOperation is not NULL.
             NULL,         // No progress callback sent.
             pOperation);  // IWMDMOperation interface, if provided.
    return hr;
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**criando um aplicativo de Gerenciador de Dispositivos de mídia Windows**](creating-a-windows-media-device-manager-application.md)
</dt> </dl>

 

 




