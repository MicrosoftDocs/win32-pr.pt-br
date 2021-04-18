---
description: O Windows 8 e o Windows Server 2012 introduzem a capacidade do software em execução em uma máquina virtual para detectar que um evento de mudança de tempo pode ter ocorrido.
ms.assetid: 0793E46B-8464-425E-8C5B-77C14DA90004
title: Identificador de geração de máquina virtual
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7df6ecbb600dbc7ae2efe14d36cb17cc75816444
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105778577"
---
# <a name="virtual-machine-generation-identifier"></a><span data-ttu-id="637e6-103">Identificador de geração de máquina virtual</span><span class="sxs-lookup"><span data-stu-id="637e6-103">Virtual machine generation identifier</span></span>

<span data-ttu-id="637e6-104">O Windows 8 e o Windows Server 2012 introduzem a capacidade do software em execução em uma máquina virtual para detectar que um evento de mudança de tempo pode ter ocorrido.</span><span class="sxs-lookup"><span data-stu-id="637e6-104">Windows 8 and Windows Server 2012 introduce the ability for software that is running on a virtual machine to detect that a time shift event may have occurred.</span></span> <span data-ttu-id="637e6-105">Eventos de turno de tempo podem ocorrer como resultado de um aplicativo de um instantâneo de máquina virtual ou da restauração de um backup de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="637e6-105">Time shift events can occur as a result of an application of a virtual machine snapshot or the restoration of a virtual machine backup.</span></span> <span data-ttu-id="637e6-106">Para obter mais informações sobre essa funcionalidade, consulte a [ID de geração de máquina Virtual White Paper](https://download.microsoft.com/download/3/1/C/31CFC307-98CA-4CA5-914C-D9772691E214/VirtualMachineGenerationID.docx).</span><span class="sxs-lookup"><span data-stu-id="637e6-106">For more information about this functionality, see the [Virtual Machine Generation ID white paper](https://download.microsoft.com/download/3/1/C/31CFC307-98CA-4CA5-914C-D9772691E214/VirtualMachineGenerationID.docx).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="637e6-107">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="637e6-107">Prerequisites</span></span>

<span data-ttu-id="637e6-108">Para usar o identificador de geração de máquina virtual de dentro de uma máquina virtual, sua máquina virtual deve estar de acordo com o seguinte.</span><span class="sxs-lookup"><span data-stu-id="637e6-108">To use the virtual machine generation identifier from inside a virtual machine your virtual machine must conform to the following.</span></span>

-   <span data-ttu-id="637e6-109">A máquina virtual deve estar em execução em um hipervisor que implemente o suporte para identificadores de geração de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="637e6-109">The virtual machine must be running on a hypervisor that implements support for virtual machine generation identifiers.</span></span> <span data-ttu-id="637e6-110">Atualmente, estes são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="637e6-110">Currently, these are the following:</span></span>
    -   <span data-ttu-id="637e6-111">Windows 8</span><span class="sxs-lookup"><span data-stu-id="637e6-111">Windows 8</span></span>
    -   <span data-ttu-id="637e6-112">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="637e6-112">Windows Server 2012</span></span>
    -   <span data-ttu-id="637e6-113">Microsoft Hyper-V Server 2012</span><span class="sxs-lookup"><span data-stu-id="637e6-113">Microsoft Hyper-V Server 2012</span></span>
-   <span data-ttu-id="637e6-114">A máquina virtual deve estar executando um sistema operacional convidado que tenha suporte para o identificador de geração de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="637e6-114">The virtual machine must be running a guest operating system that has support for the virtual machine generation identifier.</span></span> <span data-ttu-id="637e6-115">Atualmente, estes são os seguintes.</span><span class="sxs-lookup"><span data-stu-id="637e6-115">Currently, these are the following.</span></span>

    <span data-ttu-id="637e6-116">Os sistemas operacionais a seguir têm suporte nativo para o identificador de geração de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="637e6-116">The following operating systems have native support for the virtual machine generation identifier.</span></span>

    -   <span data-ttu-id="637e6-117">Windows 8</span><span class="sxs-lookup"><span data-stu-id="637e6-117">Windows 8</span></span>
    -   <span data-ttu-id="637e6-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="637e6-118">Windows Server 2012</span></span>
    -   

    <span data-ttu-id="637e6-119">A operação a seguir pode ser usada como o sistema operacional convidado se os serviços de integração do Hyper-V do Windows 8 ou do Windows Server 2012 estiverem instalados.</span><span class="sxs-lookup"><span data-stu-id="637e6-119">The following operating can be used as the guest operating system if the Hyper-V integration services from Windows 8 or Windows Server 2012 are installed.</span></span>

    -   <span data-ttu-id="637e6-120">Windows Server 2008 R2 com Service Pack 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="637e6-120">Windows Server 2008 R2 with Service Pack 1 (SP1)</span></span>
    -   <span data-ttu-id="637e6-121">Windows 7 com Service Pack 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="637e6-121">Windows 7 with Service Pack 1 (SP1)</span></span>
    -   <span data-ttu-id="637e6-122">Windows Server 2008 com Service Pack 2 (SP2)</span><span class="sxs-lookup"><span data-stu-id="637e6-122">Windows Server 2008 with Service Pack 2 (SP2)</span></span>
    -   <span data-ttu-id="637e6-123">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="637e6-123">Windows Server 2003 R2</span></span>
    -   <span data-ttu-id="637e6-124">Windows Server 2003 com Service Pack 2 (SP2)</span><span class="sxs-lookup"><span data-stu-id="637e6-124">Windows Server 2003 with Service Pack 2 (SP2)</span></span>
    -   <span data-ttu-id="637e6-125">Windows Vista com Service Pack 2 (SP2)</span><span class="sxs-lookup"><span data-stu-id="637e6-125">Windows Vista with Service Pack 2 (SP2)</span></span>
    -   <span data-ttu-id="637e6-126">Windows XP com Service Pack 3 (SP3)</span><span class="sxs-lookup"><span data-stu-id="637e6-126">Windows XP with Service Pack 3 (SP3)</span></span>

## <a name="obtaining-the-virtual-machine-generation-identifier"></a><span data-ttu-id="637e6-127">Obtendo o identificador de geração de máquina virtual</span><span class="sxs-lookup"><span data-stu-id="637e6-127">Obtaining the virtual machine generation identifier</span></span>

<span data-ttu-id="637e6-128">Para obter programaticamente o identificador de geração de máquina virtual, execute as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="637e6-128">To programmatically obtain the virtual machine generation identifier, perform the following steps.</span></span>

> [!Note]  
> <span data-ttu-id="637e6-129">O seguinte deve ser executado com privilégios de administrador ou de sistema para funcionar corretamente.</span><span class="sxs-lookup"><span data-stu-id="637e6-129">The following must be run with administrator or system privileges to function correctly.</span></span>

 

1.  <span data-ttu-id="637e6-130">Inclua o arquivo de cabeçalho "vmgenerationcounter. h" em seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="637e6-130">Include header file "vmgenerationcounter.h" in your app.</span></span> <span data-ttu-id="637e6-131">O arquivo de cabeçalho contém estas definições:</span><span class="sxs-lookup"><span data-stu-id="637e6-131">The header file contains these definitions:</span></span>
    ```C++
    DEFINE_GUID(
        GUID_DEVINTERFACE_VM_GENCOUNTER,
        0x3ff2c92b, 
        0x6598, 
        0x4e60, 
        0x8e, 
        0x1c, 
        0x0c, 
        0xcf, 
        0x49, 
        0x27, 
        0xe3, 
        0x19);

    #define VM_GENCOUNTER_SYMBOLIC_LINK_NAME L"VmGenerationCounter"

    #define IOCTL_VMGENCOUNTER_READ CTL_CODE( \
        FILE_DEVICE_ACPI, \
        0x1, METHOD_BUFFERED, \
        FILE_READ_ACCESS | FILE_WRITE_ACCESS)

    typedef struct _VM_GENCOUNTER
    {
        ULONGLONG GenerationCount;
        ULONGLONG GenerationCountHigh;
    } VM_GENCOUNTER, *PVM_GENCOUNTER;
    ```

    

2.  <span data-ttu-id="637e6-132">Abra um identificador para o " \\ \\ . \\ VmGenerationCounter "dispositivo usando a função [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) .</span><span class="sxs-lookup"><span data-stu-id="637e6-132">Open a handle to the "\\\\.\\VmGenerationCounter" device using the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function.</span></span> <span data-ttu-id="637e6-133">Como alternativa, você pode usar o Gerenciador de PnP para consumir o GUID de interface do dispositivo **\_ DEVINTERFACE \_ VM \_ GENCOUNTER** ({3ff2c92b-6598-4E60-8e1c-0ccf4927e319}).</span><span class="sxs-lookup"><span data-stu-id="637e6-133">Alternatively, you can use the PnP manager to consume the device interface **GUID\_DEVINTERFACE\_VM\_GENCOUNTER** ({3ff2c92b-6598-4e60-8e1c-0ccf4927e319}).</span></span> <span data-ttu-id="637e6-134">Esses objetos não estarão presentes se o aplicativo não estiver em execução em uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="637e6-134">These objects will not be present if the app is not running in a virtual machine.</span></span>
3.  <span data-ttu-id="637e6-135">Envie o [**IOCTL \_ VMGENCOUNTER de \_ leitura do IOCTL**](/windows/desktop/api/Vmgenerationcounter/ni-vmgenerationcounter-ioctl_vmgencounter_read) para o driver para recuperar o identificador de geração.</span><span class="sxs-lookup"><span data-stu-id="637e6-135">Send the [**IOCTL\_VMGENCOUNTER\_READ**](/windows/desktop/api/Vmgenerationcounter/ni-vmgenerationcounter-ioctl_vmgencounter_read) IOCTL to the driver to retrieve the generation identifier.</span></span>

    <span data-ttu-id="637e6-136">O IOCTL de [**\_ \_ leitura VMGENCOUNTER do IOCTL**](/windows/desktop/api/Vmgenerationcounter/ni-vmgenerationcounter-ioctl_vmgencounter_read) opera em um dos dois modos, *sondagem* e *controlado por evento*.</span><span class="sxs-lookup"><span data-stu-id="637e6-136">The [**IOCTL\_VMGENCOUNTER\_READ**](/windows/desktop/api/Vmgenerationcounter/ni-vmgenerationcounter-ioctl_vmgencounter_read) IOCTL operates in one of two modes, *polling*, and *event driven*.</span></span>

    <span data-ttu-id="637e6-137">Para emitir o IOCTL no modo de sondagem, você envia o IOCTL com um buffer de entrada de comprimento zero.</span><span class="sxs-lookup"><span data-stu-id="637e6-137">To issue the IOCTL in polling mode, you submit the IOCTL with an input buffer of zero length.</span></span> <span data-ttu-id="637e6-138">Em resposta a isso, o driver recupera o identificador de geração atual, grava-o no buffer de saída e conclui o IOCTL.</span><span class="sxs-lookup"><span data-stu-id="637e6-138">In response to this, the driver retrieves the current generation identifier, writes it to the output buffer, and completes the IOCTL.</span></span>

    <span data-ttu-id="637e6-139">Para emitir o IOCTL no modo controlado por evento, envie o IOCTL com um buffer de entrada que contém um identificador de geração existente.</span><span class="sxs-lookup"><span data-stu-id="637e6-139">To issue the IOCTL in event driven mode, submit the IOCTL with an input buffer that contains an existing generation identifier.</span></span> <span data-ttu-id="637e6-140">Em resposta a isso, o driver aguarda até que o identificador de geração atual se torne diferente do identificador de geração que foi passado.</span><span class="sxs-lookup"><span data-stu-id="637e6-140">In response to this, the driver waits until the current generation identifier becomes different from the generation identifier that was passed in.</span></span> <span data-ttu-id="637e6-141">Quando o identificador de geração é alterado, o driver grava o identificador de geração atual no buffer de saída e conclui o IOCTL.</span><span class="sxs-lookup"><span data-stu-id="637e6-141">When the generation identifier changes, the driver writes the current generation identifier to the output buffer and completes the IOCTL.</span></span>

    <span data-ttu-id="637e6-142">Em ambos os modos, o formato e o comprimento do buffer de saída são ditados pela estrutura de [**\_ GENCOUNTER da VM**](/windows/desktop/api/Vmgenerationcounter/ns-vmgenerationcounter-vm_gencounter) .</span><span class="sxs-lookup"><span data-stu-id="637e6-142">In both modes, the format and length of the output buffer is dictated by the [**VM\_GENCOUNTER**](/windows/desktop/api/Vmgenerationcounter/ns-vmgenerationcounter-vm_gencounter) structure.</span></span>

    <span data-ttu-id="637e6-143">O modo de sondagem tem suporte em todos os sistemas operacionais convidados listados acima.</span><span class="sxs-lookup"><span data-stu-id="637e6-143">Polling mode is supported on all of the guest operating systems listed above.</span></span> <span data-ttu-id="637e6-144">O modo controlado por evento tem suporte apenas no Windows Vista com SP2, Windows Server 2008 com SP2 e sistemas operacionais posteriores.</span><span class="sxs-lookup"><span data-stu-id="637e6-144">Event driven mode is supported only on Windows Vista with SP2, Windows Server 2008 with SP2, and later operating systems.</span></span> <span data-ttu-id="637e6-145">Em sistemas operacionais anteriores, o IOCTL falhará com o erro de código de erro **\_ não \_ suportado** quando emitido no modo controlado por evento.</span><span class="sxs-lookup"><span data-stu-id="637e6-145">On earlier operating systems, the IOCTL will fail with the error code **ERROR\_NOT\_SUPPORTED** when issued in event driven mode.</span></span>

    <span data-ttu-id="637e6-146">É possível que o identificador de geração mude entre o tempo que ele é recuperado pelo driver e a hora em que o IOCTL é concluído.</span><span class="sxs-lookup"><span data-stu-id="637e6-146">It is possible for the generation identifier to change between the time that it is retrieved by the driver and the time the IOCTL is completed.</span></span> <span data-ttu-id="637e6-147">Isso pode fazer com que o aplicativo cliente receba dados obsoletos.</span><span class="sxs-lookup"><span data-stu-id="637e6-147">This can result in the client app receiving stale data.</span></span> <span data-ttu-id="637e6-148">Para evitar isso, o aplicativo cliente pode usar o modo controlado por eventos para garantir que ele eventualmente aprenderá sobre todas as atualizações para o identificador de geração.</span><span class="sxs-lookup"><span data-stu-id="637e6-148">To avoid this, the client app can use event driven mode to ensure that it will eventually learn about any updates to the generation identifier.</span></span> <span data-ttu-id="637e6-149">Ao pegar o identificador atual do aplicativo cliente como entrada, o modo orientado a eventos evita possíveis condições de corrida que poderiam fazer com que o chamador perca notificações.</span><span class="sxs-lookup"><span data-stu-id="637e6-149">By taking the client app's current identifier as input, event driven mode avoids potential race conditions that would cause the caller to miss notifications.</span></span>

<span data-ttu-id="637e6-150">O exemplo de código a seguir mostra como executar as ações acima para obter o identificador de geração de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="637e6-150">The following code example shows how to perform the above actions to obtain the virtual machine generation identifier.</span></span>

> [!Note]  
> <span data-ttu-id="637e6-151">O código a seguir deve ser executado com privilégios de administrador ou de sistema para funcionar corretamente.</span><span class="sxs-lookup"><span data-stu-id="637e6-151">The following code must be run with administrator or system privileges to function correctly.</span></span>

 


```C++
HRESULT GetVmCounter(bool fWaitForChange)
{
    BOOL success = FALSE;
    DWORD error = ERROR_SUCCESS;
    VM_GENCOUNTER vmCounterOutput = {0};
    DWORD size = 0;
    HANDLE handle = INVALID_HANDLE_VALUE;
    HRESULT hr = S_OK;

    handle = CreateFile(
        L"\\\\.\\" VM_GENCOUNTER_SYMBOLIC_LINK_NAME,
        GENERIC_READ | GENERIC_WRITE,
        FILE_SHARE_READ | FILE_SHARE_WRITE,
        NULL,
        OPEN_EXISTING,
        0,
        NULL);

    if (handle == INVALID_HANDLE_VALUE)
    {
        error = GetLastError();

        wprintf(
            L"Unable to open device %s. Error code = %d.", 
            VM_GENCOUNTER_SYMBOLIC_LINK_NAME, 
            error);

        hr = HRESULT_FROM_WIN32(error);

        goto Cleanup;
    }

    /*
    Call into the driver. 

    Because the 4th parameter to DeviceIoControl (nInBufferSize) is zero, this 
    is a polling request rather than an event-driven request.
    */
    success = DeviceIoControl(
        handle,
        IOCTL_VMGENCOUNTER_READ,
        NULL,
        0,
        &vmCounterOutput,
        sizeof(vmCounterOutput),
        &size,
        NULL);

    if (!success)
    {
        error = GetLastError();

        wprintf(L"Call IOCTL_VMGENCOUNTER_READ failed with %d.", error);

        hr = HRESULT_FROM_WIN32(error);

        goto Cleanup;
    }

    wprintf(
        L"VmCounterValue: %I64x:%I64x",
        vmCounterOutput.GenerationCount,
        vmCounterOutput.GenerationCountHigh);

    if (fWaitForChange)
    {
        /*
        Call into the driver again in event-driven mode. DeviceIoControl won't 
        return until the generation identifier has changed.
        */
        success = DeviceIoControl(
            handle,
            IOCTL_VMGENCOUNTER_READ,
            &vmCounterOutput,
            sizeof(vmCounterOutput),
            &vmCounterOutput,
            sizeof(vmCounterOutput),
            &size,
            NULL);

        if (!success)
        {
            error = GetLastError();

            wprintf(L"Call IOCTL_VMGENCOUNTER_READ failed with %d.", error);

            hr = HRESULT_FROM_WIN32(error);

            goto Cleanup;
        }

        wprintf(
            L"VmCounterValue changed to: %I64x:%I64x",
            vmCounterOutput.GenerationCount,
            vmCounterOutput.GenerationCountHigh);
    }

Cleanup:

    if (handle != INVALID_HANDLE_VALUE)
    {
        CloseHandle(handle);
    }

    return hr;
};
```



## <a name="determining-if-a-time-shift-event-has-occurred"></a><span data-ttu-id="637e6-152">Determinando se ocorreu um evento de mudança de tempo</span><span class="sxs-lookup"><span data-stu-id="637e6-152">Determining if a time shift event has occurred</span></span>

<span data-ttu-id="637e6-153">Depois de obter o identificador de geração de máquina virtual, você deve armazená-lo para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="637e6-153">After you have obtained the virtual machine generation identifier, you should store it for future use.</span></span> <span data-ttu-id="637e6-154">Antes que seu aplicativo execute uma operação sensível ao tempo, como a confirmação para um banco de dados, você deve obter novamente o identificador de geração e compará-lo com o valor armazenado.</span><span class="sxs-lookup"><span data-stu-id="637e6-154">Before your app performs a time-sensitive operation, such as committing to a database, you should re-obtain the generation identifier and compare it to the stored value.</span></span> <span data-ttu-id="637e6-155">Se o identificador foi alterado, isso significa que um evento de mudança de tempo ocorreu e seu aplicativo deve agir adequadamente.</span><span class="sxs-lookup"><span data-stu-id="637e6-155">If the identifier has changed, that means that a time shift event has occurred, and your app must act appropriately.</span></span>

 

 
