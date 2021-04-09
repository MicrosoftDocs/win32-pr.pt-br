---
title: Apresentação
description: A apresentação é a etapa final do processo UPnP.
ms.assetid: e8d20ae6-2dd8-4de2-b07b-6cf4e725735e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 195399316882de71c148f2369dd2978c4cfbd728
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822539"
---
# <a name="presentation"></a><span data-ttu-id="5eedd-103">Apresentação</span><span class="sxs-lookup"><span data-stu-id="5eedd-103">Presentation</span></span>

<span data-ttu-id="5eedd-104">A apresentação é a etapa final do processo UPnP.</span><span class="sxs-lookup"><span data-stu-id="5eedd-104">Presentation is the final step in the UPnP process.</span></span> <span data-ttu-id="5eedd-105">Se um dispositivo tiver uma URL para apresentação, um ponto de controle poderá recuperar uma página dessa URL e carregar a página em um navegador.</span><span class="sxs-lookup"><span data-stu-id="5eedd-105">If a device has a URL for presentation, a control point can retrieve a page from this URL and load the page into a browser.</span></span> <span data-ttu-id="5eedd-106">Dependendo dos recursos da página de apresentação e do dispositivo, o ponto de controle pode controlar o dispositivo e exibir o status do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5eedd-106">Depending on the capabilities of the presentation page and the device, the control point can control the device and view the status of the device.</span></span>

<span data-ttu-id="5eedd-107">O caminho do recurso, que é passado para [**IUPnPRegistrar**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpregistrar) durante o registro, é onde todos os arquivos relevantes para a apresentação do dispositivo estão localizados.</span><span class="sxs-lookup"><span data-stu-id="5eedd-107">The resource path, which is passed to [**IUPnPRegistrar**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpregistrar) during registration, is where all the files relevant to the presentation of the device are located.</span></span> <span data-ttu-id="5eedd-108">Os desenvolvedores de dispositivos podem fornecer páginas separadas para cada dispositivo inserido.</span><span class="sxs-lookup"><span data-stu-id="5eedd-108">Device developers can provide separate pages for each embedded device.</span></span> <span data-ttu-id="5eedd-109">A URL de apresentação no modelo de descrição do dispositivo pode ser uma URL absoluta ou uma URL relativa.</span><span class="sxs-lookup"><span data-stu-id="5eedd-109">The presentation URL in the device description template can either be an absolute URL or a relative URL.</span></span> <span data-ttu-id="5eedd-110">Para URLs relativas, que são relativas ao caminho do recurso, o modelo de descrição do dispositivo deve conter um nome de arquivo.</span><span class="sxs-lookup"><span data-stu-id="5eedd-110">For relative URLs, which are relative to the resource path, the device description template should contain a file name.</span></span> <span data-ttu-id="5eedd-111">**IUPnPRegistrar** converte isso em uma URL com o local real.</span><span class="sxs-lookup"><span data-stu-id="5eedd-111">**IUPnPRegistrar** converts this to a URL with the actual location.</span></span> <span data-ttu-id="5eedd-112">Para URLs absolutas, o local não é modificado.</span><span class="sxs-lookup"><span data-stu-id="5eedd-112">For absolute URLs, the location is not modified.</span></span>

<span data-ttu-id="5eedd-113">Para dar suporte a scripts do lado do cliente em uma página de apresentação, informações extras normalmente são anexadas à URL na forma de uma "cadeia de caracteres de consulta".</span><span class="sxs-lookup"><span data-stu-id="5eedd-113">To support client side scripts within a presentation page, extra information is normally appended to the URL in the form of a "query string".</span></span> <span data-ttu-id="5eedd-114">As informações extras acrescentadas são a URL para o documento de descrição do dispositivo e o UDN do dispositivo ou dispositivo inserido.</span><span class="sxs-lookup"><span data-stu-id="5eedd-114">The extra information that is appended is the URL to the device description document, and the UDN of the device or embedded device.</span></span> <span data-ttu-id="5eedd-115">A URL de descrição do dispositivo pode ser usada para carregar um documento de descrição no script e, em seguida, controlar o dispositivo por meio de seus serviços.</span><span class="sxs-lookup"><span data-stu-id="5eedd-115">The device description URL can be used to load a description document in the script, and then control the device through its services.</span></span> <span data-ttu-id="5eedd-116">O UDN é usado para selecionar um dispositivo inserido do dispositivo raiz.</span><span class="sxs-lookup"><span data-stu-id="5eedd-116">The UDN is used to select an embedded device from the root device.</span></span>

<span data-ttu-id="5eedd-117">O formato da URL de apresentação modificada é: a URL de apresentação real, um ponto de interrogação ("?"), a URL de descrição do dispositivo, um sinal de adição ("+"), o dispositivo UDN.</span><span class="sxs-lookup"><span data-stu-id="5eedd-117">The format of the modified presentation URL is: the actual presentation URL, a question mark ("?"), the device description URL, a plus sign ("+"), the device UDN.</span></span> <span data-ttu-id="5eedd-118">O ponto de interrogação denota o início da cadeia de caracteres de consulta.</span><span class="sxs-lookup"><span data-stu-id="5eedd-118">The question mark denotes the start of the query string.</span></span>

<span data-ttu-id="5eedd-119">Se a URL de apresentação no modelo de descrição do dispositivo era uma URL absoluta e já continha um ponto de interrogação ("?"), as informações extras não são adicionadas à URL da apresentação.</span><span class="sxs-lookup"><span data-stu-id="5eedd-119">If the presentation URL in the device description template was an absolute URL and it already contained a question mark ("?"), then the extra information is not added to the presentation URL.</span></span>



| <span data-ttu-id="5eedd-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="5eedd-120">Description</span></span>                        | <span data-ttu-id="5eedd-121">URL</span><span class="sxs-lookup"><span data-stu-id="5eedd-121">URL</span></span>                                                                                                                                               |
|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5eedd-122">No modelo de descrição do dispositivo</span><span class="sxs-lookup"><span data-stu-id="5eedd-122">In the device description template</span></span> | <span data-ttu-id="5eedd-123">**presentationURL** MyDevice.html **/presentationURL**</span><span class="sxs-lookup"><span data-stu-id="5eedd-123">**presentationURL** MyDevice.html **/presentationURL**</span></span>                                                                                              |
| <span data-ttu-id="5eedd-124">Gerado pelo host do dispositivo</span><span class="sxs-lookup"><span data-stu-id="5eedd-124">Generated by the device host</span></span>       | <span data-ttu-id="5eedd-125">**presentationURL** https://machinename/deviceID/MyDevice.html/?https://machine/upnphost/udhisapi.dll?content=uuid:487394 ...</span><span class="sxs-lookup"><span data-stu-id="5eedd-125">**presentationURL**https://machinename/deviceID/MyDevice.html/?https://machine/upnphost/udhisapi.dll?content=uuid:487394…</span></span> <span data-ttu-id="5eedd-126">+ UDN **/presentationURL**</span><span class="sxs-lookup"><span data-stu-id="5eedd-126">+ UDN **/presentationURL**</span></span> |



 

<span data-ttu-id="5eedd-127">Um script do lado do cliente pode ter que extrair a URL de descrição do dispositivo da URL de apresentação para carregar o objeto [**IUPnPDescriptionDocument**](/windows/desktop/api/Upnp/nn-upnp-iupnpdescriptiondocument) .</span><span class="sxs-lookup"><span data-stu-id="5eedd-127">A client-side script may have to extract the device description URL from the presentation URL to load the [**IUPnPDescriptionDocument**](/windows/desktop/api/Upnp/nn-upnp-iupnpdescriptiondocument) object.</span></span> <span data-ttu-id="5eedd-128">Isso é feito por meio da cadeia de caracteres de consulta e de seu encerramento no sinal de adição ("+").</span><span class="sxs-lookup"><span data-stu-id="5eedd-128">This is done by taking the query string, and terminating it at the plus sign ("+").</span></span>


```VB
Dim QueryString
QueryString = window.location.search
Dim DescURLString
DescURLString = Trim(Mid(QueryString,2,Instr(QueryString,"+")-2))& vbCrLf

    Dim LightDesc
    Set LightDesc = CreateObject("UPnP.DescriptionDocument.1")
    LightDesc.Load(DescURLString)
```



<span data-ttu-id="5eedd-129">No caso de uma página de apresentação para um dispositivo inserido, é necessário algum trabalho adicional.</span><span class="sxs-lookup"><span data-stu-id="5eedd-129">In the case of a presentation page for an embedded device, some additional work is required.</span></span> <span data-ttu-id="5eedd-130">Depois de carregar o [**UPnPDescriptionDocument**](/windows/desktop/api/Upnp/nn-upnp-iupnpdescriptiondocument), o script deve obter a coleção de dispositivos inseridos e, em seguida, selecionar o dispositivo que corresponde ao UDN na cadeia de caracteres de consulta.</span><span class="sxs-lookup"><span data-stu-id="5eedd-130">After loading the [**UPnPDescriptionDocument**](/windows/desktop/api/Upnp/nn-upnp-iupnpdescriptiondocument), the script must obtain the collection of embedded devices, then select the device that matches the UDN in the query string.</span></span> <span data-ttu-id="5eedd-131">O script a seguir mostra como selecionar o dispositivo inserido para a página de apresentação atual.</span><span class="sxs-lookup"><span data-stu-id="5eedd-131">The following script shows how to select the embedded device for the current presentation page.</span></span> <span data-ttu-id="5eedd-132">Ele pressupõe que LightDesc já está carregado.</span><span class="sxs-lookup"><span data-stu-id="5eedd-132">It assumes LightDesc is already loaded.</span></span>


```VB
Dim LightDevice
Set LightDevice = LightDesc.RootDevice

Dim EmbeddedDevices 
set EmbeddedDevices = LightDevice.Children

Dim DeviceUdnString
DeviceUdnString = Trim(Mid(QueryString,Instr(QueryString,"+")+1,Len(QueryString)))

Dim Item
set Item = EmbeddedDevices.Item(DeviceUdnString)
```



 

 




