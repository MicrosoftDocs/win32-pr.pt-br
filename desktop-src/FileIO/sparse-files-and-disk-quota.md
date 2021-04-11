---
description: Um arquivo esparso afeta as cotas de usuário pelo tamanho nominal do arquivo, não pela quantidade real alocada de espaço em disco.
ms.assetid: 7dbe1133-f5cb-4925-9448-5d40f1c553ff
title: Arquivos esparsos e cotas de disco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 326780e2b2c5119256272c0d297613d2c32e6e6e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090675"
---
# <a name="sparse-files-and-disk-quotas"></a><span data-ttu-id="e88c6-103">Arquivos esparsos e cotas de disco</span><span class="sxs-lookup"><span data-stu-id="e88c6-103">Sparse Files and Disk Quotas</span></span>

<span data-ttu-id="e88c6-104">Um arquivo esparso afeta as cotas de usuário pelo tamanho nominal do arquivo, não pela quantidade real alocada de espaço em disco.</span><span class="sxs-lookup"><span data-stu-id="e88c6-104">A sparse file affects user quotas by the nominal size of the file, not the actual allocated amount of disk space.</span></span> <span data-ttu-id="e88c6-105">Ou seja, a criação de um arquivo de 50 MB com todos os zero bytes consome 50 MB da cota desse usuário.</span><span class="sxs-lookup"><span data-stu-id="e88c6-105">That is, creating a 50-MB file with all zero bytes consumes 50 MB of that user's quota.</span></span> <span data-ttu-id="e88c6-106">Isso significa que, à medida que o usuário grava dados no arquivo esparso, ele não precisa se preocupar em exceder seu limite de cota rígido, pois já foi cobrado pelo espaço.</span><span class="sxs-lookup"><span data-stu-id="e88c6-106">This means that as the user writes data to the sparse file, he need not worry about exceeding his hard quota limit, because he has already been charged for the space.</span></span> <span data-ttu-id="e88c6-107">Os administradores do sistema não devem contar com o tamanho de um arquivo esparso que permanece pequeno.</span><span class="sxs-lookup"><span data-stu-id="e88c6-107">System administrators should not count on the size of a sparse file remaining small.</span></span> <span data-ttu-id="e88c6-108">Portanto, eles não devem conceder aos seus usuários limites de cota rígido que excedem o espaço físico disponível, apesar do uso de arquivos esparsos.</span><span class="sxs-lookup"><span data-stu-id="e88c6-108">Therefore they should not grant their users hard quota limits that exceed the physical space available, despite the use of sparse files.</span></span>

 

 



