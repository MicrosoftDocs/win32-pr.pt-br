---
description: Os terminais de arquivo podem ser usados de duas maneiras.
ms.assetid: 5a7d6aa7-0eb8-4652-af0b-74fbdb5a2c2f
title: Usando terminais de arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d7637e83e56fddb2589bbd0858b5e994ca02855
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104091759"
---
# <a name="using-file-terminals"></a><span data-ttu-id="86ebf-103">Usando terminais de arquivo</span><span class="sxs-lookup"><span data-stu-id="86ebf-103">Using File Terminals</span></span>

<span data-ttu-id="86ebf-104">Os terminais de arquivo podem ser usados de duas maneiras.</span><span class="sxs-lookup"><span data-stu-id="86ebf-104">The file terminals can be used in two ways.</span></span> <span data-ttu-id="86ebf-105">O método mais simples é usar [**ITBasicCallControl2:: SelectTerminalOnCall**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol2-selectterminaloncall) para selecionar um terminal de arquivo (reprodução ou registro) em um objeto de chamada TAPI.</span><span class="sxs-lookup"><span data-stu-id="86ebf-105">The simplest method is to use [**ITBasicCallControl2::SelectTerminalOnCall**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol2-selectterminaloncall) to select a file terminal (playback or record) onto a TAPI call object.</span></span> <span data-ttu-id="86ebf-106">Nesse caso, a TAPI cuida da conexão dos fluxos de áudio aos terminais de faixa.</span><span class="sxs-lookup"><span data-stu-id="86ebf-106">In this case TAPI takes care of connecting the audio streams to the track terminals.</span></span>

<span data-ttu-id="86ebf-107">O segundo método permite que um aplicativo tenha um controle mais preciso sobre o mapeamento de fluxos de áudio para faixas.</span><span class="sxs-lookup"><span data-stu-id="86ebf-107">The second method allows an application to have finer control over the mapping of audio streams to tracks.</span></span> <span data-ttu-id="86ebf-108">Nesse cenário, o aplicativo enumera os fluxos disponíveis na chamada, escolhe aqueles que deseja registrar (ou use para reprodução), cria (ou localiza para reprodução) as faixas correspondentes no terminal do arquivo e seleciona as faixas em fluxos de chamada.</span><span class="sxs-lookup"><span data-stu-id="86ebf-108">In this scenario, the application enumerates the streams available on the call, picks the ones it wants to record (or use for playback), creates (or finds for playback) the corresponding tracks on the file terminal, and selects the tracks on call streams.</span></span>

<span data-ttu-id="86ebf-109">Para mais informações, consulte os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="86ebf-109">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="86ebf-110">Reprodução simples</span><span class="sxs-lookup"><span data-stu-id="86ebf-110">Simple Playback</span></span>](simple-playback.md)
-   [<span data-ttu-id="86ebf-111">Controle de reprodução controlado</span><span class="sxs-lookup"><span data-stu-id="86ebf-111">Track-Controlled Playback</span></span>](track-controlled-playback.md)
-   [<span data-ttu-id="86ebf-112">Registro simples</span><span class="sxs-lookup"><span data-stu-id="86ebf-112">Simple Record</span></span>](simple-record.md)
-   [<span data-ttu-id="86ebf-113">Rastrear registro controlado</span><span class="sxs-lookup"><span data-stu-id="86ebf-113">Track-Controlled Record</span></span>](track-controlled-record.md)

 

 



