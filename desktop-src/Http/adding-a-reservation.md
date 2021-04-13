---
title: Adicionando uma reserva
description: O banco de dados de roteamento contém a lista de reserva.
ms.assetid: c36e731c-6a0b-42a8-bc92-106a8e017b0d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 358181cbe57a046f5af54f7adf17bdadb24c3ddc
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/20/2020
ms.locfileid: "104499182"
---
# <a name="adding-a-reservation"></a><span data-ttu-id="90f18-103">Adicionando uma reserva</span><span class="sxs-lookup"><span data-stu-id="90f18-103">Adding a Reservation</span></span>

<span data-ttu-id="90f18-104">O banco de dados de roteamento contém a lista de reserva.</span><span class="sxs-lookup"><span data-stu-id="90f18-104">The routing database contains the reservation list.</span></span> <span data-ttu-id="90f18-105">A lista de reserva consiste nos usuários que têm permissão de acesso ao namespace, bem como o nível de acesso para cada usuário listado na reserva.</span><span class="sxs-lookup"><span data-stu-id="90f18-105">The reservation list consists of the users that are allowed access to the namespace, as well as the level of access for each user listed under the reservation.</span></span> <span data-ttu-id="90f18-106">Quando as reservas são adicionadas ou excluídas, o banco de dados de roteamento é pesquisado para determinar os privilégios de acesso.</span><span class="sxs-lookup"><span data-stu-id="90f18-106">When reservations are added or deleted, the routing database is searched to determine access privileges.</span></span>

<span data-ttu-id="90f18-107">Além de verificar a ID dos usuários, a API do servidor HTTP também verifica se há conflitos em reservas existentes antes de instalar uma nova reserva.</span><span class="sxs-lookup"><span data-stu-id="90f18-107">In addition to checking the users ID, the HTTP Server API also checks for conflicts in existing reservations before installing a new reservation.</span></span>

<span data-ttu-id="90f18-108">**Para adicionar uma nova reserva**</span><span class="sxs-lookup"><span data-stu-id="90f18-108">**To add a new reservation**</span></span>

1.  <span data-ttu-id="90f18-109">Se o número da porta no UrlPrefix tiver reservas ou registros para um esquema diferente do esquema no UrlPrefix, o registro falhará.</span><span class="sxs-lookup"><span data-stu-id="90f18-109">If the port number in the UrlPrefix has reservations or registrations for a scheme different from the scheme in the UrlPrefix, the registration fails.</span></span> <span data-ttu-id="90f18-110">Não há suporte para HTTP e HTTPS na mesma porta.</span><span class="sxs-lookup"><span data-stu-id="90f18-110">HTTP and HTTPS cannot be supported on the same port.</span></span>
2.  <span data-ttu-id="90f18-111">Localize o Bucket apropriado para o registro (consulte a seção [solicitações de entrada de roteamento](routing-incoming-requests.md) ), com base no tipo de host.</span><span class="sxs-lookup"><span data-stu-id="90f18-111">Locate the appropriate bucket for the registration (see the [Routing Incoming Requests](routing-incoming-requests.md) section), based on the host type.</span></span> <span data-ttu-id="90f18-112">As etapas restantes são relativas a esse Bucket.</span><span class="sxs-lookup"><span data-stu-id="90f18-112">The remaining steps are relative to this bucket.</span></span>
3.  <span data-ttu-id="90f18-113">Selecione entradas de reserva com componentes de esquema, host e porta que correspondam ao UrlPrefix que está sendo reservado.</span><span class="sxs-lookup"><span data-stu-id="90f18-113">Select reservation entries with scheme, host and port components that match the UrlPrefix being reserved.</span></span> <span data-ttu-id="90f18-114">A partir deles, localize a entrada com o *relativeUri* correspondente mais longo que não seja igual ao relativeUri na Reserva (ou seja, o *nó pai*).</span><span class="sxs-lookup"><span data-stu-id="90f18-114">From these, locate the entry with the longest matching *relativeUri* that is not equal to the relativeUri in the reservation (that is, the *parent node*).</span></span> <span data-ttu-id="90f18-115">Se a entrada existir, avalie os direitos de acesso com base na ACL atribuída a essa entrada.</span><span class="sxs-lookup"><span data-stu-id="90f18-115">If the entry exists, then evaluate access rights based on the ACL assigned to that entry.</span></span>
4.  <span data-ttu-id="90f18-116">Se um nó pai não foi encontrado, essa é uma reserva com uma relativeUri vazia ou *reserva de raiz*.</span><span class="sxs-lookup"><span data-stu-id="90f18-116">If a parent node was not found, this is a reservation with an empty relativeUri, or *root reservation*.</span></span> <span data-ttu-id="90f18-117">Conceda direitos de acesso somente se o chamador estiver registrado nas contas LocalSystem ou administrador.</span><span class="sxs-lookup"><span data-stu-id="90f18-117">Grant access rights only if the caller is registered under the LocalSystem or Administrator accounts.</span></span>
5.  <span data-ttu-id="90f18-118">Se direitos de acesso forem concedidos, verifique se há reservas duplicadas.</span><span class="sxs-lookup"><span data-stu-id="90f18-118">If access rights are granted, check for duplicate reservations.</span></span> <span data-ttu-id="90f18-119">Se existir uma entrada de reserva com o mesmo esquema, porta, host e relativeUri, um \_ código de erro já \_ existe será retornado.</span><span class="sxs-lookup"><span data-stu-id="90f18-119">If a reservation entry exists with the same scheme, port, host and relativeUri, an ERROR\_ALREADY\_EXISTS code is returned.</span></span>
    > [!Note]  
    > <span data-ttu-id="90f18-120">A atualização de uma entrada existente deve ser executada em duas etapas: excluir a entrada e adicionar uma nova.</span><span class="sxs-lookup"><span data-stu-id="90f18-120">Updating an existing entry should be performed in two steps: delete the entry and add a new one.</span></span>

     

<span data-ttu-id="90f18-121">Se as etapas acima forem realizadas com sucesso, uma nova entrada de reserva será inserida no banco de dados de reserva.</span><span class="sxs-lookup"><span data-stu-id="90f18-121">If the above steps succeed, a new reservation entry is entered into the reservation database.</span></span>

> [!Note]  
> <span data-ttu-id="90f18-122">A nova entrada é criada com a ACL especificada e não herda ACLs da entrada *pai* .</span><span class="sxs-lookup"><span data-stu-id="90f18-122">The new entry is created with the specified ACL and does not inherit ACLs from the *parent* entry.</span></span>

 

<span data-ttu-id="90f18-123">Os exemplos a seguir ilustram o processo de reserva.</span><span class="sxs-lookup"><span data-stu-id="90f18-123">The following examples illustrate the reservation process.</span></span>

-   <span data-ttu-id="90f18-124">Reserva 1: `https://+:80/vroot/subdir/` pelo administrador para o usuário A e o usuário C são bem-sucedidos e inseridos no Bucket "+".</span><span class="sxs-lookup"><span data-stu-id="90f18-124">Reservation 1: `https://+:80/vroot/subdir/` by Admin for User A and User C succeeds and is entered into the "+" bucket.</span></span>
-   <span data-ttu-id="90f18-125">Reserva 2: `https://adatum.com:80/vroot/` pelo administrador para o usuário B é bem sucedido e é inserido no Bucket "host explícito".</span><span class="sxs-lookup"><span data-stu-id="90f18-125">Reservation 2: `https://adatum.com:80/vroot/` by Admin for User B succeeds and is entered into the "Explicit host" bucket.</span></span>
-   <span data-ttu-id="90f18-126">Reserva 3: `https://adatum.com:80/vroot/subdir/otherdir/` pelo usuário B para o usuário C teve sucesso devido à reserva 2.</span><span class="sxs-lookup"><span data-stu-id="90f18-126">Reservation 3: `https://adatum.com:80/vroot/subdir/otherdir/` by User B for User C succeeds due to reservation 2.</span></span>
-   <span data-ttu-id="90f18-127">Reserva 4: `https://+:80/vroot/subdir/otherdir/` pelo usuário A para o usuário E é realizada com sucesso devido à reserva 1.</span><span class="sxs-lookup"><span data-stu-id="90f18-127">Reservation 4: `https://+:80/vroot/subdir/otherdir/` by User A for User E succeeds due to reservation 1.</span></span>
-   <span data-ttu-id="90f18-128">Reserva 5: `https://adatum.com:80/vroot/subdir/otherdir/` pelo usuário A para o usuário E falha.</span><span class="sxs-lookup"><span data-stu-id="90f18-128">Reservation 5: `https://adatum.com:80/vroot/subdir/otherdir/` by User A for User E fails.</span></span> <span data-ttu-id="90f18-129">Acesso negado devido à reserva 2.</span><span class="sxs-lookup"><span data-stu-id="90f18-129">Access denied due to reservation 2.</span></span>
-   <span data-ttu-id="90f18-130">Reserva 6: `https://+:80/vroot/subdir/` pelo administrador para o usuário A falha.</span><span class="sxs-lookup"><span data-stu-id="90f18-130">Reservation 6: `https://+:80/vroot/subdir/` by Admin for User A fails.</span></span> <span data-ttu-id="90f18-131">A reserva está em conflito com a reserva 1.</span><span class="sxs-lookup"><span data-stu-id="90f18-131">The reservation conflicts with reservation 1.</span></span>
-   <span data-ttu-id="90f18-132">Reserva 7: `https://adatum.com:80/newroot/` pelo usuário a para o usuário a falha.</span><span class="sxs-lookup"><span data-stu-id="90f18-132">Reservation 7: `https://adatum.com:80/newroot/` by User A for User A fails.</span></span> <span data-ttu-id="90f18-133">Acesso negado devido à reserva de raiz implícita de `https://adatum.com:80/` para LocalSystem ou administrador.</span><span class="sxs-lookup"><span data-stu-id="90f18-133">Access denied due to implicit root reservation of `https://adatum.com:80/` for LocalSystem or Administrator.</span></span>

<span data-ttu-id="90f18-134">As reservas podem afetar o conjunto de URLs em solicitações entregues a um processo que registrou anteriormente um UrlPrefix.</span><span class="sxs-lookup"><span data-stu-id="90f18-134">Reservations can affect the set of URLs in requests delivered to a process that has previously registered a UrlPrefix.</span></span> <span data-ttu-id="90f18-135">Por exemplo, considere o cenário a seguir.</span><span class="sxs-lookup"><span data-stu-id="90f18-135">For example, consider the following scenario.</span></span>

-   <span data-ttu-id="90f18-136">Registro: `https://adatum.com:80/vroot/` por aplicativo 1 para o usuário A.</span><span class="sxs-lookup"><span data-stu-id="90f18-136">Registration: `https://adatum.com:80/vroot/` by application 1 for User A.</span></span>
-   <span data-ttu-id="90f18-137">Uma solicitação para `https://adatum.com:80/vroot/subdir/file.htm` é entregue ao aplicativo 1.</span><span class="sxs-lookup"><span data-stu-id="90f18-137">A request for `https://adatum.com:80/vroot/subdir/file.htm` is delivered to application 1.</span></span>
-   <span data-ttu-id="90f18-138">Reserva: `https://+:80/vroot/subdir/` para o usuário B.</span><span class="sxs-lookup"><span data-stu-id="90f18-138">Reservation: `https://+:80/vroot/subdir/` for User B.</span></span>
-   <span data-ttu-id="90f18-139">Uma solicitação para `https://adatum.com:80/vroot/subdir/file.htm` agora é rejeitada.</span><span class="sxs-lookup"><span data-stu-id="90f18-139">A request for `https://adatum.com:80/vroot/subdir/file.htm` is now rejected.</span></span>
-   <span data-ttu-id="90f18-140">Registro: `https://adatum.com:80/vroot/subdir/` por aplicativo 2 para o usuário B.</span><span class="sxs-lookup"><span data-stu-id="90f18-140">Registration: `https://adatum.com:80/vroot/subdir/` by application 2 for User B.</span></span>
-   <span data-ttu-id="90f18-141">Uma solicitação para `https://adatum.com:80/vroot/subdir/file.htm` é entregue ao aplicativo 2.</span><span class="sxs-lookup"><span data-stu-id="90f18-141">A request for `https://adatum.com:80/vroot/subdir/file.htm` is delivered to application 2.</span></span>

 

 




