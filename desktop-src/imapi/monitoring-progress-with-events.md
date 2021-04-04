---
title: Progresso do monitoramento com eventos
description: Várias interfaces permitem que você implemente um manipulador de eventos para receber informações de progresso. Por exemplo, um objeto de evento pode ser anexado ao gravador de dados para receber o status da operação de gravação.
ms.assetid: 1f15a5fe-f5d7-4e09-805f-2d0380bf2bb2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ae3b425fc096234abf59d3a082fbe8a06f3f554
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103823725"
---
# <a name="monitoring-progress-with-events"></a><span data-ttu-id="5d8eb-104">Progresso do monitoramento com eventos</span><span class="sxs-lookup"><span data-stu-id="5d8eb-104">Monitoring Progress With Events</span></span>

<span data-ttu-id="5d8eb-105">Várias interfaces permitem que você implemente um manipulador de eventos para receber informações de progresso.</span><span class="sxs-lookup"><span data-stu-id="5d8eb-105">Several interfaces let you implement an event handler to receive progress information.</span></span> <span data-ttu-id="5d8eb-106">Por exemplo, um objeto de evento pode ser anexado ao gravador de dados para receber o status da operação de gravação.</span><span class="sxs-lookup"><span data-stu-id="5d8eb-106">For example, an event object can be attached to the data writer to receive status of the write operation.</span></span>

<span data-ttu-id="5d8eb-107">Um manipulador de eventos é implementado como uma sub-rotina em um script.</span><span class="sxs-lookup"><span data-stu-id="5d8eb-107">An event handler is implemented as a subroutine in a script.</span></span> <span data-ttu-id="5d8eb-108">O exemplo a seguir mostra como definir a sub-rotina e usar o método **WScript. connectobject** para conectar o manipulador de eventos ao objeto.</span><span class="sxs-lookup"><span data-stu-id="5d8eb-108">The following example shows how to define the subroutine and use the **WScript.ConnectObject** method to connect the event handler to the object.</span></span>


```VB
    ' Create the MsftDiscFormat2Data object (see the IDiscFormat2Data interface).
    Set dataWriter = CreateObject ("IMAPI2.MsftDiscFormat2Data")

    ' Attach event handler (see the DDiscFormat2DataEvents interface).
    ' The "dwBurnEvent_" parameter identifies the handler (see the 
    ' dwBurnEvent_Update subroutine).
    WScript.ConnectObject  dataWriter, "dwBurnEvent_"

' Event handler for the MsftDiscFormat2Data.Write method.
' For details of the subroutine's parameters, see the 
' DDiscFormat2DataEvents::Update method.
SUB dwBurnEvent_Update( byRef object, byRef progress )
    ' --- Other code occurs here. 
END SUB

```



<span data-ttu-id="5d8eb-109">O nome especificado para o nome do manipulador de eventos deve conter o sufixo de sublinhado (" \_ ").</span><span class="sxs-lookup"><span data-stu-id="5d8eb-109">The name specified for the event handler name must contain the underscore suffix ("\_").</span></span> <span data-ttu-id="5d8eb-110">Para formar o nome da sub-rotina, concatene o nome do método para o nome do manipulador de eventos.</span><span class="sxs-lookup"><span data-stu-id="5d8eb-110">To form the subroutine name, concatenate the method name to the event handler name.</span></span> <span data-ttu-id="5d8eb-111">Por exemplo, se você usar "dataWriterEvent \_ " como o nome do manipulador de eventos e o nome do método for "Update", o nome da sub-rotina será dataWriterEvent \_ Update.</span><span class="sxs-lookup"><span data-stu-id="5d8eb-111">For example, if you use "dataWriterEvent\_" as the event handler name and the method name is "Update", the subroutine name would be dataWriterEvent\_Update.</span></span>

<span data-ttu-id="5d8eb-112">O exemplo a seguir mostra uma abordagem alternativa para conectar o manipulador de eventos ao objeto.</span><span class="sxs-lookup"><span data-stu-id="5d8eb-112">The following example shows an alternative approach to connecting the event handler to the object.</span></span>


```VB
    ' Create object and connect the event handler in one step.
    '   Set dataWriter = _
    '   WScript.CreateObject("IMAPI2.MsftDiscFormat2Data","dwBurnEvent_")


' Event handler  
SUB dwBurnEvent_Update( byRef object, byRef progress )
    '--- Other code occurs here. 
END SUB
```



<span data-ttu-id="5d8eb-113">Se um sistema contiver um segundo dispositivo de gravação para monitorar, você precisará criar outro objeto **MsftDiscFormat2Data** e manipulador de eventos.</span><span class="sxs-lookup"><span data-stu-id="5d8eb-113">If a system contains a second burn device to monitor, you would need to create another **MsftDiscFormat2Data** object and event handler.</span></span>

<span data-ttu-id="5d8eb-114">O exemplo a seguir se baseia no exemplo de [gravação de imagem de disco](burning-a-disc.md) .</span><span class="sxs-lookup"><span data-stu-id="5d8eb-114">The following example builds on the [Burning a Disc Image](burning-a-disc.md) example.</span></span> <span data-ttu-id="5d8eb-115">O exemplo grava uma imagem ISO em um disco em branco e usa um manipulador de eventos para fornecer atualizações de progresso.</span><span class="sxs-lookup"><span data-stu-id="5d8eb-115">The example writes an ISO image to a blank disc and uses an event handler to give progress updates.</span></span>


```VB
' This script burns data files to disc in a single session 
' using files from a single directory tree. 

' Copyright (C) Microsoft Corp. 2006

Option Explicit

' *** CD/DVD disc file system types
Const FsiFileSystemISO9660 = 1
Const FsiFileSystemJoliet  = 2
Const FsiFileSystemUDF102  = 4

' *** IFormat2Data Write Action Enumerations
Const IMAPI_FORMAT2_DATA_WRITE_ACTION_VALIDATING_MEDIA      = 0
Const IMAPI_FORMAT2_DATA_WRITE_ACTION_FORMATTING_MEDIA      = 1
Const IMAPI_FORMAT2_DATA_WRITE_ACTION_INITIALIZING_HARDWARE = 2
Const IMAPI_FORMAT2_DATA_WRITE_ACTION_CALIBRATING_POWER     = 3
Const IMAPI_FORMAT2_DATA_WRITE_ACTION_WRITING_DATA          = 4
Const IMAPI_FORMAT2_DATA_WRITE_ACTION_FINALIZATION          = 5
Const IMAPI_FORMAT2_DATA_WRITE_ACTION_COMPLETED             = 6
const IMAPI_FORMAT2_DATA_WRITE_ACTION_VERIFYING             = 7

WScript.Quit(Main)

Function Main
    Dim Index                ' Index to recording drive.
    Dim Recorder             ' Recorder object
    Dim Path                 ' Directory of files to burn
    Dim Stream               ' Data stream for burning device
    
    Index = 1                ' Second drive on the system
    Path = "c:\test\imt\data\2tracks"      ' Files to transfer to disc

    ' Create a DiscMaster2 object to connect to CD/DVD drives.
    Dim g_DiscMaster
    Set g_DiscMaster = WScript.CreateObject("IMAPI2.MsftDiscMaster2")

    ' Create a DiscRecorder object for the specified burning device.
    Dim uniqueId
    set recorder = WScript.CreateObject("IMAPI2.MsftDiscRecorder2")
    uniqueId = g_DiscMaster.Item(index)
    recorder.InitializeDiscRecorder( uniqueId )

    ' Create an image stream for a specified directory.
    Dim FSI                  'Disc file system
    Dim Dir                  'Root directory of the disc file system
    Dim dataWriter    
        
    ' Create a new file system image and retrieve root directory
    Set FSI = CreateObject("IMAPI2FS.MsftFileSystemImage")
    Set Dir = FSI.Root

    ' Define the new disc format and set the recorder
    Set dataWriter = CreateObject ("IMAPI2.MsftDiscFormat2Data")
    dataWriter.recorder = Recorder
    dataWriter.ClientName = "IMAPIv2 TEST"

    FSI.FreeMediaBlocks = dataWriter.FreeSectorsOnMedia
    FSI.FileSystemsToCreate = FsiFileSystemISO9660

    ' Add the directory and its contents to the file system 
    Dir.AddTree Path, false
        
    ' Create an image from the file system
    Dim result
    Set result = FSI.CreateResultImage()
    Stream = result.ImageStream
    
    ' Attach event handler to the data writing object.
    WScript.ConnectObject  dataWriter, "dwBurnEvent_"

    ' Specify the recorder and write the stream to disc.
    WScript.Echo "Writing content to disc..."
    dataWriter.write(Stream)

    WScript.Echo "----- Finished writing content -----"
    Main = 0
End Function

' Event handler - Progress updates when writing data

SUB dwBurnEvent_Update( byRef object, byRef progress )
    DIM strTimeStatus
    strTimeStatus = "Time: " & progress.ElapsedTime & _
        " / " & progress.TotalTime
   
    SELECT CASE progress.CurrentAction
    CASE IMAPI_FORMAT2_DATA_WRITE_ACTION_VALIDATING_MEDIA
        WScript.Echo "Validating media " & strTimeStatus

    CASE IMAPI_FORMAT2_DATA_WRITE_ACTION_FORMATTING_MEDIA
        WScript.Echo "Formatting media " & strTimeStatus
        
    CASE IMAPI_FORMAT2_DATA_WRITE_ACTION_INITIALIZING_HARDWARE
        WScript.Echo "Initializing Hardware " & strTimeStatus

    CASE IMAPI_FORMAT2_DATA_WRITE_ACTION_CALIBRATING_POWER
        WScript.Echo "Calibrating Power (OPC) " & strTimeStatus

    CASE IMAPI_FORMAT2_DATA_WRITE_ACTION_WRITING_DATA
        DIM totalSectors, writtenSectors, percentDone
        totalSectors = progress.SectorCount
        writtenSectors = progress.LastWrittenLba - progress.StartLba
        percentDone = FormatPercent(writtenSectors/totalSectors)
        WScript.Echo "Progress:  " & percentDone & "  " & strTimeStatus

    CASE IMAPI_FORMAT2_DATA_WRITE_ACTION_FINALIZATION
        WScript.Echo "Finishing the writing " & strTimeStatus
    
    CASE IMAPI_FORMAT2_DATA_WRITE_ACTION_COMPLETED
        WScript.Echo "Completed the burn."

    CASE IMAPI_FORMAT2_DATA_WRITE_ACTION_VERIFYING
        WScript.Echo "Verifying the data."

    CASE ELSE
        WScript.Echo "Unknown action: " & progress.CurrentAction
    END SELECT
END SUB
```



## <a name="related-topics"></a><span data-ttu-id="5d8eb-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5d8eb-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5d8eb-117">Usando o IMAPi</span><span class="sxs-lookup"><span data-stu-id="5d8eb-117">Using IMAPI</span></span>](using-imapi.md)
</dt> <dt>

[<span data-ttu-id="5d8eb-118">**IStream**</span><span class="sxs-lookup"><span data-stu-id="5d8eb-118">**IStream**</span></span>](/windows/desktop/api/objidl/nn-objidl-istream)
</dt> <dt>

[<span data-ttu-id="5d8eb-119">**IDiscMaster2**</span><span class="sxs-lookup"><span data-stu-id="5d8eb-119">**IDiscMaster2**</span></span>](/windows/desktop/api/imapi2/nn-imapi2-idiscmaster2)
</dt> <dt>

[<span data-ttu-id="5d8eb-120">**IDiscFormat2Data**</span><span class="sxs-lookup"><span data-stu-id="5d8eb-120">**IDiscFormat2Data**</span></span>](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data)
</dt> <dt>

[<span data-ttu-id="5d8eb-121">**IFileSystemImage**</span><span class="sxs-lookup"><span data-stu-id="5d8eb-121">**IFileSystemImage**</span></span>](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage)
</dt> </dl>

 

 