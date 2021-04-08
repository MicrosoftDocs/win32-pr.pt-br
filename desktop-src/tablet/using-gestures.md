---
description: Visão geral do uso de gestos.
ms.assetid: 5bc80086-7acf-4f86-a9fb-a663de489f8b
title: Usando gestos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53c267cff446d1bb6d092ba50bde21c1b3e25184
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920880"
---
# <a name="using-gestures"></a><span data-ttu-id="7378b-103">Usando gestos</span><span class="sxs-lookup"><span data-stu-id="7378b-103">Using Gestures</span></span>

<span data-ttu-id="7378b-104">A plataforma do Tablet PC fornece o reconhecedor de gestos da Microsoft para dar suporte a gestos de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7378b-104">The Tablet PC platform provides the Microsoft gesture recognizer for supporting application gestures.</span></span> <span data-ttu-id="7378b-105">Para obter uma lista de gestos com suporte pelo reconhecedor de gestos da Microsoft, consulte a tabela de gestos de aplicativo na enumeração [**ApplicationGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture) .</span><span class="sxs-lookup"><span data-stu-id="7378b-105">For a list of gestures supported by the Microsoft gesture recognizer, see the table of application gestures in the [**ApplicationGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture) enumeration.</span></span> <span data-ttu-id="7378b-106">O Tablet PC também dá suporte a gestos do sistema.</span><span class="sxs-lookup"><span data-stu-id="7378b-106">The Tablet PC also supports system gestures.</span></span> <span data-ttu-id="7378b-107">Para obter uma lista de gestos do sistema com suporte pelo Tablet PC, consulte a tabela de gestos do sistema na enumeração [**SystemGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) .</span><span class="sxs-lookup"><span data-stu-id="7378b-107">For a list of system gestures supported by the Tablet PC, see the table of system gestures in the [**SystemGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) enumeration.</span></span>

## <a name="microsoft-gesture-recognizer"></a><span data-ttu-id="7378b-108">Reconhecedor de gestos da Microsoft</span><span class="sxs-lookup"><span data-stu-id="7378b-108">Microsoft Gesture Recognizer</span></span>

<span data-ttu-id="7378b-109">Você pode empregar o reconhecedor de gestos da Microsoft usando a propriedade [**CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectionmode) do objeto [**InkCollector**](inkcollector-class.md) , o objeto [**InkOverlay**](inkoverlay-class.md) ou o controle [InkPicture](inkpicture-control-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="7378b-109">You can employ the Microsoft gesture recognizer by using the [**CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectionmode) property of the [**InkCollector**](inkcollector-class.md) object, the [**InkOverlay**](inkoverlay-class.md) object, or the [InkPicture](inkpicture-control-reference.md) control.</span></span> <span data-ttu-id="7378b-110">A definição da propriedade **CollectionMode** como modo misto (**InkAndGesture**) ou modo somente de gesto (**GestureOnly**) passa a tinta para o reconhecedor de gestos da Microsoft por padrão.</span><span class="sxs-lookup"><span data-stu-id="7378b-110">Setting the **CollectionMode** property to mixed mode (**InkAndGesture**) or gesture-only mode (**GestureOnly**) passes ink to the Microsoft gesture recognizer by default.</span></span> <span data-ttu-id="7378b-111">Você pode empregar o reconhecedor de gestos da Microsoft com o controle [InkEdit](inkedit-control-reference.md) definindo a propriedade [**InkMode**](/windows/desktop/api/inked/nf-inked-iinkedit-get_inkmode) como **InkAndGesture**.</span><span class="sxs-lookup"><span data-stu-id="7378b-111">You can employ the Microsoft gesture recognizer with the [InkEdit](inkedit-control-reference.md) control by setting the [**InkMode**](/windows/desktop/api/inked/nf-inked-iinkedit-get_inkmode) property to **InkAndGesture**.</span></span> <span data-ttu-id="7378b-112">Você também pode usar o reconhecimento de gesto com o objeto [**RealTimeStylus**](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylus) adicionando um objeto [**GestureRecognizer**](gesturerecognizer-class.md) a uma de suas coleções de plug-ins.</span><span class="sxs-lookup"><span data-stu-id="7378b-112">You can also use gesture recognition with the [**RealTimeStylus**](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylus) object by adding a [**GestureRecognizer**](gesturerecognizer-class.md) object to one of its plug-in collections.</span></span>

<span data-ttu-id="7378b-113">No entanto, se os gestos que você deseja usar não forem suportados pela versão atual do reconhecedor de gestos da Microsoft, você poderá criar seu próprio reconhecedor e usá-lo em conjunto com o reconhecedor de gestos da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="7378b-113">However, if the gestures that you want to use are not supported by the current version of the Microsoft gesture recognizer, you can build your own recognizer and use it in conjunction with the Microsoft gesture recognizer.</span></span> <span data-ttu-id="7378b-114">Isso permite o suporte completo para os gestos em seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7378b-114">This allows full support for the gestures in your application.</span></span>

<span data-ttu-id="7378b-115">O Tablet PC usa uma caneta para algumas ou todas as entradas.</span><span class="sxs-lookup"><span data-stu-id="7378b-115">The Tablet PC uses a pen for some or all input.</span></span> <span data-ttu-id="7378b-116">Isso torna extremamente fácil escrever tinta.</span><span class="sxs-lookup"><span data-stu-id="7378b-116">This makes it extremely easy to write ink.</span></span> <span data-ttu-id="7378b-117">A plataforma do Tablet PC fornece arquitetura para entrada à caneta que dá suporte a uma estrutura em camadas de gestos.</span><span class="sxs-lookup"><span data-stu-id="7378b-117">The Tablet PC platform delivers architecture for pen input that supports a tiered structure of gestures.</span></span> <span data-ttu-id="7378b-118">Os gestos e o mapeamento são definidos para permitir que o usuário escreva e invoque gestos avançados em novas superfícies, enquanto reserva gestos que chamam mensagens de mouse tradicionais de outros aplicativos baseados no Windows.</span><span class="sxs-lookup"><span data-stu-id="7378b-118">Gestures and mapping are defined to allow the user to write and invoke advanced gestures on new surfaces, while reserving gestures that invoke traditional mouse messages of other Windows-based applications.</span></span>

<span data-ttu-id="7378b-119">A plataforma do Tablet PC apresenta dois níveis de gestos: gestos do sistema, também conhecidos como eventos do sistema e gestos do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7378b-119">The Tablet PC platform introduces two levels of gestures: system gestures, also known as system events, and application gestures.</span></span> <span data-ttu-id="7378b-120">A arquitetura da caneta dá suporte a gestos do sistema e do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7378b-120">The pen architecture supports both system and application gestures.</span></span> <span data-ttu-id="7378b-121">Há suporte para gestos de aplicativo com traço único e vários traços.</span><span class="sxs-lookup"><span data-stu-id="7378b-121">Both single-stroke and multiple-stroke application gestures are supported.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7378b-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7378b-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7378b-123">Gestos de aplicativo</span><span class="sxs-lookup"><span data-stu-id="7378b-123">Application Gestures</span></span>](application-gestures.md)
</dt> <dt>

[<span data-ttu-id="7378b-124">Gestos de movimentos</span><span class="sxs-lookup"><span data-stu-id="7378b-124">Flicks Gestures</span></span>](flicks-gestures.md)
</dt> <dt>

[<span data-ttu-id="7378b-125">Gestos do sistema</span><span class="sxs-lookup"><span data-stu-id="7378b-125">System Gestures</span></span>](system-gestures.md)
</dt> </dl>

 

 



