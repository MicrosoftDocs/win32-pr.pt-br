---
description: Descreve os processos para implementar manipuladores de eventos de dispositivo no registro.
ms.assetid: 84B12B5C-C179-4124-A1FC-B90D120336BF
title: Como registrar um manipulador para um evento de dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34ef15071b349afa3f863e7c57b64c280c2aef8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828289"
---
# <a name="how-to-register-a-handler-for-a-device-event"></a><span data-ttu-id="e9535-103">Como registrar um manipulador para um evento de dispositivo</span><span class="sxs-lookup"><span data-stu-id="e9535-103">How to Register a Handler for a Device Event</span></span>

<span data-ttu-id="e9535-104">Os manipuladores definem a parte do software da reprodução automática.</span><span class="sxs-lookup"><span data-stu-id="e9535-104">Handlers define the software portion of AutoPlay.</span></span> <span data-ttu-id="e9535-105">Eles definem o ícone do software e o nome amigável, bem como o componente de Component Object Model (COM) para instanciar e como inicializar o componente em resposta a um evento.</span><span class="sxs-lookup"><span data-stu-id="e9535-105">They define the software's icon and friendly name, as well as the Component Object Model (COM) component to instantiate and how to initialize the component in response to an event.</span></span> <span data-ttu-id="e9535-106">Cada manipulador de um evento específico é registrado como um valor na chave **EventHandler** apropriada.</span><span class="sxs-lookup"><span data-stu-id="e9535-106">Each handler for a specific event registers as a value under the appropriate **EventHandler** key.</span></span> <span data-ttu-id="e9535-107">Quando esse evento é detectado, o usuário é solicitado a escolher um manipulador de uma lista de todos os manipuladores registrados para esse evento.</span><span class="sxs-lookup"><span data-stu-id="e9535-107">When that event is detected, the user is prompted to choose a handler from a list of all the handlers registered for that event.</span></span>

## <a name="instructions"></a><span data-ttu-id="e9535-108">Instruções</span><span class="sxs-lookup"><span data-stu-id="e9535-108">Instructions</span></span>


<span data-ttu-id="e9535-109">Os manipuladores e seus valores associados são definidos sob a chave de \\ **manipuladores** AutoplayHandlers.</span><span class="sxs-lookup"><span data-stu-id="e9535-109">Handlers and their associated values are defined under the **AutoplayHandlers**\\**Handlers** key.</span></span> <span data-ttu-id="e9535-110">As subchaves diferem dependendo se o sistema pode ler o conteúdo do dispositivo diretamente ou se o dispositivo fornece conteúdo ao sistema por meio de uma interface proprietária.</span><span class="sxs-lookup"><span data-stu-id="e9535-110">Subkeys differ depending on whether the system can read device contents directly or whether the device provides contents to the system through a proprietary interface.</span></span>

<span data-ttu-id="e9535-111">O exemplo a seguir mostra as subchaves e os valores que são usados para um dispositivo, como uma câmera de vídeo digital ou um player de MP3, que fornece seu conteúdo ao sistema por meio de uma interface proprietária.</span><span class="sxs-lookup"><span data-stu-id="e9535-111">The following example shows the subkeys and values that are used for a device, such as a digital video camera or .mp3 player, that provides its contents to the system through a proprietary interface.</span></span> <span data-ttu-id="e9535-112">O manipulador de exemplo é chamado de **MyHandler**.</span><span class="sxs-lookup"><span data-stu-id="e9535-112">The example handler is called **MyHandler**.</span></span>

```
HKEY_LOCAL_MACHINE or HKEY_CURRENT_USER
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  AutoplayHandlers
                     Handlers
                        MyHandler
                           Action [REG_SZ] = Play music
                           CLSID [REG_SZ] = {a51f2ed3-634e-4a97-9d55-efcf08e7b32f}
                           DefaultIcon [REG_EXPAND_SZ] = %ProgramFiles%\Windows Media Player\wmplayer.exe,0
                           InitCmdLine [REG_SZ] = /Play
                           ProgID [REG_SZ] = WMP.PlayMusicFiles
                           Provider [REG_SZ] = Windows Media Player
```

> [!Note]  
> <span data-ttu-id="e9535-113">Embora o exemplo mostre um ProgID e um valor de identificador de classe (CLSID), na prática, esses valores são mutuamente exclusivos para que apenas um ou outro esteja presente.</span><span class="sxs-lookup"><span data-stu-id="e9535-113">While the example shows both a ProgID and a class identifier (CLSID) value, in practice these values are mutually exclusive so that only one or the other is present.</span></span> <span data-ttu-id="e9535-114">O valor de ProgID é preferencial.</span><span class="sxs-lookup"><span data-stu-id="e9535-114">The ProgID value is preferred.</span></span> <span data-ttu-id="e9535-115">Seja qual for o uso, ele deve apontar para um componente COM que implementa a interface [**IHWEventHandler**](/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler) .</span><span class="sxs-lookup"><span data-stu-id="e9535-115">Whichever is used, it should point to a COM component that implements the [**IHWEventHandler**](/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler) interface.</span></span>

 

<span data-ttu-id="e9535-116">Você pode inserir o valor da ação como um valor literal, por exemplo, "reproduzir música", conforme mostrado neste exemplo, ou como um nome de arquivo com uma cadeia de caracteres de recurso.</span><span class="sxs-lookup"><span data-stu-id="e9535-116">You can enter the Action value as a literal value, for example "Play music" as shown in this example, or as a file name with a resource string.</span></span> <span data-ttu-id="e9535-117">Você também pode inserir o valor do provedor como um valor literal ou como um nome de arquivo com uma cadeia de caracteres de recurso.</span><span class="sxs-lookup"><span data-stu-id="e9535-117">You can also enter the Provider value as a literal value or as a file name with a resource string.</span></span> <span data-ttu-id="e9535-118">A reprodução automática combina o valor da ação e o valor do provedor com a palavra "usando" para criar uma legenda amigável que é exibida na interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="e9535-118">AutoPlay combines the Action value and the Provider value with the word "using" to create a friendly caption that displays in the UI.</span></span> <span data-ttu-id="e9535-119">No exemplo, a legenda resultante é "reproduzir música usando o Windows Media Player".</span><span class="sxs-lookup"><span data-stu-id="e9535-119">In the example, the resulting caption is "Play music using Windows Media Player."</span></span>

<span data-ttu-id="e9535-120">O valor de DefaultIcon aponta para um arquivo. ico ou um recurso em um arquivo binário.</span><span class="sxs-lookup"><span data-stu-id="e9535-120">The DefaultIcon value points to either an .ico file or a resource in a binary file.</span></span> <span data-ttu-id="e9535-121">Se o valor numérico que segue o nome do arquivo binário for zero ou maior, será o valor de índice do ícone nesse arquivo binário.</span><span class="sxs-lookup"><span data-stu-id="e9535-121">If the numeric value that follows the binary file name is zero or greater, then it is the index value of the icon in that binary file.</span></span> <span data-ttu-id="e9535-122">Se for um valor negativo, será o ícone ID de recurso.</span><span class="sxs-lookup"><span data-stu-id="e9535-122">If it is a negative value, then it is the icon resource ID.</span></span> <span data-ttu-id="e9535-123">São recomendados valores de índice negativos.</span><span class="sxs-lookup"><span data-stu-id="e9535-123">Negative index values are recommended.</span></span> <span data-ttu-id="e9535-124">Nenhum valor é necessário no caso de um arquivo. ico.</span><span class="sxs-lookup"><span data-stu-id="e9535-124">No value is necessary in the case of an .ico file.</span></span> <span data-ttu-id="e9535-125">É recomendável que você use variáveis de ambiente no caminho.</span><span class="sxs-lookup"><span data-stu-id="e9535-125">It is recommended that you use environment variables in the path.</span></span>

<span data-ttu-id="e9535-126">O valor InitCmdLine passa inalterado por meio do método [**IHWEventHandler:: Initialize**](/windows/desktop/api/Shobjidl/nf-shobjidl-ihweventhandler-initialize) antes de qualquer outro método ser chamado.</span><span class="sxs-lookup"><span data-stu-id="e9535-126">The InitCmdLine value passes unaltered through the [**IHWEventHandler::Initialize**](/windows/desktop/api/Shobjidl/nf-shobjidl-ihweventhandler-initialize) method before any other methods are called.</span></span>

<span data-ttu-id="e9535-127">O exemplo a seguir mostra as subchaves e os valores que são usados para um dispositivo que pode ser lido diretamente, como uma unidade de CD-ROM ou outro disco removível.</span><span class="sxs-lookup"><span data-stu-id="e9535-127">The following example shows the subkeys and values that are used for a device that can be read directly, such as a CD-ROM drive or other removable disk.</span></span> <span data-ttu-id="e9535-128">Novamente, o manipulador de exemplo é chamado de **MyHandler**.</span><span class="sxs-lookup"><span data-stu-id="e9535-128">Again, the example handler is called **MyHandler**.</span></span>

```
HKEY_LOCAL_MACHINE or HKEY_CURRENT_USER
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  AutoplayHandlers
                     Handlers
                        MyHandler
                           Action [REG_SZ] = @%systemroot%\System32\wiaacmgr.exe,-276
                           DefaultIcon [REG_EXPAND_SZ] = %systemroot%\System32\wiaacmgr.exe,-2
                           InvokeProgID [REG_SZ] = WIA.AutoPlayDropHandler
                           InvokeVerb [REG_SZ] = open
                           Provider [REG_SZ] = @%systemroot%\System32\wiaacmgr.exe,-101
```

<span data-ttu-id="e9535-129">Neste exemplo, os valores de ação e provedor são mostrados como um nome de arquivo com uma cadeia de caracteres de recurso em vez de valores literais, mas as cadeias de caracteres que eles referenciam são usadas da mesma maneira.</span><span class="sxs-lookup"><span data-stu-id="e9535-129">In this example, the Action and Provider values are shown as a file name with a resource string rather than literal values, but the strings that they reference are used in the same manner.</span></span> <span data-ttu-id="e9535-130">Eles são combinados com a palavra "usando" para formar uma legenda amigável, conforme explicado anteriormente.</span><span class="sxs-lookup"><span data-stu-id="e9535-130">They are combined with the word "using" to form a friendly caption as explained earlier.</span></span>

<span data-ttu-id="e9535-131">Os valores InvokeProgID e InvokeVerb substituem CLSID, InitCmdLine e ProgID.</span><span class="sxs-lookup"><span data-stu-id="e9535-131">InvokeProgID and InvokeVerb values replace CLSID, InitCmdLine, and ProgID.</span></span> <span data-ttu-id="e9535-132">Os valores InvokeProgID e InvokeVerb correspondem aos nomes de chave encontrados na **\_ \_ raiz de classes hKey**, conforme mostrado na entrada de registro a seguir.</span><span class="sxs-lookup"><span data-stu-id="e9535-132">The InvokeProgID and InvokeVerb values match key names that are found under **HKEY\_CLASSES\_ROOT**, as shown in the following registry entry.</span></span> <span data-ttu-id="e9535-133">Esse conjunto de chaves de exemplo corresponde ao exemplo de manipulador específico descrito anteriormente.</span><span class="sxs-lookup"><span data-stu-id="e9535-133">This set of example keys corresponds to the specific Handler example described earlier.</span></span>

```
HKEY_CLASSES_ROOT
   WIA.AutoplayDropHandler
      shell
         open
            DropTarget
               Clsid = {F1ABE2B5-C073-4dba-B6EB-FD7A5111DD8F}
```

<span data-ttu-id="e9535-134">A função [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) usa o CLSID para implementar o aplicativo apropriado.</span><span class="sxs-lookup"><span data-stu-id="e9535-134">The [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) function uses the CLSID to implement the appropriate application.</span></span>

<span data-ttu-id="e9535-135">Depois de definir o manipulador de uma dessas duas maneiras, você precisa registrá-lo para um evento específico.</span><span class="sxs-lookup"><span data-stu-id="e9535-135">After you define the handler in either of these two ways, you need to register it for a specific event.</span></span> <span data-ttu-id="e9535-136">Você faz isso fornecendo o nome do manipulador como um valor para a chave do evento em **EventHandlers**.</span><span class="sxs-lookup"><span data-stu-id="e9535-136">You do this by providing the handler name as a value for that event's key under **EventHandlers**.</span></span> <span data-ttu-id="e9535-137">O exemplo a seguir mostra como registrar **MyHandler** como um manipulador para o evento GenericVolumeArrival.</span><span class="sxs-lookup"><span data-stu-id="e9535-137">The following example shows how to register **MyHandler** as a handler for the GenericVolumeArrival event.</span></span> <span data-ttu-id="e9535-138">Ele não tem nenhum valor de dados atribuído.</span><span class="sxs-lookup"><span data-stu-id="e9535-138">It has no assigned data value.</span></span>

```
HKEY_LOCAL_MACHINE or HKEY_CURRENT_USER
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  AutoplayHandlers
                     EventHandlers
                        GenericVolumeArrival
                           MyHandler [REG_SZ]
```

## <a name="related-topics"></a><span data-ttu-id="e9535-139">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e9535-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e9535-140">**IHWEventHandler**</span><span class="sxs-lookup"><span data-stu-id="e9535-140">**IHWEventHandler**</span></span>](/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler)
</dt> <dt>

[<span data-ttu-id="e9535-141">**CoCreateInstance**</span><span class="sxs-lookup"><span data-stu-id="e9535-141">**CoCreateInstance**</span></span>](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)
</dt> </dl>

 

 
