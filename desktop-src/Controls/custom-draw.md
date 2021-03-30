---
title: Desenho personalizado
description: O desenho personalizado não é um controle comum; é um serviço que muitos controles comuns fornecem.
ms.assetid: vs|controls|~\controls\custdraw\custdraw.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5184d06dbb8e04185bf12a43c6c71dd96b933a6a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916073"
---
# <a name="custom-draw"></a><span data-ttu-id="d8b01-103">Desenho personalizado</span><span class="sxs-lookup"><span data-stu-id="d8b01-103">Custom Draw</span></span>

<span data-ttu-id="d8b01-104">O desenho personalizado não é um controle comum; é um serviço que muitos controles comuns fornecem.</span><span class="sxs-lookup"><span data-stu-id="d8b01-104">Custom draw is not a common control; it is a service that many common controls provide.</span></span> <span data-ttu-id="d8b01-105">O serviço de desenho personalizado permite a um aplicativo maior flexibilidade na personalização da aparência de um controle.</span><span class="sxs-lookup"><span data-stu-id="d8b01-105">The custom draw service allows an application greater flexibility in customizing a control's appearance.</span></span> <span data-ttu-id="d8b01-106">Seu aplicativo pode aproveitar notificações de desenho personalizadas para alterar facilmente a fonte usada para exibir itens ou desenhar manualmente um item sem precisar fazer um desenho de proprietário completo.</span><span class="sxs-lookup"><span data-stu-id="d8b01-106">Your application can harness custom draw notifications to easily change the font used to display items or manually draw an item without having to do a full owner draw.</span></span>

<span data-ttu-id="d8b01-107">Esta seção contém informações sobre os elementos de programação usados com o desenho personalizado.</span><span class="sxs-lookup"><span data-stu-id="d8b01-107">This section contains information about the programming elements used with custom draw.</span></span>

## <a name="overviews"></a><span data-ttu-id="d8b01-108">Visões gerais</span><span class="sxs-lookup"><span data-stu-id="d8b01-108">Overviews</span></span>



| <span data-ttu-id="d8b01-109">Tópico</span><span class="sxs-lookup"><span data-stu-id="d8b01-109">Topic</span></span>                                      | <span data-ttu-id="d8b01-110">Sumário</span><span class="sxs-lookup"><span data-stu-id="d8b01-110">Contents</span></span>                                                                                                                                                               |
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d8b01-111">Sobre o desenho personalizado</span><span class="sxs-lookup"><span data-stu-id="d8b01-111">About Custom Draw</span></span>](about-custom-draw.md) | <span data-ttu-id="d8b01-112">Esta seção contém informações gerais sobre a funcionalidade de desenho Personalizada e fornece uma visão geral conceitual de como um aplicativo pode dar suporte a desenho personalizado.</span><span class="sxs-lookup"><span data-stu-id="d8b01-112">This section contains general information about custom draw functionality and provides a conceptual overview of how an application can support custom draw.</span></span><br/> |
| [<span data-ttu-id="d8b01-113">Usando o desenho personalizado</span><span class="sxs-lookup"><span data-stu-id="d8b01-113">Using Custom Draw</span></span>](using-custom-draw.md) | <span data-ttu-id="d8b01-114">Esta seção contém exemplos que demonstram como implementar o desenho personalizado.</span><span class="sxs-lookup"><span data-stu-id="d8b01-114">This section contains examples that demonstrate how to implement custom draw.</span></span> <br/>                                                                              |



 

## <a name="notifications"></a><span data-ttu-id="d8b01-115">Notificações</span><span class="sxs-lookup"><span data-stu-id="d8b01-115">Notifications</span></span>



| <span data-ttu-id="d8b01-116">Tópico</span><span class="sxs-lookup"><span data-stu-id="d8b01-116">Topic</span></span>                               | <span data-ttu-id="d8b01-117">Sumário</span><span class="sxs-lookup"><span data-stu-id="d8b01-117">Contents</span></span>                                                                                                                                                                 |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d8b01-118">\_CUSTOMDRAW nm</span><span class="sxs-lookup"><span data-stu-id="d8b01-118">NM\_CUSTOMDRAW</span></span>](nm-customdraw.md) | <span data-ttu-id="d8b01-119">Notifica uma janela pai do controle sobre as operações de desenho personalizadas.</span><span class="sxs-lookup"><span data-stu-id="d8b01-119">Notifies a control's parent window about custom drawing operations.</span></span> <span data-ttu-id="d8b01-120">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="d8b01-120">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span> <br/> |



 

## <a name="structures"></a><span data-ttu-id="d8b01-121">Estruturas</span><span class="sxs-lookup"><span data-stu-id="d8b01-121">Structures</span></span>



| <span data-ttu-id="d8b01-122">Tópico</span><span class="sxs-lookup"><span data-stu-id="d8b01-122">Topic</span></span>                                | <span data-ttu-id="d8b01-123">Sumário</span><span class="sxs-lookup"><span data-stu-id="d8b01-123">Contents</span></span>                                                                                              |
|--------------------------------------|-------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d8b01-124">**NMCUSTOMDRAW**</span><span class="sxs-lookup"><span data-stu-id="d8b01-124">**NMCUSTOMDRAW**</span></span>](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) | <span data-ttu-id="d8b01-125">Contém informações específicas para um código de notificação [nm \_ CUSTOMDRAW](nm-customdraw.md) .</span><span class="sxs-lookup"><span data-stu-id="d8b01-125">Contains information specific to an [NM\_CUSTOMDRAW](nm-customdraw.md) notification code.</span></span><br/> |



 

 

 





