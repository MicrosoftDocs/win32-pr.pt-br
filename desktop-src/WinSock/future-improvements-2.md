---
description: Melhorias futuras no código do aplicativo Winsock de exemplo.
ms.assetid: 317baa53-6bc8-42bd-8f56-480cab29ae6b
title: Aprimoramentos futuros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 938f38334a4bbe392e83efc0be12905fb7ae66a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105763070"
---
# <a name="future-improvements"></a><span data-ttu-id="17d1f-103">Aprimoramentos futuros</span><span class="sxs-lookup"><span data-stu-id="17d1f-103">Future Improvements</span></span>

<span data-ttu-id="17d1f-104">Há várias melhorias que podem ser feitas nesse aplicativo, como:</span><span class="sxs-lookup"><span data-stu-id="17d1f-104">There are several improvements that can be made to this application, such as:</span></span>

-   <span data-ttu-id="17d1f-105">Uma conexão única e persistente pode ser criada pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="17d1f-105">A single, persistent connection could be created by the application.</span></span> <span data-ttu-id="17d1f-106">O tratamento de erros apropriado teria que ser adicionado.</span><span class="sxs-lookup"><span data-stu-id="17d1f-106">Appropriate error handling would have to be added.</span></span> <span data-ttu-id="17d1f-107">Isso reduziria a sobrecarga associada à inicialização e à desmontagem da conexão.</span><span class="sxs-lookup"><span data-stu-id="17d1f-107">This would reduce the overhead associated with connection startup and teardown.</span></span>
-   <span data-ttu-id="17d1f-108">O código de resposta no servidor pode ser otimizado para consolidar respostas, reduzindo o número de pacotes enviados do servidor.</span><span class="sxs-lookup"><span data-stu-id="17d1f-108">The reply code on the server could be optimized to consolidate replies, reducing the number of packets sent from the server.</span></span>
-   <span data-ttu-id="17d1f-109">As melhorias no protocolo podem ser feitas.</span><span class="sxs-lookup"><span data-stu-id="17d1f-109">Improvements in the protocol could be made.</span></span> <span data-ttu-id="17d1f-110">Por exemplo, um bitmask de atualização poderia ser usado para significar quais células devem ser atualizadas e apenas os dados de célula enviados.</span><span class="sxs-lookup"><span data-stu-id="17d1f-110">For example, an update bitmask could be used to signify which cells are to be updated, and only that cell data sent.</span></span>
-   <span data-ttu-id="17d1f-111">As atualizações podem ser sobrepostas usando threads diferentes, para que a rede não fique ociosa enquanto a função **ComputeNext** estiver em execução.</span><span class="sxs-lookup"><span data-stu-id="17d1f-111">Updates could be overlapped using different threads, so that the network is not idle while the **ComputeNext** function is running.</span></span>

## <a name="related-topics"></a><span data-ttu-id="17d1f-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="17d1f-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="17d1f-113">Melhorando um aplicativo lento</span><span class="sxs-lookup"><span data-stu-id="17d1f-113">Improving a Slow Application</span></span>](improving-a-slow-application-2.md)
</dt> <dt>

[<span data-ttu-id="17d1f-114">A versão de linha de base: um aplicativo com muito mau desempenho</span><span class="sxs-lookup"><span data-stu-id="17d1f-114">The Baseline Version: A Very Poor Performing Application</span></span>](the-baseline-version-a-very-poor-performing-application-2.md)
</dt> <dt>

[<span data-ttu-id="17d1f-115">Revisão 1: limpando o óbvio</span><span class="sxs-lookup"><span data-stu-id="17d1f-115">Revision 1: Cleaning up the Obvious</span></span>](revision-1-cleaning-up-the-obvious-2.md)
</dt> <dt>

[<span data-ttu-id="17d1f-116">Revisão 2: redesignação para menos conexões</span><span class="sxs-lookup"><span data-stu-id="17d1f-116">Revision 2: Redesigning for Fewer Connects</span></span>](revision-2-redesigning-for-fewer-connects-2.md)
</dt> <dt>

[<span data-ttu-id="17d1f-117">Revisão 3: envio de bloco compactado</span><span class="sxs-lookup"><span data-stu-id="17d1f-117">Revision 3: Compressed Block Send</span></span>](revision-3-compressed-block-send-2.md)
</dt> </dl>

 

 



