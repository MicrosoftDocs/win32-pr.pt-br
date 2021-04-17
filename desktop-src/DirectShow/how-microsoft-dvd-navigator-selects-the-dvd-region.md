---
description: Como o navegador de DVD da Microsoft seleciona a região do DVD
ms.assetid: 407619c6-2d4b-4f7f-a861-42ee0f462ecd
title: Como o navegador de DVD da Microsoft seleciona a região do DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f8a2898725ad187946b50e567f7daa7e72a9886
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105759553"
---
# <a name="how-microsoft-dvd-navigator-selects-the-dvd-region"></a><span data-ttu-id="d8792-103">Como o navegador de DVD da Microsoft seleciona a região do DVD</span><span class="sxs-lookup"><span data-stu-id="d8792-103">How Microsoft DVD Navigator Selects the DVD Region</span></span>

<span data-ttu-id="d8792-104">O navegador de DVD da Microsoft usa o seguinte algoritmo para determinar a correspondência de região ao reproduzir discos de DVD em um PC:</span><span class="sxs-lookup"><span data-stu-id="d8792-104">The Microsoft DVD Navigator uses the following algorithm to determine region match while playing DVD discs on a PC:</span></span>

1.  <span data-ttu-id="d8792-105">O navegador de DVD Obtém a região do disco, a região da unidade e a região do decodificador.</span><span class="sxs-lookup"><span data-stu-id="d8792-105">The DVD Navigator gets the disc region, drive region, and decoder region.</span></span>
2.  <span data-ttu-id="d8792-106">Se a região do disco for "todas as regiões", o navegador de DVD reproduzirá o disco.</span><span class="sxs-lookup"><span data-stu-id="d8792-106">If the disc region is "all regions," the DVD Navigator plays the disc.</span></span>
3.  <span data-ttu-id="d8792-107">Se o disco não estiver marcado para todas as regiões, o navegador de DVD verificará se o decodificador tem uma região predefinida.</span><span class="sxs-lookup"><span data-stu-id="d8792-107">If the disc is not marked for all regions, the DVD Navigator checks whether the decoder has a preset region.</span></span>
4.  <span data-ttu-id="d8792-108">Se o decodificador tiver uma região predefinida e não corresponder à região do disco, o navegador de DVD retornará um erro indicando que ele não pode reproduzir o disco na configuração do DVD atual.</span><span class="sxs-lookup"><span data-stu-id="d8792-108">If the decoder has a preset region and it does not match the disc region, the DVD Navigator returns an error indicating that it cannot play the disc on the current DVD configuration.</span></span> <span data-ttu-id="d8792-109">Sido</span><span class="sxs-lookup"><span data-stu-id="d8792-109">(Exit)</span></span>
5.  <span data-ttu-id="d8792-110">Se a região do decodificador não estiver definida ou for igual à região do disco, o navegador de DVD verificará se a região da unidade é igual à região do disco.</span><span class="sxs-lookup"><span data-stu-id="d8792-110">If the decoder region is not set, or is the same as the disc region, the DVD Navigator checks whether the drive region is the same as the disc region.</span></span>
6.  <span data-ttu-id="d8792-111">Se a região da unidade corresponder à região do disco, o navegador de DVD reproduzirá o título.</span><span class="sxs-lookup"><span data-stu-id="d8792-111">If the drive region matches the disc region, the DVD Navigator plays the title.</span></span>
7.  <span data-ttu-id="d8792-112">Caso contrário, se a região do driver não corresponder à região do disco, o navegador de DVD invocará o código para alterar a região da unidade.</span><span class="sxs-lookup"><span data-stu-id="d8792-112">Otherwise, if the driver region does not match the disc region, the DVD Navigator invokes the code to change the drive's region.</span></span> <span data-ttu-id="d8792-113">Se o número permitido de alterações de região tiver sido esgotado, a tentativa de alteração de região falhará e o título não poderá ser reproduzido nesse sistema.</span><span class="sxs-lookup"><span data-stu-id="d8792-113">If the allowed number of region changes has been exhausted, the region change attempt fails and the title cannot be played on that system.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d8792-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d8792-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d8792-115">Suporte à alteração da região do DVD no Windows</span><span class="sxs-lookup"><span data-stu-id="d8792-115">DVD Region Change Support in Windows</span></span>](dvd-region-change-support-in-windows.md)
</dt> </dl>

 

 



