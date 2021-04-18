---
description: Uma atualização importante pode ser aplicada instalando o novo pacote de instalação para o produto atualizado.
ms.assetid: f4fb28be-5ec0-4eac-9d4d-eccf5bd61ac4
title: Aplicando as principais atualizações instalando o produto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7619b2ae2b8e1f10cac2fcfae61dde0c6dbba5d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105751659"
---
# <a name="applying-major-upgrades-by-installing-the-product"></a><span data-ttu-id="75a56-103">Aplicando as principais atualizações instalando o produto</span><span class="sxs-lookup"><span data-stu-id="75a56-103">Applying Major Upgrades by Installing the Product</span></span>

<span data-ttu-id="75a56-104">Uma atualização importante pode ser aplicada instalando o novo pacote de instalação para o produto atualizado.</span><span class="sxs-lookup"><span data-stu-id="75a56-104">A major upgrade can be applied by installing the new installation package for the upgraded product.</span></span> <span data-ttu-id="75a56-105">Como as atualizações principais recebem um código de produto diferente do produto original, a instalação da atualização deve ser tratada como uma instalação de um novo produto.</span><span class="sxs-lookup"><span data-stu-id="75a56-105">Because major upgrades get a different product code than the original product, installing the upgrade must be treated as an installation of a new product.</span></span> <span data-ttu-id="75a56-106">A atualização pode ser simplesmente instalada como outro produto.</span><span class="sxs-lookup"><span data-stu-id="75a56-106">The upgrade can simply be installed like another product.</span></span> <span data-ttu-id="75a56-107">Você pode fazer com que o novo pacote de instalação manipule a remoção do produto antigo, incluindo a [tabela de atualização](upgrade-table.md) e a ação [FindRelatedProducts](findrelatedproducts-action.md) e a [ação RemoveExistingProducts](removeexistingproducts-action.md).</span><span class="sxs-lookup"><span data-stu-id="75a56-107">You can have the new installation package handle the removal of the old product by including the [Upgrade table](upgrade-table.md) and the [FindRelatedProducts action](findrelatedproducts-action.md) and [RemoveExistingProducts action](removeexistingproducts-action.md).</span></span>

<span data-ttu-id="75a56-108">**Para propagar uma atualização principal para os usuários atuais da linha de comando**</span><span class="sxs-lookup"><span data-stu-id="75a56-108">**To propagate a major upgrade to current users from the command line**</span></span>

-   <span data-ttu-id="75a56-109">Na linha de comando, use: **msiexec/i \[** _caminho para o arquivo MSI atualizado_*_\]_*</span><span class="sxs-lookup"><span data-stu-id="75a56-109">From the command line, use: **msiexec /i \[**_path to updated msi file_*_\]_*</span></span>

<span data-ttu-id="75a56-110">**Para propagar uma atualização principal para os usuários atuais de um programa**</span><span class="sxs-lookup"><span data-stu-id="75a56-110">**To propagate a major upgrade to current users from a program**</span></span>

-   <span data-ttu-id="75a56-111">Em um programa, chame [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) e especifique o caminho para o arquivo MSI atualizado.</span><span class="sxs-lookup"><span data-stu-id="75a56-111">From a program, call [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) and specify the path to the updated msi file.</span></span>

 

 



