---
description: O tópico a seguir descreve como executar a reprodução simples.
ms.assetid: 37869822-aed7-4102-8110-5a896400885c
title: Reprodução simples
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a7d07e37721bc84abb71c683ce4441580a80e6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105789846"
---
# <a name="simple-playback"></a><span data-ttu-id="f477e-103">Reprodução simples</span><span class="sxs-lookup"><span data-stu-id="f477e-103">Simple Playback</span></span>

<span data-ttu-id="f477e-104">O tópico a seguir descreve como executar a reprodução simples.</span><span class="sxs-lookup"><span data-stu-id="f477e-104">The following topic describes how to perform simple playback.</span></span>

<span data-ttu-id="f477e-105">**Para executar a reprodução simples**</span><span class="sxs-lookup"><span data-stu-id="f477e-105">**To perform simple playback**</span></span>

1.  <span data-ttu-id="f477e-106">Selecione o terminal de reprodução de arquivo no nível de chamada.</span><span class="sxs-lookup"><span data-stu-id="f477e-106">Select the File Playback Terminal at the call level.</span></span>
2.  <span data-ttu-id="f477e-107">Crie o terminal de reprodução na chamada TAPI.</span><span class="sxs-lookup"><span data-stu-id="f477e-107">Create the Playback Terminal on the TAPI call.</span></span>
3.  <span data-ttu-id="f477e-108">Definir propriedades — nome do arquivo e tipo de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="f477e-108">Set properties—file name and type of storage.</span></span>
4.  <span data-ttu-id="f477e-109">Chame o método [**Start**](/windows/desktop/api/tapi3if/nf-tapi3if-itmediacontrol-start) no terminal de reprodução de arquivos para iniciar a reprodução de fluxos.</span><span class="sxs-lookup"><span data-stu-id="f477e-109">Call the [**Start**](/windows/desktop/api/tapi3if/nf-tapi3if-itmediacontrol-start) method on the File Playback Terminal to start playback of streams.</span></span>

<span data-ttu-id="f477e-110">O código de exemplo a seguir demonstra a reprodução simples.</span><span class="sxs-lookup"><span data-stu-id="f477e-110">The following example code demonstrates simple playback.</span></span>

<span data-ttu-id="f477e-111">Primeiro, use a interface [**ITBasicCallControl2**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol2) para criar o terminal para gravação.</span><span class="sxs-lookup"><span data-stu-id="f477e-111">First, use the [**ITBasicCallControl2**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol2) interface to create the terminal for recording.</span></span> <span data-ttu-id="f477e-112">Isso instrui o TSP/MSP a executar a reprodução de arquivos nessa chamada.</span><span class="sxs-lookup"><span data-stu-id="f477e-112">This instructs the TSP/MSP to perform file playback on this call.</span></span> <span data-ttu-id="f477e-113">O TSP/MSP cria um terminal para o aplicativo usar e o retorna em caso de sucesso.</span><span class="sxs-lookup"><span data-stu-id="f477e-113">The TSP/MSP creates a terminal for the application to use, and returns it on success.</span></span>


```C++

```



<span data-ttu-id="f477e-114">Obtenha o ponteiro de interface [**ITMediaPlayback**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediaplayback) da interface do terminal e use-o para definir o nome do arquivo a ser reproduzido.</span><span class="sxs-lookup"><span data-stu-id="f477e-114">Get the [**ITMediaPlayback**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediaplayback) interface pointer from the terminal interface and use it to set the file name to play back.</span></span>


```C++
pMediaPlayback->Release();
```



<span data-ttu-id="f477e-115">Supondo que o arquivo contenha um fluxo de áudio e a chamada tenha um fluxo de áudio de captura, o conteúdo de áudio no arquivo será reproduzido nesse fluxo.</span><span class="sxs-lookup"><span data-stu-id="f477e-115">Assuming that the file contains one audio stream, and the call has a capture audio stream, the audio content in the file will play back on that stream.</span></span>

 

 



