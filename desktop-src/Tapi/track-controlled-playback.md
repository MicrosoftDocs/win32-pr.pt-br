---
description: As etapas a seguir são executadas para a reprodução controlada por controle.
ms.assetid: 9069fb32-3978-491b-bb22-f6e736af23d7
title: Reprodução de Track-Controlled
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cc657f0d301097edd280c358a34daafa83ef356
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105813045"
---
# <a name="track-controlled-playback"></a><span data-ttu-id="e6664-103">Reprodução de Track-Controlled</span><span class="sxs-lookup"><span data-stu-id="e6664-103">Track-Controlled Playback</span></span>

<span data-ttu-id="e6664-104">Para executar a reprodução controlada pelo controle, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="e6664-104">To perform track-controlled playback, do the following:</span></span>

-   <span data-ttu-id="e6664-105">Selecione a faixa terminais em fluxos.</span><span class="sxs-lookup"><span data-stu-id="e6664-105">Select the Track Terminals onto streams.</span></span>
-   <span data-ttu-id="e6664-106">Crie o terminal de reprodução de arquivo.</span><span class="sxs-lookup"><span data-stu-id="e6664-106">Create the File Playback Terminal.</span></span>
-   <span data-ttu-id="e6664-107">Definir propriedades — nome do arquivo e tipo de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="e6664-107">Set properties—file name and type of storage.</span></span>
-   <span data-ttu-id="e6664-108">Usando um método no terminal de reprodução de arquivo, enumere os terminais de faixa de arquivo.</span><span class="sxs-lookup"><span data-stu-id="e6664-108">Using a method on the File Playback Terminal, enumerate File Track Terminals.</span></span>
-   <span data-ttu-id="e6664-109">Enumere os fluxos na chamada TAPI.</span><span class="sxs-lookup"><span data-stu-id="e6664-109">Enumerate streams on the TAPI call.</span></span>
-   <span data-ttu-id="e6664-110">Selecione o terminal de faixa de arquivo no fluxo.</span><span class="sxs-lookup"><span data-stu-id="e6664-110">Select the File Track Terminal on the stream.</span></span>
-   <span data-ttu-id="e6664-111">Chame o método [**Start**](/windows/desktop/api/tapi3if/nf-tapi3if-itmediacontrol-start) no terminal de reprodução de arquivos para iniciar a reprodução de dados gravados nos fluxos TAPI.</span><span class="sxs-lookup"><span data-stu-id="e6664-111">Call the [**Start**](/windows/desktop/api/tapi3if/nf-tapi3if-itmediacontrol-start) method on the File Playback Terminal to start playback of recorded data to the TAPI streams.</span></span>

 

 



