---
description: Este exemplo ilustra como criar um pacote de patch que aplica uma pequena atualização ao pacote de instalação de exemplo abordado em um exemplo de instalação.
ms.assetid: 17dadd64-6e81-444a-985e-1b340e4f2ee5
title: Um exemplo de aplicação de patch de atualização pequena
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36d4997a326e8fea33086a75c9cf40ecef8cb997
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105750827"
---
# <a name="a-small-update-patching-example"></a><span data-ttu-id="96c4d-103">Um exemplo de aplicação de patch de atualização pequena</span><span class="sxs-lookup"><span data-stu-id="96c4d-103">A Small Update Patching Example</span></span>

<span data-ttu-id="96c4d-104">Este exemplo ilustra como criar um [pacote de patch](patch-packages.md) que aplica uma [pequena atualização](small-updates.md) ao pacote de instalação de exemplo abordado em [um exemplo de instalação](an-installation-example.md).</span><span class="sxs-lookup"><span data-stu-id="96c4d-104">This example illustrates how to create a [patch package](patch-packages.md) that applies a [small update](small-updates.md) to the sample installation package discussed in [An Installation Example](an-installation-example.md).</span></span> <span data-ttu-id="96c4d-105">Uma pequena atualização faz alterações em um ou mais arquivos de aplicativo que são considerados muito pequenos para garantir a alteração do código do produto.</span><span class="sxs-lookup"><span data-stu-id="96c4d-105">A small update makes changes to one or more application files that are judged to be too minor to warrant changing the product code.</span></span> <span data-ttu-id="96c4d-106">Para obter mais informações [, consulte patches e atualizações](patching-and-upgrades.md).</span><span class="sxs-lookup"><span data-stu-id="96c4d-106">For more information see [Patching and Upgrades](patching-and-upgrades.md).</span></span>

<span data-ttu-id="96c4d-107">Este exemplo ilustra como criar um pacote de patches Windows Installer que atualiza o recurso de concerto do produto hipotético MNP2000 para corrigir um erro no produto original.</span><span class="sxs-lookup"><span data-stu-id="96c4d-107">This example illustrates how to create a Windows Installer patch package that updates the Concert feature of the hypothetical product MNP2000 to fix an error in the original product.</span></span> <span data-ttu-id="96c4d-108">O pacote de patch de exemplo aplica uma pequena atualização ao produto que não exige a alteração do código do produto.</span><span class="sxs-lookup"><span data-stu-id="96c4d-108">The example patch package applies a small update to the product that does not require changing the product code.</span></span> <span data-ttu-id="96c4d-109">Consulte o tópico sobre as [principais atualizações](major-upgrades.md) na seção [patches e atualizações](patching-and-upgrades.md) para obter mais informações sobre as principais atualizações.</span><span class="sxs-lookup"><span data-stu-id="96c4d-109">See the topic on [Major Upgrades](major-upgrades.md) in the [Patching and Upgrades](patching-and-upgrades.md) section for more information about major upgrades.</span></span>

<span data-ttu-id="96c4d-110">O pacote de atualização de exemplo tem as seguintes especificações:</span><span class="sxs-lookup"><span data-stu-id="96c4d-110">The sample upgrade package has the following specifications:</span></span>

-   <span data-ttu-id="96c4d-111">Ele corrige um erro secundário no cronograma de concerto exibido pelo recurso de concerto.</span><span class="sxs-lookup"><span data-stu-id="96c4d-111">It corrects a minor error in the Concert schedule displayed by the Concert feature.</span></span>
-   <span data-ttu-id="96c4d-112">Ele atualiza o código do pacote para refletir que o pacote de instalação foi alterado.</span><span class="sxs-lookup"><span data-stu-id="96c4d-112">It updates the package code to reflect the installation package has changed.</span></span>
-   <span data-ttu-id="96c4d-113">A pequena atualização pode ser aplicada por meio da aplicação de patch na instalação local do produto.</span><span class="sxs-lookup"><span data-stu-id="96c4d-113">The small update can be applied by patching the local installation of the product.</span></span>

[<span data-ttu-id="96c4d-114">Continuar</span><span class="sxs-lookup"><span data-stu-id="96c4d-114">Continue</span></span>](planning-a-small-update-patch.md)

 

 



