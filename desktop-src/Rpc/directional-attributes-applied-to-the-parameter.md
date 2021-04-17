---
title: Atributos direcionais aplicados ao parâmetro
description: Os atributos direcionais \ in \ e \ out \ determinam como o cliente e o servidor alocam e liberam memória. A tabela a seguir resume o efeito de atributos direcionais na alocação de memória.
ms.assetid: 21ab54c4-a707-4ee3-bea8-8ba216e25c16
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 752432836075b319483e3a17421f691a111689b4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105759343"
---
# <a name="directional-attributes-applied-to-the-parameter"></a><span data-ttu-id="84a4a-104">Atributos direcionais aplicados ao parâmetro</span><span class="sxs-lookup"><span data-stu-id="84a4a-104">Directional Attributes Applied to the Parameter</span></span>

<span data-ttu-id="84a4a-105">Os atributos direcionais \[ [dentro](/windows/desktop/Midl/in) \] e \[ [fora](/windows/desktop/Midl/out-idl) \] determinam como o cliente e o servidor alocam e liberam memória.</span><span class="sxs-lookup"><span data-stu-id="84a4a-105">The directional attributes \[ [in](/windows/desktop/Midl/in)\] and \[ [out](/windows/desktop/Midl/out-idl)\] determine how the client and server allocate and free memory.</span></span> <span data-ttu-id="84a4a-106">A tabela a seguir resume o efeito de atributos direcionais na alocação de memória.</span><span class="sxs-lookup"><span data-stu-id="84a4a-106">The following table summarizes the effect of directional attributes on memory allocation.</span></span>



| <span data-ttu-id="84a4a-107">Atributo direcional</span><span class="sxs-lookup"><span data-stu-id="84a4a-107">Directional attribute</span></span>    | <span data-ttu-id="84a4a-108">Memória no cliente</span><span class="sxs-lookup"><span data-stu-id="84a4a-108">Memory on client</span></span>                                                                                            | <span data-ttu-id="84a4a-109">Memória no servidor</span><span class="sxs-lookup"><span data-stu-id="84a4a-109">Memory on server</span></span>                                                                                                                                        |
|--------------------------|-------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="84a4a-110">\[[em](/windows/desktop/Midl/in)\]</span><span class="sxs-lookup"><span data-stu-id="84a4a-110">\[ [in](/windows/desktop/Midl/in)\]</span></span>       | <span data-ttu-id="84a4a-111">O aplicativo cliente deve alocar antes da chamada.</span><span class="sxs-lookup"><span data-stu-id="84a4a-111">Client application must allocate before the call.</span></span>                                                           | <span data-ttu-id="84a4a-112">O stub do servidor é alocado.</span><span class="sxs-lookup"><span data-stu-id="84a4a-112">Server stub allocates.</span></span>                                                                                                                                  |
| <span data-ttu-id="84a4a-113">\[[out](/windows/desktop/Midl/out-idl)\]</span><span class="sxs-lookup"><span data-stu-id="84a4a-113">\[ [out](/windows/desktop/Midl/out-idl)\]</span></span> | <span data-ttu-id="84a4a-114">O stub do cliente se aloca no retorno.</span><span class="sxs-lookup"><span data-stu-id="84a4a-114">Client stub allocates on return.</span></span>                                                                            | <span data-ttu-id="84a4a-115">O stub do servidor aloca somente o ponteiro de nível superior; o aplicativo de servidor deve alocar todos os ponteiros inseridos.</span><span class="sxs-lookup"><span data-stu-id="84a4a-115">Server stub allocates top-level pointer only; the server application must allocate all embedded pointers.</span></span> <span data-ttu-id="84a4a-116">O servidor também aloca novos dados conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="84a4a-116">The server also allocates new data as needed.</span></span> |
| <span data-ttu-id="84a4a-117">\[**entrada**, **saída**\]</span><span class="sxs-lookup"><span data-stu-id="84a4a-117">\[**in**, **out**\]</span></span>      | <span data-ttu-id="84a4a-118">O aplicativo cliente deve alocar dados iniciais transmitidos ao servidor; o stub do cliente aloca dados adicionais.</span><span class="sxs-lookup"><span data-stu-id="84a4a-118">Client application must allocate initial data transmitted to server; client stub allocates additional data.</span></span> | <span data-ttu-id="84a4a-119">O stub do servidor aloca dados iniciais transmitidos do cliente; o aplicativo de servidor aloca novos dados conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="84a4a-119">Server stub allocates initial data transmitted from client; the server application allocates new data as needed.</span></span>                                        |



 

<span data-ttu-id="84a4a-120">Em todos esses casos, o stub do cliente não libera memória.</span><span class="sxs-lookup"><span data-stu-id="84a4a-120">In all of these cases the client stub does not free memory.</span></span> <span data-ttu-id="84a4a-121">O aplicativo cliente deve liberar a memória antes de ser encerrado.</span><span class="sxs-lookup"><span data-stu-id="84a4a-121">The client application must free the memory before it terminates.</span></span> <span data-ttu-id="84a4a-122">O stub de servidor libera memória quando a chamada de procedimento remoto retorna (sujeito ao \[ atributo [ALLOCATE](/windows/desktop/Midl/allocate) \] ACF).</span><span class="sxs-lookup"><span data-stu-id="84a4a-122">The server stub frees memory when the remote procedure call returns (subject to the \[ [allocate](/windows/desktop/Midl/allocate)\] ACF attribute).</span></span>

 

 