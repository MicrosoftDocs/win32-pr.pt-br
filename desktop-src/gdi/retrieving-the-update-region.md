---
description: As funções GetUpdateRect e GetUpdateRgn recuperam a região de atualização atual para a janela.
ms.assetid: c0729c4f-3b00-4ab9-91b2-4a2fecee8727
title: Recuperando a região de atualização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8115f47a6c585d5b660d73bbf4fb3de21334b6c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165049"
---
# <a name="retrieving-the-update-region"></a><span data-ttu-id="710c7-103">Recuperando a região de atualização</span><span class="sxs-lookup"><span data-stu-id="710c7-103">Retrieving the Update Region</span></span>

<span data-ttu-id="710c7-104">As funções [**GetUpdateRect**](/windows/desktop/api/Winuser/nf-winuser-getupdaterect) e [**GetUpdateRgn**](/windows/desktop/api/Winuser/nf-winuser-getupdatergn) recuperam a região de atualização atual para a janela.</span><span class="sxs-lookup"><span data-stu-id="710c7-104">The [**GetUpdateRect**](/windows/desktop/api/Winuser/nf-winuser-getupdaterect) and [**GetUpdateRgn**](/windows/desktop/api/Winuser/nf-winuser-getupdatergn) functions retrieve the current update region for the window.</span></span> <span data-ttu-id="710c7-105">GetUpdateRect recupera o menor retângulo (em coordenadas lógicas) que inclui toda a região de atualização.</span><span class="sxs-lookup"><span data-stu-id="710c7-105">GetUpdateRect retrieves the smallest rectangle (in logical coordinates) that encloses the entire update region.</span></span> <span data-ttu-id="710c7-106">GetUpdateRgn recupera a própria região de atualização.</span><span class="sxs-lookup"><span data-stu-id="710c7-106">GetUpdateRgn retrieves the update region itself.</span></span> <span data-ttu-id="710c7-107">Essas funções podem ser usadas para calcular o tamanho atual da região de atualização para determinar onde executar uma operação de desenho.</span><span class="sxs-lookup"><span data-stu-id="710c7-107">These functions can be used to calculate the current size of the update region to determine where to carry out a drawing operation.</span></span>

<span data-ttu-id="710c7-108">[**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) também recupera as dimensões do menor retângulo que envolve a região de atualização atual, copiando as dimensões para o membro **RcPaint** na estrutura [**PAINTSTRUCT**](/windows/win32/api/winuser/ns-winuser-paintstruct) .</span><span class="sxs-lookup"><span data-stu-id="710c7-108">[**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) also retrieves the dimensions of the smallest rectangle enclosing the current update region, copying the dimensions to the **rcPaint** member in the [**PAINTSTRUCT**](/windows/win32/api/winuser/ns-winuser-paintstruct) structure.</span></span> <span data-ttu-id="710c7-109">Como **BeginPaint** valida a região de atualização, qualquer chamada para [**GetUpdateRect**](/windows/desktop/api/Winuser/nf-winuser-getupdaterect) e [**GetUpdateRgn**](/windows/desktop/api/Winuser/nf-winuser-getupdatergn) imediatamente após uma chamada para **BeginPaint** retorna uma região de atualização vazia.</span><span class="sxs-lookup"><span data-stu-id="710c7-109">Because **BeginPaint** validates the update region, any call to [**GetUpdateRect**](/windows/desktop/api/Winuser/nf-winuser-getupdaterect) and [**GetUpdateRgn**](/windows/desktop/api/Winuser/nf-winuser-getupdatergn) immediately after a call to **BeginPaint** returns an empty update region.</span></span>

 

 



