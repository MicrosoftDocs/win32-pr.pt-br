---
description: Exemplo de VMRPlayer
ms.assetid: 7fc893a6-afa5-4ada-9295-29122b43b21e
title: Exemplo de VMRPlayer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2214d94628a90daf0dd543f4e3a7f0166f4968a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827529"
---
# <a name="vmrplayer-sample"></a><span data-ttu-id="7a4ac-103">Exemplo de VMRPlayer</span><span class="sxs-lookup"><span data-stu-id="7a4ac-103">VMRPlayer Sample</span></span>

## <a name="description"></a><span data-ttu-id="7a4ac-104">Descrição</span><span class="sxs-lookup"><span data-stu-id="7a4ac-104">Description</span></span>

<span data-ttu-id="7a4ac-105">Este exemplo usa o filtro de processador de mixagem de vídeo 9 (VMR-9) para alfa Blend um ou dois vídeos em execução e uma imagem estática.</span><span class="sxs-lookup"><span data-stu-id="7a4ac-105">This sample uses the Video Mixing Renderer 9 (VMR-9) filter to alpha blend one or two running videos and a static image.</span></span>

## <a name="usage"></a><span data-ttu-id="7a4ac-106">Uso</span><span class="sxs-lookup"><span data-stu-id="7a4ac-106">Usage</span></span>

<span data-ttu-id="7a4ac-107">Para abrir o primeiro vídeo, escolha **abrir fluxo primário** no menu **arquivo** .</span><span class="sxs-lookup"><span data-stu-id="7a4ac-107">To open the first video, choose **Open Primary Stream** from the **File** menu.</span></span> <span data-ttu-id="7a4ac-108">Para abrir um segundo vídeo, escolha **abrir fluxo secundário** no menu **arquivo** (você deve abrir primeiro o fluxo primário).</span><span class="sxs-lookup"><span data-stu-id="7a4ac-108">To open a second video, choose **Open Secondary Stream** from the **File** menu (you must open the primary stream first).</span></span> <span data-ttu-id="7a4ac-109">Para reproduzir o vídeo, clique no botão **reproduzir** .</span><span class="sxs-lookup"><span data-stu-id="7a4ac-109">To play the video, click the **Play** button.</span></span>

<span data-ttu-id="7a4ac-110">Você pode definir a posição, o tamanho e os valores Alfa dos vídeos selecionando fluxo **principal** ou **Secondard Stream** no menu de **Propriedades do VMR** .</span><span class="sxs-lookup"><span data-stu-id="7a4ac-110">You can set the position, size, and alpha values of the videos by selecting **Primary Stream** or **Secondard Stream** from the **VMR Properties** menu.</span></span>

<span data-ttu-id="7a4ac-111">Para adicionar um bitmap estático no vídeo, escolha **imagem estática do aplicativo** no menu de **Propriedades do VMR** e clique na caixa **Exibir imagem do aplicativo** .</span><span class="sxs-lookup"><span data-stu-id="7a4ac-111">To add a static bitmap over the video, choose **Static App Image** from the **VMR Properties** menu and click the **Display App Image** box.</span></span> <span data-ttu-id="7a4ac-112">Você pode usar a mesma caixa de diálogo para controlar a posição, o tamanho e o valor alfa do bitmap.</span><span class="sxs-lookup"><span data-stu-id="7a4ac-112">You can use the same dialog to control the position, size, and alpha value of the bitmap.</span></span>

<span data-ttu-id="7a4ac-113">Para capturar a imagem de vídeo mesclada, escolha **Capturar imagem de bitmap** no menu de **Propriedades do VMR** .</span><span class="sxs-lookup"><span data-stu-id="7a4ac-113">To capture the blended video image, choose **Capture Bitmap Image** from the **VMR Properties** menu.</span></span>

<span data-ttu-id="7a4ac-114">Você também pode especificar o fluxo da imagem primária na linha de comando:</span><span class="sxs-lookup"><span data-stu-id="7a4ac-114">You can also specify the primary image stream from the command line:</span></span>

<span data-ttu-id="7a4ac-115">**VMRPlayer** **/p** *nome do arquivo*</span><span class="sxs-lookup"><span data-stu-id="7a4ac-115">**VMRPlayer** **/P** *filename*</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="7a4ac-116">Baixando o exemplo</span><span class="sxs-lookup"><span data-stu-id="7a4ac-116">Downloading the Sample</span></span>

<span data-ttu-id="7a4ac-117">Para baixar os exemplos do SDK do DirectShow, instale a versão mais recente do [SDK do Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="7a4ac-117">To download the DirectShow SDK samples, install the latest version of the [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span>

## <a name="related-topics"></a><span data-ttu-id="7a4ac-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7a4ac-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7a4ac-119">Amostras do DirectShow</span><span class="sxs-lookup"><span data-stu-id="7a4ac-119">DirectShow Samples</span></span>](directshow-samples.md)
</dt> </dl>

 

 



