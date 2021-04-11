---
title: Camada de depuração Direct2D
description: Uma extensão de tempo de execução para Direct2D que oferece mensagens de erro descritivas, detecção de vazamento de objeto, avisos de desempenho e outras indicações para ajudá-lo a criar aplicativos Direct2D.
ms.assetid: 23b522d4-0733-4892-b93d-28f899fa0f17
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f71b1364e645859059fb090634cbdae6f8c084e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104363737"
---
# <a name="direct2d-debug-layer"></a><span data-ttu-id="02453-103">Camada de depuração Direct2D</span><span class="sxs-lookup"><span data-stu-id="02453-103">Direct2D Debug Layer</span></span>

## <a name="purpose"></a><span data-ttu-id="02453-104">Finalidade</span><span class="sxs-lookup"><span data-stu-id="02453-104">Purpose</span></span>

<span data-ttu-id="02453-105">A camada de depuração Direct2D, implementada separadamente de Direct2D em sua própria DLL chamada d2d1debug.dll, fornece mensagens de depuração de tempo de design para você minimizar a falha do aplicativo em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="02453-105">The Direct2D debug layer, implemented separately from Direct2D in its own DLL named d2d1debug.dll, provides design-time debug messages for you to minimize runtime application failure.</span></span> <span data-ttu-id="02453-106">As mensagens de depuração geralmente resultam de violações de contratos de API, como parâmetros inválidos (podem ser relacionados a Direct3D), recursos inválidos, violações de threading e outros problemas de desempenho, como usar uma camada quando um clipe seria suficiente.</span><span class="sxs-lookup"><span data-stu-id="02453-106">The debug messages often result from violations of API contracts such as invalid parameters (could be Direct3D-related), invalid resources, threading violations, and other performance issues such as using a layer when a clip would suffice.</span></span>

<span data-ttu-id="02453-107">Para ajudá-lo a decidir a quantidade de informações rastreadas pela camada de depuração, a camada de depuração oferece três níveis de depuração: informações, aviso e erro.</span><span class="sxs-lookup"><span data-stu-id="02453-107">To help you decide how much information is traced by the debug layer, the debug layer offers three debug levels: information, warning, and error.</span></span> <span data-ttu-id="02453-108">Esses três níveis são interpretados da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="02453-108">These three levels are interpreted as follows:</span></span>

-   <span data-ttu-id="02453-109">**Erro:** Direct2D envia mensagens de erro graves para a camada de depuração.</span><span class="sxs-lookup"><span data-stu-id="02453-109">**Error:** Direct2D sends severe error messages to the debug layer.</span></span> <span data-ttu-id="02453-110">Por exemplo, interromper uma restrição de Threading irá gerar um erro grave.</span><span class="sxs-lookup"><span data-stu-id="02453-110">For example, breaking a threading constraint will generate a severe error.</span></span>

    <span data-ttu-id="02453-111">Além disso, uma mensagem de erro de nível dispara o ponto de interrupção para ajudá-lo a depurar.</span><span class="sxs-lookup"><span data-stu-id="02453-111">Further, a message of level error triggers the breakpoint to help you debug.</span></span>

-   <span data-ttu-id="02453-112">**AVISO:** O Direct2D envia mensagens de erro e avisos para a camada de depuração para que você possa endereçar qualquer uma dessas mensagens.</span><span class="sxs-lookup"><span data-stu-id="02453-112">**Warning:** Direct2D sends error messages and warnings to the debug layer so that you can address any of these messages.</span></span>

-   <span data-ttu-id="02453-113">**Informações:** O Direct2D envia mensagens de erro, avisos e informações adicionais de diagnóstico para a camada de depuração.</span><span class="sxs-lookup"><span data-stu-id="02453-113">**Information:** Direct2D sends error messages, warnings, and additional diagnostic information to the debug layer.</span></span> <span data-ttu-id="02453-114">Por exemplo, as mensagens de melhoria de desempenho serão enviadas neste nível de depuração.</span><span class="sxs-lookup"><span data-stu-id="02453-114">For example, performance improvement messages will be sent at this debug level.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="02453-115">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="02453-115">In this section</span></span>



| <span data-ttu-id="02453-116">Tópico</span><span class="sxs-lookup"><span data-stu-id="02453-116">Topic</span></span>                                                                                     | <span data-ttu-id="02453-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="02453-117">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="02453-118">Instalando a camada de depuração Direct2D</span><span class="sxs-lookup"><span data-stu-id="02453-118">Installing the Direct2D Debug Layer</span></span>](installing-the-direct2d-debug-layer.md)<br/> | <span data-ttu-id="02453-119">Descreve como instalar a camada de depuração Direct2D.</span><span class="sxs-lookup"><span data-stu-id="02453-119">Describes how to install the Direct2D debug layer.</span></span><br/>      |
| [<span data-ttu-id="02453-120">Visão geral da camada de depuração Direct2D</span><span class="sxs-lookup"><span data-stu-id="02453-120">Direct2D Debug Layer Overview</span></span>](direct2ddebuglayer-overview.md)<br/>               |                                                                    |
| [<span data-ttu-id="02453-121">Mensagens de depuração</span><span class="sxs-lookup"><span data-stu-id="02453-121">Debug Messages</span></span>](direct2ddebuglayer-debugmessages.md)<br/>                         | <span data-ttu-id="02453-122">Lista as mensagens de depuração da camada de depuração Direct2D.</span><span class="sxs-lookup"><span data-stu-id="02453-122">Lists the debug messages from the Direct2D Debug Layer.</span></span><br/> |



 

 

 





