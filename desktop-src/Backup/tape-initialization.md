---
title: Inicialização de fita
description: Um aplicativo deve usar a função CreateFile para criar um identificador de um dispositivo de fita. Esse identificador é usado em operações subsequentes na fita do dispositivo.
ms.assetid: 5e7eddd2-8137-4e79-b1ee-c371bc4c7f75
keywords:
- Backup de inicialização de fita
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64f77b5c4d52641d2a3f195d517e575c9e2f780f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104454205"
---
# <a name="tape-initialization"></a><span data-ttu-id="5f12a-105">Inicialização de fita</span><span class="sxs-lookup"><span data-stu-id="5f12a-105">Tape Initialization</span></span>

<span data-ttu-id="5f12a-106">Um aplicativo deve usar a função [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) para criar um identificador de um dispositivo de fita.</span><span class="sxs-lookup"><span data-stu-id="5f12a-106">An application must use the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function to create a handle of a tape device.</span></span> <span data-ttu-id="5f12a-107">Esse identificador é usado em operações subsequentes na fita do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5f12a-107">This handle is used in subsequent operations on the tape in the device.</span></span>

<span data-ttu-id="5f12a-108">Antes que um aplicativo grave em uma fita, a fita deve ser formatada de acordo com as necessidades do aplicativo e os recursos da unidade de fita que está sendo usada.</span><span class="sxs-lookup"><span data-stu-id="5f12a-108">Before an application writes to a tape, the tape must be formatted according to the needs of the application and the capabilities of the tape drive being used.</span></span> <span data-ttu-id="5f12a-109">A função [**CreateTapePartition**](/windows/desktop/api/Winbase/nf-winbase-createtapepartition) reformata uma fita, criando um determinado número de partições de um tamanho especificado.</span><span class="sxs-lookup"><span data-stu-id="5f12a-109">The [**CreateTapePartition**](/windows/desktop/api/Winbase/nf-winbase-createtapepartition) function reformats a tape, creating on it a given number of partitions of a specified size.</span></span>

<span data-ttu-id="5f12a-110">A função [**PrepareTape**](/windows/desktop/api/Winbase/nf-winbase-preparetape) prepara uma fita para ser acessada ou removida.</span><span class="sxs-lookup"><span data-stu-id="5f12a-110">The [**PrepareTape**](/windows/desktop/api/Winbase/nf-winbase-preparetape) function prepares a tape to be accessed or removed.</span></span> <span data-ttu-id="5f12a-111">Essa função pode carregar, descarregar, bloquear ou desbloquear uma fita.</span><span class="sxs-lookup"><span data-stu-id="5f12a-111">This function can load, unload, lock, or unlock a tape.</span></span> <span data-ttu-id="5f12a-112">Essa função também pode esticar a fita movendo a fita para o fim da fita e de volta para o início.</span><span class="sxs-lookup"><span data-stu-id="5f12a-112">This function can also tension the tape by moving the tape to the end of the tape and back to the beginning.</span></span>

<span data-ttu-id="5f12a-113">Para recuperar e definir informações sobre uma fita e uma unidade de fita, um aplicativo usa as funções [**Gettapeparameters**](/windows/desktop/api/Winbase/nf-winbase-gettapeparameters), [**setfitaparameters**](/windows/desktop/api/Winbase/nf-winbase-settapeparameters)e [**GetTapeStatus**](/windows/desktop/api/Winbase/nf-winbase-gettapestatus) .</span><span class="sxs-lookup"><span data-stu-id="5f12a-113">To retrieve and set information about a tape and tape drive, an application uses the [**GetTapeParameters**](/windows/desktop/api/Winbase/nf-winbase-gettapeparameters), [**SetTapeParameters**](/windows/desktop/api/Winbase/nf-winbase-settapeparameters), and [**GetTapeStatus**](/windows/desktop/api/Winbase/nf-winbase-gettapestatus) functions.</span></span>

<span data-ttu-id="5f12a-114">[**Gettapeparameters**](/windows/desktop/api/Winbase/nf-winbase-gettapeparameters) recupera informações que descrevem uma fita ou uma unidade de fita.</span><span class="sxs-lookup"><span data-stu-id="5f12a-114">[**GetTapeParameters**](/windows/desktop/api/Winbase/nf-winbase-gettapeparameters) retrieves information that describes a tape or a tape drive.</span></span> <span data-ttu-id="5f12a-115">As informações da fita incluem o tipo, a densidade e o tamanho do bloco da fita; o número de partições na fita; a quantidade de fitas restantes; e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="5f12a-115">The tape information includes the tape's type, density, and block size; the number of partitions on the tape; the amount of tape remaining; and so on.</span></span> <span data-ttu-id="5f12a-116">As informações da unidade de fita incluem o tamanho do bloco padrão da unidade, a contagem máxima de partições e os recursos com suporte.</span><span class="sxs-lookup"><span data-stu-id="5f12a-116">The tape drive information includes the drive's default block size, the maximum partition count, and the features that are supported.</span></span>

<span data-ttu-id="5f12a-117">[**Setfitaparameters**](/windows/desktop/api/Winbase/nf-winbase-settapeparameters) define o tamanho do bloco de fita ou define os sinalizadores de unidade de fita que indicam se a unidade dá suporte a correção de erro de hardware, compactação de dados, enchimento de dados ou qualquer combinação dos três.</span><span class="sxs-lookup"><span data-stu-id="5f12a-117">[**SetTapeParameters**](/windows/desktop/api/Winbase/nf-winbase-settapeparameters) either sets the tape block size or sets the tape drive flags that indicate whether the drive supports hardware error correction, data compression, data padding, or any combination of the three.</span></span>

<span data-ttu-id="5f12a-118">[**GetTapeStatus**](/windows/desktop/api/Winbase/nf-winbase-gettapestatus) indica se a unidade de fita está pronta para processar comandos de fita.</span><span class="sxs-lookup"><span data-stu-id="5f12a-118">[**GetTapeStatus**](/windows/desktop/api/Winbase/nf-winbase-gettapestatus) indicates whether the tape drive is ready to process tape commands.</span></span>

 

 