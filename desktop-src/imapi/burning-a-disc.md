---
title: Gravando uma imagem de disco
description: A criação de mestre (gravação de um disco) usando o IMAPi consiste nas seguintes etapas construir uma imagem do sistema de arquivos que contém os diretórios e arquivos a serem gravados no disco. Configure um gravador de disco para se comunicar com o dispositivo óptico. Crie um gravador de dados e grave a imagem em disco.
ms.assetid: f2eee14e-695d-4678-b3c1-b521ab4d4a7e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6e3086f728ca0b0826a001d26841edcfe07c6a1
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104293989"
---
# <a name="burning-a-disc-image"></a><span data-ttu-id="da850-103">Gravando uma imagem de disco</span><span class="sxs-lookup"><span data-stu-id="da850-103">Burning a Disc Image</span></span>

<span data-ttu-id="da850-104">A criação de mestre (gravação de um disco) usando o IMAPi consiste nas seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="da850-104">Mastering (burning a disc) using IMAPI consists of the following steps:</span></span>

1.  <span data-ttu-id="da850-105">Construa uma imagem do sistema de arquivos que contém os diretórios e arquivos para gravar o disco.</span><span class="sxs-lookup"><span data-stu-id="da850-105">Construct a file system image that contains the directories and files to write disc.</span></span>
2.  <span data-ttu-id="da850-106">[Configure um gravador de disco](#set-up-a-disc-recorder) para se comunicar com o dispositivo óptico.</span><span class="sxs-lookup"><span data-stu-id="da850-106">[Set up a disc recorder](#set-up-a-disc-recorder) to communicate with the optical device.</span></span>
3.  <span data-ttu-id="da850-107">[Crie um gravador de dados](#create-a-data-writer-and-write-the-burn-image) e grave a imagem em disco.</span><span class="sxs-lookup"><span data-stu-id="da850-107">[Create a data writer](#create-a-data-writer-and-write-the-burn-image) and burn the image to disc.</span></span>

<span data-ttu-id="da850-108">Para obter um exemplo que grava uma imagem de disco, consulte [exemplo de VBScript](#vbscript-example).</span><span class="sxs-lookup"><span data-stu-id="da850-108">For an example that burns a disc image, see [VBScript example](#vbscript-example).</span></span>

## <a name="construct-a-burn-image"></a><span data-ttu-id="da850-109">Construir uma imagem de gravação</span><span class="sxs-lookup"><span data-stu-id="da850-109">Construct a burn image</span></span>

<span data-ttu-id="da850-110">Uma imagem de gravação é um fluxo de dados que está pronto para ser gravado na mídia óptica.</span><span class="sxs-lookup"><span data-stu-id="da850-110">A burn image is a data stream that is ready to be written to optical media.</span></span> <span data-ttu-id="da850-111">A imagem de gravação para formatos ISO9660, Joliet e UDF consiste em um sistema de arquivos de diretórios e arquivos individuais.</span><span class="sxs-lookup"><span data-stu-id="da850-111">The burn image for ISO9660, Joliet and UDF formats consists of a file system of individual files and directories.</span></span> <span data-ttu-id="da850-112">O objeto **CFileSystemImage** é o objeto do sistema de arquivos que contém os arquivos e diretórios a serem colocados na mídia óptica.</span><span class="sxs-lookup"><span data-stu-id="da850-112">The **CFileSystemImage** object is the file system object that holds the files and directories to place on the optical media.</span></span> <span data-ttu-id="da850-113">A interface [**IFileSystemImage**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage) fornece acesso ao objeto e às configurações do sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="da850-113">The [**IFileSystemImage**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage) interface provides access to the file system object and settings.</span></span>

<span data-ttu-id="da850-114">Depois de criar o objeto do sistema de arquivos, chame os métodos [**IFileSystemImage:: CreateFileItem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createfileitem) e [**IFileSystemImage:: CreateDirectoryItem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createdirectoryitem) para criar os objetos de arquivo e diretório, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="da850-114">After creating the file system object, call the [**IFileSystemImage::CreateFileItem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createfileitem) and [**IFileSystemImage::CreateDirectoryItem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createdirectoryitem) methods to create the file and directory objects, respectively.</span></span> <span data-ttu-id="da850-115">Os objetos de arquivo e diretório podem ser usados para fornecer detalhes específicos sobre o arquivo e o diretório.</span><span class="sxs-lookup"><span data-stu-id="da850-115">The file and directory objects can be used to provide specific details about the file and directory.</span></span> <span data-ttu-id="da850-116">Os métodos do manipulador de eventos disponíveis para [**IFileSystemImage**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage) podem identificar o arquivo atual que está sendo adicionado à imagem do sistema de arquivos, o número de setores já copiados e o número total de setores a serem copiados.</span><span class="sxs-lookup"><span data-stu-id="da850-116">The event handler methods available for [**IFileSystemImage**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage) can identify the current file being added to the file system image, the number of sectors already copied, and the total number of sectors to be copied.</span></span>

<span data-ttu-id="da850-117">Opcionalmente, uma imagem de inicialização pode ser anexada ao sistema de arquivos usando a propriedade [**IFileSystemImage::p UT \_ BootImageOptions**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-put_bootimageoptions) .</span><span class="sxs-lookup"><span data-stu-id="da850-117">Optionally, a boot image can be attached to the file system using the [**IFileSystemImage::put\_BootImageOptions**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-put_bootimageoptions) property.</span></span> <span data-ttu-id="da850-118">Para obter um exemplo, consulte [adicionando uma imagem de inicialização](adding-a-boot-image.md).</span><span class="sxs-lookup"><span data-stu-id="da850-118">For an example, see [Adding a Boot Image](adding-a-boot-image.md).</span></span>

<span data-ttu-id="da850-119">Por fim, chame [**IFileSystemImage:: CreateResultImage**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createresultimage) para criar um fluxo de dados e fornece acesso por meio de [**IFileSystemImageResult**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimageresult).</span><span class="sxs-lookup"><span data-stu-id="da850-119">Finally, call [**IFileSystemImage::CreateResultImage**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createresultimage) to create a data stream and provides access through [**IFileSystemImageResult**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimageresult).</span></span> <span data-ttu-id="da850-120">O novo fluxo de dados pode então ser fornecido diretamente para o método [**IDiscFormat2Data:: Write**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-write) ou ser salvo em um arquivo para uso posterior.</span><span class="sxs-lookup"><span data-stu-id="da850-120">The new data stream can then be provided directly to the [**IDiscFormat2Data::Write**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-write) method or be saved to a file for later use.</span></span>

## <a name="set-up-a-disc-recorder"></a><span data-ttu-id="da850-121">Configurar um gravador de disco</span><span class="sxs-lookup"><span data-stu-id="da850-121">Set up a disc recorder</span></span>

<span data-ttu-id="da850-122">O objeto **MsftDiscMaster2** fornece uma enumeração dos dispositivos ópticos no sistema.</span><span class="sxs-lookup"><span data-stu-id="da850-122">The **MsftDiscMaster2** object provides an enumeration of the optical devices on the system.</span></span> <span data-ttu-id="da850-123">A interface [**IDiscMaster2**](/windows/desktop/api/imapi2/nn-imapi2-idiscmaster2) fornece acesso à enumeração de dispositivo resultante.</span><span class="sxs-lookup"><span data-stu-id="da850-123">The [**IDiscMaster2**](/windows/desktop/api/imapi2/nn-imapi2-idiscmaster2) interface provides access to the resultant device enumeration.</span></span> <span data-ttu-id="da850-124">Percorra as enumerações para localizar um dispositivo de gravação apropriado.</span><span class="sxs-lookup"><span data-stu-id="da850-124">Traverse the enumerations to locate an appropriate recording device.</span></span> <span data-ttu-id="da850-125">O objeto **MsftDiscMaster2** também fornece notificações de eventos quando dispositivos ópticos são adicionados ou excluídos de um computador.</span><span class="sxs-lookup"><span data-stu-id="da850-125">The **MsftDiscMaster2** object also provides event notifications when optical devices are added to or deleted from a computer.</span></span>

<span data-ttu-id="da850-126">Depois de encontrar um gravador óptico e recuperar sua ID, crie um objeto **MsftDiscRecorder2** e inicialize o gravador usando a ID do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="da850-126">After finding an optical recorder and retrieving its ID, create an **MsftDiscRecorder2** object and initialize the recorder using the device ID.</span></span> <span data-ttu-id="da850-127">A interface [**IDiscRecorder2**](/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2) fornece acesso ao objeto do gravador, bem como algumas informações básicas do dispositivo, como ID do fornecedor, ID do produto, revisão do produto e métodos para ejetar a mídia e fechar a bandeja.</span><span class="sxs-lookup"><span data-stu-id="da850-127">The [**IDiscRecorder2**](/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2) interface provides access to the recorder object as well as some basic device information such as vendor ID, product ID, product revision, and methods to eject the media and close the tray.</span></span>

## <a name="create-a-data-writer-and-write-the-burn-image"></a><span data-ttu-id="da850-128">Criar um gravador de dados e gravar a imagem de gravação</span><span class="sxs-lookup"><span data-stu-id="da850-128">Create a data writer and write the burn image</span></span>

<span data-ttu-id="da850-129">O objeto **MsftDiscFormat2Data** fornece o método de escrita, as propriedades sobre a função de gravação e as propriedades específicas de mídia.</span><span class="sxs-lookup"><span data-stu-id="da850-129">The **MsftDiscFormat2Data** object provides the writing method, the properties about the write function and media-specific properties.</span></span> <span data-ttu-id="da850-130">A interface [**IDiscFormat2Data**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data) fornece acesso ao objeto **MsftDiscFormat2Data** .</span><span class="sxs-lookup"><span data-stu-id="da850-130">The [**IDiscFormat2Data**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data) interface provides access to the **MsftDiscFormat2Data** object.</span></span>

<span data-ttu-id="da850-131">O gravador de disco vincula-se ao gravador de formato usando a propriedade [**IDiscFormat2Data::p UT \_ Recorder**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-put_recorder) .</span><span class="sxs-lookup"><span data-stu-id="da850-131">The disc recorder links to the format writer using the [**IDiscFormat2Data::put\_Recorder**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-put_recorder) property.</span></span> <span data-ttu-id="da850-132">Depois que o gravador estiver associado ao gravador de formato, você poderá executar consultas em relação à mídia e atualizar as propriedades específicas de gravação antes de gravar a imagem de resultado em disco usando o método [**IDiscFormat2Data:: Write**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-write) .</span><span class="sxs-lookup"><span data-stu-id="da850-132">After the recorder is bound to the format writer, you can perform queries regarding the media and update write-specific properties before writing the result image to disc using the [**IDiscFormat2Data::Write**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-write) method.</span></span>

<span data-ttu-id="da850-133">Outras interfaces de gravação de formato fornecidas pelo IMAPi funcionam da mesma forma; interfaces de escrita de formato adicionais incluem:</span><span class="sxs-lookup"><span data-stu-id="da850-133">Other format writing interfaces provided by IMAPI work similarly; additional format writing interfaces include:</span></span>

-   <span data-ttu-id="da850-134">[**IDiscFormat2Erase**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2erase) apaga a mídia óptica regravável.</span><span class="sxs-lookup"><span data-stu-id="da850-134">[**IDiscFormat2Erase**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2erase) erases rewritable optical media.</span></span>
-   <span data-ttu-id="da850-135">[**IDiscFormat2RawCD**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2rawcd) grava uma imagem bruta em mídia óptica.</span><span class="sxs-lookup"><span data-stu-id="da850-135">[**IDiscFormat2RawCD**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2rawcd) writes a raw image to optical media.</span></span>
-   <span data-ttu-id="da850-136">[**IDiscFormat2TrackAtOnce**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2trackatonce) grava faixas de áudio em mídia óptica.</span><span class="sxs-lookup"><span data-stu-id="da850-136">[**IDiscFormat2TrackAtOnce**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2trackatonce) writes audio tracks to optical media.</span></span>

> [!Note]  
> <span data-ttu-id="da850-137">É possível que uma transição de estado de energia ocorra durante uma operação de gravação (ou seja, logoff do usuário ou suspensão do sistema) que leva à interrupção do processo de gravação e possível perda de dados.</span><span class="sxs-lookup"><span data-stu-id="da850-137">It is possible for a power state transition to take place during a burn operation (i.e. user log-off or system suspend) which leads to the interruption of the burn process and possible data loss.</span></span> <span data-ttu-id="da850-138">Para considerações de programação, consulte [impedindo o logoff ou suspender durante uma gravação](preventing-logoff-or-suspend-during-a-burn.md).</span><span class="sxs-lookup"><span data-stu-id="da850-138">For programming considerations, see [Preventing Logoff or Suspend During a Burn](preventing-logoff-or-suspend-during-a-burn.md).</span></span>

 

## <a name="vbscript-example"></a><span data-ttu-id="da850-139">Exemplo de VBScript</span><span class="sxs-lookup"><span data-stu-id="da850-139">VBScript example</span></span>

<span data-ttu-id="da850-140">Este exemplo de script mostra como usar os objetos IMAPi para gravar mídia óptica; mais especificamente, grave um diretório em um disco em branco. O código não contém nenhuma verificação de erro e pressupõe o seguinte:</span><span class="sxs-lookup"><span data-stu-id="da850-140">This script example shows how to use the IMAPI objects to burn optical media; more specifically, write a directory to a blank disc. The code contains no error checking, and assumes the following:</span></span>

-   <span data-ttu-id="da850-141">Um dispositivo de disco compatível está instalado no sistema.</span><span class="sxs-lookup"><span data-stu-id="da850-141">A compatible disc device is installed on the system.</span></span>
-   <span data-ttu-id="da850-142">O dispositivo de disco é a segunda unidade do sistema.</span><span class="sxs-lookup"><span data-stu-id="da850-142">The disc device is the second drive on the system.</span></span>
-   <span data-ttu-id="da850-143">Um disco compatível é inserido no dispositivo de disco.</span><span class="sxs-lookup"><span data-stu-id="da850-143">A compatible disc is inserted in the disc device.</span></span>
-   <span data-ttu-id="da850-144">O disco está em branco.</span><span class="sxs-lookup"><span data-stu-id="da850-144">The disc is blank.</span></span>
-   <span data-ttu-id="da850-145">Os arquivos a serem gravados no disco estão localizados em "g: \\ burndir".</span><span class="sxs-lookup"><span data-stu-id="da850-145">Files to write to disc are located in "g:\\burndir".</span></span>

<span data-ttu-id="da850-146">Funcionalidades adicionais, como verificação de erros, compatibilidade de dispositivos e mídias, notificação de eventos e cálculo de espaço livre no disco, podem ser adicionadas a esse script.</span><span class="sxs-lookup"><span data-stu-id="da850-146">Additional functionality such as error checking, device and media compatibility, event notification, and calculating free space on the disc can be added to this script.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="da850-147">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="da850-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="da850-148">Usando o IMAPi</span><span class="sxs-lookup"><span data-stu-id="da850-148">Using IMAPI</span></span>](using-imapi.md)
</dt> <dt>

[<span data-ttu-id="da850-149">**IDiscFormat2Data**</span><span class="sxs-lookup"><span data-stu-id="da850-149">**IDiscFormat2Data**</span></span>](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data)
</dt> <dt>

[<span data-ttu-id="da850-150">**IDiscFormat2Erase**</span><span class="sxs-lookup"><span data-stu-id="da850-150">**IDiscFormat2Erase**</span></span>](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2erase)
</dt> <dt>

[<span data-ttu-id="da850-151">**IDiscFormat2RawCD**</span><span class="sxs-lookup"><span data-stu-id="da850-151">**IDiscFormat2RawCD**</span></span>](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2rawcd)
</dt> <dt>

[<span data-ttu-id="da850-152">**IDiscFormat2TrackAtOnce**</span><span class="sxs-lookup"><span data-stu-id="da850-152">**IDiscFormat2TrackAtOnce**</span></span>](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2trackatonce)
</dt> <dt>

[<span data-ttu-id="da850-153">**IDiscMaster2**</span><span class="sxs-lookup"><span data-stu-id="da850-153">**IDiscMaster2**</span></span>](/windows/desktop/api/imapi2/nn-imapi2-idiscmaster2)
</dt> <dt>

[<span data-ttu-id="da850-154">**IDiscRecorder2**</span><span class="sxs-lookup"><span data-stu-id="da850-154">**IDiscRecorder2**</span></span>](/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2)
</dt> <dt>

[<span data-ttu-id="da850-155">**IFileSystemImage**</span><span class="sxs-lookup"><span data-stu-id="da850-155">**IFileSystemImage**</span></span>](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage)
</dt> <dt>

[<span data-ttu-id="da850-156">**IStream**</span><span class="sxs-lookup"><span data-stu-id="da850-156">**IStream**</span></span>](/windows/desktop/api/objidl/nn-objidl-istream)
</dt> </dl>

 

 