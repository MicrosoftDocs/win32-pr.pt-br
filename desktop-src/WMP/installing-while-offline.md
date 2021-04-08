---
title: Instalando enquanto estiver offline
description: Instalando enquanto estiver offline
ms.assetid: 29d80b6b-161d-44a7-b91e-70766b849c55
keywords:
- Armazenamentos online do Windows Media Player, instalando enquanto estiver offline
- lojas online, instalando enquanto estiver offline
- Digite 1 lojas online, instalando enquanto estiver offline
- Digite 2 lojas online, instalando enquanto estiver offline
- Lojas online do Windows Media Player, instalações offline
- lojas online, instalações offline
- tipos 1 lojas online, instalações offline
- tipo 2 lojas online, instalações offline
- Instalando lojas online offline
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cad7048926f218ea7be74a2522eb32c58241a017
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822742"
---
# <a name="installing-while-offline"></a><span data-ttu-id="9a188-112">Instalando enquanto estiver offline</span><span class="sxs-lookup"><span data-stu-id="9a188-112">Installing While Offline</span></span>

<span data-ttu-id="9a188-113">Os usuários podem instalar o Windows Media Player enquanto não estiverem conectados à Internet.</span><span class="sxs-lookup"><span data-stu-id="9a188-113">Users can install Windows Media Player while not connected to the Internet.</span></span> <span data-ttu-id="9a188-114">Quando isso acontece, a instalação do Windows Media Player localiza o ServiceInfo.xml documento especificado pelo parâmetro de linha de comando *serviceInfo* .</span><span class="sxs-lookup"><span data-stu-id="9a188-114">When this happens, Windows Media Player setup locates the ServiceInfo.xml document specified by the *ServiceInfo* command line parameter.</span></span> <span data-ttu-id="9a188-115">Se o atributo de **chave** corresponder ao parâmetro de linha de comando *defaultservice* , a instalação aplicará informações dos seguintes elementos ao Windows Media Player:</span><span class="sxs-lookup"><span data-stu-id="9a188-115">If the **Key** attribute matches the *DefaultService* command line parameter, setup applies information from the following elements to Windows Media Player:</span></span>

-   <span data-ttu-id="9a188-116">FriendlyName.</span><span class="sxs-lookup"><span data-stu-id="9a188-116">FriendlyName.</span></span> <span data-ttu-id="9a188-117">O nome amigável da loja online é mostrado na interface do usuário do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="9a188-117">The friendly name of the online store is shown in the Windows Media Player user interface.</span></span>
-   <span data-ttu-id="9a188-118">Cor.</span><span class="sxs-lookup"><span data-stu-id="9a188-118">Color.</span></span> <span data-ttu-id="9a188-119">As cores especificadas são aplicadas à barra de tarefas e aos botões.</span><span class="sxs-lookup"><span data-stu-id="9a188-119">The specified colors are applied to the taskbar and buttons.</span></span>
-   <span data-ttu-id="9a188-120">ServiceTask1, ServiceTask2 e ServiceTask3.</span><span class="sxs-lookup"><span data-stu-id="9a188-120">ServiceTask1, ServiceTask2, and ServiceTask3.</span></span> <span data-ttu-id="9a188-121">Os elementos filho ButtonText e ButtonTip são definidos.</span><span class="sxs-lookup"><span data-stu-id="9a188-121">The ButtonText and ButtonTip child elements are set.</span></span> <span data-ttu-id="9a188-122">O atributo de URL não está definido.</span><span class="sxs-lookup"><span data-stu-id="9a188-122">The URL attribute is not set.</span></span> <span data-ttu-id="9a188-123">A URL é definida quando o usuário se conecta à Internet e o Windows Media Player recupera sua lista de lojas online da maneira normal.</span><span class="sxs-lookup"><span data-stu-id="9a188-123">URL is set once the user connects to the Internet and Windows Media Player retrieves its list of online stores in the normal fashion.</span></span>
-   <span data-ttu-id="9a188-124">Imagem.</span><span class="sxs-lookup"><span data-stu-id="9a188-124">Image.</span></span> <span data-ttu-id="9a188-125">Os atributos MenuURL e ServiceLargeURL estão definidos.</span><span class="sxs-lookup"><span data-stu-id="9a188-125">The MenuURL and ServiceLargeURL attributes are set.</span></span> <span data-ttu-id="9a188-126">Essas URLs devem apontar para as imagens que você instalou no disco rígido do usuário usando o protocolo file://.</span><span class="sxs-lookup"><span data-stu-id="9a188-126">These URLs must point to images you installed on the user's hard disk by using the file:// protocol.</span></span>

<span data-ttu-id="9a188-127">Quando o usuário tenta exibir a loja online, o Windows Media Player exibe uma mensagem informando ao usuário que uma conexão com a Internet é necessária.</span><span class="sxs-lookup"><span data-stu-id="9a188-127">When the user attempts to view the online store, Windows Media Player displays a message informing the user that an Internet connection is required.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9a188-128">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9a188-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9a188-129">**Elemento Color**</span><span class="sxs-lookup"><span data-stu-id="9a188-129">**Color Element**</span></span>](color-element.md)
</dt> <dt>

[<span data-ttu-id="9a188-130">**Elemento FriendlyName**</span><span class="sxs-lookup"><span data-stu-id="9a188-130">**FriendlyName Element**</span></span>](friendlyname-element.md)
</dt> <dt>

[<span data-ttu-id="9a188-131">**Elemento de imagem**</span><span class="sxs-lookup"><span data-stu-id="9a188-131">**Image Element**</span></span>](image-element.md)
</dt> <dt>

[<span data-ttu-id="9a188-132">**Informações comuns às lojas online tipo 1 e tipo 2**</span><span class="sxs-lookup"><span data-stu-id="9a188-132">**Information Common to Type 1 and Type 2 Online Stores**</span></span>](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="9a188-133">**Elemento serviceInfo**</span><span class="sxs-lookup"><span data-stu-id="9a188-133">**ServiceInfo Element**</span></span>](serviceinfo-element.md)
</dt> <dt>

[<span data-ttu-id="9a188-134">**Elemento ServiceTask1**</span><span class="sxs-lookup"><span data-stu-id="9a188-134">**ServiceTask1 Element**</span></span>](servicetask1-element.md)
</dt> <dt>

[<span data-ttu-id="9a188-135">**Elemento ServiceTask2**</span><span class="sxs-lookup"><span data-stu-id="9a188-135">**ServiceTask2 Element**</span></span>](servicetask2-element.md)
</dt> <dt>

[<span data-ttu-id="9a188-136">**Elemento ServiceTask3**</span><span class="sxs-lookup"><span data-stu-id="9a188-136">**ServiceTask3 Element**</span></span>](servicetask3-element.md)
</dt> <dt>

[<span data-ttu-id="9a188-137">**Configurando a loja online inicial**</span><span class="sxs-lookup"><span data-stu-id="9a188-137">**Setting the Initial Online Store**</span></span>](setting-the-initial-online-store.md)
</dt> <dt>

[<span data-ttu-id="9a188-138">**Parâmetros de linha de comando de instalação para lojas online**</span><span class="sxs-lookup"><span data-stu-id="9a188-138">**Setup Command-line Parameters for Online Stores**</span></span>](setup-command-line-parameters-for-online-stores.md)
</dt> </dl>

 

 




