---
title: Client Security durante uma chamada assíncrona
description: Client Security durante uma chamada assíncrona
ms.assetid: 26d1f2c2-cb08-49f1-8beb-b99b029f0d8c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bea2f83bf6341704dd0265a37ec2f64b79e9b2a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636714"
---
# <a name="client-security-during-an-asynchronous-call"></a><span data-ttu-id="29d94-103">Client Security durante uma chamada assíncrona</span><span class="sxs-lookup"><span data-stu-id="29d94-103">Client Security During an Asynchronous Call</span></span>

<span data-ttu-id="29d94-104">O Gerenciador de proxy criado pelo MIDL para objetos que usam marshaling padrão implementa a interface [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) .</span><span class="sxs-lookup"><span data-stu-id="29d94-104">The proxy manager created by MIDL for objects that use standard marshaling implements the [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) interface.</span></span> <span data-ttu-id="29d94-105">Os clientes podem gerenciar a segurança de chamadas com marshaling consultando **IClientSecurity** no objeto de chamada e obtendo ou alterando as configurações de segurança.</span><span class="sxs-lookup"><span data-stu-id="29d94-105">Clients can manage the security of marshaled calls by querying for **IClientSecurity** on the call object and obtaining or changing security settings.</span></span>

## <a name="related-topics"></a><span data-ttu-id="29d94-106">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="29d94-106">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="29d94-107">Fazendo uma chamada assíncrona</span><span class="sxs-lookup"><span data-stu-id="29d94-107">Making an Asynchronous Call</span></span>](making-an-asynchronous-call.md)
</dt> </dl>

 

 




