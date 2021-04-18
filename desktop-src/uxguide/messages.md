---
title: Mensagens (noções básicas de Design)
description: As mensagens são qualquer tipo de mensagem que os usuários precisam ou desejam ver à medida que usam seu aplicativo. Saiba como apresentar erros, avisos, confirmações e notificações em seu aplicativo.
ms.assetid: 700F1F1F-B41D-4C0A-B2EC-91C84E46E526
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: dba3296c9824b2153184c45b6a021ea823b4d151
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "105770547"
---
# <a name="messages-design-basics"></a><span data-ttu-id="43793-104">Mensagens (noções básicas de Design)</span><span class="sxs-lookup"><span data-stu-id="43793-104">Messages (Design basics)</span></span>

> [!NOTE]
> <span data-ttu-id="43793-105">Este guia de design foi criado para o Windows 7 e não foi atualizado para versões mais recentes do Windows.</span><span class="sxs-lookup"><span data-stu-id="43793-105">This design guide was created for Windows 7 and has not been updated for newer versions of Windows.</span></span> <span data-ttu-id="43793-106">Grande parte da orientação ainda se aplica em princípio, mas a apresentação e os exemplos não refletem nossas [diretrizes de design atuais](/windows/uwp/design/).</span><span class="sxs-lookup"><span data-stu-id="43793-106">Much of the guidance still applies in principle, but the presentation and examples do not reflect our [current design guidance](/windows/uwp/design/).</span></span>

<span data-ttu-id="43793-107">As mensagens são qualquer tipo de mensagem que os usuários precisam ou desejam ver à medida que usam seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="43793-107">Messages are any kind of message users need or want to see as they use your app.</span></span> <span data-ttu-id="43793-108">Saiba como apresentar erros, avisos, confirmações e notificações em seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="43793-108">Learn how to present errors, warning, confirmations, and notifications in your app.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="43793-109">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="43793-109">In this section</span></span>



| <span data-ttu-id="43793-110">Tópico</span><span class="sxs-lookup"><span data-stu-id="43793-110">Topic</span></span>                                        | <span data-ttu-id="43793-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="43793-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                     |
|----------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="43793-112">Mensagens de erro</span><span class="sxs-lookup"><span data-stu-id="43793-112">Error Messages</span></span>](mess-error.md)<br/>  | <span data-ttu-id="43793-113">Uma mensagem de erro alerta os usuários sobre um problema que já ocorreu.</span><span class="sxs-lookup"><span data-stu-id="43793-113">An error message alerts users of a problem that has already occurred.</span></span> <span data-ttu-id="43793-114">Por outro lado, uma mensagem de aviso alerta os usuários de uma condição que pode causar um problema no futuro.</span><span class="sxs-lookup"><span data-stu-id="43793-114">By contrast, a warning message alerts users of a condition that might cause a problem in the future.</span></span> <span data-ttu-id="43793-115">As mensagens de erro podem ser apresentadas usando caixas de diálogo modais, mensagens in-loco, notificações ou balões.</span><span class="sxs-lookup"><span data-stu-id="43793-115">Error messages can be presented using modal dialog boxes, in-place messages, notifications, or balloons.</span></span><br/>                                                  |
| [<span data-ttu-id="43793-116">Mensagens de aviso</span><span class="sxs-lookup"><span data-stu-id="43793-116">Warning Messages</span></span>](mess-warn.md)<br/> | <span data-ttu-id="43793-117">Uma mensagem de aviso é uma caixa de diálogo modal, uma mensagem in-loco, uma notificação ou um balão que alerta o usuário sobre uma condição que pode causar um problema no futuro.</span><span class="sxs-lookup"><span data-stu-id="43793-117">A warning message is a modal dialog box, in-place message, notification, or balloon that alerts the user of a condition that might cause a problem in the future.</span></span><br/>                                                                                                                                                                    |
| [<span data-ttu-id="43793-118">Confirmações</span><span class="sxs-lookup"><span data-stu-id="43793-118">Confirmations</span></span>](mess-confirm.md)<br/> | <span data-ttu-id="43793-119">Uma confirmação é uma caixa de diálogo modal que pergunta se o usuário deseja prosseguir com uma ação.</span><span class="sxs-lookup"><span data-stu-id="43793-119">A confirmation is a modal dialog box that asks if the user wants to proceed with an action.</span></span><br/>                                                                                                                                                                                                                                          |
| [<span data-ttu-id="43793-120">Notificações</span><span class="sxs-lookup"><span data-stu-id="43793-120">Notifications</span></span>](mess-notif.md)<br/>   | <span data-ttu-id="43793-121">Uma notificação informa os usuários de eventos que não estão relacionados à atividade do usuário atual, exibindo brevemente um balão de um ícone na área de notificação.</span><span class="sxs-lookup"><span data-stu-id="43793-121">A notification informs users of events that are unrelated to the current user activity, by briefly displaying a balloon from an icon in the notification area.</span></span> <span data-ttu-id="43793-122">A notificação pode resultar de uma ação do usuário ou de um evento de sistema significativo ou pode oferecer informações potencialmente úteis do Microsoft Windows ou de um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="43793-122">The notification could result from a user action or significant system event, or could offer potentially useful information from Microsoft Windows or an application.</span></span><br/> |



 

 

