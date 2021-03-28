---
description: Para editar uma imagem armazenada em um metarquivo avançado, um aplicativo deve executar as tarefas descritas no procedimento a seguir.
ms.assetid: 19d9c523-cff8-47e1-bbf2-16d8991dac3b
title: Editando um metarquivo avançado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c86dc9cc609d616bf82ae3f0a13d8d63e827e3eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091188"
---
# <a name="editing-an-enhanced-metafile"></a><span data-ttu-id="21c58-103">Editando um metarquivo avançado</span><span class="sxs-lookup"><span data-stu-id="21c58-103">Editing an Enhanced Metafile</span></span>

<span data-ttu-id="21c58-104">Para editar uma imagem armazenada em um metarquivo avançado, um aplicativo deve executar as tarefas descritas no procedimento a seguir.</span><span class="sxs-lookup"><span data-stu-id="21c58-104">To edit a picture stored in an enhanced metafile, an application must perform the tasks described in the following procedure.</span></span>

<span data-ttu-id="21c58-105">**Para editar uma imagem armazenada em um metarquivo avançado**</span><span class="sxs-lookup"><span data-stu-id="21c58-105">**To edit a picture stored in an enhanced metafile**</span></span>

1.  <span data-ttu-id="21c58-106">Use o teste de impacto para capturar as coordenadas do cursor e recuperar a posição do objeto (linha, arco, retângulo, elipse, polígono ou forma irregular) que o usuário deseja alterar.</span><span class="sxs-lookup"><span data-stu-id="21c58-106">Use hit-testing to capture the cursor coordinates and retrieve the position of the object (line, arc, rectangle, ellipse, polygon, or irregular shape) that the user wants to alter.</span></span>
2.  <span data-ttu-id="21c58-107">Converta essas coordenadas em unidades lógicas (ou mundiais).</span><span class="sxs-lookup"><span data-stu-id="21c58-107">Convert these coordinates to logical (or world) units.</span></span>
3.  <span data-ttu-id="21c58-108">Chame a função [**EnumEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-enumenhmetafile) e examine cada registro de metarquivo.</span><span class="sxs-lookup"><span data-stu-id="21c58-108">Call the [**EnumEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-enumenhmetafile) function and examine each metafile record.</span></span>
4.  <span data-ttu-id="21c58-109">Determine se um determinado registro corresponde a uma função de desenho GDI.</span><span class="sxs-lookup"><span data-stu-id="21c58-109">Determine whether a given record corresponds to a GDI drawing function.</span></span>
5.  <span data-ttu-id="21c58-110">Se tiver, determine se as coordenadas armazenadas no registro correspondem à linha, ao arco, à elipse ou a outros elementos gráficos que interseccionam as coordenadas especificadas pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="21c58-110">If it does, determine whether the coordinates stored in the record correspond to the line, arc, ellipse, or other graphics element that intersects the coordinates specified by the user.</span></span>
6.  <span data-ttu-id="21c58-111">Ao localizar o registro que corresponde à saída que o usuário deseja alterar, apague o objeto na tela que corresponde ao registro original.</span><span class="sxs-lookup"><span data-stu-id="21c58-111">Upon finding the record that corresponds to the output that the user wants to alter, erase the object on the screen that corresponds to the original record.</span></span>
7.  <span data-ttu-id="21c58-112">Exclua o registro correspondente do metarquivo, salvando um ponteiro em seu local.</span><span class="sxs-lookup"><span data-stu-id="21c58-112">Delete the corresponding record from the metafile, saving a pointer to its location.</span></span>
8.  <span data-ttu-id="21c58-113">Permitir que o usuário redesenhe ou substitua o objeto.</span><span class="sxs-lookup"><span data-stu-id="21c58-113">Permit the user to redraw or replace the object.</span></span>
9.  <span data-ttu-id="21c58-114">Converta as funções GDI usadas para desenhar o novo objeto em um ou mais registros de metarquivo avançado.</span><span class="sxs-lookup"><span data-stu-id="21c58-114">Convert the GDI functions used to draw the new object into one or more enhanced-metafile records.</span></span>
10. <span data-ttu-id="21c58-115">Armazene esses registros no metarquivo avançado.</span><span class="sxs-lookup"><span data-stu-id="21c58-115">Store these records in the enhanced metafile.</span></span>

 

 



