---
description: Windows 8 e Windows Server 2012 introduzem a capacidade do software em execução em uma máquina virtual de detectar que um evento de deslocamento de tempo pode ter ocorrido.
ms.assetid: 0793E46B-8464-425E-8C5B-77C14DA90004
title: Identificador de geração de máquina virtual
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d810a1a65e95f4dde0ccf9779b1e955f2630623e362ffbf94ab8ca36d51d116e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119899006"
---
# <a name="virtual-machine-generation-identifier"></a>Identificador de geração de máquina virtual

Windows 8 e Windows Server 2012 introduzem a capacidade do software em execução em uma máquina virtual de detectar que um evento de deslocamento de tempo pode ter ocorrido. Eventos de deslocamento de tempo podem ocorrer como resultado de um aplicativo de um instantâneo de máquina virtual ou da restauração de um backup de máquina virtual. Para obter mais informações sobre essa funcionalidade, consulte a [ID](https://download.microsoft.com/download/3/1/C/31CFC307-98CA-4CA5-914C-D9772691E214/VirtualMachineGenerationID.docx)de Geração de Máquina Virtual white paper .

## <a name="prerequisites"></a>Pré-requisitos

Para usar o identificador de geração de máquina virtual de dentro de uma máquina virtual, sua máquina virtual deve estar em conformidade com o seguinte.

-   A máquina virtual deve estar em execução em um hipervisor que implementa suporte para identificadores de geração de máquina virtual. Atualmente, estes são os seguintes:
    -   Windows 8
    -   Windows Server 2012
    -   Microsoft Hyper-V Server 2012
-   A máquina virtual deve estar executando um sistema operacional convidado que tenha suporte para o identificador de geração de máquina virtual. Atualmente, esses são os seguintes.

    Os sistemas operacionais a seguir têm suporte nativo para o identificador de geração de máquina virtual.

    -   Windows 8
    -   Windows Server 2012
    -   

    A operação a seguir poderá ser usada como o sistema operacional convidado se os serviços de integração do Hyper-V Windows 8 ou Windows Server 2012 estão instalados.

    -   Windows Server 2008 R2 com Service Pack 1 (SP1)
    -   Windows 7 com Service Pack 1 (SP1)
    -   Windows Server 2008 com Service Pack 2 (SP2)
    -   Windows Server 2003 R2
    -   Windows Server 2003 com Service Pack 2 (SP2)
    -   Windows Vista com Service Pack 2 (SP2)
    -   Windows XP com Service Pack 3 (SP3)

## <a name="obtaining-the-virtual-machine-generation-identifier"></a>Obtendo o identificador de geração de máquina virtual

Para obter programaticamente o identificador de geração de máquina virtual, execute as etapas a seguir.

> [!Note]  
> O seguinte deve ser executado com privilégios de administrador ou sistema para funcionar corretamente.

 

1.  Inclua o arquivo de header "vmgenerationcounter.h" em seu aplicativo. O arquivo de header contém estas definições:
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

    

2.  Abra um alça para o " \\ \\ . \\ Dispositivo VmGenerationCounter" usando a [**função CreateFile.**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) Como alternativa, você pode usar o gerenciador pnP para consumir o GUID da interface do dispositivo **\_ DEVINTERFACE \_ VM \_ GENCOUNTER** ({3ff2c92b-6598-4e60-8e1c-0ccf4927e319}). Esses objetos não estarão presentes se o aplicativo não estiver em execução em uma máquina virtual.
3.  Envie o [**IOCTL IOCTL DE LEITURA de \_ VMGENCOUNTER \_**](/windows/desktop/api/Vmgenerationcounter/ni-vmgenerationcounter-ioctl_vmgencounter_read) para o driver para recuperar o identificador de geração.

    O [**IOCTL DE LEITURA DE \_ VMGENCOUNTER \_**](/windows/desktop/api/Vmgenerationcounter/ni-vmgenerationcounter-ioctl_vmgencounter_read) IOCTL opera em um dos dois modos, *sondando* e orientado *a eventos.*

    Para emitir o IOCTL no modo de sondagem, envie o IOCTL com um buffer de entrada de comprimento zero. Em resposta a isso, o driver recupera o identificador de geração atual, grava-o no buffer de saída e conclui o IOCTL.

    Para emitir o IOCTL no modo orientado por eventos, envie o IOCTL com um buffer de entrada que contém um identificador de geração existente. Em resposta a isso, o driver aguarda até que o identificador de geração atual se torne diferente do identificador de geração que foi passado. Quando o identificador de geração muda, o driver grava o identificador de geração atual no buffer de saída e conclui o IOCTL.

    Em ambos os modos, o formato e o comprimento do buffer de saída são ditados pela estrutura [**\_ GENCOUNTER da VM.**](/windows/desktop/api/Vmgenerationcounter/ns-vmgenerationcounter-vm_gencounter)

    O modo de sondagem tem suporte em todos os sistemas operacionais convidados listados acima. O modo orientado a eventos tem suporte apenas no Windows Vista com SP2, Windows Server 2008 com SP2 e sistemas operacionais posteriores. Em sistemas operacionais anteriores, o IOCTL falhará com o código de erro **ERROR \_ NOT \_ SUPPORTED** quando emitido no modo orientado por eventos.

    É possível que o identificador de geração altere entre o momento em que ele é recuperado pelo driver e a hora em que o IOCTL é concluído. Isso pode fazer com que o aplicativo cliente receba dados stale. Para evitar isso, o aplicativo cliente pode usar o modo orientado a eventos para garantir que ele acabará aprendendo sobre as atualizações do identificador de geração. Ao levar o identificador atual do aplicativo cliente como entrada, o modo orientado por eventos evita possíveis condições de corrida que faria com que o chamador perca notificações.

O exemplo de código a seguir mostra como executar as ações acima para obter o identificador de geração de máquina virtual.

> [!Note]  
> O código a seguir deve ser executado com privilégios de administrador ou sistema para funcionar corretamente.

 


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



## <a name="determining-if-a-time-shift-event-has-occurred"></a>Determinando se ocorreu um evento de deslocamento de tempo

Depois de obter o identificador de geração de máquina virtual, armazene-o para uso futuro. Antes que seu aplicativo execute uma operação sensível ao tempo, como a confirmação de um banco de dados, você deve obter o identificador de geração e compará-lo com o valor armazenado. Se o identificador tiver sido alterado, isso significa que ocorreu um evento de deslocamento de tempo e seu aplicativo deve agir adequadamente.

 

 
