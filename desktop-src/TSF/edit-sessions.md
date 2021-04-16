---
title: Editar sessões
description: Quando um serviço de texto deve obter, modificar ou definir texto em um contexto, ele deve solicitar uma sessão de edição.
ms.assetid: e4115227-1036-4892-986d-dc4cef5b178e
keywords:
- TSF (estrutura de serviços de texto), editar sessão
- TSF (estrutura de serviços de texto), editar sessão
- serviços de texto, sessão de edição
- sessão de edição
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81897c3c63539626776b693a22be9096f973d02e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104498798"
---
# <a name="edit-sessions"></a><span data-ttu-id="8f582-107">Editar sessões</span><span class="sxs-lookup"><span data-stu-id="8f582-107">Edit Sessions</span></span>

<span data-ttu-id="8f582-108">Quando um serviço de texto deve obter, modificar ou definir texto em um contexto, ele deve solicitar uma *sessão de edição*.</span><span class="sxs-lookup"><span data-stu-id="8f582-108">When a text service must obtain, modify, or set text in a context, it must request an *edit session*.</span></span> <span data-ttu-id="8f582-109">Quando uma sessão de edição é solicitada, o Gerenciador de TSF negocia com o proprietário do contexto de destino para um bloqueio de documento do tipo solicitado.</span><span class="sxs-lookup"><span data-stu-id="8f582-109">When an edit session is requested, the TSF manager negotiates with the owner of the target context for a document lock of the requested type.</span></span> <span data-ttu-id="8f582-110">Quando o bloqueio de documento é concedido, o Gerenciador de TSF permite que o serviço de texto Leia e/ou grave texto de ou para o contexto.</span><span class="sxs-lookup"><span data-stu-id="8f582-110">When the document lock is granted, the TSF manager enables the text service to read and/or write text to or from the context.</span></span>

 

 




