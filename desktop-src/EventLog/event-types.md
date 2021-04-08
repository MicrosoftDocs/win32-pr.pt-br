---
description: Há cinco tipos de eventos que podem ser registrados em log. Todos eles têm dados comuns bem definidos e podem, opcionalmente, incluir dados específicos de eventos.
ms.assetid: 4ab4a284-a4cd-4cf7-a9d2-e4a75fce01b9
title: Tipos de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3832f90ccdb8dafc676c139f92665efde732533c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827952"
---
# <a name="event-types"></a><span data-ttu-id="cc8f8-104">Tipos de eventos</span><span class="sxs-lookup"><span data-stu-id="cc8f8-104">Event Types</span></span>

<span data-ttu-id="cc8f8-105">Há cinco tipos de eventos que podem ser registrados em log.</span><span class="sxs-lookup"><span data-stu-id="cc8f8-105">There are five types of events that can be logged.</span></span> <span data-ttu-id="cc8f8-106">Todos eles têm dados comuns bem definidos e podem, opcionalmente, incluir dados específicos de eventos.</span><span class="sxs-lookup"><span data-stu-id="cc8f8-106">All of these have well-defined common data and can optionally include event-specific data.</span></span>

<span data-ttu-id="cc8f8-107">O aplicativo indica o tipo de evento quando relata um evento.</span><span class="sxs-lookup"><span data-stu-id="cc8f8-107">The application indicates the event type when it reports an event.</span></span> <span data-ttu-id="cc8f8-108">Cada evento deve ser de um único tipo.</span><span class="sxs-lookup"><span data-stu-id="cc8f8-108">Each event must be of a single type.</span></span> <span data-ttu-id="cc8f8-109">O Visualizador de Eventos exibe um ícone diferente para cada tipo na exibição de lista do log de eventos.</span><span class="sxs-lookup"><span data-stu-id="cc8f8-109">The Event Viewer displays a different icon for each type in the list view of the event log.</span></span>

<span data-ttu-id="cc8f8-110">A tabela a seguir descreve os cinco tipos de evento usados no log de eventos.</span><span class="sxs-lookup"><span data-stu-id="cc8f8-110">The following table describes the five event types used in event logging.</span></span>



| <span data-ttu-id="cc8f8-111">Tipo de evento</span><span class="sxs-lookup"><span data-stu-id="cc8f8-111">Event type</span></span>        | <span data-ttu-id="cc8f8-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="cc8f8-112">Description</span></span>                                                                                                                                                                                                                                                                                              |
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc8f8-113">**Erro**</span><span class="sxs-lookup"><span data-stu-id="cc8f8-113">**Error**</span></span>         | <span data-ttu-id="cc8f8-114">Um evento que indica um problema significativo, como perda de dados ou perda de funcionalidade.</span><span class="sxs-lookup"><span data-stu-id="cc8f8-114">An event that indicates a significant problem such as loss of data or loss of functionality.</span></span> <span data-ttu-id="cc8f8-115">Por exemplo, se um serviço não for carregado durante a inicialização, um evento de erro será registrado.</span><span class="sxs-lookup"><span data-stu-id="cc8f8-115">For example, if a service fails to load during startup, an Error event is logged.</span></span>                                                                                                                           |
| <span data-ttu-id="cc8f8-116">**Aviso**</span><span class="sxs-lookup"><span data-stu-id="cc8f8-116">**Warning**</span></span>       | <span data-ttu-id="cc8f8-117">Um evento que não é necessariamente significativo, mas pode indicar um possível problema futuro.</span><span class="sxs-lookup"><span data-stu-id="cc8f8-117">An event that is not necessarily significant, but may indicate a possible future problem.</span></span> <span data-ttu-id="cc8f8-118">Por exemplo, quando há pouco espaço em disco, um evento de aviso é registrado.</span><span class="sxs-lookup"><span data-stu-id="cc8f8-118">For example, when disk space is low, a Warning event is logged.</span></span> <span data-ttu-id="cc8f8-119">Se um aplicativo puder se recuperar de um evento sem perda de funcionalidade ou dados, ele geralmente poderá classificar o evento como um evento de aviso.</span><span class="sxs-lookup"><span data-stu-id="cc8f8-119">If an application can recover from an event without loss of functionality or data, it can generally classify the event as a Warning event.</span></span>     |
| <span data-ttu-id="cc8f8-120">**Informações**</span><span class="sxs-lookup"><span data-stu-id="cc8f8-120">**Information**</span></span>   | <span data-ttu-id="cc8f8-121">Um evento que descreve a operação bem-sucedida de um aplicativo, driver ou serviço.</span><span class="sxs-lookup"><span data-stu-id="cc8f8-121">An event that describes the successful operation of an application, driver, or service.</span></span> <span data-ttu-id="cc8f8-122">Por exemplo, quando um driver de rede é carregado com êxito, pode ser apropriado registrar um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="cc8f8-122">For example, when a network driver loads successfully, it may be appropriate to log an Information event.</span></span> <span data-ttu-id="cc8f8-123">Observe que geralmente é inapropriado que um aplicativo de área de trabalho registre um evento sempre que ele for iniciado.</span><span class="sxs-lookup"><span data-stu-id="cc8f8-123">Note that it is generally inappropriate for a desktop application to log an event each time it starts.</span></span> |
| <span data-ttu-id="cc8f8-124">**Auditoria Bem-sucedida**</span><span class="sxs-lookup"><span data-stu-id="cc8f8-124">**Success Audit**</span></span> | <span data-ttu-id="cc8f8-125">Um evento que registra uma tentativa de acesso de segurança auditada que é bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="cc8f8-125">An event that records an audited security access attempt that is successful.</span></span> <span data-ttu-id="cc8f8-126">Por exemplo, a tentativa bem-sucedida do usuário de fazer logon no sistema é registrada como um evento de auditoria com êxito.</span><span class="sxs-lookup"><span data-stu-id="cc8f8-126">For example, a user's successful attempt to log on to the system is logged as a Success Audit event.</span></span>                                                                                                                        |
| <span data-ttu-id="cc8f8-127">**Auditoria com Falha**</span><span class="sxs-lookup"><span data-stu-id="cc8f8-127">**Failure Audit**</span></span> | <span data-ttu-id="cc8f8-128">Um evento que registra uma tentativa de acesso de segurança auditada que falha.</span><span class="sxs-lookup"><span data-stu-id="cc8f8-128">An event that records an audited security access attempt that fails.</span></span> <span data-ttu-id="cc8f8-129">Por exemplo, se um usuário tentar acessar uma unidade de rede e falhar, a tentativa será registrada como um evento de auditoria de falha.</span><span class="sxs-lookup"><span data-stu-id="cc8f8-129">For example, if a user tries to access a network drive and fails, the attempt is logged as a Failure Audit event.</span></span>                                                                                                                   |



 

<span data-ttu-id="cc8f8-130">As atividades selecionadas de usuários podem ser rastreadas por auditoria de eventos de segurança e, em seguida, colocando entradas no log de segurança de um computador.</span><span class="sxs-lookup"><span data-stu-id="cc8f8-130">Selected activities of users can be tracked by auditing security events and then placing entries in a computer's security log.</span></span>

 

 



