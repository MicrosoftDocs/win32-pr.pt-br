---
description: Para aplicar uma atualização principal usando Windows Installer, o pacote de instalação do produto original deve especificar uma propriedade UpgradeCode, descrita em preparando um aplicativo para atualizações principais futuras, e o pacote de atualização deve ter uma tabela de atualização.
ms.assetid: 041f5bab-cb13-4e17-8465-484bcd3c6957
title: Atualizando a tabela de atualização para uma atualização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc1b4c2cc2b650d49fb4ba40f97d69ed84911273
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091394"
---
# <a name="updating-upgrade-table-for-an-upgrade"></a><span data-ttu-id="380a7-103">Atualizando a tabela de atualização para uma atualização</span><span class="sxs-lookup"><span data-stu-id="380a7-103">Updating Upgrade Table for an Upgrade</span></span>

<span data-ttu-id="380a7-104">Para aplicar uma atualização principal usando Windows Installer, o pacote de instalação do produto original deve especificar uma propriedade [**UpgradeCode**](upgradecode.md) , descrita em [preparando um aplicativo para atualizações principais futuras](preparing-an-application-for-future-major-upgrades.md), e o pacote de atualização deve ter uma [tabela de atualização](upgrade-table.md).</span><span class="sxs-lookup"><span data-stu-id="380a7-104">To apply a major upgrade using Windows Installer, the original product installation package must specify an [**UpgradeCode**](upgradecode.md) Property, described in [Preparing an Application for Future Major Upgrades](preparing-an-application-for-future-major-upgrades.md), and the upgrade package must have an [Upgrade table](upgrade-table.md).</span></span>

<span data-ttu-id="380a7-105">Para obter mais informações sobre as principais atualizações, consulte [principais atualizações](major-upgrades.md) em [aplicação de patches e atualizações](patching-and-upgrades.md).</span><span class="sxs-lookup"><span data-stu-id="380a7-105">For more information about major upgrades, see [Major Upgrades](major-upgrades.md) in [Patching and Upgrades](patching-and-upgrades.md).</span></span>

<span data-ttu-id="380a7-106">O pacote de instalação do MNP2000.msi foi atribuído a uma propriedade [**UpgradeCode**](upgradecode.md) , conforme descrito na seção [especificando propriedades](specifying-properties.md).</span><span class="sxs-lookup"><span data-stu-id="380a7-106">The installation package of MNP2000.msi was assigned an [**UpgradeCode**](upgradecode.md) property, as described in the section [Specifying Properties](specifying-properties.md).</span></span>

<span data-ttu-id="380a7-107">Windows Installer aplicará a atualização se o usuário já tiver instalado o 1,0 para versões 1,4 (inclusivo) do idioma inglês MNP2000.</span><span class="sxs-lookup"><span data-stu-id="380a7-107">Windows Installer applies the upgrade if the user has already installed the 1.0 to 1.4 versions (inclusive) of English language MNP2000.</span></span> <span data-ttu-id="380a7-108">Windows Installer migra todas as configurações de recurso do produto original para o produto atualizado.</span><span class="sxs-lookup"><span data-stu-id="380a7-108">Windows Installer migrates all of the original product's feature settings to the upgraded product.</span></span> <span data-ttu-id="380a7-109">O instalador remove os arquivos que pertencem aos produtos originais que não estão sendo usados pela atualização do produto.</span><span class="sxs-lookup"><span data-stu-id="380a7-109">The installer removes the files belonging to the original products not being used by the product's upgrade.</span></span>

<span data-ttu-id="380a7-110">Se sua cópia de MNP2001.msi não incluir uma [tabela de atualização](upgrade-table.md), use Orca ou outro editor de tabela, para importar uma tabela de atualização vazia para o banco de dados do Schema.msi.</span><span class="sxs-lookup"><span data-stu-id="380a7-110">If your copy of MNP2001.msi does not include an [Upgrade table](upgrade-table.md), use Orca, or another table editor, to import an empty Upgrade table into the database from Schema.msi.</span></span> <span data-ttu-id="380a7-111">O SDK fornece uma cópia de Schema.msi.</span><span class="sxs-lookup"><span data-stu-id="380a7-111">The SDK provides a copy of Schema.msi.</span></span> <span data-ttu-id="380a7-112">Use o editor de banco de dados para abrir MNP2001.msi e insira os dados a seguir na tabela de atualização vazia.</span><span class="sxs-lookup"><span data-stu-id="380a7-112">Use your database editor to open MNP2001.msi and enter the following data into the empty Upgrade table.</span></span>



| <span data-ttu-id="380a7-113">UpgradeCode</span><span class="sxs-lookup"><span data-stu-id="380a7-113">UpgradeCode</span></span>                            | <span data-ttu-id="380a7-114">VersionMin</span><span class="sxs-lookup"><span data-stu-id="380a7-114">VersionMin</span></span> | <span data-ttu-id="380a7-115">VersionMax</span><span class="sxs-lookup"><span data-stu-id="380a7-115">VersionMax</span></span> | <span data-ttu-id="380a7-116">Idioma</span><span class="sxs-lookup"><span data-stu-id="380a7-116">Language</span></span> | <span data-ttu-id="380a7-117">Atributos</span><span class="sxs-lookup"><span data-stu-id="380a7-117">Attributes</span></span> | <span data-ttu-id="380a7-118">Remover</span><span class="sxs-lookup"><span data-stu-id="380a7-118">Remove</span></span> | <span data-ttu-id="380a7-119">Açãoproperty</span><span class="sxs-lookup"><span data-stu-id="380a7-119">ActionProperty</span></span> |
|----------------------------------------|------------|------------|----------|------------|--------|----------------|
| <span data-ttu-id="380a7-120">{908E378A-9551-4772-BF1D-5CFAF6FD9CB4}</span><span class="sxs-lookup"><span data-stu-id="380a7-120">{908E378A-9551-4772-BF1D-5CFAF6FD9CB4}</span></span> | <span data-ttu-id="380a7-121">01.00.0000</span><span class="sxs-lookup"><span data-stu-id="380a7-121">01.00.0000</span></span> | <span data-ttu-id="380a7-122">01.40.0000</span><span class="sxs-lookup"><span data-stu-id="380a7-122">01.40.0000</span></span> | <span data-ttu-id="380a7-123">1046</span><span class="sxs-lookup"><span data-stu-id="380a7-123">1033</span></span>     | <span data-ttu-id="380a7-124">769</span><span class="sxs-lookup"><span data-stu-id="380a7-124">769</span></span>        |        | <span data-ttu-id="380a7-125">OLDAPPFOUND</span><span class="sxs-lookup"><span data-stu-id="380a7-125">OLDAPPFOUND</span></span>    |



 

[<span data-ttu-id="380a7-126">Continuar</span><span class="sxs-lookup"><span data-stu-id="380a7-126">Continue</span></span>](updating-properties-for-an-upgrade.md)

 

 



