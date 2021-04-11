---
description: Disponibilidade de codec e suporte de plataforma
ms.assetid: 6b3d09c9-e91f-4c62-92f7-c2643e51987f
title: Disponibilidade de codec e suporte de plataforma
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcc485c5f8db9ff7883263cd614578705eccd3fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170863"
---
# <a name="codec-availability-and-platform-support"></a><span data-ttu-id="1ba94-103">Disponibilidade de codec e suporte de plataforma</span><span class="sxs-lookup"><span data-stu-id="1ba94-103">Codec Availability and Platform Support</span></span>

<span data-ttu-id="1ba94-104">A Microsoft recomenda que os fornecedores de câmera incluam os codecs de WIC (Windows Imaging Component) atualizados na distribuição de software com novas câmeras e que o codec atualizado seja instalado com a instalação de software do fornecedor padrão Windows 7, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="1ba94-104">Microsoft recommends that camera vendors include updated RAW Windows Imaging Component (WIC) codecs in the software distribution with new cameras and that the updated codec be installed with the default vendor software installation Windows 7, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="1ba94-105">Os fornecedores de câmera também devem fornecer o último codec do WIC como um download de seus sites de suporte.</span><span class="sxs-lookup"><span data-stu-id="1ba94-105">Camera vendors should also provide the latest WIC codec as a download from their support sites.</span></span>

## <a name="codec-discovery"></a><span data-ttu-id="1ba94-106">Descoberta de codec</span><span class="sxs-lookup"><span data-stu-id="1ba94-106">Codec Discovery</span></span>

<span data-ttu-id="1ba94-107">A Microsoft está fazendo o seguinte para ajudar a apontar os usuários para sites de fornecedores para downloads de codec:</span><span class="sxs-lookup"><span data-stu-id="1ba94-107">Microsoft is doing the following to help point users to vendors' Web sites for codec downloads:</span></span>

-   <span data-ttu-id="1ba94-108">No Windows Explorer, se um usuário clicar duas vezes em um arquivo não reconhecido (o caso padrão quando um arquivo bruto estiver no computador, mas o codec ainda não estiver instalado), uma caixa de diálogo relatará que o arquivo não é reconhecido e perguntará se o usuário deseja encontrar um programa que entenda o arquivo.</span><span class="sxs-lookup"><span data-stu-id="1ba94-108">In Windows Explorer, if a user double-clicks a file that is not recognized (the default case when a RAW file is on the computer, but the codec is not installed yet), a dialog box reports that the file is not recognized and asks whether the user wants to find a program that understands the file.</span></span> <span data-ttu-id="1ba94-109">A Microsoft mantém um serviço de redirecionamento existente para encaminhar os usuários aos sites de fornecedores que podem fornecer o programa para entender o arquivo.</span><span class="sxs-lookup"><span data-stu-id="1ba94-109">Microsoft maintains an existing redirection service to forward users to vendors' Web sites that can supply the program to understand the file.</span></span> <span data-ttu-id="1ba94-110">Esse recurso existe no Windows XP e no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="1ba94-110">This facility exists in Windows XP and in Windows Vista.</span></span>
-   <span data-ttu-id="1ba94-111">A Galeria de fotos do Windows, a Galeria de fotos do Windows Live e o Visualizador de fotos do Windows 7 reconhecem um conjunto de extensões de arquivo como arquivos BRUTOs.</span><span class="sxs-lookup"><span data-stu-id="1ba94-111">The Windows Photo Gallery, Windows Live Photo Gallery, and the Windows 7 Photo Viewer recognize a set of file extensions as RAW files.</span></span> <span data-ttu-id="1ba94-112">Se os arquivos desse conjunto forem encontrados em pastas que qualquer um desses aplicativos estão olhando e um codec para o arquivo ainda não estiver instalado, uma caixa de diálogo será exibida, conforme descrito no parágrafo anterior.</span><span class="sxs-lookup"><span data-stu-id="1ba94-112">If files from that set are found in folders that any of these applications are looking at, and a codec for the file is not already installed, then a dialog box appears, as described in the preceding paragraph.</span></span>

<span data-ttu-id="1ba94-113">Para obter mais informações sobre a descoberta de codecs, consulte disponibilidade de codec e suporte de plataforma.</span><span class="sxs-lookup"><span data-stu-id="1ba94-113">For more information about codec discovery, see Codec Availability and Platform Support.</span></span>

## <a name="windows-xp-platform-support"></a><span data-ttu-id="1ba94-114">Suporte à plataforma Windows XP</span><span class="sxs-lookup"><span data-stu-id="1ba94-114">Windows XP Platform Support</span></span>

<span data-ttu-id="1ba94-115">A Microsoft lançou o Windows XP SP3 com o WIC e um instalador de WIC autônomo para o Windows XP SP2.</span><span class="sxs-lookup"><span data-stu-id="1ba94-115">Microsoft has released Windows XP SP3 with WIC, and a standalone WIC installer for Windows XP SP2.</span></span> <span data-ttu-id="1ba94-116">Eles usam codecs WIC para habilitar o suporte para miniaturas e visualizações nessas plataformas.</span><span class="sxs-lookup"><span data-stu-id="1ba94-116">These use WIC codecs to enable support for thumbnails and previews on those platforms.</span></span> <span data-ttu-id="1ba94-117">Portanto, é importante que o download e a instalação do codec tenham suporte e testados no Windows 7, no Windows Vista e no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="1ba94-117">Therefore, it is important that codec download and installation be supported and tested on the Windows 7, Windows Vista, and Windows XP.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1ba94-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1ba94-118">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="1ba94-119">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="1ba94-119">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="1ba94-120">Visão geral do Windows Imaging Component</span><span class="sxs-lookup"><span data-stu-id="1ba94-120">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="1ba94-121">Diretrizes do WIC para formatos de imagem bruta de câmera</span><span class="sxs-lookup"><span data-stu-id="1ba94-121">WIC Guidelines for Camera RAW Image Formats</span></span>](-wic-rawguidelines.md)
</dt> <dt>

[<span data-ttu-id="1ba94-122">Como escrever um CODEC de WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="1ba94-122">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> </dl>

 

 



