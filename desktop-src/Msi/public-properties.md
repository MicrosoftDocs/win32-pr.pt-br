---
description: As propriedades públicas podem ser criadas no banco de dados de instalação da mesma forma que as propriedades privadas.
ms.assetid: 032aa55f-d97a-4455-bd32-571b0e05763b
title: Propriedades públicas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 822dfc55e0ab659e5580580edd04eb156540cb61
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828257"
---
# <a name="public-properties"></a><span data-ttu-id="10b46-103">Propriedades públicas</span><span class="sxs-lookup"><span data-stu-id="10b46-103">Public Properties</span></span>

<span data-ttu-id="10b46-104">As propriedades públicas podem ser criadas no banco de dados de instalação da mesma forma que [as propriedades privadas](private-properties.md).</span><span class="sxs-lookup"><span data-stu-id="10b46-104">Public properties can be authored into the installation database in the same way as [private properties](private-properties.md).</span></span> <span data-ttu-id="10b46-105">Além disso, os valores das propriedades públicas podem ser alterados por um usuário ou administrador do sistema definindo a propriedade na linha de comando, aplicando uma transformação ou interagindo com uma interface do usuário criada.</span><span class="sxs-lookup"><span data-stu-id="10b46-105">In addition, the values of public properties can be changed by a user or system administrator by setting the property on the command line, by applying a transform, or by interacting with an authored user interface.</span></span> <span data-ttu-id="10b46-106">Nomes de propriedade pública não podem conter letras minúsculas.</span><span class="sxs-lookup"><span data-stu-id="10b46-106">Public property names cannot contain lowercase letters.</span></span> <span data-ttu-id="10b46-107">Consulte [restrições em nomes de propriedade](restrictions-on-property-names.md).</span><span class="sxs-lookup"><span data-stu-id="10b46-107">See [Restrictions on Property Names](restrictions-on-property-names.md).</span></span>

<span data-ttu-id="10b46-108">Normalmente, as propriedades públicas são definidas pelos usuários durante a instalação.</span><span class="sxs-lookup"><span data-stu-id="10b46-108">Public properties are commonly set by users during the installation.</span></span> <span data-ttu-id="10b46-109">Por exemplo, a propriedade Public property [**INSTALLLEVEL**](installlevel.md) pode ser especificada na linha de comando usada para iniciar a instalação ou escolhida usando uma interface do usuário criada.</span><span class="sxs-lookup"><span data-stu-id="10b46-109">For example, the public property [**INSTALLLEVEL**](installlevel.md) property can be specified at the command line used to launch the installation or chosen by using an authored user interface.</span></span>

<span data-ttu-id="10b46-110">Os valores de propriedade pública podem ser substituídos em uma linha de comando, usando uma ação [padrão](standard-actions.md) ou [personalizada](custom-actions.md) , aplicando uma transformação ou fazendo com que o usuário interaja com uma interface do usuário criada.</span><span class="sxs-lookup"><span data-stu-id="10b46-110">Public property values can be overridden either at a command line, by using a [standard](standard-actions.md) or [custom](custom-actions.md) action, by applying a transform, or by having the user interact with an authored user interface.</span></span> <span data-ttu-id="10b46-111">Para limpar uma propriedade pública na tabela de propriedades, deixe-a fora da tabela.</span><span class="sxs-lookup"><span data-stu-id="10b46-111">To clear a public property in the property table, leave it out of the table.</span></span> <span data-ttu-id="10b46-112">As propriedades que devem ser definidas pela interface do usuário durante a instalação e, em seguida, passadas para a fase de execução da instalação do devem ser públicas.</span><span class="sxs-lookup"><span data-stu-id="10b46-112">Properties that are to be set by the user interface during the installation and then passed to the execution phase of the installation must be public.</span></span>

<span data-ttu-id="10b46-113">Para obter uma lista das propriedades públicas padrão usadas pelo instalador, consulte [referência de propriedade](property-reference.md).</span><span class="sxs-lookup"><span data-stu-id="10b46-113">For a list of the standard public properties used by the installer see [Property Reference](property-reference.md).</span></span> <span data-ttu-id="10b46-114">Um autor também pode definir uma propriedade pública personalizada inserindo o nome da propriedade e um valor inicial na [tabela de propriedades](property-table.md).</span><span class="sxs-lookup"><span data-stu-id="10b46-114">An author can also define a custom public property by entering the property's name and an initial value into the [Property table](property-table.md).</span></span> <span data-ttu-id="10b46-115">Todas as propriedades públicas podem ser substituídas por todos os usuários se qualquer uma das condições a seguir for verdadeira.</span><span class="sxs-lookup"><span data-stu-id="10b46-115">All public properties can be overridden by all users if any of the following conditions are true.</span></span>

-   <span data-ttu-id="10b46-116">O usuário é um administrador do sistema.</span><span class="sxs-lookup"><span data-stu-id="10b46-116">The user is a system administrator.</span></span>
-   <span data-ttu-id="10b46-117">A política de EnableUserControl por máquina é definida como 1.</span><span class="sxs-lookup"><span data-stu-id="10b46-117">The per-machine EnableUserControl policy is set to 1.</span></span> <span data-ttu-id="10b46-118">Consulte [política do sistema](system-policy.md).</span><span class="sxs-lookup"><span data-stu-id="10b46-118">See [System Policy](system-policy.md).</span></span>
-   <span data-ttu-id="10b46-119">A propriedade [**EnableUserControl**](-enableusercontrol.md) é definida como 1.</span><span class="sxs-lookup"><span data-stu-id="10b46-119">The [**EnableUserControl**](-enableusercontrol.md) property is set to 1.</span></span>
-   <span data-ttu-id="10b46-120">Essa é uma instalação não gerenciada que não está sendo feita com privilégios elevados.</span><span class="sxs-lookup"><span data-stu-id="10b46-120">This is an unmanaged installation that is not being done with elevated privileges.</span></span>

<span data-ttu-id="10b46-121">Se nenhuma das condições acima for verdadeira, o instalador assume como padrão a limitação de quais propriedades públicas podem ser substituídas por um usuário que não seja um administrador do sistema.</span><span class="sxs-lookup"><span data-stu-id="10b46-121">If none of the above conditions are true, the installer defaults to limiting which public properties can be overridden by a user that is not a system administrator.</span></span> <span data-ttu-id="10b46-122">Consulte [**Propriedades públicas restritas**](restricted-public-properties.md).</span><span class="sxs-lookup"><span data-stu-id="10b46-122">See [**Restricted Public Properties**](restricted-public-properties.md).</span></span>

 

 



