---
title: Enviando o arquivo para o dispositivo
description: Enviando o arquivo para o dispositivo
ms.assetid: 202185b8-f10e-4108-a950-60658c006cec
keywords:
- Windows Media Gerenciador de Dispositivos, enviando arquivos para dispositivos
- Gerenciador de Dispositivos, enviando arquivos para dispositivos
- Guia de programação, enviando arquivos para dispositivos
- aplicativos de área de trabalho, enviando arquivos para dispositivos
- Criando aplicativos do Windows Media Gerenciador de Dispositivos, enviando arquivos para dispositivos
- gravando arquivos em dispositivos, enviando arquivos para dispositivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65be0c18a6022538dc5573d936f63392234e9c15
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104498716"
---
# <a name="sending-the-file-to-the-device"></a>Enviando o arquivo para o dispositivo

Depois que o arquivo tiver sido transcodificado, se necessário, e todos os metadados incluindo o formato tiverem sido definidos, seu aplicativo poderá enviar o arquivo para o dispositivo. Para fazer isso, você deve primeiro obter uma interface **IWMDMStorageControl** (ou uma versão posterior) para um local de destino no dispositivo. Os sinalizadores de **inserção** especificam se o novo armazenamento deve ser um irmão ou filho do destino. Depois de ter chegado ao destino, você pode chamar [**IWMDMStorageControl:: Insert**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-insert), [**IWMDMStorageControl2:: Insert2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol2-insert2)ou [**IWMDMStorageControl3:: Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3) para transferir o arquivo. O aplicativo pode lidar com a leitura dos próprios dados do arquivo implementando [**IWMDMOperation**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation), ou pode permitir que o método **Insert** Leia e transfira o arquivo automaticamente, não fornecendo um ponteiro para um **IWMDMOperation** implementado pelo aplicativo.

O código C++ a seguir demonstra como chamar **Insert3** para gravar um arquivo em um dispositivo. Se o ponteiro *pOperation* passado para **Insert3** for **NULL**, o arquivo será enviado em uma etapa; Se esse ponteiro for um ponteiro de interface válido, o Windows Media Gerenciador de Dispositivos chamará o método de retorno de chamada para obter dados em blocos. Para obter detalhes sobre como implementar o **IWMDMOperation**, consulte [manipulando transferências de arquivos manualmente](handling-file-transfers-manually.md).


```C++
// Set the flags for the operation
UINT flags = WMDM_MODE_BLOCK | // Synchronous call. 
    WMDM_STORAGECONTROL_INSERTINTO | // Insert it into the destination folder.
    WMDM_CONTENT_FILE | // We're inserting a file.
    WMDM_FILE_CREATE_OVERWRITE; // Overwrite existing files.
if (pOperation != NULL)
    flags |= WMDM_CONTENT_OPERATIONINTERFACE;

// Send the file and metadata.
hr = pStgCtl3->Insert3(
    flags,
    WMDM_FILE_ATTR_FOLDER, // The current storage is a folder.
    const_cast<WCHAR*>(pwszFileName), // Source file.
    L"My New File.wma",//NULL, // Destination file name.
    pOperation, // NULL to allow the SDK to read the file; 
                // non-NULL to present raw data bytes to the SDK.
    pProgress, // Interface to send simple progress notifications.
    pMetadata, // IWMDMMetaData interface previously created and filled.
    NULL, 
    &pNewStorage); // Out: handle to the new storage, if the method succeeds.
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Gravando arquivos no dispositivo**](writing-files-to-the-device.md)
</dt> </dl>

 

 




