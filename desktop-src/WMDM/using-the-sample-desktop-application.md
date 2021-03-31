---
title: Usando o aplicativo de desktop de exemplo
description: Usando o aplicativo de desktop de exemplo
ms.assetid: 5e3e5283-9e27-4f6a-93a9-84d84f2e875a
keywords:
- Gerenciador de Dispositivos de mídia do Windows, amostras
- Gerenciador de Dispositivos, exemplos
- aplicativos de área de trabalho, exemplos
- Windows Media Gerenciador de Dispositivos, exemplo de aplicativo da área de trabalho
- Gerenciador de Dispositivos, exemplo de aplicativo de desktop
- exemplos, aplicativos de desktop
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd511ea5241f458d2cd926dc8fb2f3681757ff8b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635317"
---
# <a name="using-the-sample-desktop-application"></a><span data-ttu-id="40bfc-109">Usando o aplicativo de desktop de exemplo</span><span class="sxs-lookup"><span data-stu-id="40bfc-109">Using the Sample Desktop Application</span></span>

<span data-ttu-id="40bfc-110">O aplicativo de desktop de exemplo é uma janela básica de dois painéis, um pouco semelhante ao Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="40bfc-110">The sample desktop application is a basic two-paned window somewhat like Windows Explorer.</span></span> <span data-ttu-id="40bfc-111">Ele permite que você procure o conteúdo de um dispositivo, usando uma exibição de árvore exibição de pastas no painel esquerdo e arquivos no painel direito.</span><span class="sxs-lookup"><span data-stu-id="40bfc-111">It allows you to browse the contents of a device, using a tree view display of folders in the left pane, and files in the right pane.</span></span> <span data-ttu-id="40bfc-112">A raiz de cada árvore de pastas é logicamente considerada um dispositivo diferente, embora alguns dispositivos possam se representar como vários objetos (um para cada armazenamento raiz).</span><span class="sxs-lookup"><span data-stu-id="40bfc-112">The root of each folder tree is logically considered a different device, although some devices might represent themselves as several objects (one for each root storage).</span></span> <span data-ttu-id="40bfc-113">Para ler as propriedades básicas de uma pasta ou de um arquivo, clique com o botão direito do mouse no objeto e selecione **Propriedades**.</span><span class="sxs-lookup"><span data-stu-id="40bfc-113">To read the basic properties of either a folder or a file, right-click the object and select **Properties**.</span></span>

<span data-ttu-id="40bfc-114">Você pode excluir arquivos no dispositivo selecionando um arquivo no painel direito e selecionando **excluir** no menu **arquivo** .</span><span class="sxs-lookup"><span data-stu-id="40bfc-114">You can delete files on the device by selecting a file in the right pane and selecting **Delete** on the **File** menu.</span></span> <span data-ttu-id="40bfc-115">Para adicionar arquivos de mídia ao dispositivo, você pode arrastar arquivos da área de trabalho para o painel direito do programa.</span><span class="sxs-lookup"><span data-stu-id="40bfc-115">To add media files to the device, you can drag files from the desktop onto the right pane of the program.</span></span> <span data-ttu-id="40bfc-116">Observe que os arquivos devem ter um formato de mídia com suporte no dispositivo; arquivos de formatos inaceitáveis (arquivos que não são de mídia, como arquivos. txt ou formatos de mídia não suportados pelo dispositivo) não serão enviados para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="40bfc-116">Note that files must be of a media format supported by the device; files of unacceptable formats (non-media files such as .txt files, or media formats not supported by the device) will not be sent to the device.</span></span> <span data-ttu-id="40bfc-117">(Observe que essa restrição é a do programa; O Windows Media Gerenciador de Dispositivos permite que você envie qualquer arquivo para um dispositivo se o dispositivo o aceitar.)</span><span class="sxs-lookup"><span data-stu-id="40bfc-117">(Note that this restriction is the program's; Windows Media Device Manager enables you to send any file to a device if the device will accept it.)</span></span>

<span data-ttu-id="40bfc-118">Para capturar eventos de retorno de chamada enviados para a interface [**IWMDMOperation**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation) , você deve marcar a opção "usar a interface de operação" no menu **Opções** .</span><span class="sxs-lookup"><span data-stu-id="40bfc-118">To capture callback events sent to the [**IWMDMOperation**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation) interface, you must check the "Use Operation Interface" option in the **Options** menu.</span></span>

<span data-ttu-id="40bfc-119">O menu **Opções** também permite que você escolha se deseja usar várias interfaces mais avançadas com recursos compatíveis com dispositivos avançados.</span><span class="sxs-lookup"><span data-stu-id="40bfc-119">The **Options** menu also enables you to choose whether to use several more advanced interfaces with features supported by advanced devices.</span></span>

<span data-ttu-id="40bfc-120">O menu **contêineres** tem opções para permitir que você crie uma lista de reprodução ou um álbum.</span><span class="sxs-lookup"><span data-stu-id="40bfc-120">The **Containers** menu has options to allow you to create a playlist or an album.</span></span> <span data-ttu-id="40bfc-121">Para criar uma lista de reprodução, selecione uma ou mais músicas no dispositivo e clique em **criar playlist** no menu **contêineres** .</span><span class="sxs-lookup"><span data-stu-id="40bfc-121">To create a playlist, select one or more songs on the device and click **Create Playlist** on the **Containers** menu.</span></span> <span data-ttu-id="40bfc-122">Esse recurso funciona apenas em dispositivos MTP, pois o código só dá suporte à criação de um arquivo de playlist "virtual".</span><span class="sxs-lookup"><span data-stu-id="40bfc-122">This feature only works on MTP devices, because the code only supports the creation of an "virtual" playlist file.</span></span> <span data-ttu-id="40bfc-123">(Uma playlist virtual é uma lista de reprodução que é especificada somente por valores de metadados, em vez de por um arquivo físico, por exemplo, um arquivo WPL.) O dispositivo deve dar suporte a listas de reprodução vazias para usar esse recurso.</span><span class="sxs-lookup"><span data-stu-id="40bfc-123">(A virtual playlist is a playlist that is specified only by metadata values, rather than by a physical file, for example a WPL file.) The device must support empty playlists to use this feature.</span></span>

<span data-ttu-id="40bfc-124">Para criar um álbum (uma lista de reprodução com uma imagem associada), selecione uma ou mais músicas no dispositivo e clique em **criar álbum** no menu **contêineres** .</span><span class="sxs-lookup"><span data-stu-id="40bfc-124">To create an album (a playlist with an associated image), select one or more songs on the device and click **Create Album** on the **Containers** menu.</span></span> <span data-ttu-id="40bfc-125">Uma caixa de diálogo permite que você navegue até um arquivo de imagem no computador para associá-lo ao álbum.</span><span class="sxs-lookup"><span data-stu-id="40bfc-125">A dialog box allows you to browse to a picture file on your computer to associate with the album.</span></span> <span data-ttu-id="40bfc-126">Da mesma forma que cria listas de reprodução, o aplicativo cria um arquivo de álbum "vazio"; Se o dispositivo não oferecer suporte a álbuns vazios, esse recurso não funcionará.</span><span class="sxs-lookup"><span data-stu-id="40bfc-126">Similarly to the way it creates playlists, the application creates an "empty" album file; if the device does not support empty albums, this feature will not work.</span></span>

## <a name="related-topics"></a><span data-ttu-id="40bfc-127">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="40bfc-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="40bfc-128">**Aplicativo de desktop de exemplo**</span><span class="sxs-lookup"><span data-stu-id="40bfc-128">**Sample Desktop Application**</span></span>](sample-desktop-application.md)
</dt> </dl>

 

 




