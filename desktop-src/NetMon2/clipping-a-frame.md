---
description: Você pode especificar que o driver corte os quadros.
ms.assetid: a4f53568-684b-48cf-835b-915cefb45a5d
title: Recortando um quadro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1507b82ffedeb26939d5d954f116bb009ed0ab41
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105811823"
---
# <a name="clipping-a-frame"></a><span data-ttu-id="d670f-103">Recortando um quadro</span><span class="sxs-lookup"><span data-stu-id="d670f-103">Clipping a Frame</span></span>

<span data-ttu-id="d670f-104">Você pode especificar que o driver corte os quadros.</span><span class="sxs-lookup"><span data-stu-id="d670f-104">You can specify that the driver clip the frames.</span></span> <span data-ttu-id="d670f-105">(Se as outras seções de filtro de captura forem omitidas, essa poderá ser a única função do seu filtro de captura).</span><span class="sxs-lookup"><span data-stu-id="d670f-105">(If the other capture filter sections are omitted, this may be the only function of your capture filter).</span></span> <span data-ttu-id="d670f-106">Se o campo **nFrameBytesToCopy** não for zero (0), seu valor especificará quantos bytes de cada quadro receberão para reter.</span><span class="sxs-lookup"><span data-stu-id="d670f-106">If the **nFrameBytesToCopy** field is not zero (0), its value specifies how many bytes of each frame received to retain.</span></span> <span data-ttu-id="d670f-107">Se o campo for zero, o quadro inteiro será retido.</span><span class="sxs-lookup"><span data-stu-id="d670f-107">If the field is zero, then the whole frame is retained.</span></span>

> [!Note]  
> <span data-ttu-id="d670f-108">Você pode cortar qualquer quadro que passe as outras partes do filtro de captura definindo **nFrameBytesToCopy**.</span><span class="sxs-lookup"><span data-stu-id="d670f-108">You may clip any frame that passes the other portions of your capture filter by setting **nFrameBytesToCopy**.</span></span>

 

 

 



