---
title: Criando um disco de várias sessões
ms.assetid: 327304c4-fdb9-47c6-9b19-49100b933590
description: 'Saiba mais sobre: Criando um disco de várias sessões'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2db17b8a16f46797fc0f6de2bf94850e3b3039bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104461238"
---
# <a name="creating-a-multisession-disc"></a>Criando um disco de várias sessões

A [API de mestre de imagem](about-imapi.md) (IMAPI) dá suporte à adição e remoção de arquivos para, ou do, os seguintes tipos de disco de várias sessões:

-   CD-R/CD-RW
-   Single-Layer DVD + R/DVD-R
-   DVD + R de camada dupla
-   BD-R
-   DVD-RW/DVD + RW (**somente Windows 7**)
-   DVD-RAM (**somente Windows 7**)
-   BD-RE (**somente Windows 7**)

A criação de um disco de várias sessões usando IMAPi consiste nas etapas a seguir. Cada uma dessas etapas documentadas contém a parte relevante do exemplo de script completo Visual Basic fornecido na seção final.

## <a name="initializing-the-disc-recorder"></a>Inicializando o gravador de disco

Antes da inicialização do dispositivo, o objeto **MsftDiscMaster2** fornece uma enumeração dos dispositivos ópticos no sistema. A interface [**IDiscMaster2**](/windows/desktop/api/imapi2/nn-imapi2-idiscmaster2) fornece acesso a essa enumeração de dispositivo para facilitar o local do dispositivo de gravação apropriado. O objeto **MsftDiscMaster2** também fornece notificações de eventos quando dispositivos ópticos são adicionados ou removidos de um computador.

Depois de localizar um gravador óptico e recuperar a ID atribuída a ele, crie um novo objeto **MsftDiscMaster2** e inicialize o gravador usando a ID de dispositivo específica.

A interface [**IDiscRecorder2**](/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2) fornece acesso a informações básicas do dispositivo, como ID do fornecedor, ID do produto, revisão do produto, bem como os métodos para ejetar mídia ou fechar a bandeja.

> [!Note]  
> As constantes e dimensões adicionais declaradas no exemplo a seguir são usadas posteriormente no script de exemplo completo localizado na seção final deste documento. Esses elementos não são necessários para o ato de inicializar um gravador de disco.

 


```VB
' **_ CD/DVD disc file system types
Const FsiFileSystemISO9660 = 1
Const FsiFileSystemJoliet  = 2
Const FsiFileSystemUDF102  = 4

WScript.Quit(Main)

Function Main
    Dim Index                ' Index to recording drive.
    Dim Recorder             ' Recorder object
    Dim Path                 ' Directory of files to add
    Dim Stream               ' Data stream for burning device
    
    Index = 0                ' First drive on the system
    Path = "G:\BurnDir"      ' Files to add to the disc

    ' Create a DiscMaster2 object to connect to optical drives.
    Dim DiscMaster
    Set DiscMaster = WScript.CreateObject("IMAPI2.MsftDiscMaster2")

    ' Create a DiscRecorder2 object for the specified burning device.
    Dim UniqueId
    set Recorder = WScript.CreateObject("IMAPI2.MsftDiscRecorder2")
    UniqueId = DiscMaster.Item(Index)
    Recorder.InitializeDiscRecorder(UniqueId)
```



## <a name="creating-a-data-writer"></a>Criando um gravador de dados

O objeto _ *MsftDiscFormat2Data** fornece o método de escrita, suas propriedades, bem como as propriedades específicas de mídia. A interface [**IDiscFormat2Data**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data) fornece acesso a esse objeto.

O gravador de disco é associado ao gravador de formato usando a propriedade [**IDiscFormat2Data::p UT \_ Recorder**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-put_recorder) . Depois que o gravador está associado ao gravador de formato, as consultas de propriedade específicas de mídia e gravação podem ser executadas antes de gravar a imagem de resultado em disco usando o método [**IDiscFormat2Data:: Write**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-write) .

> [!Note]  
> A cadeia de caracteres de nome do cliente especificada no código de exemplo abaixo deve ser ajustada conforme apropriado para o aplicativo específico.

 


```VB
    ' Create a DiscFormat2Data object and set the recorder
    Dim DataWriter
    Set DataWriter = CreateObject ("IMAPI2.MsftDiscFormat2Data")
    DataWriter.Recorder = Recorder
    DataWriter.ClientName = "IMAPIv2 TEST"
```



## <a name="creating-the-file-system-object"></a>Criando o objeto do sistema de arquivos

Para gravar uma nova sessão, uma imagem de gravação deve ser gerada para ela primeiro. Uma imagem de gravação para formatos **ISO9660**, **Joliet** e **UDF** consiste em sistemas de arquivos de diretórios e arquivos individuais. O objeto **MsftFileSystemImage** é o objeto do sistema de arquivos que contém os arquivos e diretórios a serem colocados na mídia óptica. A interface [**IFileSystemImage**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage) fornece acesso ao objeto e às configurações do sistema de arquivos.


```VB
    ' Create a new file system image object
    Dim FSI
    Set FSI = CreateObject("IMAPI2FS.MsftFileSystemImage")
```



## <a name="importing-a-file-system"></a>Importando um sistema de arquivos

Antes de continuar, verifique se o disco não está em branco verificando a propriedade [**IDiscFormat2:: get \_ MediaHeuristicallyBlank**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2-get_mediaheuristicallyblank) .

Depois de criar o objeto **MsftFileSystemImage** , a propriedade [**IFileSystemImage::p UT \_ MultisessionInterfaces**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-put_multisessioninterfaces) deve ser inicializada antes de uma chamada para o método [**IFileSystemImage:: ImportFileSystem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-importfilesystem) ou [**IFileSystemImage:: ImportSpecificFileSystem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-importspecificfilesystem) para importar o sistema de arquivos da última sessão gravada. Esses métodos preencherão automaticamente o objeto **MsftFileSystemImage** com informações que descrevem os arquivos e diretórios gravados anteriormente.

> [!Note]  
> A propriedade [**IFileSystemImage::p UT \_ MultisessionInterfaces**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-put_multisessioninterfaces) normalmente é inicializada com as interfaces de várias sessões fornecidas pelo gravador de dados por meio da propriedade [**IDiscFormat2Data:: get \_ MultisessionInterfaces**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-get_multisessioninterfaces) .

 

As tentativas de definir a propriedade **IFileSystemImage::p UT \_ MultisessionInterfaces** falharão se o IMAPI não oferecer suporte a várias sessões para a mídia inserida no momento ou se a mídia não puder ser anexada por algum outro motivo (por exemplo, porque está fechada).

Se a sessão de gravação anterior contiver mais de um tipo de sistema de arquivos, o método [**IFileSystemImage:: ImportFileSystem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-importfilesystem) importará informações do tipo de sistema de arquivos mais avançado presente. Por exemplo, no exemplo fornecido neste tópico, UDF é o sistema de arquivos importado. No entanto, o uso do método [**IFileSystemImage:: ImportSpecificFileSystem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-importspecificfilesystem) permite a seleção específica do sistema de arquivos a ser importado.

> [!Note]  
> O método [**IFileSystemImage:: IdentifyFileSystemsOnDisc**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-identifyfilesystemsondisc) pode ser usado para determinar quais sistemas de arquivos estão disponíveis no disco.

 


```VB
    ' Import the last session, if the disc is not empty, or initialize
    ' the file system, if the disc is empty
    If Not DataWriter.MediaHeuristicallyBlank _
    Then
        On Error Resume Next
        FSI.MultisessionInterfaces = DataWriter.MultisessionInterfaces
        If Err.Number <> 0 _
        Then
            WScript.Echo "Multisession is not supported for this disc"
            Main = 1
            Exit Function
        End If
        On Error Goto 0

        WScript.Echo "Importing data from the previous session..."
        FSI.ImportFileSystem()
    Else 
        FSI.ChooseImageDefaults(Recorder)
    End If
```



## <a name="adding-or-removing-files-to-the-file-system"></a>Adicionando ou removendo arquivos no sistema de arquivos

Depois de criar o objeto do sistema de arquivos e importar o sistema de arquivos da sessão anterior, chame os métodos [**IFileSystemImage:: CreateFileItem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createfileitem) e [**IFileSystemImage:: CreateDirectoryItem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createdirectoryitem) para criar novos objetos de arquivo e diretório, respectivamente. Os objetos de arquivo e diretório fornecem detalhes específicos sobre os arquivos e diretórios. Como alternativa, o método [**IFsiDirectoryItem:: addtree**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-addtree) de um objeto de diretório, representado por meio da interface [**IFsiDirectoryItem**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsidirectoryitem) , pode ser usado para adicionar arquivos e diretórios existentes de outro dispositivo de armazenamento (ou seja, um disco rígido).

O método de atualização do manipulador de eventos disponível para [**IFileSystemImage**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage) identifica o arquivo atual que está sendo adicionado à imagem do sistema de arquivos, o número de setores já copiados e o número total de setores a serem copiados.

Para remover arquivos e diretórios existentes do sistema de arquivos, use os métodos [**IFsiDirectoryItem:: Remove**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-remove) e [**IFsiDirectoryItem:: RemoveTree**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-removetree) dos objetos de diretório representados por meio da interface [**IFsiDirectoryItem**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsidirectoryitem) . A propriedade de [**\_ raiz IFileSystemImage:: Get**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-get_root) é usada para obter um ponteiro para o diretório raiz do sistema de arquivos e a interface **IFsiDirectoryItem** para percorrer a árvore de diretórios.

> [!Note]  
> Os arquivos e diretórios removidos por meio dos métodos [**IFsiDirectoryItem:: Remove**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-remove) e [**IFsiDirectoryItem:: RemoveTree**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-removetree) não são fisicamente removidos do disco, e o software avançado pode recuperar facilmente as informações excluídas.

 


```VB
    ' Add the directory and its contents to the file system 
    WScript.Echo "Adding " & Path & " directory to the disc..."
    FSI.Root.AddTree Path, false
```



## <a name="constructing-a-file-system-image"></a>Construindo uma imagem do sistema de arquivos

A etapa final é chamar [**IFileSystemImage:: CreateResultImage**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createresultimage) para criar um fluxo de dados para a imagem de gravação e fornecer acesso a ele por meio da interface [**IFileSystemImageResult**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimageresult) . Esse fluxo de dados pode ser fornecido diretamente para o método [**IDiscFormat2Data:: Write**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-write) ou ser salvo em um arquivo para uso posterior.


```VB
    ' Create an image from the file system image object
    Dim Result
    Set Result = FSI.CreateResultImage()
    Stream = Result.ImageStream
```



## <a name="example-summary"></a>Resumo de exemplo

O exemplo de script a seguir Visual Basic mostra como usar objetos IMAPi para criar discos com várias sessões. O exemplo cria uma nova sessão e adiciona um diretório ao disco. Para simplificar, o código não executa verificação de erro extensiva e pressupõe o seguinte:

-   Um dispositivo de disco compatível está instalado no sistema.
-   O dispositivo de disco é a primeira unidade no sistema.
-   Um disco compatível é inserido no dispositivo de disco.
-   Os arquivos a serem adicionados ao disco estão localizados em "g: \\ burndir".

Funcionalidades adicionais, como verificação de erros extensiva, compatibilidade de dispositivo e mídia, notificação de eventos e cálculo de espaço livre no disco, podem ser adicionadas ao script.


```VB
' This script adds data files from a single directory tree to a
' disc (a new session is added, if the disc already contains data)

' Copyright (C) Microsoft. All rights reserved.

Option Explicit

' **_ CD/DVD disc file system types
Const FsiFileSystemISO9660 = 1
Const FsiFileSystemJoliet  = 2
Const FsiFileSystemUDF102  = 4

WScript.Quit(Main)

Function Main
    Dim Index                ' Index to recording drive.
    Dim Recorder             ' Recorder object
    Dim Path                 ' Directory of files to add
    Dim Stream               ' Data stream for burning device
    
    Index = 0                ' First drive on the system
    Path = "G:\BurnDir"      ' Files to add to the disc

    ' Create a DiscMaster2 object to connect to optical drives.
    Dim DiscMaster
    Set DiscMaster = WScript.CreateObject("IMAPI2.MsftDiscMaster2")

    ' Create a DiscRecorder2 object for the specified burning device.
    Dim UniqueId
    set Recorder = WScript.CreateObject("IMAPI2.MsftDiscRecorder2")
    UniqueId = DiscMaster.Item(Index)
    Recorder.InitializeDiscRecorder(UniqueId)

    ' Create a DiscFormat2Data object and set the recorder
    Dim DataWriter
    Set DataWriter = CreateObject ("IMAPI2.MsftDiscFormat2Data")
    DataWriter.Recorder = Recorder
    DataWriter.ClientName = "IMAPIv2 TEST"

    ' Create a new file system image object
    Dim FSI
    Set FSI = CreateObject("IMAPI2FS.MsftFileSystemImage")

    ' Import the last session, if the disc is not empty, or initialize
    ' the file system, if the disc is empty
    If Not DataWriter.MediaHeuristicallyBlank _
    Then
        On Error Resume Next
        FSI.MultisessionInterfaces = DataWriter.MultisessionInterfaces
        If Err.Number <> 0 _
        Then
            WScript.Echo "Multisession is not supported for this disc"
            Main = 1
            Exit Function
        End If
        On Error Goto 0

        WScript.Echo "Importing data from the previous session..."
        FSI.ImportFileSystem()
    Else 
        FSI.ChooseImageDefaults(Recorder)
    End If

    ' Add the directory and its contents to the file system 
    WScript.Echo "Adding " & Path & " directory to the disc..."
    FSI.Root.AddTree Path, false

    ' Create an image from the file system image object
    Dim Result
    Set Result = FSI.CreateResultImage()
    Stream = Result.ImageStream
    
    ' Write stream to disc using the specified recorder
    WScript.Echo "Writing content to the disc..."
    DataWriter.Write(Stream)

    WScript.Echo "Finished writing content."
    Main = 0
End Function

```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando o IMAPi](using-imapi.md)
</dt> <dt>

[_ *IStream**](/windows/desktop/api/objidl/nn-objidl-istream)
</dt> <dt>

[**IDiscMaster2**](/windows/desktop/api/imapi2/nn-imapi2-idiscmaster2)
</dt> <dt>

[**IDiscFormat2Data**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data)
</dt> <dt>

[**IFileSystemImage**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage)
</dt> </dl>

 

 
