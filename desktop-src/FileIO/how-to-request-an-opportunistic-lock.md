---
description: Os bloqueios oportunistas são solicitados abrindo primeiro um arquivo com permissões e sinalizadores apropriados para o aplicativo que abre o arquivo. Todos os arquivos para os quais os bloqueios oportunistas serão solicitados devem ser abertos para a operação sobreposta (assíncrona).
ms.assetid: a55d38c6-46e3-48e6-9b5b-d4f4234d8c07
title: Como solicitar um bloqueio oportunista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0dd6b99eb32ce191db78b55c4f8b79dafa340b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103836999"
---
# <a name="how-to-request-an-opportunistic-lock"></a><span data-ttu-id="57033-104">Como solicitar um bloqueio oportunista</span><span class="sxs-lookup"><span data-stu-id="57033-104">How to Request an Opportunistic Lock</span></span>

<span data-ttu-id="57033-105">Os aplicativos cliente solicitam diretamente os bloqueios oportunistas somente quando o bloqueio é destinado a um arquivo no servidor local.</span><span class="sxs-lookup"><span data-stu-id="57033-105">Client applications directly request opportunistic locks only when the lock is intended for a file on the local server.</span></span> <span data-ttu-id="57033-106">Ao acessar arquivos em servidores remotos, ele é o redirecionador de rede, e não o aplicativo cliente, que solicita o bloqueio oportunista do servidor remoto.</span><span class="sxs-lookup"><span data-stu-id="57033-106">When accessing files on remote servers, it is the network redirector, and not the client application, that requests the opportunistic lock from the remote server.</span></span>

<span data-ttu-id="57033-107">Os bloqueios oportunistas são solicitados abrindo primeiro um arquivo com permissões e sinalizadores apropriados para o aplicativo que abre o arquivo.</span><span class="sxs-lookup"><span data-stu-id="57033-107">Opportunistic locks are requested by first opening a file with permissions and flags appropriate to the application opening the file.</span></span> <span data-ttu-id="57033-108">Todos os arquivos para os quais os bloqueios oportunistas serão solicitados devem ser abertos para a operação sobreposta (assíncrona).</span><span class="sxs-lookup"><span data-stu-id="57033-108">All files for which opportunistic locks will be requested must be opened for overlapped (asynchronous) operation.</span></span> <span data-ttu-id="57033-109">Depois que os arquivos forem abertos para operação sobreposta, use a função [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) com o código de controle apropriado para solicitar um bloqueio oportunista.</span><span class="sxs-lookup"><span data-stu-id="57033-109">After the files are opened for overlapped operation, use the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function with the appropriate control code to request an opportunistic lock.</span></span> <span data-ttu-id="57033-110">Para obter uma lista das operações de bloqueio oportunista, consulte [operações de bloqueio oportunista](opportunistic-lock-operations.md).</span><span class="sxs-lookup"><span data-stu-id="57033-110">For a list of the opportunistic lock operations, see [Opportunistic Lock Operations](opportunistic-lock-operations.md).</span></span>

<span data-ttu-id="57033-111">Os aplicativos são notificados de que um bloqueio oportunista é interrompido usando o membro **hEvent** da estrutura [**sobreposta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) associada ao arquivo.</span><span class="sxs-lookup"><span data-stu-id="57033-111">Applications are notified that an opportunistic lock is broken by using the **hEvent** member of the [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure associated with the file.</span></span> <span data-ttu-id="57033-112">Os aplicativos também podem usar funções como [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) e [**HasOverlappedIoCompleted**](/windows/desktop/api/winbase/nf-winbase-hasoverlappediocompleted).</span><span class="sxs-lookup"><span data-stu-id="57033-112">Applications may also use functions such as [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) and [**HasOverlappedIoCompleted**](/windows/desktop/api/winbase/nf-winbase-hasoverlappediocompleted).</span></span> <span data-ttu-id="57033-113">O aplicativo é responsável por associar o arquivo correto ao bloqueio oportunista rompido.</span><span class="sxs-lookup"><span data-stu-id="57033-113">The application is responsible for associating the correct file with the broken opportunistic lock.</span></span>

<span data-ttu-id="57033-114">Para obter mais informações sobre notificação, consulte [sincronização](/windows/desktop/Sync/synchronization).</span><span class="sxs-lookup"><span data-stu-id="57033-114">For more information on notification, see [Synchronization](/windows/desktop/Sync/synchronization).</span></span>

 

 
