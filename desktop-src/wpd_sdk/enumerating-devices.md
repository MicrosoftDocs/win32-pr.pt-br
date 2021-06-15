---
title: Enumerando dispositivos (WPD)
description: Saiba como um aplicativo enumera dispositivos usando a função EnumerateAllDevices, que obtém uma contagem de dispositivos conectados e informações específicas do dispositivo.
ms.assetid: 28ded3cf-b0c8-4c90-ab39-efc879adb6e7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6465b04e6f1a18a0bdb74f0ce883cf9161371fb6
ms.sourcegitcommit: 51ef825fb48f15e1aa30e8795988f10dc2b2155c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/14/2021
ms.locfileid: "112068592"
---
# <a name="enumerating-devices-wpd"></a><span data-ttu-id="ab13b-103">Enumerando dispositivos (WPD)</span><span class="sxs-lookup"><span data-stu-id="ab13b-103">Enumerating devices (WPD)</span></span>

<span data-ttu-id="ab13b-104">A primeira tarefa concluída pela maioria dos aplicativos é a enumeração dos dispositivos conectados ao computador.</span><span class="sxs-lookup"><span data-stu-id="ab13b-104">The first task completed by most applications is the enumeration of the devices connected to the computer.</span></span> <span data-ttu-id="ab13b-105">Essa tarefa e a recuperação de informações do dispositivo (como fabricante, nome amigável e descrição) são suportadas pela interface [**IPortableDeviceManager**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager) .</span><span class="sxs-lookup"><span data-stu-id="ab13b-105">This task, and the retrieval of device information (such as manufacturer, friendly name, and description), is supported by the [**IPortableDeviceManager**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager) interface.</span></span>

<span data-ttu-id="ab13b-106">A função EnumerateAllDevices no módulo DeviceEnumeration. cpp contém código que demonstra a recuperação da contagem de dispositivos conectados e, depois que a contagem é recuperada, a recuperação de informações específicas do dispositivo para cada dispositivo conectado.</span><span class="sxs-lookup"><span data-stu-id="ab13b-106">The EnumerateAllDevices function in the DeviceEnumeration.cpp module contains code that demonstrates the retrieval of the count of connected devices and, once the count is retrieved, the retrieval of device-specific information for each connected device.</span></span>

<span data-ttu-id="ab13b-107">A função EnumerateAllDevices realiza quatro tarefas principais:</span><span class="sxs-lookup"><span data-stu-id="ab13b-107">The EnumerateAllDevices function accomplishes four primary tasks:</span></span>

1.  <span data-ttu-id="ab13b-108">Cria o objeto do Gerenciador de dispositivos portátil.</span><span class="sxs-lookup"><span data-stu-id="ab13b-108">Creates the portable device manager object.</span></span>
2.  <span data-ttu-id="ab13b-109">Recupera uma contagem de dispositivos conectados.</span><span class="sxs-lookup"><span data-stu-id="ab13b-109">Retrieves a count of connected devices.</span></span>
3.  <span data-ttu-id="ab13b-110">Recupera informações do dispositivo (para os dispositivos conectados).</span><span class="sxs-lookup"><span data-stu-id="ab13b-110">Retrieves device information (for the connected devices).</span></span>
4.  <span data-ttu-id="ab13b-111">Libera a memória usada ao recuperar as informações do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ab13b-111">Frees the memory used when retrieving the device information.</span></span>

<span data-ttu-id="ab13b-112">Cada uma dessas quatro tarefas é descrita mais detalhadamente nas seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="ab13b-112">Each of these four tasks is described in more detail in the following sections.</span></span>

<span data-ttu-id="ab13b-113">A primeira etapa no processo de enumeração do dispositivo é a criação de um objeto do Gerenciador de dispositivos portátil.</span><span class="sxs-lookup"><span data-stu-id="ab13b-113">The first step in the device enumeration process is the creation of a portable device manager object.</span></span> <span data-ttu-id="ab13b-114">Isso é feito chamando a função CoCreateInstance e passando o identificador de classe (CLSID) para o objeto, especificando o contexto no qual o código será executado, especificando um identificador de referência para a interface IPortableDeviceManager e, em seguida, fornecendo uma variável de ponteiro que recebe o ponteiro de interface IPortableDeviceManager.</span><span class="sxs-lookup"><span data-stu-id="ab13b-114">This is done by calling the CoCreateInstance function and passing the class identifier (CLSID) for the object, specifying the context in which the code will run, specifying a reference identifier for the IPortableDeviceManager interface, and then supplying a pointer variable that receives the IPortableDeviceManager interface pointer.</span></span>


```C++
HRESULT hr = CoCreateInstance(CLSID_PortableDeviceManager,
                              NULL,
                              CLSCTX_INPROC_SERVER,
                              IID_PPV_ARGS(&pPortableDeviceManager));
if (FAILED(hr))
{
    printf("! Failed to CoCreateInstance CLSID_PortableDeviceManager, hr = 0x%lx\n",hr);
}
```



<span data-ttu-id="ab13b-115">Depois de obter um ponteiro de interface [**IPortableDeviceManager**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager) , você pode começar a chamar métodos nessa interface.</span><span class="sxs-lookup"><span data-stu-id="ab13b-115">Once you obtain an [**IPortableDeviceManager**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager) interface pointer, you can begin calling methods on this interface.</span></span> <span data-ttu-id="ab13b-116">O primeiro método chamado na função EnumerateAllDevices é [**IPortableDeviceManager:: Devices**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicemanager-getdevices).</span><span class="sxs-lookup"><span data-stu-id="ab13b-116">The first method called in the EnumerateAllDevices function is [**IPortableDeviceManager::GetDevices**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicemanager-getdevices).</span></span> <span data-ttu-id="ab13b-117">Quando esse método é chamado com o primeiro argumento definido como **NULL**, ele retorna a contagem de dispositivos conectados.</span><span class="sxs-lookup"><span data-stu-id="ab13b-117">When this method is called with the first argument set to **NULL**, it returns the count of connected devices.</span></span>


```C++
if (SUCCEEDED(hr))
{
    hr = pPortableDeviceManager->GetDevices(NULL, &cPnPDeviceIDs);
    if (FAILED(hr))
    {
        printf("! Failed to get number of devices on the system, hr = 0x%lx\n",hr);
    }
}

// Report the number of devices found.  NOTE: we will report 0, if an error
// occured.

printf("\n%d Windows Portable Device(s) found on the system\n\n", cPnPDeviceIDs);
```



<span data-ttu-id="ab13b-118">Depois de recuperar a contagem de dispositivos conectados, você pode usar esse valor para recuperar informações de dispositivo para cada dispositivo conectado.</span><span class="sxs-lookup"><span data-stu-id="ab13b-118">After you have retrieved the count of connected devices, you can use this value to retrieve device information for each connected device.</span></span> <span data-ttu-id="ab13b-119">Esse processo começa passando uma matriz de ponteiros de cadeia de caracteres como o primeiro argumento e uma contagem do número de elementos que essa matriz pode conter como o segundo argumento (essa contagem deve ser, pelo menos, igual ao número de dispositivos disponíveis).</span><span class="sxs-lookup"><span data-stu-id="ab13b-119">This process begins by passing an array of string pointers as the first argument and a count of the number of elements that this array can hold as the second argument (this count should at least be equal to the number of available devices).</span></span>

<span data-ttu-id="ab13b-120">As cadeias de caracteres retornadas por esse método são os nomes Plug and Play dos dispositivos conectados.</span><span class="sxs-lookup"><span data-stu-id="ab13b-120">The strings returned by this method are the Plug and Play names of the connected devices.</span></span> <span data-ttu-id="ab13b-121">Esses nomes, por sua vez, são passados para outros métodos na interface [**IPortableDeviceManager**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager) para recuperar informações específicas do dispositivo, como o nome amigável, o nome do fabricante e a descrição do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ab13b-121">These names, in turn, are passed to other methods on the [**IPortableDeviceManager**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager) interface to retrieve device-specific information such as the friendly name, the manufacturer's name, and the device description.</span></span> <span data-ttu-id="ab13b-122">(Esses nomes também são usados para abrir uma conexão com o dispositivo quando um aplicativo chama o método [**IPortableDevice:: Open**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open) .)</span><span class="sxs-lookup"><span data-stu-id="ab13b-122">(These names are also used to open a connection to the device when an application calls the [**IPortableDevice::Open**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open) method.)</span></span>


```C++
if (SUCCEEDED(hr) && (cPnPDeviceIDs > 0))
{
    pPnpDeviceIDs = new (std::nothrow) PWSTR[cPnPDeviceIDs];
    if (pPnpDeviceIDs != NULL)
    {
        DWORD dwIndex = 0;

        hr = pPortableDeviceManager->GetDevices(pPnpDeviceIDs, &cPnPDeviceIDs);
        if (SUCCEEDED(hr))
        {
            // For each device found, display the devices friendly name,
            // manufacturer, and description strings.
            for (dwIndex = 0; dwIndex < cPnPDeviceIDs; dwIndex++)
            {
                printf("[%d] ", dwIndex);
                DisplayFriendlyName(pPortableDeviceManager, pPnpDeviceIDs[dwIndex]);
                printf("    ");
                DisplayManufacturer(pPortableDeviceManager, pPnpDeviceIDs[dwIndex]);
                printf("    ");
                DisplayDescription(pPortableDeviceManager, pPnpDeviceIDs[dwIndex]);
            }
        }
        else
        {
            printf("! Failed to get the device list from the system, hr = 0x%lx\n",hr);
        }
```



<span data-ttu-id="ab13b-123">Depois de recuperar as informações do dispositivo, você precisará liberar a memória associada às cadeias de caracteres apontadas pela matriz de ponteiros de cadeia.</span><span class="sxs-lookup"><span data-stu-id="ab13b-123">Once you've retrieved the device information, you will need to free the memory associated with the strings pointed to by the array of string pointers.</span></span> <span data-ttu-id="ab13b-124">Também será necessário excluir essa matriz.</span><span class="sxs-lookup"><span data-stu-id="ab13b-124">You will also need to delete this array.</span></span>


```C++
for (dwIndex = 0; dwIndex < cPnPDeviceIDs; dwIndex++)
{
    CoTaskMemFree(pPnpDeviceIDs[dwIndex]);
    pPnpDeviceIDs[dwIndex] = NULL;
}

// Delete the array of PWSTR pointers
delete [] pPnpDeviceIDs;
pPnpDeviceIDs = NULL;
```



## <a name="related-topics"></a><span data-ttu-id="ab13b-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ab13b-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ab13b-126">**Interface IPortableDeviceManager**</span><span class="sxs-lookup"><span data-stu-id="ab13b-126">**IPortableDeviceManager Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager)
</dt> <dt>

[<span data-ttu-id="ab13b-127">**Guia de programação**</span><span class="sxs-lookup"><span data-stu-id="ab13b-127">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 



