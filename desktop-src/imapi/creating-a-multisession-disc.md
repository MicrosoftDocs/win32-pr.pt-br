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
# <a name="creating-a-multisession-disc"></a><span data-ttu-id="541f5-103">Criando um disco de várias sessões</span><span class="sxs-lookup"><span data-stu-id="541f5-103">Creating a Multisession Disc</span></span>

<span data-ttu-id="541f5-104">A [API de mestre de imagem](about-imapi.md) (IMAPI) dá suporte à adição e remoção de arquivos para, ou do, os seguintes tipos de disco de várias sessões:</span><span class="sxs-lookup"><span data-stu-id="541f5-104">The [Image Mastering API](about-imapi.md) (IMAPI) supports the addition and removal of files to, or from, the following multisession disc types:</span></span>

-   <span data-ttu-id="541f5-105">CD-R/CD-RW</span><span class="sxs-lookup"><span data-stu-id="541f5-105">CD-R/CD-RW</span></span>
-   <span data-ttu-id="541f5-106">Single-Layer DVD + R/DVD-R</span><span class="sxs-lookup"><span data-stu-id="541f5-106">Single-Layer DVD+R/DVD-R</span></span>
-   <span data-ttu-id="541f5-107">DVD + R de camada dupla</span><span class="sxs-lookup"><span data-stu-id="541f5-107">DVD+R Dual Layer</span></span>
-   <span data-ttu-id="541f5-108">BD-R</span><span class="sxs-lookup"><span data-stu-id="541f5-108">BD-R</span></span>
-   <span data-ttu-id="541f5-109">DVD-RW/DVD + RW (**somente Windows 7**)</span><span class="sxs-lookup"><span data-stu-id="541f5-109">DVD-RW/DVD+RW (**Windows 7 Only**)</span></span>
-   <span data-ttu-id="541f5-110">DVD-RAM (**somente Windows 7**)</span><span class="sxs-lookup"><span data-stu-id="541f5-110">DVD-RAM (**Windows 7 Only**)</span></span>
-   <span data-ttu-id="541f5-111">BD-RE (**somente Windows 7**)</span><span class="sxs-lookup"><span data-stu-id="541f5-111">BD-RE (**Windows 7 Only**)</span></span>

<span data-ttu-id="541f5-112">A criação de um disco de várias sessões usando IMAPi consiste nas etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="541f5-112">Creation of a multisession disc using IMAPI consists of the following steps.</span></span> <span data-ttu-id="541f5-113">Cada uma dessas etapas documentadas contém a parte relevante do exemplo de script completo Visual Basic fornecido na seção final.</span><span class="sxs-lookup"><span data-stu-id="541f5-113">Each of these documented steps contains the relevant portion of the complete Visual Basic script example provided in the final section.</span></span>

## <a name="initializing-the-disc-recorder"></a><span data-ttu-id="541f5-114">Inicializando o gravador de disco</span><span class="sxs-lookup"><span data-stu-id="541f5-114">Initializing the Disc Recorder</span></span>

<span data-ttu-id="541f5-115">Antes da inicialização do dispositivo, o objeto **MsftDiscMaster2** fornece uma enumeração dos dispositivos ópticos no sistema.</span><span class="sxs-lookup"><span data-stu-id="541f5-115">Prior to device initialization, the **MsftDiscMaster2** object provides an enumeration of the optical devices on the system.</span></span> <span data-ttu-id="541f5-116">A interface [**IDiscMaster2**](/windows/desktop/api/imapi2/nn-imapi2-idiscmaster2) fornece acesso a essa enumeração de dispositivo para facilitar o local do dispositivo de gravação apropriado.</span><span class="sxs-lookup"><span data-stu-id="541f5-116">The [**IDiscMaster2**](/windows/desktop/api/imapi2/nn-imapi2-idiscmaster2) interface provides access to this device enumeration to facilitate the location of the appropriate recording device.</span></span> <span data-ttu-id="541f5-117">O objeto **MsftDiscMaster2** também fornece notificações de eventos quando dispositivos ópticos são adicionados ou removidos de um computador.</span><span class="sxs-lookup"><span data-stu-id="541f5-117">The **MsftDiscMaster2** object also provides event notifications when optical devices are added to or removed from a machine.</span></span>

<span data-ttu-id="541f5-118">Depois de localizar um gravador óptico e recuperar a ID atribuída a ele, crie um novo objeto **MsftDiscMaster2** e inicialize o gravador usando a ID de dispositivo específica.</span><span class="sxs-lookup"><span data-stu-id="541f5-118">After locating an optical recorder and retrieving the ID assigned to it, create a new **MsftDiscMaster2** object and initialize the recorder using the specific device ID.</span></span>

<span data-ttu-id="541f5-119">A interface [**IDiscRecorder2**](/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2) fornece acesso a informações básicas do dispositivo, como ID do fornecedor, ID do produto, revisão do produto, bem como os métodos para ejetar mídia ou fechar a bandeja.</span><span class="sxs-lookup"><span data-stu-id="541f5-119">The [**IDiscRecorder2**](/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2) interface provides access to basic device information such as vendor ID, product ID, product revision, as well as the methods to eject media or close the tray.</span></span>

> [!Note]  
> <span data-ttu-id="541f5-120">As constantes e dimensões adicionais declaradas no exemplo a seguir são usadas posteriormente no script de exemplo completo localizado na seção final deste documento.</span><span class="sxs-lookup"><span data-stu-id="541f5-120">The additional constants and dimensions declared in the following sample are used later in the complete sample script located in the final section of this document.</span></span> <span data-ttu-id="541f5-121">Esses elementos não são necessários para o ato de inicializar um gravador de disco.</span><span class="sxs-lookup"><span data-stu-id="541f5-121">These elements are not required for the act of initializing a disc recorder.</span></span>

 


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



## <a name="creating-a-data-writer"></a><span data-ttu-id="541f5-122">Criando um gravador de dados</span><span class="sxs-lookup"><span data-stu-id="541f5-122">Creating a Data Writer</span></span>

<span data-ttu-id="541f5-123">O objeto _ *MsftDiscFormat2Data*\* fornece o método de escrita, suas propriedades, bem como as propriedades específicas de mídia.</span><span class="sxs-lookup"><span data-stu-id="541f5-123">The _ *MsftDiscFormat2Data*\* object provides the writing method, its properties, as well as the media-specific properties.</span></span> <span data-ttu-id="541f5-124">A interface [**IDiscFormat2Data**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data) fornece acesso a esse objeto.</span><span class="sxs-lookup"><span data-stu-id="541f5-124">The [**IDiscFormat2Data**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data) interface provides access to this object.</span></span>

<span data-ttu-id="541f5-125">O gravador de disco é associado ao gravador de formato usando a propriedade [**IDiscFormat2Data::p UT \_ Recorder**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-put_recorder) .</span><span class="sxs-lookup"><span data-stu-id="541f5-125">The disc recorder binds to the format writer using the [**IDiscFormat2Data::put\_Recorder**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-put_recorder) property.</span></span> <span data-ttu-id="541f5-126">Depois que o gravador está associado ao gravador de formato, as consultas de propriedade específicas de mídia e gravação podem ser executadas antes de gravar a imagem de resultado em disco usando o método [**IDiscFormat2Data:: Write**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-write) .</span><span class="sxs-lookup"><span data-stu-id="541f5-126">After the recorder is bound to the format writer, media and write-specific property queries can be performed prior to writing the result image to disc using the [**IDiscFormat2Data::Write**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-write) method.</span></span>

> [!Note]  
> <span data-ttu-id="541f5-127">A cadeia de caracteres de nome do cliente especificada no código de exemplo abaixo deve ser ajustada conforme apropriado para o aplicativo específico.</span><span class="sxs-lookup"><span data-stu-id="541f5-127">The client name string specified in the sample code below should be adjusted as appropriate for the specific application.</span></span>

 


```VB
    ' Create a DiscFormat2Data object and set the recorder
    Dim DataWriter
    Set DataWriter = CreateObject ("IMAPI2.MsftDiscFormat2Data")
    DataWriter.Recorder = Recorder
    DataWriter.ClientName = "IMAPIv2 TEST"
```



## <a name="creating-the-file-system-object"></a><span data-ttu-id="541f5-128">Criando o objeto do sistema de arquivos</span><span class="sxs-lookup"><span data-stu-id="541f5-128">Creating the File System Object</span></span>

<span data-ttu-id="541f5-129">Para gravar uma nova sessão, uma imagem de gravação deve ser gerada para ela primeiro.</span><span class="sxs-lookup"><span data-stu-id="541f5-129">In order to record a new session, a burn image must be generated for it first.</span></span> <span data-ttu-id="541f5-130">Uma imagem de gravação para formatos **ISO9660**, **Joliet** e **UDF** consiste em sistemas de arquivos de diretórios e arquivos individuais.</span><span class="sxs-lookup"><span data-stu-id="541f5-130">A burn image for **ISO9660**, **Joliet** and **UDF** formats consist of file systems of individual files and directories.</span></span> <span data-ttu-id="541f5-131">O objeto **MsftFileSystemImage** é o objeto do sistema de arquivos que contém os arquivos e diretórios a serem colocados na mídia óptica.</span><span class="sxs-lookup"><span data-stu-id="541f5-131">The **MsftFileSystemImage** object is the file system object that contains the files and directories to be placed on the optical media.</span></span> <span data-ttu-id="541f5-132">A interface [**IFileSystemImage**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage) fornece acesso ao objeto e às configurações do sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="541f5-132">The [**IFileSystemImage**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage) interface provides access to the file system object and settings.</span></span>


```VB
    ' Create a new file system image object
    Dim FSI
    Set FSI = CreateObject("IMAPI2FS.MsftFileSystemImage")
```



## <a name="importing-a-file-system"></a><span data-ttu-id="541f5-133">Importando um sistema de arquivos</span><span class="sxs-lookup"><span data-stu-id="541f5-133">Importing a File System</span></span>

<span data-ttu-id="541f5-134">Antes de continuar, verifique se o disco não está em branco verificando a propriedade [**IDiscFormat2:: get \_ MediaHeuristicallyBlank**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2-get_mediaheuristicallyblank) .</span><span class="sxs-lookup"><span data-stu-id="541f5-134">Before proceeding, ensure that the disc is not blank by checking the [**IDiscFormat2::get\_MediaHeuristicallyBlank**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2-get_mediaheuristicallyblank) property.</span></span>

<span data-ttu-id="541f5-135">Depois de criar o objeto **MsftFileSystemImage** , a propriedade [**IFileSystemImage::p UT \_ MultisessionInterfaces**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-put_multisessioninterfaces) deve ser inicializada antes de uma chamada para o método [**IFileSystemImage:: ImportFileSystem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-importfilesystem) ou [**IFileSystemImage:: ImportSpecificFileSystem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-importspecificfilesystem) para importar o sistema de arquivos da última sessão gravada.</span><span class="sxs-lookup"><span data-stu-id="541f5-135">After creating the **MsftFileSystemImage** object, the [**IFileSystemImage::put\_MultisessionInterfaces**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-put_multisessioninterfaces) property should be initialized prior to a call to either the [**IFileSystemImage::ImportFileSystem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-importfilesystem) or [**IFileSystemImage::ImportSpecificFileSystem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-importspecificfilesystem) method to import the file system from the last recorded session.</span></span> <span data-ttu-id="541f5-136">Esses métodos preencherão automaticamente o objeto **MsftFileSystemImage** com informações que descrevem os arquivos e diretórios gravados anteriormente.</span><span class="sxs-lookup"><span data-stu-id="541f5-136">These methods will automatically populate the **MsftFileSystemImage** object with information describing the previously recorded files and directories.</span></span>

> [!Note]  
> <span data-ttu-id="541f5-137">A propriedade [**IFileSystemImage::p UT \_ MultisessionInterfaces**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-put_multisessioninterfaces) normalmente é inicializada com as interfaces de várias sessões fornecidas pelo gravador de dados por meio da propriedade [**IDiscFormat2Data:: get \_ MultisessionInterfaces**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-get_multisessioninterfaces) .</span><span class="sxs-lookup"><span data-stu-id="541f5-137">The [**IFileSystemImage::put\_MultisessionInterfaces**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-put_multisessioninterfaces) property is typically initialized with the multisession interfaces provided by the data writer via the [**IDiscFormat2Data::get\_MultisessionInterfaces**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-get_multisessioninterfaces) property.</span></span>

 

<span data-ttu-id="541f5-138">As tentativas de definir a propriedade **IFileSystemImage::p UT \_ MultisessionInterfaces** falharão se o IMAPI não oferecer suporte a várias sessões para a mídia inserida no momento ou se a mídia não puder ser anexada por algum outro motivo (por exemplo, porque está fechada).</span><span class="sxs-lookup"><span data-stu-id="541f5-138">Attempts to set the **IFileSystemImage::put\_MultisessionInterfaces** property will fail if IMAPI does not support multisession for the currently inserted media or the media cannot be appended for some other reason (e.g. because it is closed).</span></span>

<span data-ttu-id="541f5-139">Se a sessão de gravação anterior contiver mais de um tipo de sistema de arquivos, o método [**IFileSystemImage:: ImportFileSystem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-importfilesystem) importará informações do tipo de sistema de arquivos mais avançado presente.</span><span class="sxs-lookup"><span data-stu-id="541f5-139">If the previous burn session contained more than one file system type, the [**IFileSystemImage::ImportFileSystem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-importfilesystem) method will import information from the most advanced file system type present.</span></span> <span data-ttu-id="541f5-140">Por exemplo, no exemplo fornecido neste tópico, UDF é o sistema de arquivos importado.</span><span class="sxs-lookup"><span data-stu-id="541f5-140">For example, in the example provided in this topic, UDF is the imported file system.</span></span> <span data-ttu-id="541f5-141">No entanto, o uso do método [**IFileSystemImage:: ImportSpecificFileSystem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-importspecificfilesystem) permite a seleção específica do sistema de arquivos a ser importado.</span><span class="sxs-lookup"><span data-stu-id="541f5-141">However, use of the [**IFileSystemImage::ImportSpecificFileSystem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-importspecificfilesystem) method allows the specific selection of the file system to import.</span></span>

> [!Note]  
> <span data-ttu-id="541f5-142">O método [**IFileSystemImage:: IdentifyFileSystemsOnDisc**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-identifyfilesystemsondisc) pode ser usado para determinar quais sistemas de arquivos estão disponíveis no disco.</span><span class="sxs-lookup"><span data-stu-id="541f5-142">The [**IFileSystemImage::IdentifyFileSystemsOnDisc**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-identifyfilesystemsondisc) method can be used to determine which file systems are available on the disc.</span></span>

 


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



## <a name="adding-or-removing-files-to-the-file-system"></a><span data-ttu-id="541f5-143">Adicionando ou removendo arquivos no sistema de arquivos</span><span class="sxs-lookup"><span data-stu-id="541f5-143">Adding or Removing Files to the File System</span></span>

<span data-ttu-id="541f5-144">Depois de criar o objeto do sistema de arquivos e importar o sistema de arquivos da sessão anterior, chame os métodos [**IFileSystemImage:: CreateFileItem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createfileitem) e [**IFileSystemImage:: CreateDirectoryItem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createdirectoryitem) para criar novos objetos de arquivo e diretório, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="541f5-144">After creating the file system object and importing the file system from the previous session, call the [**IFileSystemImage::CreateFileItem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createfileitem) and [**IFileSystemImage::CreateDirectoryItem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createdirectoryitem) methods to create new file and directory objects, respectively.</span></span> <span data-ttu-id="541f5-145">Os objetos de arquivo e diretório fornecem detalhes específicos sobre os arquivos e diretórios.</span><span class="sxs-lookup"><span data-stu-id="541f5-145">The file and directory objects provide specific details about the files and directories.</span></span> <span data-ttu-id="541f5-146">Como alternativa, o método [**IFsiDirectoryItem:: addtree**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-addtree) de um objeto de diretório, representado por meio da interface [**IFsiDirectoryItem**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsidirectoryitem) , pode ser usado para adicionar arquivos e diretórios existentes de outro dispositivo de armazenamento (ou seja, um disco rígido).</span><span class="sxs-lookup"><span data-stu-id="541f5-146">Alternatively, the [**IFsiDirectoryItem::AddTree**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-addtree) method of a directory object, represented via the [**IFsiDirectoryItem**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsidirectoryitem) interface, can be used to add existing files and directories from another storage device (i.e. a hard drive).</span></span>

<span data-ttu-id="541f5-147">O método de atualização do manipulador de eventos disponível para [**IFileSystemImage**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage) identifica o arquivo atual que está sendo adicionado à imagem do sistema de arquivos, o número de setores já copiados e o número total de setores a serem copiados.</span><span class="sxs-lookup"><span data-stu-id="541f5-147">The event handler update method available for [**IFileSystemImage**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage) identifies the current file being added to the file system image, the number of sectors already copied, and the total number of sectors to be copied.</span></span>

<span data-ttu-id="541f5-148">Para remover arquivos e diretórios existentes do sistema de arquivos, use os métodos [**IFsiDirectoryItem:: Remove**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-remove) e [**IFsiDirectoryItem:: RemoveTree**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-removetree) dos objetos de diretório representados por meio da interface [**IFsiDirectoryItem**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsidirectoryitem) .</span><span class="sxs-lookup"><span data-stu-id="541f5-148">To remove existing files and directories from the file system, use the [**IFsiDirectoryItem::Remove**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-remove) and [**IFsiDirectoryItem::RemoveTree**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-removetree) methods of the directory objects represented via the [**IFsiDirectoryItem**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsidirectoryitem) interface.</span></span> <span data-ttu-id="541f5-149">A propriedade de [**\_ raiz IFileSystemImage:: Get**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-get_root) é usada para obter um ponteiro para o diretório raiz do sistema de arquivos e a interface **IFsiDirectoryItem** para percorrer a árvore de diretórios.</span><span class="sxs-lookup"><span data-stu-id="541f5-149">The [**IFileSystemImage::get\_Root**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-get_root) property is used to get a pointer to the root directory of the file system and the **IFsiDirectoryItem** interface to traverse through the directory tree.</span></span>

> [!Note]  
> <span data-ttu-id="541f5-150">Os arquivos e diretórios removidos por meio dos métodos [**IFsiDirectoryItem:: Remove**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-remove) e [**IFsiDirectoryItem:: RemoveTree**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-removetree) não são fisicamente removidos do disco, e o software avançado pode recuperar facilmente as informações excluídas.</span><span class="sxs-lookup"><span data-stu-id="541f5-150">Files and directories removed via the [**IFsiDirectoryItem::Remove**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-remove) and [**IFsiDirectoryItem::RemoveTree**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-removetree) methods are not physically removed from the disc, and advanced software can easily recover the deleted information.</span></span>

 


```VB
    ' Add the directory and its contents to the file system 
    WScript.Echo "Adding " & Path & " directory to the disc..."
    FSI.Root.AddTree Path, false
```



## <a name="constructing-a-file-system-image"></a><span data-ttu-id="541f5-151">Construindo uma imagem do sistema de arquivos</span><span class="sxs-lookup"><span data-stu-id="541f5-151">Constructing a File System Image</span></span>

<span data-ttu-id="541f5-152">A etapa final é chamar [**IFileSystemImage:: CreateResultImage**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createresultimage) para criar um fluxo de dados para a imagem de gravação e fornecer acesso a ele por meio da interface [**IFileSystemImageResult**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimageresult) .</span><span class="sxs-lookup"><span data-stu-id="541f5-152">The final step is to call [**IFileSystemImage::CreateResultImage**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createresultimage) to create a data stream for the burn image and provide access to it through the [**IFileSystemImageResult**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimageresult) interface.</span></span> <span data-ttu-id="541f5-153">Esse fluxo de dados pode ser fornecido diretamente para o método [**IDiscFormat2Data:: Write**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-write) ou ser salvo em um arquivo para uso posterior.</span><span class="sxs-lookup"><span data-stu-id="541f5-153">This data stream can either be provided directly to the [**IDiscFormat2Data::Write**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-write) method or be saved to a file for later use.</span></span>


```VB
    ' Create an image from the file system image object
    Dim Result
    Set Result = FSI.CreateResultImage()
    Stream = Result.ImageStream
```



## <a name="example-summary"></a><span data-ttu-id="541f5-154">Resumo de exemplo</span><span class="sxs-lookup"><span data-stu-id="541f5-154">Example Summary</span></span>

<span data-ttu-id="541f5-155">O exemplo de script a seguir Visual Basic mostra como usar objetos IMAPi para criar discos com várias sessões.</span><span class="sxs-lookup"><span data-stu-id="541f5-155">The following Visual Basic script example shows how to use IMAPI objects to create multisession discs.</span></span> <span data-ttu-id="541f5-156">O exemplo cria uma nova sessão e adiciona um diretório ao disco. Para simplificar, o código não executa verificação de erro extensiva e pressupõe o seguinte:</span><span class="sxs-lookup"><span data-stu-id="541f5-156">The example creates a new session and adds a directory to the disc. For the sake of simplicity, the code does not perform extensive error checking, and assumes the following:</span></span>

-   <span data-ttu-id="541f5-157">Um dispositivo de disco compatível está instalado no sistema.</span><span class="sxs-lookup"><span data-stu-id="541f5-157">A compatible disc device is installed on the system.</span></span>
-   <span data-ttu-id="541f5-158">O dispositivo de disco é a primeira unidade no sistema.</span><span class="sxs-lookup"><span data-stu-id="541f5-158">The disc device is the first drive on the system.</span></span>
-   <span data-ttu-id="541f5-159">Um disco compatível é inserido no dispositivo de disco.</span><span class="sxs-lookup"><span data-stu-id="541f5-159">A compatible disc is inserted in the disc device.</span></span>
-   <span data-ttu-id="541f5-160">Os arquivos a serem adicionados ao disco estão localizados em "g: \\ burndir".</span><span class="sxs-lookup"><span data-stu-id="541f5-160">Files to add to the disc are located in "g:\\burndir".</span></span>

<span data-ttu-id="541f5-161">Funcionalidades adicionais, como verificação de erros extensiva, compatibilidade de dispositivo e mídia, notificação de eventos e cálculo de espaço livre no disco, podem ser adicionadas ao script.</span><span class="sxs-lookup"><span data-stu-id="541f5-161">Additional functionality such as extensive error checking, device and media compatibility, event notification, and calculation of free space on the disc can be added to the script.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="541f5-162">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="541f5-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="541f5-163">Usando o IMAPi</span><span class="sxs-lookup"><span data-stu-id="541f5-163">Using IMAPI</span></span>](using-imapi.md)
</dt> <dt>

[<span data-ttu-id="541f5-164">_ *IStream*\*</span><span class="sxs-lookup"><span data-stu-id="541f5-164">_ *IStream*\*</span></span>](/windows/desktop/api/objidl/nn-objidl-istream)
</dt> <dt>

[<span data-ttu-id="541f5-165">**IDiscMaster2**</span><span class="sxs-lookup"><span data-stu-id="541f5-165">**IDiscMaster2**</span></span>](/windows/desktop/api/imapi2/nn-imapi2-idiscmaster2)
</dt> <dt>

[<span data-ttu-id="541f5-166">**IDiscFormat2Data**</span><span class="sxs-lookup"><span data-stu-id="541f5-166">**IDiscFormat2Data**</span></span>](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data)
</dt> <dt>

[<span data-ttu-id="541f5-167">**IFileSystemImage**</span><span class="sxs-lookup"><span data-stu-id="541f5-167">**IFileSystemImage**</span></span>](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage)
</dt> </dl>

 

 
