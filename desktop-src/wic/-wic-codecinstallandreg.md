---
description: Ao instalar um codec, você deve registrá-lo no registro. Você também deve verificar se o cache de miniaturas é atualizado caso já existam imagens no seu formato no computador.
ms.assetid: 7aec54cb-40ac-495c-99d9-9c397b740b21
title: Instalação e registro de codec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d83616071bebdbab14bfdc7dd0f879df3d49789d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105797653"
---
# <a name="codec-installation-and-registration"></a><span data-ttu-id="09dfe-104">Instalação e registro de codec</span><span class="sxs-lookup"><span data-stu-id="09dfe-104">Codec Installation and Registration</span></span>

<span data-ttu-id="09dfe-105">Ao instalar um codec, você deve registrá-lo no registro.</span><span class="sxs-lookup"><span data-stu-id="09dfe-105">When you install a codec, you must register it in the registry.</span></span> <span data-ttu-id="09dfe-106">Você também deve verificar se o cache de miniaturas é atualizado caso já existam imagens no seu formato no computador.</span><span class="sxs-lookup"><span data-stu-id="09dfe-106">You must also make sure the thumbnail cache gets updated in case any images in your format already exist on the computer.</span></span>

<span data-ttu-id="09dfe-107">Este tópico contém as seguintes seções:</span><span class="sxs-lookup"><span data-stu-id="09dfe-107">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="09dfe-108">Registrando um codec</span><span class="sxs-lookup"><span data-stu-id="09dfe-108">Registering a Codec</span></span>](#registering-a-codec)
-   [<span data-ttu-id="09dfe-109">Atualizando o cache de miniaturas ao instalar o codec</span><span class="sxs-lookup"><span data-stu-id="09dfe-109">Updating the Thumbnail Cache When Installing Your Codec</span></span>](#updating-the-thumbnail-cache-when-installing-your-codec)
-   [<span data-ttu-id="09dfe-110">Disponibilizando o codec WIC-Enabled para os usuários</span><span class="sxs-lookup"><span data-stu-id="09dfe-110">Making Your WIC-Enabled Codec Available To Users</span></span>](#making-your-wic-enabled-codec-available-to-users)
-   [<span data-ttu-id="09dfe-111">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="09dfe-111">Related topics</span></span>](#related-topics)

## <a name="registering-a-codec"></a><span data-ttu-id="09dfe-112">Registrando um codec</span><span class="sxs-lookup"><span data-stu-id="09dfe-112">Registering a Codec</span></span>

<span data-ttu-id="09dfe-113">Ao registrar um codec, na verdade você está registrando dois componentes: o codificador e o decodificador.</span><span class="sxs-lookup"><span data-stu-id="09dfe-113">When you register a codec, you are actually registering two components: the encoder and the decoder.</span></span> <span data-ttu-id="09dfe-114">Você também precisa fazer entradas do registro para registrar seu formato de contêiner com os manipuladores de metadados para os formatos de metadados aos quais o formato de imagem dá suporte.</span><span class="sxs-lookup"><span data-stu-id="09dfe-114">You also need to make registry entries to register your container format with the metadata handlers for the metadata formats that your image format supports.</span></span>

<span data-ttu-id="09dfe-115">Os tópicos a seguir descrevem as entradas de Registro necessárias para registrar seu Codec:</span><span class="sxs-lookup"><span data-stu-id="09dfe-115">The following topics describe the registry entries you need to register your codec:</span></span>

[<span data-ttu-id="09dfe-116">Entradas gerais do registro</span><span class="sxs-lookup"><span data-stu-id="09dfe-116">General Registry Entries</span></span>](-wic-generalregentries.md)

[<span data-ttu-id="09dfe-117">Entradas de registro específicas do codificador</span><span class="sxs-lookup"><span data-stu-id="09dfe-117">Encoder-Specific Registry Entries</span></span>](-wic-encoderregentries.md)

[<span data-ttu-id="09dfe-118">Entradas de registro específicas do decodificador</span><span class="sxs-lookup"><span data-stu-id="09dfe-118">Decoder-Specific Registry Entries</span></span>](-wic-decoderregentries.md)

[<span data-ttu-id="09dfe-119">Integração com a Galeria de fotos do Windows e o Windows Explorer</span><span class="sxs-lookup"><span data-stu-id="09dfe-119">Integration with Windows Photo Gallery and Windows Explorer</span></span>](-wic-integrationregentries.md)

## <a name="updating-the-thumbnail-cache-when-installing-your-codec"></a><span data-ttu-id="09dfe-120">Atualizando o cache de miniaturas ao instalar o codec</span><span class="sxs-lookup"><span data-stu-id="09dfe-120">Updating the Thumbnail Cache When Installing Your Codec</span></span>

<span data-ttu-id="09dfe-121">Quando um codec é instalado, o instalador precisa chamar a função a seguir depois de gravar suas entradas de registro.</span><span class="sxs-lookup"><span data-stu-id="09dfe-121">When a codec is installed, the installer needs to call the following function after writing its registry entries.</span></span>


```C++
SHChangeNotify(SHCNE_ASSOCCHANGED, SHCNF_IDLIST, NULL, NULL)
```



<span data-ttu-id="09dfe-122">Essa chamada notifica o Windows de que novas informações de associação de arquivo estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="09dfe-122">This call notifies Windows that new file association information is available.</span></span> <span data-ttu-id="09dfe-123">Se as imagens no seu formato de imagem já existirem no computador, o cache de miniaturas conterá miniaturas padrão para elas, pois nenhum decodificador estava disponível para extrair as miniaturas quando as imagens foram adquiridas pela primeira vez.</span><span class="sxs-lookup"><span data-stu-id="09dfe-123">If images in your image format already exist on the computer, the thumbnail cache will contain default thumbnails for them because no decoder was available to extract the thumbnails when the images were first acquired.</span></span> <span data-ttu-id="09dfe-124">Quando você notifica o Windows de que uma nova associação de arquivo está disponível, o cache em miniatura descarta todas as miniaturas vazias e extrai as miniaturas reais dos arquivos que agora podem ser decodificados.</span><span class="sxs-lookup"><span data-stu-id="09dfe-124">When you notify Windows that a new file association is available, the thumbnail cache discards any empty thumbnails and extracts the actual thumbnails from the files that can now be decoded.</span></span>

## <a name="making-your-wic-enabled-codec-available-to-users"></a><span data-ttu-id="09dfe-125">Disponibilizando o codec WIC-Enabled para os usuários</span><span class="sxs-lookup"><span data-stu-id="09dfe-125">Making Your WIC-Enabled Codec Available To Users</span></span>

<span data-ttu-id="09dfe-126">Se você for um fabricante de câmera, poderá enviar seus codecs brutos na caixa com suas câmeras.</span><span class="sxs-lookup"><span data-stu-id="09dfe-126">If you are a camera manufacturer, you can ship your raw codecs in the box with your cameras.</span></span> <span data-ttu-id="09dfe-127">Você também pode postar seus codecs na página de download do seu site da Web.</span><span class="sxs-lookup"><span data-stu-id="09dfe-127">You can also post your codecs on the Download page of your Web site.</span></span> <span data-ttu-id="09dfe-128">No entanto, se um usuário adquire um arquivo de imagem em seu formato de alguma outra fonte, como um amigo, um associado comercial ou algum outro site, talvez não saiba onde obter o codec para decodificá-lo.</span><span class="sxs-lookup"><span data-stu-id="09dfe-128">However, if a user acquires an image file in your format from some other source, such as a friend, business associate, or some other Web site, they may not know where to get the codec to decode it with.</span></span>

<span data-ttu-id="09dfe-129">Devido a esse problema, o Windows oferece uma maneira mais fácil para os usuários do seu formato de imagem localizarem seu codec e baixá-lo em seu computador, começando com o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="09dfe-129">Because of this issue, Windows offers an easier way for users of your image format to find your codec and download it onto their computer, starting with Windows Vista.</span></span> <span data-ttu-id="09dfe-130">Se a Galeria de fotos do Windows reconhecer uma extensão de nome de arquivo como um formato de imagem e o codec para esse formato não estiver instalado, uma caixa de diálogo informa ao usuário que a foto não pode ser exibida e pergunta se o usuário deseja baixar o software necessário para exibi-lo.</span><span class="sxs-lookup"><span data-stu-id="09dfe-130">If the Windows Photo Gallery recognizes a file name extension as an image format, and the codec for that format is not installed, a dialog box tells the user that the photo can’t be displayed, and asks whether the user wants to download the software required to display it.</span></span> <span data-ttu-id="09dfe-131">Quando o usuário aceita, um site hospedado pela Microsoft é exibido com um link para o site de download do fabricante do codec.</span><span class="sxs-lookup"><span data-stu-id="09dfe-131">When the user accepts, a Microsoft-hosted Web site appears with a link to the codec manufacturer’s download site.</span></span> <span data-ttu-id="09dfe-132">(Opcionalmente, você pode solicitar que os usuários sejam levados diretamente ao seu site de download.)</span><span class="sxs-lookup"><span data-stu-id="09dfe-132">(Optionally, you can request that users be taken directly to your download site.)</span></span>

<span data-ttu-id="09dfe-133">Se desejar que as extensões de nome de arquivo do formato de imagem sejam reconhecidas pela galeria de fotos do Windows para que os usuários possam ser direcionados para o site de download, você deverá fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="09dfe-133">If you want your image format’s file name extensions to be recognized by the Windows Photo Gallery so that users can be directed to your download site, you must do the following:</span></span>

1.  <span data-ttu-id="09dfe-134">Forneça um site de download para seu codec.</span><span class="sxs-lookup"><span data-stu-id="09dfe-134">Provide a download site for your codec.</span></span> <span data-ttu-id="09dfe-135">(Você pode ter uma página separada para cada codec que fornecer ou uma página que forneça downloads para todos os seus codecs.)</span><span class="sxs-lookup"><span data-stu-id="09dfe-135">(You can have a separate page for each codec you provide, or one page that provides downloads for all your codecs.)</span></span>

    <span data-ttu-id="09dfe-136">O site de download deve ser localizado e facilmente pesquisável por modelo de câmera.</span><span class="sxs-lookup"><span data-stu-id="09dfe-136">The download site should be localized and easily searchable by camera model.</span></span>

2.  <span data-ttu-id="09dfe-137">Forneça à Microsoft uma lista de extensões para seus formatos de imagem e as URLs para seus sites de download.</span><span class="sxs-lookup"><span data-stu-id="09dfe-137">Provide Microsoft with a list of extensions for your image formats, and the URLs for your download sites.</span></span>

<span data-ttu-id="09dfe-138">Você deve informar à Microsoft sobre as extensões para quaisquer novos codecs desenvolvidas no futuro e de quaisquer alterações nas URLs de seus sites de download, para que as novas informações possam ser adicionadas à galeria de fotos do Windows.</span><span class="sxs-lookup"><span data-stu-id="09dfe-138">You must inform Microsoft of the extensions for any new codecs you develop in the future, and of any changes to the URLs of your download sites, so that the new information can be added to the Windows Photo Gallery.</span></span>

## <a name="related-topics"></a><span data-ttu-id="09dfe-139">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="09dfe-139">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="09dfe-140">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="09dfe-140">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="09dfe-141">Implementando IWICMetadataBlockWriter</span><span class="sxs-lookup"><span data-stu-id="09dfe-141">Implementing IWICMetadataBlockWriter</span></span>](-wic-imp-iwicmetadatablockwriter.md)
</dt> <dt>

[<span data-ttu-id="09dfe-142">Conclusão (como escrever um CODEC de WIC-Enabled)</span><span class="sxs-lookup"><span data-stu-id="09dfe-142">Conclusion (How to Write a WIC-Enabled CODEC)</span></span>](-wic-howtowriteacodec-conclusion.md)
</dt> <dt>

[<span data-ttu-id="09dfe-143">Como escrever um CODEC de WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="09dfe-143">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="09dfe-144">Visão geral do Windows Imaging Component</span><span class="sxs-lookup"><span data-stu-id="09dfe-144">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



