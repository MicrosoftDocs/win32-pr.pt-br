---
title: Bluetooth e escutar, selecionar e fechamento
description: O Bluetooth usa as funções escutar, selecionar e fechamento sem qualquer modificação da programação padrão de soquetes do Windows.
ms.assetid: b64440de-bc63-4e3b-bfd9-5cf783f36c23
keywords:
- Bluetooth
- fechamento
- ouvir
- select
- Bluetooth e escutar
- Bluetooth e escutar, selecione
- Bluetooth e escutar, selecionar e fechamento
- ouvir
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e442cfc0593ab5be297902487c7c3ccdf056b4e0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104454161"
---
# <a name="bluetooth-and-listen-select-and-closesocket"></a><span data-ttu-id="d6241-111">Bluetooth e escutar, selecionar e fechamento</span><span class="sxs-lookup"><span data-stu-id="d6241-111">Bluetooth and listen, select, and closesocket</span></span>

<span data-ttu-id="d6241-112">O Bluetooth usa as funções [**escutar**](/windows/desktop/api/winsock2/nf-winsock2-listen), [**selecionar**](/windows/desktop/api/winsock2/nf-winsock2-select)e [**fechamento**](/windows/desktop/api/winsock/nf-winsock-closesocket) sem qualquer modificação da programação padrão de soquetes do Windows.</span><span class="sxs-lookup"><span data-stu-id="d6241-112">Bluetooth uses the [**listen**](/windows/desktop/api/winsock2/nf-winsock2-listen), [**select**](/windows/desktop/api/winsock2/nf-winsock2-select), and [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) functions without any modification from standard Windows Sockets programming.</span></span>

<span data-ttu-id="d6241-113">Assim como ocorre com o Windows Sockets, a função [**fechamento**](/windows/desktop/api/winsock/nf-winsock-closesocket) libera recursos associados ao soquete.</span><span class="sxs-lookup"><span data-stu-id="d6241-113">As with Windows Sockets, the [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) function frees resources associated with the socket.</span></span>

<span data-ttu-id="d6241-114">Ao chamar a função [**Listen**](/windows/desktop/api/winsock2/nf-winsock2-listen) , é altamente recomendável que um valor baixo seja usado para o parâmetro de lista de *pendências* (normalmente de 2 a 4), já que apenas algumas conexões de cliente são aceitas.</span><span class="sxs-lookup"><span data-stu-id="d6241-114">When calling the [**listen**](/windows/desktop/api/winsock2/nf-winsock2-listen) function, it is strongly recommended that a low value is used for the *backlog* parameter (typically 2 to 4), since only a few client connections are accepted.</span></span> <span data-ttu-id="d6241-115">Isso reduz os recursos do sistema que são alocados para uso pelo soquete de escuta.</span><span class="sxs-lookup"><span data-stu-id="d6241-115">This reduces the system resources that are allocated for use by the listening socket.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d6241-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d6241-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d6241-117">Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="d6241-117">Windows Sockets</span></span>](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[<span data-ttu-id="d6241-118">**fechamento**</span><span class="sxs-lookup"><span data-stu-id="d6241-118">**closesocket**</span></span>](/windows/desktop/api/winsock/nf-winsock-closesocket)
</dt> <dt>

[<span data-ttu-id="d6241-119">**ouvir**</span><span class="sxs-lookup"><span data-stu-id="d6241-119">**listen**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-listen)
</dt> <dt>

[<span data-ttu-id="d6241-120">**Não**</span><span class="sxs-lookup"><span data-stu-id="d6241-120">**select**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-select)
</dt> </dl>

 

 