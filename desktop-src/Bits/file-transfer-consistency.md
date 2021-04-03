---
title: Consistência de transferência de arquivo
description: O BITS garante que a versão do arquivo que ele transfere seja consistente com base no tamanho do arquivo e no carimbo de data/hora, não conteúdo (o BITS não protege contra ataques man-in-the-Middle).
ms.assetid: ba82f172-a3ac-49d6-bccd-7d0b68ba66de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 533bc0c0db9708528d4ae919572d6e4c1d251ac8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822298"
---
# <a name="file-transfer-consistency"></a><span data-ttu-id="79946-103">Consistência de transferência de arquivo</span><span class="sxs-lookup"><span data-stu-id="79946-103">File Transfer Consistency</span></span>

<span data-ttu-id="79946-104">O BITS garante que a versão do arquivo que ele transfere seja consistente com base no tamanho do arquivo e no carimbo de data/hora, não conteúdo (o BITS não protege contra ataques man-in-the-Middle).</span><span class="sxs-lookup"><span data-stu-id="79946-104">BITS guarantees that the version of the file it transfers is consistent based on the file size and time stamp, not content (BITS does not protect against man-in-the-middle attacks).</span></span> <span data-ttu-id="79946-105">Para verificar o conteúdo por conta própria, você pode usar o método [**IBackgroundCopyFile3:: Gettemporárioname**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyfile3-gettemporaryname) para obter o nome do arquivo que contém o conteúdo baixado, verificar o conteúdo usando seu próprio mecanismo e, em seguida, chamar o método [**IBackgroundCopyFile3:: setvalidable**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyfile3-setvalidationstate) para indicar ao bits se o conteúdo do arquivo for válido.</span><span class="sxs-lookup"><span data-stu-id="79946-105">To verify the contents yourself, you can use the [**IBackgroundCopyFile3::GetTemporaryName**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyfile3-gettemporaryname) method to get the name of the file that contains the downloaded content, verify the contents using your own mechanism, and then call the [**IBackgroundCopyFile3::SetValidationState**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyfile3-setvalidationstate) method to indicate to BITS if the contents of the file is valid.</span></span> <span data-ttu-id="79946-106">Se você definir o estado de validação como **false** e o conteúdo for do servidor de origem, o trabalho entrará no estado de erro.</span><span class="sxs-lookup"><span data-stu-id="79946-106">If you set the validation state to **FALSE** and the content is from the origin server, the job goes into the error state.</span></span> <span data-ttu-id="79946-107">Se o conteúdo for de um par, o BITS baixará o arquivo do servidor de origem.</span><span class="sxs-lookup"><span data-stu-id="79946-107">If the content is from a peer, BITS downloads the file from the origin server.</span></span>

<span data-ttu-id="79946-108">Para downloads, se o tamanho do arquivo ou o carimbo de data/hora for alterado enquanto o BITS estiver transferindo o arquivo, o BITS reiniciará a transferência somente desse arquivo.</span><span class="sxs-lookup"><span data-stu-id="79946-108">For downloads, if the file size or time stamp changes while BITS is transferring the file, BITS restarts the transfer of that file only.</span></span> <span data-ttu-id="79946-109">Por exemplo, se o trabalho de download contiver dois arquivos e os arquivos forem atualizados no servidor enquanto o BITS estiver transferindo o segundo arquivo, o BITS reiniciará a transferência somente do segundo arquivo.</span><span class="sxs-lookup"><span data-stu-id="79946-109">For example, if the download job contains two files and the files are updated on the server while BITS is transferring the second file, BITS restarts the transfer of the second file only.</span></span> <span data-ttu-id="79946-110">O primeiro arquivo, que já foi transferido com êxito, não é atualizado para refletir as novas alterações.</span><span class="sxs-lookup"><span data-stu-id="79946-110">The first file, which already transferred successfully, is not updated to reflect the new changes.</span></span>

<span data-ttu-id="79946-111">Observe que, se você possuir o arquivo que está sendo baixado do servidor, deverá criar uma nova URL para cada nova versão do arquivo.</span><span class="sxs-lookup"><span data-stu-id="79946-111">Note that if you own the file being downloaded from the server, you should create a new URL for each new version of the file.</span></span> <span data-ttu-id="79946-112">Se você usar a mesma URL para novas versões do arquivo, alguns servidores proxy poderão atender a dados obsoletos de seu cache porque eles não verificam com o servidor original se o arquivo está obsoleto.</span><span class="sxs-lookup"><span data-stu-id="79946-112">If you use the same URL for new versions of the file, some proxy servers may serve stale data from their cache because they do not verify with the original server if the file is stale.</span></span>

<span data-ttu-id="79946-113">Para carregamentos, se o tamanho do arquivo ou o carimbo de data/hora for alterado durante a transferência de arquivo, o BITS gerará um erro e o trabalho será colocado no estado de erro BG do \_ estado do trabalho \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="79946-113">For uploads, if the file size or time stamp changes during the file transfer, BITS generates an error and the job is placed in the BG\_JOB\_STATE\_ERROR state.</span></span>

<span data-ttu-id="79946-114">O BITS não sincroniza solicitações de transferência quando um ou mais usuários solicitam que o mesmo arquivo seja transferido para o mesmo local.</span><span class="sxs-lookup"><span data-stu-id="79946-114">BITS does not synchronize transfer requests when one or more users request that the same file be transferred to the same location.</span></span> <span data-ttu-id="79946-115">O BITS transfere o arquivo para cada solicitação separadamente.</span><span class="sxs-lookup"><span data-stu-id="79946-115">BITS transfers the file for each request separately.</span></span>

 

 




