---
title: Bluetooth e getsockopt
description: O Bluetooth usa a função getsockopt para consultar vários parâmetros associados ao canal do servidor ou à conexão.
ms.assetid: 9593fd6c-b55d-45d8-a9d9-87ebcd09d1bd
keywords:
- Bluetooth
- getsockopt
- Bluetooth e getsockopt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dede19b27eea39b7d1e778b3e92312a5e148c0ec
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641365"
---
# <a name="bluetooth-and-getsockopt"></a><span data-ttu-id="756de-106">Bluetooth e getsockopt</span><span class="sxs-lookup"><span data-stu-id="756de-106">Bluetooth and getsockopt</span></span>

<span data-ttu-id="756de-107">O Bluetooth usa a função [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) para consultar vários parâmetros associados ao canal do servidor ou à conexão.</span><span class="sxs-lookup"><span data-stu-id="756de-107">Bluetooth uses the [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) function to query various parameters associated with the server channel or the connection.</span></span> <span data-ttu-id="756de-108">O uso de **getsockopt** com Bluetooth tem os seguintes requisitos:</span><span class="sxs-lookup"><span data-stu-id="756de-108">Use of **getsockopt** with Bluetooth has the following requirements:</span></span>

-   <span data-ttu-id="756de-109">O parâmetro *s* de [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) deve ser um soquete Bluetooth válido.</span><span class="sxs-lookup"><span data-stu-id="756de-109">The *s* parameter of [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) must be a valid Bluetooth socket.</span></span>
-   <span data-ttu-id="756de-110">O parâmetro de *nível* de [**GETSOCKOPT**](/windows/desktop/api/winsock/nf-winsock-getsockopt) deve ser sol \_ RFCOMM.</span><span class="sxs-lookup"><span data-stu-id="756de-110">The *level* parameter of [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) must be SOL\_RFCOMM.</span></span>

<span data-ttu-id="756de-111">Para obter uma lista de opções de soquete Bluetooth disponíveis, consulte [Opções de soquete e Bluetooth](bluetooth-and-socket-options.md).</span><span class="sxs-lookup"><span data-stu-id="756de-111">For a listing of available Bluetooth socket options, see [Bluetooth and Socket Options](bluetooth-and-socket-options.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="756de-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="756de-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="756de-113">Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="756de-113">Windows Sockets</span></span>](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[<span data-ttu-id="756de-114">**getsockopt**</span><span class="sxs-lookup"><span data-stu-id="756de-114">**getsockopt**</span></span>](/windows/desktop/api/winsock/nf-winsock-getsockopt)
</dt> </dl>

 

 