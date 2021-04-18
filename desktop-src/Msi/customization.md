---
description: Como o Windows Installer mantém todas as informações sobre a instalação em um banco de dados relacional, a instalação de um aplicativo ou produto pode ser personalizada para grupos de usuários específicos aplicando operações de transformação ao pacote.
ms.assetid: 98c5cda2-a01a-4bdd-840f-76c0ffacd194
title: Personalização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5238cc145bc4a47bff459cb6caa30be37e1ca6ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105756735"
---
# <a name="customization"></a><span data-ttu-id="f83b5-103">Personalização</span><span class="sxs-lookup"><span data-stu-id="f83b5-103">Customization</span></span>

<span data-ttu-id="f83b5-104">Como o Windows Installer mantém todas as informações sobre a instalação em um banco de dados relacional, a instalação de um aplicativo ou produto pode ser personalizada para grupos de usuários específicos aplicando operações de transformação ao pacote.</span><span class="sxs-lookup"><span data-stu-id="f83b5-104">Because the Windows Installer keeps all information about the installation in a relational database, the installation of an application or product can be customized for particular user groups by applying transform operations to the package.</span></span> <span data-ttu-id="f83b5-105">As transformações podem ser usadas para encapsular as várias personalizações de um pacote base exigido por diferentes grupos de dados.</span><span class="sxs-lookup"><span data-stu-id="f83b5-105">Transforms can be used to encapsulate the various customizations of a base package required by different workgroups.</span></span> <span data-ttu-id="f83b5-106">Para obter mais informações, consulte [mesclagens e transformações](merges-and-transforms.md).</span><span class="sxs-lookup"><span data-stu-id="f83b5-106">For more information, see [Merges and Transforms](merges-and-transforms.md).</span></span>

<span data-ttu-id="f83b5-107">Várias transformações de um pacote base podem ser aplicadas imediatamente durante a instalação.</span><span class="sxs-lookup"><span data-stu-id="f83b5-107">Multiple transforms of a base package can be applied on-the-fly during installation.</span></span> <span data-ttu-id="f83b5-108">Isso fornece um mecanismo para atribuir com eficiência instalações personalizadas a diferentes grupos de usuários.</span><span class="sxs-lookup"><span data-stu-id="f83b5-108">This provides a mechanism for efficiently assigning customized installations to different groups of users.</span></span> <span data-ttu-id="f83b5-109">Por exemplo, isso seria útil em organizações nas quais os departamentos de suporte da equipe e Finanças exigem diferentes instalações de um produto específico.</span><span class="sxs-lookup"><span data-stu-id="f83b5-109">For example, this would be useful in organizations where the finance and staff support departments require different installations of a particular product.</span></span> <span data-ttu-id="f83b5-110">O produto pode ser disponibilizado para todos na organização por uma [instalação administrativa](administrative-installation.md) do pacote base para um único ponto de instalação administrativa.</span><span class="sxs-lookup"><span data-stu-id="f83b5-110">The product can be made available to everyone in the organization by an [administrative installation](administrative-installation.md) of the base package to a single administrative installation point.</span></span> <span data-ttu-id="f83b5-111">Cada grupo de trabalho pode, então, receber automaticamente sua personalização apropriada por meio de uma transformação imediata ao instalar o produto.</span><span class="sxs-lookup"><span data-stu-id="f83b5-111">Each work group can then automatically receive their appropriate customization by means of an on-the-fly transform when they install the product.</span></span>

 

 



