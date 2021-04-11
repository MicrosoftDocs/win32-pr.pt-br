---
title: Parâmetro de animação da área do cliente
description: O sinalizador de animação da área de cliente indica se o usuário deseja desabilitar animações em elementos da interface do usuário.
ms.assetid: 4a3ec9da-d5ae-4cd9-8222-f02143895ce4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c62e25fdb08022d53cbe9e818a0a1089988cd6a6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104162400"
---
# <a name="client-area-animation-parameter"></a><span data-ttu-id="ade63-103">Parâmetro de animação da área do cliente</span><span class="sxs-lookup"><span data-stu-id="ade63-103">Client area animation parameter</span></span>

<span data-ttu-id="ade63-104">O parâmetro de animação da área de cliente indica se o usuário deseja desabilitar animações em elementos de interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="ade63-104">The client area animation parameter indicates whether the user wants to disable animations in UI elements.</span></span> <span data-ttu-id="ade63-105">Os recursos de exibição, como Flash, intermitência, cintilação e movimentação de conteúdo, podem causar capturas de usuários com Epilepsias sensíveis a fotos.</span><span class="sxs-lookup"><span data-stu-id="ade63-105">Display features such as flashing, blinking, flickering, and moving content can cause seizures in users with photo-sensitive epilepsy.</span></span> <span data-ttu-id="ade63-106">Esse parâmetro permite que você habilite ou desabilite todas essas animações.</span><span class="sxs-lookup"><span data-stu-id="ade63-106">This parameter enables you to enable or disable all such animations.</span></span>

<span data-ttu-id="ade63-107">Os aplicativos usam os sinalizadores **SPI \_ GETCLIENTAREAANIMATION** e **SPI \_ SETCLIENTAREAANIMATION** com a função [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) para ativar ou desativar animações da área do cliente.</span><span class="sxs-lookup"><span data-stu-id="ade63-107">Applications use the **SPI\_GETCLIENTAREAANIMATION** and **SPI\_SETCLIENTAREAANIMATION** flags with the [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) function to turn client area animations on or off.</span></span>

 

 