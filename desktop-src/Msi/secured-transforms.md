---
description: As transformações protegidas às vezes são necessárias por motivos de segurança.
ms.assetid: c6019b28-b0a7-4104-9d78-b4b4228635b8
title: Transformações protegidas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e498d6049a2c913ca78f12b6a8700a104af37c4e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837400"
---
# <a name="secured-transforms"></a><span data-ttu-id="0e60e-103">Transformações protegidas</span><span class="sxs-lookup"><span data-stu-id="0e60e-103">Secured Transforms</span></span>

<span data-ttu-id="0e60e-104">As transformações protegidas às vezes são necessárias por motivos de segurança.</span><span class="sxs-lookup"><span data-stu-id="0e60e-104">Secured transforms are sometimes necessary for security reasons.</span></span> <span data-ttu-id="0e60e-105">As transformações protegidas são armazenadas localmente no computador do usuário em um local em que, em um sistema de arquivos seguro, o usuário não tem acesso de gravação.</span><span class="sxs-lookup"><span data-stu-id="0e60e-105">Secured transforms are stored locally on the user's computer in a location where, on a secure file system, the user does not have write access.</span></span> <span data-ttu-id="0e60e-106">Essas transformações são armazenadas em cache nesse local durante a instalação ou o anúncio do pacote.</span><span class="sxs-lookup"><span data-stu-id="0e60e-106">Such transforms are cached in this location during the installation or advertisement of the package.</span></span> <span data-ttu-id="0e60e-107">Somente administradores e sistema local têm acesso de gravação a esse local.</span><span class="sxs-lookup"><span data-stu-id="0e60e-107">Only administrators and local system have write access to this location.</span></span> <span data-ttu-id="0e60e-108">Um usuário não administrador não poderá modificar o arquivo de transformação.</span><span class="sxs-lookup"><span data-stu-id="0e60e-108">A non-admin user would not be able to modify the transform file.</span></span> <span data-ttu-id="0e60e-109">Durante as instalações subsequentes de [instalação sob demanda](installation-on-demand.md) ou [manutenção](maintenance-installation.md) do pacote, o instalador usa as transformações em cache.</span><span class="sxs-lookup"><span data-stu-id="0e60e-109">During subsequent [installation-on-demand](installation-on-demand.md) or [maintenance installations](maintenance-installation.md) of the package, the installer uses the cached transforms.</span></span>

<span data-ttu-id="0e60e-110">Para especificar o armazenamento de transformação seguro, defina a [política TransformsSecure](transformssecure-policy.md), defina a propriedade [**TransformsSecure**](transformssecure.md) ou passe o símbolo @ ou \| na lista transformações.</span><span class="sxs-lookup"><span data-stu-id="0e60e-110">To specify secured transform storage, set the [TransformsSecure policy](transformssecure-policy.md), set the [**TRANSFORMSSECURE**](transformssecure.md) property, or pass the @ or \| symbol in the transforms list.</span></span> <span data-ttu-id="0e60e-111">Observe que você não pode incluir transformações seguras e não seguras na mesma lista de transformações.</span><span class="sxs-lookup"><span data-stu-id="0e60e-111">Note that you cannot include secured and unsecured transforms in the same transforms list.</span></span> <span data-ttu-id="0e60e-112">Consulte [aplicando transformações](applying-transforms.md).</span><span class="sxs-lookup"><span data-stu-id="0e60e-112">See [Applying Transforms](applying-transforms.md).</span></span>

<span data-ttu-id="0e60e-113">A remoção do produto por qualquer usuário remove todas as transformações protegidas desse produto do computador do usuário.</span><span class="sxs-lookup"><span data-stu-id="0e60e-113">The removal of the product by any user removes all secured transforms for that product from the user's computer.</span></span>

<span data-ttu-id="0e60e-114">Se o instalador descobrir que uma transformação segura não está disponível localmente, ele tentará restaurar o cache de transformação de uma origem.</span><span class="sxs-lookup"><span data-stu-id="0e60e-114">If the installer finds that a secured transform is not locally available, it then attempts to restore the transform cache from a source.</span></span> <span data-ttu-id="0e60e-115">As transformações seguras podem ser seguras-em-fonte ou caminho completo seguro:</span><span class="sxs-lookup"><span data-stu-id="0e60e-115">Secure transforms can be secure-at-source or secure-full-path:</span></span>

-   <span data-ttu-id="0e60e-116">As [transformações de origem segura](secure-at-source-transforms.md) que estão faltando no cache de transformação local são restauradas da raiz da origem do arquivo. msi.</span><span class="sxs-lookup"><span data-stu-id="0e60e-116">[Secure-at-source transforms](secure-at-source-transforms.md) that are missing from the local transform cache are restored from the root of the source of the .msi file.</span></span>
-   <span data-ttu-id="0e60e-117">[Seguras-as transformações de caminho completo](secure-full-path-transforms.md) que estão ausentes do cache de transformação local são restauradas do caminho completo original especificado pela lista de transformações.</span><span class="sxs-lookup"><span data-stu-id="0e60e-117">[Secure-full-path transforms](secure-full-path-transforms.md) that are missing from the local transform cache are restored from the original full path specified by the transforms list.</span></span>

 

 



