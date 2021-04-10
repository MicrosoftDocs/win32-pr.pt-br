---
title: Bluetooth e setsockopt
description: O Bluetooth usa a função setsockopt para definir vários parâmetros associados ao canal do servidor ou à conexão.
ms.assetid: ab78baed-5556-4d7b-88a6-e3ceb93afa8c
keywords:
- Bluetooth
- setsockopt
- Bluetooth e setsockopt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 943839a49788b76e597596aee9cba65fa4b8d30d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294129"
---
# <a name="bluetooth-and-setsockopt"></a><span data-ttu-id="bcc50-106">Bluetooth e setsockopt</span><span class="sxs-lookup"><span data-stu-id="bcc50-106">Bluetooth and setsockopt</span></span>

<span data-ttu-id="bcc50-107">O Bluetooth usa a função [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) para definir vários parâmetros associados ao canal do servidor ou à conexão.</span><span class="sxs-lookup"><span data-stu-id="bcc50-107">Bluetooth uses the [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function to set various parameters associated with the server channel or the connection.</span></span> <span data-ttu-id="bcc50-108">O uso de **setsockopt** com Bluetooth tem os seguintes requisitos:</span><span class="sxs-lookup"><span data-stu-id="bcc50-108">Use of **setsockopt** with Bluetooth has the following requirements:</span></span>

-   <span data-ttu-id="bcc50-109">O parâmetro *s* de [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) deve ser um soquete Bluetooth válido.</span><span class="sxs-lookup"><span data-stu-id="bcc50-109">The *s* parameter of [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) must be a valid Bluetooth socket.</span></span>
-   <span data-ttu-id="bcc50-110">O parâmetro de *nível* de [**SETSOCKOPT**](/windows/desktop/api/winsock/nf-winsock-setsockopt) deve ser sol \_ RFCOMM.</span><span class="sxs-lookup"><span data-stu-id="bcc50-110">The *level* parameter of [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) must be SOL\_RFCOMM.</span></span>

<span data-ttu-id="bcc50-111">Para obter uma lista de opções de soquete Bluetooth disponíveis, consulte [Opções de soquete e Bluetooth](bluetooth-and-socket-options.md).</span><span class="sxs-lookup"><span data-stu-id="bcc50-111">For a listing of available Bluetooth socket options, see [Bluetooth and Socket Options](bluetooth-and-socket-options.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="bcc50-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="bcc50-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bcc50-113">Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="bcc50-113">Windows Sockets</span></span>](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[<span data-ttu-id="bcc50-114">**setsockopt**</span><span class="sxs-lookup"><span data-stu-id="bcc50-114">**setsockopt**</span></span>](/windows/desktop/api/winsock/nf-winsock-setsockopt)
</dt> </dl>

 

 