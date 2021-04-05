---
description: Uma pequena atualização faz alterações em um ou mais arquivos de aplicativo que são muito menores para garantir a alteração do código do produto.
ms.assetid: c74ef2bd-9cf5-4ec0-bfff-1fad0e17ba98
title: Pequenas atualizações
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80ca87e825f462a98cc7fc80ad42d2b09b7931d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089982"
---
# <a name="small-updates"></a><span data-ttu-id="a9619-103">Pequenas atualizações</span><span class="sxs-lookup"><span data-stu-id="a9619-103">Small Updates</span></span>

<span data-ttu-id="a9619-104">Uma pequena atualização faz alterações em um ou mais arquivos de aplicativo que são muito menores para garantir a alteração do código do produto.</span><span class="sxs-lookup"><span data-stu-id="a9619-104">A small update makes changes to one or more application files that are too minor to warrant changing the product code.</span></span> <span data-ttu-id="a9619-105">Uma pequena atualização também é conhecida como atualização de QFE (rápida correção de engenharia).</span><span class="sxs-lookup"><span data-stu-id="a9619-105">A small update is also commonly referred to as a quick fix engineering (QFE) update.</span></span> <span data-ttu-id="a9619-106">Uma pequena atualização não permite a reorganização da árvore de componentes de recursos.</span><span class="sxs-lookup"><span data-stu-id="a9619-106">A small update does not permit reorganization of the feature-component tree.</span></span>

<span data-ttu-id="a9619-107">Uma pequena atualização típica altera apenas um ou dois arquivos ou uma chave do registro.</span><span class="sxs-lookup"><span data-stu-id="a9619-107">A typical small update changes only one or two files or a registry key.</span></span> <span data-ttu-id="a9619-108">Como uma pequena atualização altera as informações no arquivo. msi, o código do pacote de instalação deve ser alterado.</span><span class="sxs-lookup"><span data-stu-id="a9619-108">Because a small update changes the information in the .msi file, the installation package code must be changed.</span></span> <span data-ttu-id="a9619-109">O código do pacote é armazenado na propriedade [**Resumo do número de revisão**](revision-number-summary.md) do fluxo de informações de [Resumo](summary-information-stream.md).</span><span class="sxs-lookup"><span data-stu-id="a9619-109">The package code is stored in the [**Revision Number Summary**](revision-number-summary.md) property of the [Summary Information Stream](summary-information-stream.md).</span></span>

<span data-ttu-id="a9619-110">O código do produto nunca é alterado com uma pequena atualização, portanto, todas as alterações introduzidas por uma pequena atualização precisam ser consistentes com as diretrizes descritas em [alterando o código do produto](changing-the-product-code.md).</span><span class="sxs-lookup"><span data-stu-id="a9619-110">The product code is never changed with a small update, so all of the changes introduced by a small update have to be consistent with the guidelines described in [Changing the Product Code](changing-the-product-code.md).</span></span> <span data-ttu-id="a9619-111">Uma atualização requer uma [atualização importante](major-upgrades.md) para alterar o [**ProductCode**](productcode.md).</span><span class="sxs-lookup"><span data-stu-id="a9619-111">An update requires a [major upgrade](major-upgrades.md) to change the [**ProductCode**](productcode.md).</span></span> <span data-ttu-id="a9619-112">Se for necessário diferenciar os produtos sem alterar o código do produto, use uma [atualização secundária](minor-upgrades.md).</span><span class="sxs-lookup"><span data-stu-id="a9619-112">If it is necessary to differentiate between products without changing the product code, use a [minor upgrade](minor-upgrades.md).</span></span>

<span data-ttu-id="a9619-113">Para obter informações sobre como aplicar um pacote de patch de atualização pequena a um pacote Windows Installer, consulte [criando um patch de atualização pequeno](creating-a-small-update-patch.md), [aplicando pequenas atualizações por meio da aplicação de patch na instalação local do produto](applying-small-updates-by-patching-the-local-installation-of-the-product.md), [aplicando pequenas atualizações reinstalando o produto](applying-small-updates-by-reinstalling-the-product.md)e [aplicando pequenas atualizações por meio de patch de uma imagem administrativa](applying-small-updates-by-patching-an-administrative-image.md).</span><span class="sxs-lookup"><span data-stu-id="a9619-113">For information on how to apply a small update patch package to a Windows Installer package, see [Creating a Small Update Patch](creating-a-small-update-patch.md), [Applying Small Updates by Patching the Local Installation of the Product](applying-small-updates-by-patching-the-local-installation-of-the-product.md), [Applying Small Updates by Reinstalling the Product](applying-small-updates-by-reinstalling-the-product.md), and [Applying Small Updates by Patching an Administrative Image](applying-small-updates-by-patching-an-administrative-image.md).</span></span>

 

 



