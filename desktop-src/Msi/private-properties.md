---
description: As propriedades privadas são usadas internamente pelo instalador e seus valores devem ser inseridos no banco de dados pelo autor do pacote de instalação ou definidos pelo instalador durante a instalação para os valores determinados pelo ambiente operacional.
ms.assetid: 7d574bf0-bcb3-4e19-9659-fe741ace9f21
title: Propriedades particulares
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab7b0196be016fecb625e139f308219582620d40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105750224"
---
# <a name="private-properties"></a><span data-ttu-id="39a6d-103">Propriedades particulares</span><span class="sxs-lookup"><span data-stu-id="39a6d-103">Private Properties</span></span>

<span data-ttu-id="39a6d-104">As propriedades privadas são usadas internamente pelo instalador e seus valores devem ser inseridos no banco de dados pelo autor do pacote de instalação ou definidos pelo instalador durante a instalação para os valores determinados pelo ambiente operacional.</span><span class="sxs-lookup"><span data-stu-id="39a6d-104">Private properties are used internally by the installer and their values must be entered into the database by the author of the installation package or set by the installer during the installation to values determined by the operating environment.</span></span> <span data-ttu-id="39a6d-105">A única maneira de um usuário poder interagir com propriedades privadas é por meio de [eventos de controle](control-events.md) na interface do usuário criada do pacote.</span><span class="sxs-lookup"><span data-stu-id="39a6d-105">The only way a user can interact with private properties is through [Control Events](control-events.md) in the package's authored user interface.</span></span> <span data-ttu-id="39a6d-106">Nomes de propriedade privada devem incluir letras minúsculas.</span><span class="sxs-lookup"><span data-stu-id="39a6d-106">Private property names must include lowercase letters.</span></span> <span data-ttu-id="39a6d-107">Consulte [restrições em nomes de propriedade](restrictions-on-property-names.md).</span><span class="sxs-lookup"><span data-stu-id="39a6d-107">See [Restrictions on Property Names](restrictions-on-property-names.md).</span></span>

<span data-ttu-id="39a6d-108">As propriedades privadas normalmente descrevem o ambiente operacional.</span><span class="sxs-lookup"><span data-stu-id="39a6d-108">Private properties commonly describe the operating environment.</span></span> <span data-ttu-id="39a6d-109">Por exemplo, se a instalação for executada em uma plataforma Windows, o instalador definirá a propriedade [**WindowsFolder**](windowsfolder.md) para o valor especificado na tabela de propriedades.</span><span class="sxs-lookup"><span data-stu-id="39a6d-109">For example, if the installation is run on a Windows platform, the installer sets the [**WindowsFolder**](windowsfolder.md) property to the value specified in the Property table.</span></span>

<span data-ttu-id="39a6d-110">Os valores de propriedade privada não podem ser substituídos em uma linha de comando.</span><span class="sxs-lookup"><span data-stu-id="39a6d-110">Private property values cannot be overridden at a command line.</span></span> <span data-ttu-id="39a6d-111">Para limpar uma propriedade privada de uma instalação, deixe-a fora da [tabela de propriedades](property-table.md).</span><span class="sxs-lookup"><span data-stu-id="39a6d-111">To clear a private property from an installation, leave it out of the [Property table](property-table.md).</span></span> <span data-ttu-id="39a6d-112">No Windows XP e no Windows 2000, você não pode definir uma propriedade particular na fase de interface do usuário da instalação e, em seguida, passar o valor para a fase de execução.</span><span class="sxs-lookup"><span data-stu-id="39a6d-112">On Windows XP, and Windows 2000 you cannot set a private property in the user interface phase of the installation and then pass the value to the execution phase.</span></span>

<span data-ttu-id="39a6d-113">Para obter uma lista de todas as propriedades particulares padrão usadas pelo instalador, consulte [referência de propriedade](property-reference.md).</span><span class="sxs-lookup"><span data-stu-id="39a6d-113">For a list of all the standard private properties used by the installer, see [Property Reference](property-reference.md).</span></span> <span data-ttu-id="39a6d-114">Você pode definir uma propriedade privada personalizada inserindo o nome da propriedade e o valor inicial na tabela de propriedades.</span><span class="sxs-lookup"><span data-stu-id="39a6d-114">You can define a custom private property by entering the property's name and initial value in the Property table.</span></span> <span data-ttu-id="39a6d-115">Nomes de propriedade privada devem sempre incluir letras minúsculas.</span><span class="sxs-lookup"><span data-stu-id="39a6d-115">Private property names must always include lowercase letters.</span></span>

## <a name="related-topics"></a><span data-ttu-id="39a6d-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="39a6d-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="39a6d-117">Propriedades públicas</span><span class="sxs-lookup"><span data-stu-id="39a6d-117">Public Properties</span></span>](public-properties.md)
</dt> </dl>

 

 



