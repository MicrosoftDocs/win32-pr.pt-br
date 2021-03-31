---
description: As transformações inseridas são armazenadas dentro do arquivo. msi do pacote. Isso garante aos usuários que a transformação está sempre disponível quando o pacote de instalação está disponível. Como alternativa, as transformações podem ser fornecidas aos usuários como arquivos. MST autônomos.
ms.assetid: f7b265df-4b34-44ea-85ab-8dbca4797517
title: Transformações inseridas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 301e7f188da1a46411636ef90b7e6ae327a06c22
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011150"
---
# <a name="embedded-transforms"></a><span data-ttu-id="f6e79-105">Transformações inseridas</span><span class="sxs-lookup"><span data-stu-id="f6e79-105">Embedded Transforms</span></span>

<span data-ttu-id="f6e79-106">As transformações inseridas são armazenadas dentro do arquivo. msi do pacote.</span><span class="sxs-lookup"><span data-stu-id="f6e79-106">Embedded transforms are stored inside the .msi file of the package.</span></span> <span data-ttu-id="f6e79-107">Isso garante aos usuários que a transformação está sempre disponível quando o pacote de instalação está disponível.</span><span class="sxs-lookup"><span data-stu-id="f6e79-107">This guarantees to users that the transform is always available when the installation package is available.</span></span> <span data-ttu-id="f6e79-108">Como alternativa, as transformações podem ser fornecidas aos usuários como arquivos. MST autônomos.</span><span class="sxs-lookup"><span data-stu-id="f6e79-108">Alternatively, transforms may be provided to users as standalone .mst files.</span></span>

<span data-ttu-id="f6e79-109">Para adicionar uma transformação inserida à lista transformações, adicione dois-pontos (:) prefixo para o nome do arquivo.</span><span class="sxs-lookup"><span data-stu-id="f6e79-109">To add an embedded transform to the transforms list, add a colon (:) prefix to the file name.</span></span> <span data-ttu-id="f6e79-110">Como o instalador sempre pode obter a transformação do armazenamento no arquivo. msi, as transformações incorporadas não são armazenadas em cache no computador do usuário.</span><span class="sxs-lookup"><span data-stu-id="f6e79-110">Because the installer can always obtain the transform from storage in the .msi file, embedded transforms are not cached on the user's computer.</span></span> <span data-ttu-id="f6e79-111">As transformações incorporadas podem ser usadas em combinação com [transformações protegidas](secured-transforms.md) ou [transformações não seguras](unsecured-transforms.md).</span><span class="sxs-lookup"><span data-stu-id="f6e79-111">Embedded transforms may be used in combination with [secured transforms](secured-transforms.md) or [unsecured transforms](unsecured-transforms.md).</span></span> <span data-ttu-id="f6e79-112">Para obter mais informações, consulte [aplicando transformações](applying-transforms.md).</span><span class="sxs-lookup"><span data-stu-id="f6e79-112">For more information, see [Applying Transforms](applying-transforms.md).</span></span>

 

 



