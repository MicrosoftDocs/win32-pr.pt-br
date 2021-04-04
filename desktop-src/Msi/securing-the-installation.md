---
description: Adicione todas as propriedades de senha da tabela CustomUserAccounts à propriedade MsiHiddenProperties na tabela de propriedades.
ms.assetid: 682f534c-10a2-4260-b21d-7075d8c1620c
title: Protegendo a instalação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: add5211327508dbbf6531c48c3d2ae40f095375d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922901"
---
# <a name="securing-the-installation"></a><span data-ttu-id="5d1bc-103">Protegendo a instalação</span><span class="sxs-lookup"><span data-stu-id="5d1bc-103">Securing the Installation</span></span>

<span data-ttu-id="5d1bc-104">Adicione todas as propriedades de senha da tabela CustomUserAccounts à propriedade [**MsiHiddenProperties**](msihiddenproperties.md) na [tabela de propriedades](property-table.md).</span><span class="sxs-lookup"><span data-stu-id="5d1bc-104">Add all of the Password properties from the CustomUserAccounts table to the [**MsiHiddenProperties**](msihiddenproperties.md) property in the [Property table](property-table.md).</span></span> <span data-ttu-id="5d1bc-105">Adicione os nomes das ações personalizadas adiadas à propriedade **MsiHiddenProperties** também.</span><span class="sxs-lookup"><span data-stu-id="5d1bc-105">Add the names of the deferred custom actions to the **MsiHiddenProperties** property as well.</span></span> <span data-ttu-id="5d1bc-106">Isso impedirá que o instalador grave os valores de propriedade confidenciais (as senhas) no log e garantirá que esses valores não sejam registrados quando as ações personalizadas adiadas usarem os valores como a propriedade CustomActionData.</span><span class="sxs-lookup"><span data-stu-id="5d1bc-106">This will prevent the installer from writing the sensitive property values (the passwords) into the log and will ensure these values are not logged when the deferred custom actions use the values as the CustomActionData property.</span></span>

<span data-ttu-id="5d1bc-107">Para que a senha do usuário esteja disponível no serviço Windows Installer, a propriedade password deve ser adicionada à propriedade [**SecureCustomProperties**](securecustomproperties.md) .</span><span class="sxs-lookup"><span data-stu-id="5d1bc-107">For the user's password to be available in the Windows Installer service, the password property must be added to the [**SecureCustomProperties**](securecustomproperties.md) property.</span></span>

[<span data-ttu-id="5d1bc-108">Tabela de propriedades</span><span class="sxs-lookup"><span data-stu-id="5d1bc-108">Property Table</span></span>](property-table.md)



| <span data-ttu-id="5d1bc-109">Propriedade</span><span class="sxs-lookup"><span data-stu-id="5d1bc-109">Property</span></span>                                                 | <span data-ttu-id="5d1bc-110">Valor</span><span class="sxs-lookup"><span data-stu-id="5d1bc-110">Value</span></span>                                                        |
|----------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="5d1bc-111">**MsiHiddenProperties**</span><span class="sxs-lookup"><span data-stu-id="5d1bc-111">**MsiHiddenProperties**</span></span>](msihiddenproperties.md)       | <span data-ttu-id="5d1bc-112">TESTUSERPASSWORD; CreateAccount; RemoveAccount; RollbackAccount</span><span class="sxs-lookup"><span data-stu-id="5d1bc-112">TESTUSERPASSWORD;CreateAccount;RemoveAccount;RollbackAccount</span></span> |
| [<span data-ttu-id="5d1bc-113">**SecureCustomProperties**</span><span class="sxs-lookup"><span data-stu-id="5d1bc-113">**SecureCustomProperties**</span></span>](securecustomproperties.md) | <span data-ttu-id="5d1bc-114">TESTUSERPASSWORD</span><span class="sxs-lookup"><span data-stu-id="5d1bc-114">TESTUSERPASSWORD</span></span>                                             |



 

<span data-ttu-id="5d1bc-115">Isso conclui o exemplo.</span><span class="sxs-lookup"><span data-stu-id="5d1bc-115">This concludes the sample.</span></span>

 

 



