---
title: Estruturas (mensagens de entrada do ponteiro e notificações)
description: Os tópicos nesta seção fornecem as especificações de referência para mensagens de entrada de ponteiro e estruturas de notificações.
ms.assetid: 2224DCD0-DAE1-4AC2-AB36-23D114801138
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: bc796c3924df9a1a349ea2180123f88f56d6a96c
ms.sourcegitcommit: 4570ac533e129ff88b23f2c2b69e0140ead3a4a4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/26/2021
ms.locfileid: "105798314"
---
# <a name="pointer-input-messages-and-notifications-structures"></a><span data-ttu-id="2c16e-103">Estruturas de mensagens e notificações de entrada de ponteiro</span><span class="sxs-lookup"><span data-stu-id="2c16e-103">Pointer Input Messages and Notifications structures</span></span>

<span data-ttu-id="2c16e-104">Os tópicos nesta seção fornecem as especificações de referência para [mensagens de entrada de ponteiro e](messages-and-notifications-portal.md) estruturas de notificações.</span><span class="sxs-lookup"><span data-stu-id="2c16e-104">The topics in this section provide the reference specifications for [Pointer Input Messages and Notifications](messages-and-notifications-portal.md) structures.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="2c16e-105">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="2c16e-105">In this section</span></span>



| <span data-ttu-id="2c16e-106">Tópico</span><span class="sxs-lookup"><span data-stu-id="2c16e-106">Topic</span></span>                                                                            | <span data-ttu-id="2c16e-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="2c16e-107">Description</span></span>                                                                                                                                                                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2c16e-108">**INPUT_TRANSFORM**</span><span class="sxs-lookup"><span data-stu-id="2c16e-108">**INPUT_TRANSFORM**</span></span>](/previous-versions/windows/desktop/api)<br/>                           | <span data-ttu-id="2c16e-109">Define a matriz que representa uma transformação em um consumidor de mensagem.</span><span class="sxs-lookup"><span data-stu-id="2c16e-109">Defines the matrix that represents a transform on a message consumer.</span></span> <span data-ttu-id="2c16e-110">Essa matriz pode ser usada para transformar dados de entrada de ponteiro de coordenadas de cliente em coordenadas de tela, enquanto o inverso pode ser usado para transformar dados de entrada de ponteiro de coordenadas de tela em coordenadas de cliente.</span><span class="sxs-lookup"><span data-stu-id="2c16e-110">This matrix can be used to transform pointer input data from client coordinates to screen coordinates, while the inverse can be used to transform pointer input data from screen coordinates to client coordinates.</span></span> <br/>                                                                 |
| [<span data-ttu-id="2c16e-111">**POINTER_INFO**</span><span class="sxs-lookup"><span data-stu-id="2c16e-111">**POINTER_INFO**</span></span>](/previous-versions/windows/desktop/api)<br/>                          | <span data-ttu-id="2c16e-112">Contém informações básicas de ponteiros comuns a todos os tipos de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="2c16e-112">Contains basic pointer information common to all pointer types.</span></span> <span data-ttu-id="2c16e-113">Os aplicativos podem recuperar essas informações usando as funções [**GetPointerInfo**](/previous-versions/windows/desktop/api), [**GetPointerFrameInfo**](/previous-versions/windows/desktop/api), [**GetPointerInfoHistory**](/previous-versions/windows/desktop/api) e [**GetPointerFrameInfoHistory**](/previous-versions/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="2c16e-113">Applications can retrieve this information using the [**GetPointerInfo**](/previous-versions/windows/desktop/api), [**GetPointerFrameInfo**](/previous-versions/windows/desktop/api), [**GetPointerInfoHistory**](/previous-versions/windows/desktop/api) and [**GetPointerFrameInfoHistory**](/previous-versions/windows/desktop/api) functions.</span></span> <br/> |
| [<span data-ttu-id="2c16e-114">**POINTER_PEN_INFO**</span><span class="sxs-lookup"><span data-stu-id="2c16e-114">**POINTER_PEN_INFO**</span></span>](/previous-versions/windows/desktop/api)<br/>                 | <span data-ttu-id="2c16e-115">Define informações básicas sobre a caneta comum a todos os tipos de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="2c16e-115">Defines basic pen information common to all pointer types.</span></span> <br/>                                                                                                                                                                                                                                                                                                |
| [<span data-ttu-id="2c16e-116">**POINTER_TOUCH_INFO**</span><span class="sxs-lookup"><span data-stu-id="2c16e-116">**POINTER_TOUCH_INFO**</span></span>](/previous-versions/windows/desktop/api)<br/>             | <span data-ttu-id="2c16e-117">Define informações de toque básico comuns a todos os tipos de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="2c16e-117">Defines basic touch information common to all pointer types.</span></span><br/>                                                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="2c16e-118">**TOUCHPREDICTIONPARAMETERS**</span><span class="sxs-lookup"><span data-stu-id="2c16e-118">**TOUCHPREDICTIONPARAMETERS**</span></span>](/previous-versions/windows/desktop/api)<br/> | <span data-ttu-id="2c16e-119">Contém detalhes de entrada de hardware que podem ser usados para prever destinos de toque e ajudar a compensar a latência de hardware ao processar a entrada de toque e de gesto que contém dados de distância e velocidade.</span><span class="sxs-lookup"><span data-stu-id="2c16e-119">Contains hardware input details that can be used to predict touch targets and help compensate for hardware latency when processing touch and gesture input that contains distance and velocity data.</span></span><br/>                                                                                                                                                       |



 

## <a name="related-topics"></a><span data-ttu-id="2c16e-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2c16e-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2c16e-121">Referência de mensagem de entrada do ponteiro</span><span class="sxs-lookup"><span data-stu-id="2c16e-121">Pointer Input Message Reference</span></span>](wmpointer-reference.md)
</dt> </dl>

 

 





