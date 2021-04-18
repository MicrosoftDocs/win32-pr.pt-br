---
description: As transformações que não foram protegidas, conforme descrito em transformações seguras, são transformações não seguras por padrão.
ms.assetid: feace6c3-7828-44d0-8d2b-482a02e8e0c0
title: Transformações não seguras
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6743898142197d87d4e3fef5d0f48778f6261ff4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105785422"
---
# <a name="unsecured-transforms"></a><span data-ttu-id="3d4f4-103">Transformações não seguras</span><span class="sxs-lookup"><span data-stu-id="3d4f4-103">Unsecured Transforms</span></span>

<span data-ttu-id="3d4f4-104">As transformações que não foram protegidas, conforme descrito em [transformações seguras](secured-transforms.md) , são transformações não seguras por padrão.</span><span class="sxs-lookup"><span data-stu-id="3d4f4-104">Transforms that have not been secured as described in [Secured Transforms](secured-transforms.md) are unsecured transforms by default.</span></span>

<span data-ttu-id="3d4f4-105">Para aplicar uma transformação não segura ao instalar um pacote, passe os nomes de arquivo de transformação na propriedade [**TRANSformações**](transforms.md) ou na cadeia de caracteres de linha de comando.</span><span class="sxs-lookup"><span data-stu-id="3d4f4-105">To apply an unsecured transform when installing a package, pass the transform file names in the [**TRANSFORMS**](transforms.md) property or command line string.</span></span> <span data-ttu-id="3d4f4-106">Não inicie a cadeia de caracteres com os caracteres @ ou \| ou defina a [política TransformsSecure](transformssecure-policy.md) ou a propriedade [**TransformsSecure**](transformssecure.md) .</span><span class="sxs-lookup"><span data-stu-id="3d4f4-106">Do not begin the string with the @ or \| characters or set the [TransformsSecure policy](transformssecure-policy.md) or the [**TRANSFORMSSECURE**](transformssecure.md) property.</span></span> <span data-ttu-id="3d4f4-107">Observe que você não pode combinar transformações não seguras e [transformações protegidas](secured-transforms.md) na mesma lista de transformações.</span><span class="sxs-lookup"><span data-stu-id="3d4f4-107">Note that you cannot combine unsecured transforms and [secured transforms](secured-transforms.md) in the same transforms list.</span></span>

<span data-ttu-id="3d4f4-108">Se o pacote estiver instalado ou anunciado no [contexto de instalação](installation-context.md)por usuário e tiver transformações desprotegidas, o instalador salvará a origem da transformação na pasta dados do aplicativo no perfil do usuário.</span><span class="sxs-lookup"><span data-stu-id="3d4f4-108">If the package is installed or advertised in the per-user [installation context](installation-context.md), and has unsecured transforms, the installer saves the transform source in the Application Data folder in the user's profile.</span></span> <span data-ttu-id="3d4f4-109">Isso permite que um usuário mantenha a personalização de um produto durante a movimentação entre computadores.</span><span class="sxs-lookup"><span data-stu-id="3d4f4-109">This enables a user to maintain their customization of a product while moving between computers.</span></span>

<span data-ttu-id="3d4f4-110">Se o pacote estiver instalado ou anunciado no [contexto de instalação](installation-context.md)por máquina e usar transformações não seguras, o instalador salvará a origem da transformação na pasta% windir% \\ Installer.</span><span class="sxs-lookup"><span data-stu-id="3d4f4-110">If the package is installed or advertised in the per-machine [installation context](installation-context.md), and uses unsecured transforms, the installer saves the transform source in the %windir%\\Installer folder.</span></span>

<span data-ttu-id="3d4f4-111">Durante uma primeira instalação do pacote, o instalador primeiro procura a transformação na origem fornecida pela propriedade [**TRANSformações**](transforms.md) ou cadeia de caracteres de linha de comando.</span><span class="sxs-lookup"><span data-stu-id="3d4f4-111">During a first-time installation of the package, the installer first searches for the transform at the source supplied by the [**TRANSFORMS**](transforms.md) property or command line string.</span></span> <span data-ttu-id="3d4f4-112">Se essa fonte não estiver disponível, o instalador pesquisará a transformação na origem do pacote ao lado do arquivo. msi.</span><span class="sxs-lookup"><span data-stu-id="3d4f4-112">If this source is unavailable, the installer then searches for the transform at the source of the package next to the .msi file.</span></span>

<span data-ttu-id="3d4f4-113">Durante uma [instalação de manutenção](maintenance-installation.md), o instalador pesquisa a transformação no local do cache.</span><span class="sxs-lookup"><span data-stu-id="3d4f4-113">During a [maintenance installation](maintenance-installation.md), the installer searches for the transform at the cache location.</span></span> <span data-ttu-id="3d4f4-114">Se a cópia armazenada em cache da transformação ficar indisponível, o instalador pesquisará a transformação na origem do pacote ao lado do arquivo. msi.</span><span class="sxs-lookup"><span data-stu-id="3d4f4-114">If the cached copy of the transform becomes unavailable, the installer searches for the transform at the source of the package next to the .msi file.</span></span>

<span data-ttu-id="3d4f4-115">Para obter mais informações, consulte [aplicando transformações](applying-transforms.md) e [resiliência de origem](source-resiliency.md).</span><span class="sxs-lookup"><span data-stu-id="3d4f4-115">For more information, see [Applying Transforms](applying-transforms.md) and [Source Resiliency](source-resiliency.md).</span></span>

 

 



