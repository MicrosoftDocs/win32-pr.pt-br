---
title: Lendo de um arquivo
description: Lendo de um arquivo
ms.assetid: 7c728304-7d05-4e28-a9bd-83b5b1af39be
keywords:
- Função AVIFileInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba1ffe866e454a898c5c3b91c7721c24f6a861ed
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005935"
---
# <a name="reading-from-a-file"></a><span data-ttu-id="6cf7c-104">Lendo de um arquivo</span><span class="sxs-lookup"><span data-stu-id="6cf7c-104">Reading from a File</span></span>

<span data-ttu-id="6cf7c-105">Você pode recuperar informações sobre um arquivo aberto usando a função [**AVIFileInfo**](/windows/desktop/api/Vfw/nf-vfw-avifileinfo) .</span><span class="sxs-lookup"><span data-stu-id="6cf7c-105">You can retrieve information about an open file by using the [**AVIFileInfo**](/windows/desktop/api/Vfw/nf-vfw-avifileinfo) function.</span></span> <span data-ttu-id="6cf7c-106">Essa função preenche a estrutura [**AVIFILEINFO**](/windows/desktop/api/Vfw/ns-vfw-avifileinfoa) com tais informações como a taxa máxima de dados, o número de fluxos no arquivo, se o arquivo usa um índice e se o arquivo está protegido por direitos autorais.</span><span class="sxs-lookup"><span data-stu-id="6cf7c-106">This function fills the [**AVIFILEINFO**](/windows/desktop/api/Vfw/ns-vfw-avifileinfoa) structure with such information as the maximum data rate, the number of streams in the file, whether the file uses an index, and whether the file is copyrighted.</span></span>

<span data-ttu-id="6cf7c-107">Para recuperar informações suplementares em um arquivo AVI, use a função [**AVIFileReadData**](/windows/desktop/api/Vfw/nf-vfw-avifilereaddata) .</span><span class="sxs-lookup"><span data-stu-id="6cf7c-107">To retrieve supplementary information in an AVI file, use the [**AVIFileReadData**](/windows/desktop/api/Vfw/nf-vfw-avifilereaddata) function.</span></span> <span data-ttu-id="6cf7c-108">As informações complementares são aplicáveis ao arquivo inteiro e não estão incluídas nos cabeçalhos de arquivo normais.</span><span class="sxs-lookup"><span data-stu-id="6cf7c-108">Supplementary information is applicable to the entire file and is not included in the normal file headers.</span></span> <span data-ttu-id="6cf7c-109">Por exemplo, o nome da empresa ou pessoa que mantém os direitos autorais de um arquivo pode ser informações complementares.</span><span class="sxs-lookup"><span data-stu-id="6cf7c-109">For example, the name of the company or person who holds the copyrights of a file could be supplementary information.</span></span> <span data-ttu-id="6cf7c-110">As informações suplementares não aderem a um formato específico; Ele pode ser específico do arquivo.</span><span class="sxs-lookup"><span data-stu-id="6cf7c-110">Supplementary information does not adhere to a specific format; it can be file specific.</span></span> <span data-ttu-id="6cf7c-111">**AVIFileReadData** retorna as informações suplementares em um buffer fornecido pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6cf7c-111">**AVIFileReadData** returns the supplementary information in an application-supplied buffer.</span></span>

 

 




