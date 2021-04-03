---
description: Este tópico fornece um procedimento para executar a gravação controlada por controle de fluxos de áudio.
ms.assetid: 57df081f-df41-4187-910b-939e3d82d7a0
title: Registro de Track-Controlled
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 366b996e590c313cec3ca2e67e12008403e4a4cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828674"
---
# <a name="track-controlled-record"></a><span data-ttu-id="26d09-103">Registro de Track-Controlled</span><span class="sxs-lookup"><span data-stu-id="26d09-103">Track-Controlled Record</span></span>

<span data-ttu-id="26d09-104">Este tópico fornece um procedimento para executar a gravação controlada por controle de fluxos de áudio.</span><span class="sxs-lookup"><span data-stu-id="26d09-104">This topic provides a procedure for performing track-controlled recording of audio streams.</span></span>

<span data-ttu-id="26d09-105">**Para executar a gravação controlada pelo controle de fluxos de áudio**</span><span class="sxs-lookup"><span data-stu-id="26d09-105">**To perform track-controlled recording of audio streams**</span></span>

1.  <span data-ttu-id="26d09-106">Selecione Arquivo faixas terminais em fluxos.</span><span class="sxs-lookup"><span data-stu-id="26d09-106">Select File Track Terminals onto streams.</span></span>
2.  <span data-ttu-id="26d09-107">Crie o terminal de registro de arquivo.</span><span class="sxs-lookup"><span data-stu-id="26d09-107">Create the File Record Terminal.</span></span>
3.  <span data-ttu-id="26d09-108">Defina o nome do arquivo.</span><span class="sxs-lookup"><span data-stu-id="26d09-108">Set the file name.</span></span>
4.  <span data-ttu-id="26d09-109">Enumere os fluxos na chamada TAPI.</span><span class="sxs-lookup"><span data-stu-id="26d09-109">Enumerate streams on the TAPI call.</span></span> <span data-ttu-id="26d09-110">Para essas etapas, consulte o procedimento a seguir.</span><span class="sxs-lookup"><span data-stu-id="26d09-110">For these steps, see the following procedure.</span></span>
5.  <span data-ttu-id="26d09-111">Chame o método [**Start**](/windows/desktop/api/tapi3if/nf-tapi3if-itmediacontrol-start) no terminal de registro de arquivo para iniciar a gravação de fluxo.</span><span class="sxs-lookup"><span data-stu-id="26d09-111">Call the [**Start**](/windows/desktop/api/tapi3if/nf-tapi3if-itmediacontrol-start) method on the File Record Terminal to start stream recording.</span></span>

<span data-ttu-id="26d09-112">**Para enumerar fluxos na chamada TAPI**</span><span class="sxs-lookup"><span data-stu-id="26d09-112">**To enumerate streams on the TAPI call**</span></span>

1.  <span data-ttu-id="26d09-113">Crie uma faixa do mesmo tipo e direção de áudio que o fluxo.</span><span class="sxs-lookup"><span data-stu-id="26d09-113">Create a track of the same audio type and direction as the stream.</span></span>
2.  <span data-ttu-id="26d09-114">Defina as propriedades da faixa para o formato de áudio.</span><span class="sxs-lookup"><span data-stu-id="26d09-114">Set the track properties for audio format.</span></span> <span data-ttu-id="26d09-115">Se não estiver definido, o formato será o mesmo que o formato de fluxos.</span><span class="sxs-lookup"><span data-stu-id="26d09-115">If not set, the format will be the same as the streams format.</span></span>
3.  <span data-ttu-id="26d09-116">Selecione a faixa no fluxo.</span><span class="sxs-lookup"><span data-stu-id="26d09-116">Select the track on the stream.</span></span>

<span data-ttu-id="26d09-117">Se uma faixa for selecionada em vários fluxos, isso implica misturar fluxos.</span><span class="sxs-lookup"><span data-stu-id="26d09-117">If one track is selected on multiple streams, this implies mixing streams.</span></span>

 

 



