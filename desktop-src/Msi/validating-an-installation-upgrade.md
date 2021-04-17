---
description: Sempre que fizer alterações no pacote, os autores de pacotes de atualização sempre devem executar a validação em seus pacotes antes de tentar instalar o pacote pela primeira vez e executar novamente a validação.
ms.assetid: c578c020-18be-47ea-8f59-c1bbd45f1260
title: Validando uma atualização de instalação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cab7f45d3d5c19a71dac8c7a2d0150409b3a45f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105754334"
---
# <a name="validating-an-installation-upgrade"></a><span data-ttu-id="23ead-103">Validando uma atualização de instalação</span><span class="sxs-lookup"><span data-stu-id="23ead-103">Validating an Installation Upgrade</span></span>

<span data-ttu-id="23ead-104">Sempre que fizer alterações no pacote, os autores de pacotes de atualização sempre devem executar a validação em seus pacotes antes de tentar instalar o pacote pela primeira vez e executar novamente a validação.</span><span class="sxs-lookup"><span data-stu-id="23ead-104">Whenever making any changes to the package, authors of upgrade packages should always run validation on their packages before attempting to install the package for the first time and rerun validation.</span></span> <span data-ttu-id="23ead-105">Execute a validação em um pacote de atualização da mesma maneira que para um pacote de instalação.</span><span class="sxs-lookup"><span data-stu-id="23ead-105">Run validation on an upgrade package in the same way as for an installation package.</span></span> <span data-ttu-id="23ead-106">Para obter detalhes, consulte [Validando um banco de dados de instalação](validating-an-installation-database.md).</span><span class="sxs-lookup"><span data-stu-id="23ead-106">For details, see [Validating an Installation Database](validating-an-installation-database.md).</span></span>

<span data-ttu-id="23ead-107">Isso conclui o pacote de atualização de exemplo.</span><span class="sxs-lookup"><span data-stu-id="23ead-107">This completes the sample upgrade package.</span></span> <span data-ttu-id="23ead-108">Para instalar a atualização, primeiro instale MNP2000.msi e, em seguida, instale o MNP2001.msi.</span><span class="sxs-lookup"><span data-stu-id="23ead-108">To install the upgrade first install MNP2000.msi and then install MNP2001.msi.</span></span> <span data-ttu-id="23ead-109">Quando você desinstala o MNP2001, os produtos original e de atualização são removidos do seu computador.</span><span class="sxs-lookup"><span data-stu-id="23ead-109">When you uninstall MNP2001 both the original and upgrade products are removed from your computer.</span></span>

## <a name="next-example"></a><span data-ttu-id="23ead-110">Próximo exemplo</span><span class="sxs-lookup"><span data-stu-id="23ead-110">Next example</span></span>

[<span data-ttu-id="23ead-111">Um exemplo de transformação de personalização</span><span class="sxs-lookup"><span data-stu-id="23ead-111">A Customization Transform Example</span></span>](a-customization-transform-example.md)

 

 



