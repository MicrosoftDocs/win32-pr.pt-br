---
description: Os certificados são concedidos de acordo com as políticas que definem os critérios que os solicitantes devem atender para receber um certificado.
ms.assetid: ad79dc0d-6457-4459-80e6-ab340436ecac
title: Independência de política
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c0d99b5babeced0fb87d9e603038e23a40859b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104296956"
---
# <a name="policy-independence"></a><span data-ttu-id="adf3d-103">Independência de política</span><span class="sxs-lookup"><span data-stu-id="adf3d-103">Policy Independence</span></span>

<span data-ttu-id="adf3d-104">Os certificados são concedidos de acordo com as políticas que definem os critérios que os solicitantes devem atender para receber um certificado.</span><span class="sxs-lookup"><span data-stu-id="adf3d-104">Certificates are granted according to policies that define criteria that requesters must meet to receive a certificate.</span></span> <span data-ttu-id="adf3d-105">Por exemplo, uma política pode ser conceder certificados comerciais somente se os candidatos apresentarem sua identificação pessoalmente.</span><span class="sxs-lookup"><span data-stu-id="adf3d-105">For example, one policy may be to grant commercial certificates only if applicants present their identification in person.</span></span> <span data-ttu-id="adf3d-106">Outra política pode conceder [*credenciais*](../secgloss/c-gly.md) com base em solicitações de email.</span><span class="sxs-lookup"><span data-stu-id="adf3d-106">Another policy may grant [*credentials*](../secgloss/c-gly.md) based on email requests.</span></span> <span data-ttu-id="adf3d-107">Uma agência que emite cartões de crédito pode optar por consultar um banco de dados e fazer consultas telefônicas antes de emitir um cartão.</span><span class="sxs-lookup"><span data-stu-id="adf3d-107">An agency that issues credit cards may choose to consult a database and make phone inquiries before issuing a card.</span></span>

<span data-ttu-id="adf3d-108">As políticas são implementadas em módulos de política escritos em C++, C ou Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="adf3d-108">Policies are implemented in policy modules written in C++, C, or Visual Basic.</span></span> <span data-ttu-id="adf3d-109">As funções de serviços de certificados são isoladas de quaisquer alterações na política que uma agência possa implementar.</span><span class="sxs-lookup"><span data-stu-id="adf3d-109">Certificate Services functions are isolated from any changes in policy that an agency might implement.</span></span> <span data-ttu-id="adf3d-110">As alterações na política podem ser totalmente implementadas no código do módulo de política de servidor.</span><span class="sxs-lookup"><span data-stu-id="adf3d-110">Changes in policy can be fully implemented in the server policy module code.</span></span> <span data-ttu-id="adf3d-111">Uma AC ( [*autoridade de certificação*](../secgloss/c-gly.md) ) corporativa deve usar apenas o módulo de política corporativa fornecido pela Microsoft.</span><span class="sxs-lookup"><span data-stu-id="adf3d-111">An enterprise [*certification authority*](../secgloss/c-gly.md) (CA) should use only the Microsoft-provided enterprise policy module.</span></span>

 

 
