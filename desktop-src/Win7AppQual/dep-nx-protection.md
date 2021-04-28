---
description: Proteção de DEP/NX
ms.assetid: 92F628E4-6106-42F7-B868-A3101C7A3F0A
title: Proteção de DEP/NX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3565460cbfd2e6b13c3c5ba6b1f0693a3d5b25ba
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088564"
---
# <a name="depnx-protection"></a><span data-ttu-id="c1935-103">Proteção de DEP/NX</span><span class="sxs-lookup"><span data-stu-id="c1935-103">DEP/NX Protection</span></span>

<span data-ttu-id="c1935-104">A partir do Windows Internet Explorer 7 no Windows Vista, o item do painel de controle da Internet inclui uma opção **habilitar proteção de memória** para ajudar a mitigar os ataques online.</span><span class="sxs-lookup"><span data-stu-id="c1935-104">Starting with Windows Internet Explorer 7 on Windows Vista, the Internet control panel item includes an **Enable memory protection** option to help mitigate online attacks.</span></span> <span data-ttu-id="c1935-105">Essa opção também é conhecida como DEP ( *prevenção de execução de dados* ) ou *não executar* (NX).</span><span class="sxs-lookup"><span data-stu-id="c1935-105">This option is also referred to as *Data Execution Prevention* (DEP) or *No-Execute* (NX).</span></span> <span data-ttu-id="c1935-106">Quando essa opção está habilitada, ela funciona com o processador para ajudar a evitar ataques de estouro de buffer bloqueando a execução de código da memória marcada como não executável.</span><span class="sxs-lookup"><span data-stu-id="c1935-106">When this option is enabled, it works with the processor to help prevent buffer overflow attacks by blocking code execution from memory that is marked as non-executable.</span></span>

<span data-ttu-id="c1935-107">No Windows Internet Explorer 8 no sistema operacional Windows Vista com Service Pack 1 (SP1) ou em uma versão posterior, essa opção é habilitada por padrão.</span><span class="sxs-lookup"><span data-stu-id="c1935-107">In Windows Internet Explorer 8 on the Windows Vista with Service Pack 1 (SP1) operating system or a later version, this option is enabled by default.</span></span> <span data-ttu-id="c1935-108">O DEP/NX não protege contra todas as vulnerabilidades baseadas em memória.</span><span class="sxs-lookup"><span data-stu-id="c1935-108">DEP/NX does not protect against all memory-based vulnerabilities.</span></span> <span data-ttu-id="c1935-109">Mas quando ele é combinado com outras tecnologias como o ASLR (Address Space layout Randomization), ele ajuda a evitar vulnerabilidades de estouro de buffer comuns no Windows Internet Explorer e os complementos que ele carrega.</span><span class="sxs-lookup"><span data-stu-id="c1935-109">But when it is combined with other technologies like Address Space Layout Randomization (ASLR), it helps prevent common buffer overflow vulnerabilities in Windows Internet Explorer and the add-ons that it loads.</span></span> <span data-ttu-id="c1935-110">Nenhuma interação adicional do usuário é necessária para fornecer essa proteção, e nenhum prompt novo é introduzido.</span><span class="sxs-lookup"><span data-stu-id="c1935-110">No additional user interaction is required to provide this protection, and no new prompts are introduced.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c1935-111">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c1935-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c1935-112">Corrigindo problemas de compatibilidade em aplicativos Web usando o modo de exibição de compatibilidade</span><span class="sxs-lookup"><span data-stu-id="c1935-112">Fixing Compatibility Issues in Web Applications by Using Compatibility View</span></span>](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 



