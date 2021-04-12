---
title: Sobre o WER
description: O Relatório de Erros do Windows (WER) é uma infra-estrutura de comentários flexível baseada em eventos, criada para coletar informações sobre os problemas de hardware e software que o Windows pode detectar, relatar as informações à Microsoft e fornecer aos usuários qualquer solução disponível. Para obter informações sobre os aprimoramentos do WER, consulte What ' s New in WER.
ms.assetid: d26b3d2a-51cf-41d9-936b-f1b45778ea61
keywords:
- Relatório de Erros do Windows de relatório de erros do Windows, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37ab7622c3e0b3a7bebff64e6c8373f2d163ba23
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292415"
---
# <a name="about-wer"></a><span data-ttu-id="93483-105">Sobre o WER</span><span class="sxs-lookup"><span data-stu-id="93483-105">About WER</span></span>

<span data-ttu-id="93483-106">O Relatório de Erros do Windows (WER) é uma infra-estrutura de comentários flexível baseada em eventos, criada para coletar informações sobre os problemas de hardware e software que o Windows pode detectar, relatar as informações à Microsoft e fornecer aos usuários qualquer solução disponível.</span><span class="sxs-lookup"><span data-stu-id="93483-106">Windows Error Reporting (WER) is a flexible event-based feedback infrastructure designed to gather information about the hardware and software problems that Windows can detect, report the information to Microsoft, and provide users with any available solutions.</span></span> <span data-ttu-id="93483-107">Para obter informações sobre os aprimoramentos do WER, consulte [What ' s New in WER](what-s-new-in-wer.md).</span><span class="sxs-lookup"><span data-stu-id="93483-107">For information about the improvements to WER, see [What's New in WER](what-s-new-in-wer.md).</span></span>

<span data-ttu-id="93483-108">A partir do Windows Vista, o Windows fornece falha, sem resposta e relatório de erros de falha do kernel por padrão, sem a necessidade de alterações no seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="93483-108">Beginning with Windows Vista, Windows provides crash, no response, and kernel fault error reporting by default without requiring changes to your application.</span></span> <span data-ttu-id="93483-109">Em vez disso, os aplicativos usam a API WER para gerar relatórios de erros para problemas específicos do aplicativo que não estão relacionados a falhas, não respostas ou falha do kernel.</span><span class="sxs-lookup"><span data-stu-id="93483-109">Applications instead use the WER API to generate error reports for application-specific issues that are not related to crashes, non-responses, or kernel faults.</span></span>

<span data-ttu-id="93483-110">Para gerar relatórios de erros para problemas específicos do aplicativo, o aplicativo deve criar uma breve descrição do problema usando algumas partes básicas de informações denominadas *parâmetros de relatório*.</span><span class="sxs-lookup"><span data-stu-id="93483-110">To generate error reports for application-specific issues, the application must create a short description of the problem using a few basic pieces of information called *report parameters*.</span></span> <span data-ttu-id="93483-111">Os parâmetros de relatório incluem informações como o nome do aplicativo, a versão do aplicativo, o nome do módulo, a versão do módulo e o código de erro.</span><span class="sxs-lookup"><span data-stu-id="93483-111">Report parameters include information such as the application name, application version, module name, module version, and error code.</span></span> <span data-ttu-id="93483-112">A combinação desses parâmetros de relatório descreve um problema exclusivo.</span><span class="sxs-lookup"><span data-stu-id="93483-112">The combination of these report parameters describes a unique problem.</span></span>

<span data-ttu-id="93483-113">Quando o WER verifica uma solução, ele se comunica com o servidor WER na Microsoft perguntando primeiro se o problema já é conhecido.</span><span class="sxs-lookup"><span data-stu-id="93483-113">When WER checks for a solution, it communicates with the WER server at Microsoft by first asking if the problem is already known.</span></span> <span data-ttu-id="93483-114">O servidor responde de uma das seguintes maneiras:</span><span class="sxs-lookup"><span data-stu-id="93483-114">The server responds in one of the following ways:</span></span>

-   <span data-ttu-id="93483-115">Se o problema for conhecido e houver uma solução, o servidor enviará a solução para o computador cliente e o WER exibirá essas informações para o usuário.</span><span class="sxs-lookup"><span data-stu-id="93483-115">If the problem is known and there is a solution, the server sends the solution to the client computer and WER displays this information to the user.</span></span>
-   <span data-ttu-id="93483-116">Se o problema estiver sendo investigado, o servidor poderá enviar uma resposta que indica o status.</span><span class="sxs-lookup"><span data-stu-id="93483-116">If the problem is being investigated, the server may send a response that indicates the status.</span></span> <span data-ttu-id="93483-117">Se o desenvolvedor precisar de mais informações para resolver o problema, o servidor solicitará informações adicionais do WER e o WER solicitará permissão ao usuário para enviar essas informações.</span><span class="sxs-lookup"><span data-stu-id="93483-117">If the developer needs more information to solve the problem, the server requests additional information from WER and WER asks the user for permission to send this information.</span></span>
-   <span data-ttu-id="93483-118">Se o problema não for conhecido, o servidor criará um problema para um desenvolvedor investigar e enviar uma resposta de WER que indica o status.</span><span class="sxs-lookup"><span data-stu-id="93483-118">If the problem is not known, the server creates an issue for a developer to investigate and sends WER a response that indicates the status.</span></span>

<span data-ttu-id="93483-119">Usando esse processo, o WER coleta mais informações, se necessário, ou envia uma solução para o usuário quando disponível.</span><span class="sxs-lookup"><span data-stu-id="93483-119">Using this process, WER gathers more information if needed or sends a solution to the user when available.</span></span> <span data-ttu-id="93483-120">No Windows Vista, o usuário pode ir para **relatórios de problemas e soluções** a qualquer momento para exibir as soluções disponíveis, verificar se novas soluções estão disponíveis ou gerenciar seus outros relatórios e configurações do WER.</span><span class="sxs-lookup"><span data-stu-id="93483-120">On Windows Vista, the user can go to **Problem Reports and Solutions** at any time to view available solutions, check whether new solutions are available, or manage their other WER reports and settings.</span></span> <span data-ttu-id="93483-121">No Windows 7, os **relatórios de problemas e as soluções** agora são chamados de **central de ações**.</span><span class="sxs-lookup"><span data-stu-id="93483-121">On Windows 7, the **Problem Reports and Solutions** is now called the **Action Center**.</span></span> <span data-ttu-id="93483-122">Clique **em Iniciar** e digite "exibir" em **Pesquisar programas e arquivos** e, em seguida, selecione **Exibir todos os relatórios de problemas**, **Exibir histórico de confiabilidade** ou **Exibir soluções para problemas**.</span><span class="sxs-lookup"><span data-stu-id="93483-122">Click **Start** and enter "view" in **Search programs and files** and then select **View all problem reports**, **View reliability history**, or **View solutions to problems**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="93483-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="93483-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="93483-124">Relatório de Erros do Windows</span><span class="sxs-lookup"><span data-stu-id="93483-124">Windows Error Reporting</span></span>](windows-error-reporting.md)
</dt> </dl>

 

 




