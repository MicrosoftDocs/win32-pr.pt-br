---
title: Outras informações de conexão
description: Os membros da estrutura RASDIALPARAMS também podem especificar as informações de conexão a seguir.
ms.assetid: 95a8dd78-e424-4d0b-899a-69deb9e1b9cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea4d006cd3cb31d5dc7229043b2a8ef169c22d76
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917411"
---
# <a name="other-connection-information"></a><span data-ttu-id="0ec12-103">Outras informações de conexão</span><span class="sxs-lookup"><span data-stu-id="0ec12-103">Other Connection Information</span></span>

<span data-ttu-id="0ec12-104">Os membros da estrutura [**RASDIALPARAMS**](/previous-versions/windows/desktop/legacy/aa377238(v=vs.85)) também podem especificar as informações de conexão a seguir.</span><span class="sxs-lookup"><span data-stu-id="0ec12-104">The members of the [**RASDIALPARAMS**](/previous-versions/windows/desktop/legacy/aa377238(v=vs.85)) structure can also specify the following connection information.</span></span>

-   <span data-ttu-id="0ec12-105">Um número de telefone para substituir o número na entrada do catálogo telefônico.</span><span class="sxs-lookup"><span data-stu-id="0ec12-105">A phone number to override the number in the phone-book entry.</span></span>
-   <span data-ttu-id="0ec12-106">Um número de telefone de [retorno](callback-connections.md) de chamada que o servidor remoto pode chamar de volta para estabelecer a conexão.</span><span class="sxs-lookup"><span data-stu-id="0ec12-106">A [callback](callback-connections.md) phone number that the remote server can call back to establish the connection.</span></span>
-   <span data-ttu-id="0ec12-107">O nome do domínio de rede remota no qual a autenticação deve ocorrer.</span><span class="sxs-lookup"><span data-stu-id="0ec12-107">The name of the remote network domain on which the authentication is to occur.</span></span>

<span data-ttu-id="0ec12-108">Para o número de retorno de chamada e o domínio, os membros do [**RASDIALPARAMS**](/previous-versions/windows/desktop/legacy/aa377238(v=vs.85)) podem indicar que o RAS deve usar as informações na entrada do catálogo telefônico ou pode fornecer informações que substituam os dados do catálogo telefônico.</span><span class="sxs-lookup"><span data-stu-id="0ec12-108">For the callback number and the domain, the [**RASDIALPARAMS**](/previous-versions/windows/desktop/legacy/aa377238(v=vs.85)) members can either indicate that RAS should use the information in the phone-book entry, or it can provide information that overrides the phone-book data.</span></span>

<span data-ttu-id="0ec12-109">Um cliente RAS pode usar o parâmetro *lpRasDialExtensions* da função [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) para controlar se o RAS usa um prefixo ou sufixo de número de telefone especificado em uma entrada de catálogo telefônico.</span><span class="sxs-lookup"><span data-stu-id="0ec12-109">A RAS client can use the *lpRasDialExtensions* parameter of the [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) function to control whether RAS uses a phone number prefix or suffix specified in a phone-book entry.</span></span>

 

 