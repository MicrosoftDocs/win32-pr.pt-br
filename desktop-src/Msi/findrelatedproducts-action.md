---
description: A ação FindRelatedProducts é executada em cada registro da tabela de atualização em sequência e compara o código de atualização, a versão do produto e o idioma em cada linha aos produtos instalados no sistema.
ms.assetid: 7efcb767-9bdf-43a4-83b8-61b6fc84adf6
title: Ação FindRelatedProducts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a87973631e51315df17a156bc8c57aa9facd84f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297082"
---
# <a name="findrelatedproducts-action"></a><span data-ttu-id="9527b-103">Ação FindRelatedProducts</span><span class="sxs-lookup"><span data-stu-id="9527b-103">FindRelatedProducts Action</span></span>

<span data-ttu-id="9527b-104">A ação FindRelatedProducts é executada em cada registro da [tabela de atualização](upgrade-table.md) em sequência e compara o código de atualização, a versão do produto e o idioma em cada linha aos produtos instalados no sistema.</span><span class="sxs-lookup"><span data-stu-id="9527b-104">The FindRelatedProducts action runs through each record of the [Upgrade table](upgrade-table.md) in sequence and compares the upgrade code, product version, and language in each row to products installed on the system.</span></span> <span data-ttu-id="9527b-105">Quando o FindRelatedProducts detecta uma correspondência entre as informações de atualização e um produto instalado, ele anexa o código do produto à propriedade especificada na coluna Actionproperty da Atualizaçãotable.</span><span class="sxs-lookup"><span data-stu-id="9527b-105">When FindRelatedProducts detects a correspondence between the upgrade information and an installed product, it appends the product code to the property specified in the ActionProperty column of the UpgradeTable.</span></span>

<span data-ttu-id="9527b-106">A ação FindRelatedProducts é executada apenas na primeira vez em que o produto é instalado.</span><span class="sxs-lookup"><span data-stu-id="9527b-106">The FindRelatedProducts action only runs the first time the product is installed.</span></span> <span data-ttu-id="9527b-107">A ação FindRelatedProducts não é executada durante o modo de manutenção ou a desinstalação.</span><span class="sxs-lookup"><span data-stu-id="9527b-107">The FindRelatedProducts action does not run during maintenance mode or uninstallation.</span></span>

## <a name="database-tables-queried"></a><span data-ttu-id="9527b-108">Tabelas de banco de dados consultadas</span><span class="sxs-lookup"><span data-stu-id="9527b-108">Database Tables Queried</span></span>

<span data-ttu-id="9527b-109">Esta ação consulta a tabela a seguir:</span><span class="sxs-lookup"><span data-stu-id="9527b-109">This action queries the following table:</span></span>

[<span data-ttu-id="9527b-110">Atualizar tabela</span><span class="sxs-lookup"><span data-stu-id="9527b-110">Upgrade Table</span></span>](upgrade-table.md)

## <a name="properties-used"></a><span data-ttu-id="9527b-111">Propriedades usadas</span><span class="sxs-lookup"><span data-stu-id="9527b-111">Properties Used</span></span>

<span data-ttu-id="9527b-112">A ação FindRelatedProducts usa a propriedade [**UpgradeCode**](upgradecode.md) e as informações de versão e idioma criadas na tabela de atualização para detectar os produtos instalados afetados pela atualização pendente.</span><span class="sxs-lookup"><span data-stu-id="9527b-112">The FindRelatedProducts action uses the [**UpgradeCode**](upgradecode.md) property and the version and language information authored into the Upgrade table to detect installed products affected by the pending upgrade.</span></span> <span data-ttu-id="9527b-113">Ele acrescenta o código do produto dos produtos detectados à propriedade na coluna Actionproperty da Atualizaçãotable.</span><span class="sxs-lookup"><span data-stu-id="9527b-113">It appends the product code of detected products to the property in the ActionProperty column of the UpgradeTable.</span></span>

<span data-ttu-id="9527b-114">O FindRelatedProducts reconhece apenas os produtos existentes que foram instalados usando o Windows Installer com um. msi que define uma propriedade [**UpgradeCode**](upgradecode.md) , uma propriedade [**ProductVersion**](productversion.md) e um valor para a propriedade [**ProductLanguage**](productlanguage.md) que é um dos idiomas listados na propriedade [**Summary do modelo**](template-summary.md) .</span><span class="sxs-lookup"><span data-stu-id="9527b-114">FindRelatedProducts only recognizes existing products that have been installed using the Windows Installer with an .msi that defines an [**UpgradeCode**](upgradecode.md) property, a [**ProductVersion**](productversion.md) property, and a value for the [**ProductLanguage**](productlanguage.md) property that is one of the languages listed in the [**Template Summary**](template-summary.md) Property.</span></span>

<span data-ttu-id="9527b-115">Observe que FindRelatedProducts usa o idioma retornado por [**MsiGetProductInfo**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoa).</span><span class="sxs-lookup"><span data-stu-id="9527b-115">Note that FindRelatedProducts uses the language returned by [**MsiGetProductInfo**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoa).</span></span> <span data-ttu-id="9527b-116">Para que o FindRelatedProducts funcione corretamente, o autor do pacote deve ter certeza de que a propriedade [**ProductLanguage**](productlanguage.md) na [tabela de propriedades](property-table.md) está definida como um idioma que também está listado na propriedade [**Summary do modelo**](template-summary.md) .</span><span class="sxs-lookup"><span data-stu-id="9527b-116">For FindRelatedProducts to work correctly, the package author must be sure that the [**ProductLanguage**](productlanguage.md) property in the [Property table](property-table.md) is set to a language that is also listed in the [**Template Summary**](template-summary.md) Property.</span></span> <span data-ttu-id="9527b-117">Consulte [preparando um aplicativo para atualizações importantes futuras](preparing-an-application-for-future-major-upgrades.md).</span><span class="sxs-lookup"><span data-stu-id="9527b-117">See [Preparing an Application for Future Major Upgrades](preparing-an-application-for-future-major-upgrades.md).</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="9527b-118">Restrições de sequência</span><span class="sxs-lookup"><span data-stu-id="9527b-118">Sequence Restrictions</span></span>

<span data-ttu-id="9527b-119">FindRelatedProducts deve ser criado na [tabela InstallUISequence](installuisequence-table.md) e nas tabelas [InstallExecuteSequence](installexecutesequence-table.md) .</span><span class="sxs-lookup"><span data-stu-id="9527b-119">FindRelatedProducts should be authored into the [InstallUISequence table](installuisequence-table.md) and [InstallExecuteSequence](installexecutesequence-table.md) tables.</span></span> <span data-ttu-id="9527b-120">O instalador impede que os produtos FindRelated sejam executados no InstallExecuteSequence se a ação já tiver sido executada no InstallUISequence.</span><span class="sxs-lookup"><span data-stu-id="9527b-120">The installer prevents FindRelated Products from running in InstallExecuteSequence if the action has already run in InstallUISequence.</span></span> <span data-ttu-id="9527b-121">A ação FindRelatedProducts deve vir antes da [ação MigrateFeatureStates](migratefeaturestates-action.md) e da [ação RemoveExistingProducts](removeexistingproducts-action.md).</span><span class="sxs-lookup"><span data-stu-id="9527b-121">The FindRelatedProducts action must come before the [MigrateFeatureStates action](migratefeaturestates-action.md) and the [RemoveExistingProducts action](removeexistingproducts-action.md).</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="9527b-122">Mensagens ActionData</span><span class="sxs-lookup"><span data-stu-id="9527b-122">ActionData Messages</span></span>

<span data-ttu-id="9527b-123">O FindRelatedProducts envia uma mensagem de dados de ação para cada produto relacionado que ele detecta no sistema.</span><span class="sxs-lookup"><span data-stu-id="9527b-123">FindRelatedProducts sends an action data message for each related product it detects on the system.</span></span>

 

 



