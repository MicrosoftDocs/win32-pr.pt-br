---
title: Gravando uma imagem de disco
description: A criação de mestre (gravação de um disco) usando o IMAPi consiste nas seguintes etapas construir uma imagem do sistema de arquivos que contém os diretórios e arquivos a serem gravados no disco. Configure um gravador de disco para se comunicar com o dispositivo óptico. Crie um gravador de dados e grave a imagem em disco.
ms.assetid: f2eee14e-695d-4678-b3c1-b521ab4d4a7e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 237a4aa73b6820b75b4a9a1ed03baeeb87ac093bfc549cb9cc0ed947077515dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118758906"
---
# <a name="burning-a-disc-image"></a>Gravando uma imagem de disco

A criação de mestre (gravação de um disco) usando o IMAPi consiste nas seguintes etapas:

1.  Construa uma imagem do sistema de arquivos que contém os diretórios e arquivos para gravar o disco.
2.  [Configure um gravador de disco](#set-up-a-disc-recorder) para se comunicar com o dispositivo óptico.
3.  [Crie um gravador de dados](#create-a-data-writer-and-write-the-burn-image) e grave a imagem em disco.

Para obter um exemplo que grava uma imagem de disco, consulte [exemplo de VBScript](#vbscript-example).

## <a name="construct-a-burn-image"></a>Construir uma imagem de gravação

Uma imagem de gravação é um fluxo de dados que está pronto para ser gravado na mídia óptica. A imagem de gravação para formatos ISO9660, Joliet e UDF consiste em um sistema de arquivos de diretórios e arquivos individuais. O objeto **CFileSystemImage** é o objeto do sistema de arquivos que contém os arquivos e diretórios a serem colocados na mídia óptica. A interface [**IFileSystemImage**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage) fornece acesso ao objeto e às configurações do sistema de arquivos.

Depois de criar o objeto do sistema de arquivos, chame os métodos [**IFileSystemImage:: CreateFileItem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createfileitem) e [**IFileSystemImage:: CreateDirectoryItem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createdirectoryitem) para criar os objetos de arquivo e diretório, respectivamente. Os objetos de arquivo e diretório podem ser usados para fornecer detalhes específicos sobre o arquivo e o diretório. Os métodos do manipulador de eventos disponíveis para [**IFileSystemImage**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage) podem identificar o arquivo atual que está sendo adicionado à imagem do sistema de arquivos, o número de setores já copiados e o número total de setores a serem copiados.

Opcionalmente, uma imagem de inicialização pode ser anexada ao sistema de arquivos usando a propriedade [**IFileSystemImage::p UT \_ BootImageOptions**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-put_bootimageoptions) . Para obter um exemplo, consulte [adicionando uma imagem de inicialização](adding-a-boot-image.md).

Por fim, chame [**IFileSystemImage:: CreateResultImage**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createresultimage) para criar um fluxo de dados e fornece acesso por meio de [**IFileSystemImageResult**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimageresult). O novo fluxo de dados pode então ser fornecido diretamente para o método [**IDiscFormat2Data:: Write**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-write) ou ser salvo em um arquivo para uso posterior.

## <a name="set-up-a-disc-recorder"></a>Configurar um gravador de disco

O objeto **MsftDiscMaster2** fornece uma enumeração dos dispositivos ópticos no sistema. A interface [**IDiscMaster2**](/windows/desktop/api/imapi2/nn-imapi2-idiscmaster2) fornece acesso à enumeração de dispositivo resultante. Percorra as enumerações para localizar um dispositivo de gravação apropriado. O objeto **MsftDiscMaster2** também fornece notificações de eventos quando dispositivos ópticos são adicionados ou excluídos de um computador.

Depois de encontrar um gravador óptico e recuperar sua ID, crie um objeto **MsftDiscRecorder2** e inicialize o gravador usando a ID do dispositivo. A interface [**IDiscRecorder2**](/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2) fornece acesso ao objeto do gravador, bem como algumas informações básicas do dispositivo, como ID do fornecedor, ID do produto, revisão do produto e métodos para ejetar a mídia e fechar a bandeja.

## <a name="create-a-data-writer-and-write-the-burn-image"></a>Criar um gravador de dados e gravar a imagem de gravação

O objeto **MsftDiscFormat2Data** fornece o método de escrita, as propriedades sobre a função de gravação e as propriedades específicas de mídia. A interface [**IDiscFormat2Data**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data) fornece acesso ao objeto **MsftDiscFormat2Data** .

O gravador de disco vincula-se ao gravador de formato usando a propriedade [**IDiscFormat2Data::p UT \_ Recorder**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-put_recorder) . Depois que o gravador estiver associado ao gravador de formato, você poderá executar consultas em relação à mídia e atualizar as propriedades específicas de gravação antes de gravar a imagem de resultado em disco usando o método [**IDiscFormat2Data:: Write**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-write) .

Outras interfaces de gravação de formato fornecidas pelo IMAPi funcionam da mesma forma; interfaces de escrita de formato adicionais incluem:

-   [**IDiscFormat2Erase**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2erase) apaga a mídia óptica regravável.
-   [**IDiscFormat2RawCD**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2rawcd) grava uma imagem bruta em mídia óptica.
-   [**IDiscFormat2TrackAtOnce**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2trackatonce) grava faixas de áudio em mídia óptica.

> [!Note]  
> É possível que uma transição de estado de energia ocorra durante uma operação de gravação (ou seja, logoff do usuário ou suspensão do sistema) que leva à interrupção do processo de gravação e possível perda de dados. Para considerações de programação, consulte [impedindo o logoff ou suspender durante uma gravação](preventing-logoff-or-suspend-during-a-burn.md).

 

## <a name="vbscript-example"></a>Exemplo de VBScript

Este exemplo de script mostra como usar os objetos IMAPi para gravar mídia óptica; mais especificamente, grave um diretório em um disco em branco. O código não contém nenhuma verificação de erro e pressupõe o seguinte:

-   Um dispositivo de disco compatível está instalado no sistema.
-   O dispositivo de disco é a segunda unidade do sistema.
-   Um disco compatível é inserido no dispositivo de disco.
-   O disco está em branco.
-   Os arquivos a serem gravados no disco estão localizados em "g: \\ burndir".

Funcionalidades adicionais, como verificação de erros, compatibilidade de dispositivos e mídias, notificação de eventos e cálculo de espaço livre no disco, podem ser adicionadas a esse script.


```VB
' This script burns data files to disc in a single session 
' using files from a single directory tree.
 
' Copyright (C) Microsoft Corp. 2006

Option Explicit

' *** CD/DVD disc file system types
Const FsiFileSystemISO9660 = 1
Const FsiFileSystemJoliet  = 2
Const FsiFileSystemUDF102  = 4

WScript.Quit(Main)

Function Main
    Dim Index                ' Index to recording drive.
    Dim Recorder             ' Recorder object
    Dim Path                 ' Directory of files to burn
    Dim Stream               ' Data stream for burning device
    
    Index = 1                ' Second drive on the system
    Path = "g:\BurnDir"      ' Files to transfer to disc

    ' Create a DiscMaster2 object to connect to optical drives.
    Dim g_DiscMaster
    Set g_DiscMaster = WScript.CreateObject("IMAPI2.MsftDiscMaster2")

    ' Create a DiscRecorder object for the specified burning device.
    Dim uniqueId
    set recorder = WScript.CreateObject("IMAPI2.MsftDiscRecorder2")
    uniqueId = g_DiscMaster.Item(index)
    recorder.InitializeDiscRecorder( uniqueId )

    ' Create an image stream for a specified directory.
    Dim FSI                  ' Disc file system
    Dim Dir                  ' Root directory of the disc file system
    Dim dataWriter    
        
    ' Create a new file system image and retrieve root directory
    Set FSI = CreateObject("IMAPI2FS.MsftFileSystemImage")
    Set Dir = FSI.Root

    'Create the new disc format and set the recorder
    Set dataWriter = CreateObject ("IMAPI2.MsftDiscFormat2Data")
    dataWriter.recorder = Recorder
    dataWriter.ClientName = "IMAPIv2 TEST"

    FSI.ChooseImageDefaults(recorder)
        
    ' Add the directory and its contents to the file system 
    Dir.AddTree Path, false
        
    ' Create an image from the file system
    Dim result
    Set result = FSI.CreateResultImage()
    Stream = result.ImageStream
    
    ' Write stream to disc using the specified recorder.
    WScript.Echo "Writing content to disc..."
    dataWriter.write(Stream)

    WScript.Echo "----- Finished writing content -----"
    Main = 0
End Function

```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando o IMAPi](using-imapi.md)
</dt> <dt>

[**IDiscFormat2Data**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data)
</dt> <dt>

[**IDiscFormat2Erase**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2erase)
</dt> <dt>

[**IDiscFormat2RawCD**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2rawcd)
</dt> <dt>

[**IDiscFormat2TrackAtOnce**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2trackatonce)
</dt> <dt>

[**IDiscMaster2**](/windows/desktop/api/imapi2/nn-imapi2-idiscmaster2)
</dt> <dt>

[**IDiscRecorder2**](/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2)
</dt> <dt>

[**IFileSystemImage**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage)
</dt> <dt>

[**IStream**](/windows/desktop/api/objidl/nn-objidl-istream)
</dt> </dl>

 

 