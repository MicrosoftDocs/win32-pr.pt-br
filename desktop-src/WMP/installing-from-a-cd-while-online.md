---
title: Instalando de um CD enquanto estiver online
description: Instalando de um CD enquanto estiver online
ms.assetid: 4cf34f0e-caa0-42d1-b99a-51bbb7f0a7df
keywords:
- Armazenamentos online do Windows Media Player, instalando do CD enquanto estiver online
- lojas online, instalando do CD enquanto estiver online
- Digite 1 lojas online, instalando do CD enquanto estiver online
- Digite 2 lojas online, instalando do CD enquanto estiver online
- Armazenamentos online do Windows Media Player, instalações online do CD
- lojas online, instalações online do CD
- Digite 1 lojas online, instalações online do CD
- Digite 2 lojas online, instalações online do CD
- Armazenamentos online do Windows Media Player, instalações de CD quando estiverem online
- lojas online, instalações de CD enquanto estão online
- Digite 1 lojas online, instalações de CD quando estiverem online
- Digite 2 lojas online, instalações de CD quando estiverem online
- Instalando lojas online do CD enquanto estiver online
- Instalações de CD de lojas online enquanto estão online
- instalações online de lojas online
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd57015e64dece444b1a91afebe3144bee117caa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105800127"
---
# <a name="installing-from-a-cd-while-online"></a><span data-ttu-id="97d9b-118">Instalando de um CD enquanto estiver online</span><span class="sxs-lookup"><span data-stu-id="97d9b-118">Installing from a CD While Online</span></span>

<span data-ttu-id="97d9b-119">Os usuários podem instalar o Windows Media Player a partir de um CD enquanto estiverem conectados à Internet.</span><span class="sxs-lookup"><span data-stu-id="97d9b-119">Users can install Windows Media Player from a CD while connected to the Internet.</span></span> <span data-ttu-id="97d9b-120">Quando isso acontece, a instalação do Windows Media Player localiza o documento serviceInfo especificado pelo parâmetro de linha de comando *serviceInfo* .</span><span class="sxs-lookup"><span data-stu-id="97d9b-120">When this happens, Windows Media Player setup locates the ServiceInfo document specified by the *ServiceInfo* command line parameter.</span></span> <span data-ttu-id="97d9b-121">Se o atributo de **chave** corresponder ao parâmetro de linha de comando *defaultservice* , a instalação inspecionará o elemento install para personalizar o processo de instalação.</span><span class="sxs-lookup"><span data-stu-id="97d9b-121">If the **Key** attribute matches the *DefaultService* command line parameter, setup inspects the Install element to customize the setup process.</span></span> <span data-ttu-id="97d9b-122">Usando os valores de atributo, a instalação exibe o contrato de licença de usuário final (EULA) e sua declaração de privacidade, além de recuperar e instalar o arquivo. cab no computador do usuário.</span><span class="sxs-lookup"><span data-stu-id="97d9b-122">Using the attribute values, setup displays your End User License Agreement (EULA) and your privacy statement, and also retrieves and installs your .cab file to the user's computer.</span></span> <span data-ttu-id="97d9b-123">Por exemplo, você pode usar esse recurso para instalar a versão mais recente de um objeto COM que sua loja online requer.</span><span class="sxs-lookup"><span data-stu-id="97d9b-123">For example, you can use this feature to install the latest version of a COM object that your online store requires.</span></span>

<span data-ttu-id="97d9b-124">Após a instalação, o Windows Media Player define o armazenamento online inicial usando o nome da chave que você especificou para o parâmetro de linha de comando *defaultservice* .</span><span class="sxs-lookup"><span data-stu-id="97d9b-124">After it is installed, Windows Media Player sets the initial online store using the key name you specified for the *DefaultService* command line parameter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="97d9b-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="97d9b-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="97d9b-126">**Informações comuns às lojas online tipo 1 e tipo 2**</span><span class="sxs-lookup"><span data-stu-id="97d9b-126">**Information Common to Type 1 and Type 2 Online Stores**</span></span>](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="97d9b-127">**Elemento de instalação**</span><span class="sxs-lookup"><span data-stu-id="97d9b-127">**Install Element**</span></span>](install-element.md)
</dt> <dt>

[<span data-ttu-id="97d9b-128">**Documento do serviceInfo**</span><span class="sxs-lookup"><span data-stu-id="97d9b-128">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> <dt>

[<span data-ttu-id="97d9b-129">**Configurando a loja online inicial**</span><span class="sxs-lookup"><span data-stu-id="97d9b-129">**Setting the Initial Online Store**</span></span>](setting-the-initial-online-store.md)
</dt> <dt>

[<span data-ttu-id="97d9b-130">**Parâmetros de linha de comando de instalação para lojas online**</span><span class="sxs-lookup"><span data-stu-id="97d9b-130">**Setup Command-line Parameters for Online Stores**</span></span>](setup-command-line-parameters-for-online-stores.md)
</dt> </dl>

 

 




