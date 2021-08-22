---
title: Enumerando dispositivos (WPD)
description: Saiba como um aplicativo enumera dispositivos usando a função EnumerateAllDevices, que obtém uma contagem de dispositivos conectados e informações específicas do dispositivo.
ms.assetid: 28ded3cf-b0c8-4c90-ab39-efc879adb6e7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6cfe1c1b4dee11383a4c36eaea43974f7e0439ae4ff2370a90e99b1702a8e0d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119083570"
---
# <a name="enumerating-devices-wpd"></a>Enumerando dispositivos (WPD)

A primeira tarefa concluída pela maioria dos aplicativos é a enumeração dos dispositivos conectados ao computador. Essa tarefa e a recuperação de informações do dispositivo (como fabricante, nome amigável e descrição) são suportadas pela interface [**IPortableDeviceManager**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager) .

A função EnumerateAllDevices no módulo DeviceEnumeration. cpp contém código que demonstra a recuperação da contagem de dispositivos conectados e, depois que a contagem é recuperada, a recuperação de informações específicas do dispositivo para cada dispositivo conectado.

A função EnumerateAllDevices realiza quatro tarefas principais:

1.  Cria o objeto do Gerenciador de dispositivos portátil.
2.  Recupera uma contagem de dispositivos conectados.
3.  Recupera informações do dispositivo (para os dispositivos conectados).
4.  Libera a memória usada ao recuperar as informações do dispositivo.

Cada uma dessas quatro tarefas é descrita mais detalhadamente nas seções a seguir.

A primeira etapa no processo de enumeração do dispositivo é a criação de um objeto do Gerenciador de dispositivos portátil. Isso é feito chamando a função CoCreateInstance e passando o identificador de classe (CLSID) para o objeto, especificando o contexto no qual o código será executado, especificando um identificador de referência para a interface IPortableDeviceManager e, em seguida, fornecendo uma variável de ponteiro que recebe o ponteiro de interface IPortableDeviceManager.


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



Depois de obter um ponteiro de interface [**IPortableDeviceManager**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager) , você pode começar a chamar métodos nessa interface. O primeiro método chamado na função EnumerateAllDevices é [**IPortableDeviceManager:: Devices**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicemanager-getdevices). Quando esse método é chamado com o primeiro argumento definido como **NULL**, ele retorna a contagem de dispositivos conectados.


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



Depois de recuperar a contagem de dispositivos conectados, você pode usar esse valor para recuperar informações de dispositivo para cada dispositivo conectado. Esse processo começa passando uma matriz de ponteiros de cadeia de caracteres como o primeiro argumento e uma contagem do número de elementos que essa matriz pode conter como o segundo argumento (essa contagem deve ser, pelo menos, igual ao número de dispositivos disponíveis).

As cadeias de caracteres retornadas por esse método são os nomes Plug and Play dos dispositivos conectados. Esses nomes, por sua vez, são passados para outros métodos na interface [**IPortableDeviceManager**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager) para recuperar informações específicas do dispositivo, como o nome amigável, o nome do fabricante e a descrição do dispositivo. (Esses nomes também são usados para abrir uma conexão com o dispositivo quando um aplicativo chama o método [**IPortableDevice:: Open**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open) .)


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



Depois de recuperar as informações do dispositivo, você precisará liberar a memória associada às cadeias de caracteres apontadas pela matriz de ponteiros de cadeia. Também será necessário excluir essa matriz.


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



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Interface IPortableDeviceManager**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager)
</dt> <dt>

[**Guia de programação**](programming-guide.md)
</dt> </dl>

 

 



