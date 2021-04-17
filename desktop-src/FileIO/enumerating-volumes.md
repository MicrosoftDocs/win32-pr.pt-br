---
description: Para fazer uma lista completa dos volumes em um computador ou manipular cada volume por vez, você pode enumerar volumes.
ms.assetid: 5adcd59a-48b7-4373-a10b-c352962f715a
title: Enumerando volumes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc294d72fa3fad24536b175ee7e5e023066586c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105761733"
---
# <a name="enumerating-volumes"></a><span data-ttu-id="3513f-103">Enumerando volumes</span><span class="sxs-lookup"><span data-stu-id="3513f-103">Enumerating Volumes</span></span>

<span data-ttu-id="3513f-104">Para fazer uma lista completa dos volumes em um computador ou manipular cada volume por vez, você pode enumerar volumes.</span><span class="sxs-lookup"><span data-stu-id="3513f-104">To make a complete list of the volumes on a computer, or to manipulate each volume in turn, you can enumerate volumes.</span></span> <span data-ttu-id="3513f-105">Em um volume, você pode [verificar se há pastas montadas](enumerating-volume-mount-points.md) ou outros objetos no volume.</span><span class="sxs-lookup"><span data-stu-id="3513f-105">Within a volume, you can [scan for mounted folders](enumerating-volume-mount-points.md) or other objects on the volume.</span></span>

<span data-ttu-id="3513f-106">Três funções permitem que um aplicativo enumere volumes em um computador:</span><span class="sxs-lookup"><span data-stu-id="3513f-106">Three functions allow an application to enumerate volumes on a computer:</span></span>

-   [<span data-ttu-id="3513f-107">**FindFirstVolume**</span><span class="sxs-lookup"><span data-stu-id="3513f-107">**FindFirstVolume**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew)
-   [<span data-ttu-id="3513f-108">**FindNextVolume**</span><span class="sxs-lookup"><span data-stu-id="3513f-108">**FindNextVolume**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-findnextvolumew)
-   [<span data-ttu-id="3513f-109">**FindVolumeClose**</span><span class="sxs-lookup"><span data-stu-id="3513f-109">**FindVolumeClose**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-findvolumeclose)

<span data-ttu-id="3513f-110">Essas três funções operam de maneira muito semelhante às funções [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea), [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea)e [**FindClose**](/windows/desktop/api/FileAPI/nf-fileapi-findclose) .</span><span class="sxs-lookup"><span data-stu-id="3513f-110">These three functions operate in a manner very similar to the [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea), [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea), and [**FindClose**](/windows/desktop/api/FileAPI/nf-fileapi-findclose) functions.</span></span>

<span data-ttu-id="3513f-111">Inicie uma pesquisa de volumes com [**FindFirstVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew).</span><span class="sxs-lookup"><span data-stu-id="3513f-111">Begin a search for volumes with [**FindFirstVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew).</span></span> <span data-ttu-id="3513f-112">Se a pesquisa for bem-sucedida, processe os resultados de acordo com o design do seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="3513f-112">If the search is successful, process the results according to the design of your application.</span></span> <span data-ttu-id="3513f-113">Em seguida, use [**FindNextVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findnextvolumew) em um loop para localizar e processar cada volume subsequente.</span><span class="sxs-lookup"><span data-stu-id="3513f-113">Then use [**FindNextVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findnextvolumew) in a loop to locate and process each subsequent volume.</span></span> <span data-ttu-id="3513f-114">Quando o fornecimento de volumes for esgotado, feche a pesquisa com [**FindVolumeClose**](/windows/desktop/api/FileAPI/nf-fileapi-findvolumeclose).</span><span class="sxs-lookup"><span data-stu-id="3513f-114">When the supply of volumes is exhausted, close the search with [**FindVolumeClose**](/windows/desktop/api/FileAPI/nf-fileapi-findvolumeclose).</span></span>

<span data-ttu-id="3513f-115">Você não deve assumir nenhuma correlação entre a ordem dos volumes que são retornados por essas funções e a ordem dos volumes que são retornados por outras funções ou ferramentas.</span><span class="sxs-lookup"><span data-stu-id="3513f-115">You should not assume any correlation between the order of the volumes that are returned by these functions and the order of the volumes that are returned by other functions or tools.</span></span> <span data-ttu-id="3513f-116">Em particular, não assuma nenhuma correlação entre a ordem de volume e as letras da unidade, conforme atribuído pelo BIOS (se houver) ou pelo administrador do disco.</span><span class="sxs-lookup"><span data-stu-id="3513f-116">In particular, do not assume any correlation between volume order and drive letters as assigned by the BIOS (if any) or the Disk Administrator.</span></span>

<span data-ttu-id="3513f-117">Consulte [exemplos de pastas montadas](volume-mount-point-examples.md) para obter um exemplo de como enumerar os volumes em um computador.</span><span class="sxs-lookup"><span data-stu-id="3513f-117">See [Mounted Folder Examples](volume-mount-point-examples.md) for an example of how to enumerate the volumes on a computer.</span></span>

 

 



