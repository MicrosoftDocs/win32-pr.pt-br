---
title: Trabalhando com dispositivos portáteis
description: Trabalhando com dispositivos portáteis
ms.assetid: 145ede07-a23b-486b-a561-9c87a48b72a8
keywords:
- Windows Media Player, dispositivos portáteis
- Modelo de objeto do Windows Media Player, dispositivos portáteis
- modelo de objeto, dispositivos portáteis
- Controle ActiveX do Windows Media Player, dispositivos portáteis
- Controle ActiveX, dispositivos portáteis
- Controle ActiveX móvel do Windows Media Player, dispositivos portáteis
- Windows Media Player Mobile, dispositivos portáteis
- dispositivos portáteis, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b64c6e7047864b899a2d7dca2ba4754cc7cb5dc2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292784"
---
# <a name="working-with-portable-devices"></a><span data-ttu-id="f9f4e-111">Trabalhando com dispositivos portáteis</span><span class="sxs-lookup"><span data-stu-id="f9f4e-111">Working with Portable Devices</span></span>

<span data-ttu-id="f9f4e-112">Esta seção descreve como usar um controle ActiveX do Windows Media Player remoto para trabalhar com dispositivos portáteis.</span><span class="sxs-lookup"><span data-stu-id="f9f4e-112">This section describes how to use a remoted Windows Media Player ActiveX control to work with portable devices.</span></span>

<span data-ttu-id="f9f4e-113">Os exemplos de código nesta seção usam classes Active Template Library (ATL), como **CComPtr**.</span><span class="sxs-lookup"><span data-stu-id="f9f4e-113">The code examples in this section use Active Template Library (ATL) classes, such as **CComPtr**.</span></span>

## <a name="included-headers"></a><span data-ttu-id="f9f4e-114">Cabeçalhos incluídos</span><span class="sxs-lookup"><span data-stu-id="f9f4e-114">Included Headers</span></span>

<span data-ttu-id="f9f4e-115">Para usar o código nesta seção, inclua os seguintes cabeçalhos:</span><span class="sxs-lookup"><span data-stu-id="f9f4e-115">To use the code in this section, include the following headers:</span></span>


```C++
#include <atlbase.h>
#include <atlcom.h>
#include <atlwin.h>
#include <commctrl.h>
#include "wmp.h"
#include "wmpids.h"
```



## <a name="iwmpplayer-pointer"></a><span data-ttu-id="f9f4e-116">Ponteiro IWMPPlayer</span><span class="sxs-lookup"><span data-stu-id="f9f4e-116">IWMPPlayer Pointer</span></span>

<span data-ttu-id="f9f4e-117">O ponteiro **IWMPPlayer** é armazenado em uma variável de membro.</span><span class="sxs-lookup"><span data-stu-id="f9f4e-117">The **IWMPPlayer** pointer is stored in a member variable.</span></span>


```C++
CComPtr<IWMPPlayer> m_spPlayer;
```



## <a name="devices-are-stored-in-an-array"></a><span data-ttu-id="f9f4e-118">Os dispositivos são armazenados em uma matriz</span><span class="sxs-lookup"><span data-stu-id="f9f4e-118">Devices are Stored in an Array</span></span>

<span data-ttu-id="f9f4e-119">O código de exemplo acessa a seguinte variável de membro, a ser declarada no cabeçalho do projeto:</span><span class="sxs-lookup"><span data-stu-id="f9f4e-119">The example code accesses the following member variable, to be declared in the project header:</span></span>


```C++
IWMPSyncDevice **m_ppWMPDevices; // Points to the custom device array.
```



<span data-ttu-id="f9f4e-120">A contagem de dispositivos é armazenada em uma variável de membro.</span><span class="sxs-lookup"><span data-stu-id="f9f4e-120">The device count is stored in a member variable.</span></span>


```C++
int m_cDevices; // Count of devices.
```



## <a name="retrieving-a-device-pointer"></a><span data-ttu-id="f9f4e-121">Recuperando um ponteiro de dispositivo</span><span class="sxs-lookup"><span data-stu-id="f9f4e-121">Retrieving a Device Pointer</span></span>

<span data-ttu-id="f9f4e-122">Um ponteiro para um dispositivo específico é recuperado por meio de seu índice de matriz usando um código semelhante ao seguinte:</span><span class="sxs-lookup"><span data-stu-id="f9f4e-122">A pointer to a particular device is retrieved through its array index by using code similar to the following:</span></span>


```C++
CComPtr<IWMPSyncDevice> spSyncDevice(m_ppWMPDevices[lIndex]);
```



<span data-ttu-id="f9f4e-123">Observe que o índice mostrado nos exemplos anteriores não é o índice de parceria para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f9f4e-123">Note that the index shown in the preceding examples is not the partnership index for the device.</span></span> <span data-ttu-id="f9f4e-124">É o índice para o dispositivo na matriz personalizada de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="f9f4e-124">It is the index to the device in the custom array of devices.</span></span>

## <a name="cleaning-up"></a><span data-ttu-id="f9f4e-125">Limpeza</span><span class="sxs-lookup"><span data-stu-id="f9f4e-125">Cleaning Up</span></span>

<span data-ttu-id="f9f4e-126">Os exemplos usam a seguinte função para liberar a memória na matriz de dispositivo e para liberar os ponteiros de interface:</span><span class="sxs-lookup"><span data-stu-id="f9f4e-126">The examples use the following function to free the memory in the device array and to release the interface pointers:</span></span>


```C++
void CMainDlg::FreeDeviceArray()
{
    if(m_ppWMPDevices)
    {
        for(long i = 0; i < m_cDevices; i++)
        {
            m_ppWMPDevices[i]->Release();
        }
 
        delete[] m_ppWMPDevices;
        m_ppWMPDevices = NULL;        
    }
}
```



## <a name="devices-are-displayed-in-a-list-box"></a><span data-ttu-id="f9f4e-127">Os dispositivos são exibidos em uma caixa de listagem</span><span class="sxs-lookup"><span data-stu-id="f9f4e-127">Devices are Displayed in a List Box</span></span>

<span data-ttu-id="f9f4e-128">A função GetSelectedDeviceIndex retorna o índice do dispositivo selecionado pelo usuário em uma caixa de listagem usando o seguinte código:</span><span class="sxs-lookup"><span data-stu-id="f9f4e-128">The GetSelectedDeviceIndex function returns the index of the device the user selected in a list box by using the following code:</span></span>


```C++
long CMainDlg::GetSelectedDeviceIndex()
{
    return (long)SendMessage(GetDlgItem(IDC_DEVICES), LB_GETCURSEL, 0, 0);
}
```



## <a name="user-interface-state-is-managed-by-a-single-function"></a><span data-ttu-id="f9f4e-129">O estado da interface do usuário é gerenciado por uma única função</span><span class="sxs-lookup"><span data-stu-id="f9f4e-129">User Interface State is Managed by a Single Function</span></span>

<span data-ttu-id="f9f4e-130">A função SetUIState gerencia a interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="f9f4e-130">The SetUIState function manages the user interface.</span></span>


```C++
SetUIState(UIState 
NewState, BOOL 
bConnected)
```



<span data-ttu-id="f9f4e-131">Os detalhes dessa função não são relevantes para as discussões nesta seção, mas lembre-se de que essa função executa tarefas como habilitar ou desabilitar controles e alterar o texto de exibição na interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="f9f4e-131">The details of this function are not relevant to the discussions in this section, but be aware that this function performs tasks like enabling or disabling controls and changing display text in the user interface.</span></span>

<span data-ttu-id="f9f4e-132">A enumeração UIState foi definida da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="f9f4e-132">The UIState enumeration was defined as follows:</span></span>


```C++
enum UIState
{
    Partnership,
    NoPartnership,
    Synchronizing
};
```



<span data-ttu-id="f9f4e-133">O parâmetro *bConnected* especifica se a interface do usuário deve ser configurada para um dispositivo conectado (true significa que o dispositivo está conectado).</span><span class="sxs-lookup"><span data-stu-id="f9f4e-133">The *bConnected* parameter specifies whether to configure the user interface for a connected device (TRUE means the device is connected).</span></span> <span data-ttu-id="f9f4e-134">Os parâmetros *NewState* e *bConnected* transmitem as informações necessárias para que a função faça seu trabalho.</span><span class="sxs-lookup"><span data-stu-id="f9f4e-134">The *NewState* and *bConnected* parameters convey the information needed for the function to do its work.</span></span>

<span data-ttu-id="f9f4e-135">As seções a seguir fornecem explicações sobre o código de exemplo:</span><span class="sxs-lookup"><span data-stu-id="f9f4e-135">The following sections provide explanations of the example code:</span></span>

-   [<span data-ttu-id="f9f4e-136">Enumerando dispositivos</span><span class="sxs-lookup"><span data-stu-id="f9f4e-136">Enumerating Devices</span></span>](enumerating-devices.md)
-   [<span data-ttu-id="f9f4e-137">Recuperando atributos do dispositivo</span><span class="sxs-lookup"><span data-stu-id="f9f4e-137">Retrieving Device Attributes</span></span>](retrieving-device-attributes.md)
-   [<span data-ttu-id="f9f4e-138">Mostrando o progresso da sincronização</span><span class="sxs-lookup"><span data-stu-id="f9f4e-138">Showing Synchronization Progress</span></span>](showing-synchronization-progress.md)
-   [<span data-ttu-id="f9f4e-139">Gerenciando listas de reprodução de sincronização</span><span class="sxs-lookup"><span data-stu-id="f9f4e-139">Managing Synchronization Playlists</span></span>](managing-synchronization-playlists.md)

## <a name="related-topics"></a><span data-ttu-id="f9f4e-140">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f9f4e-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f9f4e-141">**Guia de controle do Player**</span><span class="sxs-lookup"><span data-stu-id="f9f4e-141">**Player Control Guide**</span></span>](player-control-guide.md)
</dt> </dl>

 

 




