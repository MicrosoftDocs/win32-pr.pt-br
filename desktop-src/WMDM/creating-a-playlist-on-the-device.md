---
title: Criando uma lista de reprodução no dispositivo
description: Criando uma lista de reprodução no dispositivo
ms.assetid: 9f803e1a-ff33-443a-9448-e8c875d77e51
keywords:
- Gerenciador de Dispositivos de mídia do Windows, listas de reprodução
- Gerenciador de Dispositivos, listas de reprodução
- Guia de programação, listas de reprodução
- aplicativos de área de trabalho, listas de reprodução
- criação de aplicativos do Windows Media Gerenciador de Dispositivos, listas de reprodução
- listas de reprodução abstratas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c287cc406b795db07fde3f10103822dea32185a5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292055"
---
# <a name="creating-a-playlist-on-the-device"></a><span data-ttu-id="cfb16-109">Criando uma lista de reprodução no dispositivo</span><span class="sxs-lookup"><span data-stu-id="cfb16-109">Creating a Playlist on the Device</span></span>

<span data-ttu-id="cfb16-110">O SDK do Windows Media Gerenciador de Dispositivos fornece os meios para um aplicativo MTP criar uma lista de reprodução em um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cfb16-110">The Windows Media Device Manager SDK provides the means for an MTP application to create a playlist on a device.</span></span> <span data-ttu-id="cfb16-111">Esse tipo de lista de reprodução é chamado de lista de reprodução *abstrata* , porque o arquivo criado no dispositivo não contém dados de mídia, mas apenas metadados, que contêm os links para os arquivos de mídia na lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="cfb16-111">This type of playlist is called an *abstract* playlist, because the file created on the device contains no media data, but only metadata, which holds the links to media files in the playlist.</span></span>

<span data-ttu-id="cfb16-112">Outros itens abstratos que podem ser criados no dispositivo incluem álbuns (basicamente listas de reprodução com propriedades extras, como arte de capa), contatos e mensagens.</span><span class="sxs-lookup"><span data-stu-id="cfb16-112">Other abstract items that can be created on the device include albums (essentially playlists with extra properties such as cover art), contacts, and messages.</span></span>

<span data-ttu-id="cfb16-113">**Para criar uma lista de reprodução**</span><span class="sxs-lookup"><span data-stu-id="cfb16-113">**To create a playlist**</span></span>

1.  <span data-ttu-id="cfb16-114">Adquira uma interface [**IWMDMDevice3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice3) para o dispositivo de destino.</span><span class="sxs-lookup"><span data-stu-id="cfb16-114">Acquire an [**IWMDMDevice3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice3) interface to the target device.</span></span>
2.  <span data-ttu-id="cfb16-115">Chame [**IWMDMDevice3:: GetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty) para obter a \_ Propriedade g wszWMDMFormatsSupported.</span><span class="sxs-lookup"><span data-stu-id="cfb16-115">Call [**IWMDMDevice3::GetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty) to obtain the g\_wszWMDMFormatsSupported property.</span></span>
3.  <span data-ttu-id="cfb16-116">Se não houver suporte para nenhum formato de lista de reprodução, não permita enviar listas de reprodução para o dispositivo e ignore as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="cfb16-116">If no playlist formats are supported, disallow sending playlists to the device, and skip the following steps.</span></span> <span data-ttu-id="cfb16-117">Caso contrário, escolha o código de formato com suporte do dispositivo que corresponda melhor ao tipo de objeto pretendido.</span><span class="sxs-lookup"><span data-stu-id="cfb16-117">Otherwise, choose the device-supported format code that matches most closely the intended object type.</span></span> <span data-ttu-id="cfb16-118">Os códigos de \_ formato genérico WMDM FORMATCODE \_ ABSTRACTAUDIOVIDEOPLAYLIST e WMDM \_ FORMATCODE \_ ABSTRACTAUDIOLAYLIST são os mais comumente suportados.</span><span class="sxs-lookup"><span data-stu-id="cfb16-118">The generic WMDM\_FORMATCODE\_ABSTRACTAUDIOVIDEOPLAYLIST and WMDM\_FORMATCODE\_ABSTRACTAUDIOLAYLIST format codes are the most commonly supported.</span></span>
4.  <span data-ttu-id="cfb16-119">Obtenha uma interface [**IWMDMStorage3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage3) para o armazenamento (a raiz ou uma pasta) em que você deseja criar o objeto.</span><span class="sxs-lookup"><span data-stu-id="cfb16-119">Obtain an [**IWMDMStorage3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage3) interface for the storage (the root or a folder) where you want to create the object.</span></span> <span data-ttu-id="cfb16-120">Alguns dispositivos funcionarão melhor se o objeto de playlist for colocado em uma pasta de nível superior chamada "playlists".</span><span class="sxs-lookup"><span data-stu-id="cfb16-120">Some devices work best if the playlist object is placed in a top level folder named "Playlists".</span></span>
5.  <span data-ttu-id="cfb16-121">Crie um objeto de metadados vazio usando [**IWMDMStorage3:: CreateEmptyMetadataObject**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-createemptymetadataobject).</span><span class="sxs-lookup"><span data-stu-id="cfb16-121">Create an empty metadata object by using [**IWMDMStorage3::CreateEmptyMetadataObject**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-createemptymetadataobject).</span></span>
6.  <span data-ttu-id="cfb16-122">Usando a interface **IWMDMMetaData** obtida na etapa anterior, chame [**IWMDMMetaData:: AddItem**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmmetadata-additem) para adicionar o código de formato escolhido (da etapa 3) às propriedades de metadados de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="cfb16-122">Using the **IWMDMMetaData** interface obtained in the previous step, call [**IWMDMMetaData::AddItem**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmmetadata-additem) to add your chosen format code (from step 3) to the storage metadata properties.</span></span>
7.  <span data-ttu-id="cfb16-123">Obtenha a interface [**IWMDMStorageControl3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstoragecontrol3) da interface **IWMDMStorage3** .</span><span class="sxs-lookup"><span data-stu-id="cfb16-123">Obtain the [**IWMDMStorageControl3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstoragecontrol3) interface from the **IWMDMStorage3** interface.</span></span>
8.  <span data-ttu-id="cfb16-124">Chame [**IWMDMStorageControl3:: Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3) para inserir um novo arquivo de lista de reprodução no armazenamento selecionado.</span><span class="sxs-lookup"><span data-stu-id="cfb16-124">Call [**IWMDMStorageControl3::Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3) to insert a new playlist file in the selected storage.</span></span> <span data-ttu-id="cfb16-125">Esse arquivo contém os metadados representados pela interface **IWMDMMetaData** criada na etapa 5 e passados para **Insert3**.</span><span class="sxs-lookup"><span data-stu-id="cfb16-125">This file contains the metadata represented by the **IWMDMMetaData** interface you created in step 5 and passed to **Insert3**.</span></span> <span data-ttu-id="cfb16-126">O método retorna uma interface **IWMDMStorage** para o arquivo de lista de reprodução; Você pode consultar a interface [**IWMDMStorage4**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage4) .</span><span class="sxs-lookup"><span data-stu-id="cfb16-126">The method returns an **IWMDMStorage** interface for the playlist file; you can query for the [**IWMDMStorage4**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage4) interface.</span></span>
9.  <span data-ttu-id="cfb16-127">Chame [**IWMDMStorage4:: Setreferenciations**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage4-setreferences) para criar referências às interfaces **IWMDMStorage** dos arquivos de mídia na lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="cfb16-127">Call [**IWMDMStorage4::SetReferences**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage4-setreferences) to create references to the **IWMDMStorage** interfaces of the media files in the playlist.</span></span>

<span data-ttu-id="cfb16-128">Para obter um exemplo de código, consulte a \_ função OnCreatePlaylist no [aplicativo de desktop de exemplo](sample-desktop-application.md).</span><span class="sxs-lookup"><span data-stu-id="cfb16-128">For example code, see the \_OnCreatePlaylist function in the [Sample Desktop Application](sample-desktop-application.md).</span></span>

> [!Note]  
> <span data-ttu-id="cfb16-129">O provedor de serviços MTP fornecido pela Microsoft permite que um aplicativo defina referências em metadados.</span><span class="sxs-lookup"><span data-stu-id="cfb16-129">The Microsoft-provided MTP service provider enables an application to set references in metadata.</span></span> <span data-ttu-id="cfb16-130">Para implementar listas de reprodução, seu aplicativo deve estar se comunicando com um dispositivo MTP ou usando um provedor de serviços personalizado que pode manipular objetos abstratos.</span><span class="sxs-lookup"><span data-stu-id="cfb16-130">To implement playlists, your application must be communicating with an MTP device or using a custom service provider that can handle abstract objects.</span></span> <span data-ttu-id="cfb16-131">O provedor de serviços CE manipula a playlist e os objetos de álbum.</span><span class="sxs-lookup"><span data-stu-id="cfb16-131">The CE service provider handles playlist and album objects.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="cfb16-132">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="cfb16-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cfb16-133">**Gravando arquivos no dispositivo**</span><span class="sxs-lookup"><span data-stu-id="cfb16-133">**Writing Files to the Device**</span></span>](writing-files-to-the-device.md)
</dt> </dl>

 

 




