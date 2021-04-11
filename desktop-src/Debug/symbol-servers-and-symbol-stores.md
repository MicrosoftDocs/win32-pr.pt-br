---
description: Configurar símbolos corretamente para depuração pode ser uma tarefa desafiadora, especialmente para a depuração de kernel.
ms.assetid: 96b2c9db-58fb-4c28-b17c-3b1cc06ed96b
title: '{1&gt;{2&gt;Servidor e repositórios de símbolos&lt;2}&lt;1}'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 644410fcb929308a259c5fc752f55742bfb23bae
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104163980"
---
# <a name="symbol-server-and-symbol-stores"></a><span data-ttu-id="ad51a-103">{1&gt;{2&gt;Servidor e repositórios de símbolos&lt;2}&lt;1}</span><span class="sxs-lookup"><span data-stu-id="ad51a-103">Symbol Server and Symbol Stores</span></span>

<span data-ttu-id="ad51a-104">Configurar símbolos corretamente para depuração pode ser uma tarefa desafiadora, especialmente para a depuração de kernel.</span><span class="sxs-lookup"><span data-stu-id="ad51a-104">Setting up symbols correctly for debugging can be a challenging task, particularly for kernel debugging.</span></span> <span data-ttu-id="ad51a-105">Geralmente, é necessário que você conheça os nomes e as versões de todos os produtos em seu computador.</span><span class="sxs-lookup"><span data-stu-id="ad51a-105">It often requires that you know the names and releases of all products on your computer.</span></span> <span data-ttu-id="ad51a-106">O depurador deve ser capaz de localizar os arquivos de símbolo que correspondem a cada versão do produto e service pack.</span><span class="sxs-lookup"><span data-stu-id="ad51a-106">The debugger must be able to locate the symbol files that correspond to each product release and service pack.</span></span> <span data-ttu-id="ad51a-107">Isso pode resultar em um caminho de símbolo muito longo que consiste em uma longa lista de diretórios.</span><span class="sxs-lookup"><span data-stu-id="ad51a-107">This can result in an extremely long symbol path consisting of a long list of directories.</span></span>

<span data-ttu-id="ad51a-108">Para simplificar essas dificuldades na coordenação de arquivos de símbolo, use o *servidor de símbolos*.</span><span class="sxs-lookup"><span data-stu-id="ad51a-108">To simplify these difficulties in coordinating symbol files, use the *symbol server*.</span></span> <span data-ttu-id="ad51a-109">O servidor de símbolos permite que os depuradores recuperem automaticamente os arquivos de símbolo corretos sem nomes de produtos, versões ou números de Build.</span><span class="sxs-lookup"><span data-stu-id="ad51a-109">The symbol server enables the debuggers to automatically retrieve the correct symbol files without product names, releases, or build numbers.</span></span> <span data-ttu-id="ad51a-110">As ferramentas de depuração para Windows contêm o servidor de símbolos SymSrv.</span><span class="sxs-lookup"><span data-stu-id="ad51a-110">Debugging Tools for Windows contains the SymSrv symbol server.</span></span>

<span data-ttu-id="ad51a-111">O servidor de símbolos é ativado incluindo uma determinada cadeia de texto no caminho do símbolo.</span><span class="sxs-lookup"><span data-stu-id="ad51a-111">The symbol server is activated by including a certain text string in the symbol path.</span></span> <span data-ttu-id="ad51a-112">Cada vez que o depurador precisa carregar símbolos para um módulo carregado recentemente, ele chama o servidor de símbolos para localizar os arquivos de símbolo apropriados.</span><span class="sxs-lookup"><span data-stu-id="ad51a-112">Each time the debugger needs to load symbols for a newly loaded module, it calls the symbol server to locate the appropriate symbol files.</span></span> <span data-ttu-id="ad51a-113">O servidor de símbolos localiza os arquivos em um *repositório de símbolos*.</span><span class="sxs-lookup"><span data-stu-id="ad51a-113">The symbol server locates the files in a *symbol store*.</span></span> <span data-ttu-id="ad51a-114">Essa é uma coleção de arquivos de símbolos, um índice e uma ferramenta que podem ser usados por um administrador para adicionar e excluir arquivos.</span><span class="sxs-lookup"><span data-stu-id="ad51a-114">This is a collection of symbol files, an index, and a tool that can be used by an administrator to add and delete files.</span></span> <span data-ttu-id="ad51a-115">Os arquivos são indexados de acordo com parâmetros exclusivos, como o carimbo de data/hora e o tamanho da imagem.</span><span class="sxs-lookup"><span data-stu-id="ad51a-115">The files are indexed according to unique parameters such as the time stamp and image size.</span></span> <span data-ttu-id="ad51a-116">As ferramentas de depuração para Windows contêm uma ferramenta de armazenamento de símbolos chamada SymStore.</span><span class="sxs-lookup"><span data-stu-id="ad51a-116">Debugging Tools for Windows contains a symbol store tool called SymStore.</span></span>

<span data-ttu-id="ad51a-117">Para obter mais informações, consulte:</span><span class="sxs-lookup"><span data-stu-id="ad51a-117">For more information, see:</span></span>

-   [<span data-ttu-id="ad51a-118">Usando SymSrv</span><span class="sxs-lookup"><span data-stu-id="ad51a-118">Using SymSrv</span></span>](using-symsrv.md)
-   [<span data-ttu-id="ad51a-119">Usando SymStore</span><span class="sxs-lookup"><span data-stu-id="ad51a-119">Using SymStore</span></span>](using-symstore.md)
-   [<span data-ttu-id="ad51a-120">Usando outros armazenamentos de símbolo</span><span class="sxs-lookup"><span data-stu-id="ad51a-120">Using Other Symbol Stores</span></span>](using-other-symbol-stores.md)
-   [<span data-ttu-id="ad51a-121">Opções de Command-Line de SymStore</span><span class="sxs-lookup"><span data-stu-id="ad51a-121">SymStore Command-Line Options</span></span>](symstore-command-line-options.md)
-   [<span data-ttu-id="ad51a-122">Servidores de símbolos e firewalls da Internet</span><span class="sxs-lookup"><span data-stu-id="ad51a-122">Symbol Server and Internet Firewalls</span></span>](symbol-servers-and-internet-firewalls.md)

## <a name="related-topics"></a><span data-ttu-id="ad51a-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ad51a-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ad51a-124">Arquivos de Símbolo</span><span class="sxs-lookup"><span data-stu-id="ad51a-124">Symbol Files</span></span>](symbol-files.md)
</dt> </dl>

 

 



