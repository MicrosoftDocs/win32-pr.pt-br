---
title: Entradas de registro para acompanhar o progresso da instalação
description: Entradas de registro para acompanhar o progresso da instalação
ms.assetid: 898f9117-94fd-4230-9378-b8c6a4401a96
keywords:
- Windows Media Player, acompanhando o progresso da instalação
- Windows Media Player, acompanhamento do progresso da instalação
- Windows Media Player, acompanhamento de progresso de instalações
- Windows Media Player, registro
- registro, acompanhamento do progresso da instalação
- registro, acompanhamento do progresso da instalação
- registro, acompanhamento de progresso de instalações
- registro, configurações do Windows Media Player
- acompanhamento do progresso da instalação
- Instalando o rastreamento de progresso
- rastreamento de progresso de instalações
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3add1d2feb668ee90418704b9a11b0072530f120
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104006150"
---
# <a name="registry-entries-for-tracking-installation-progress"></a><span data-ttu-id="6ebc6-114">Entradas de registro para acompanhar o progresso da instalação</span><span class="sxs-lookup"><span data-stu-id="6ebc6-114">Registry Entries for Tracking Installation Progress</span></span>

<span data-ttu-id="6ebc6-115">O programa de instalação do Windows Media Player 11,wm.exe de instalação \_ , grava as seguintes entradas no registro para que os programas de instalação possam acompanhar o progresso do programa de instalação do Windows Media Player à medida que ele é executado.</span><span class="sxs-lookup"><span data-stu-id="6ebc6-115">The Windows Media Player 11 setup program, setup\_wm.exe, writes the following entries in the registry so that installation programs can track the progress of the Windows Media Player setup program as it runs.</span></span>


```C++
[HKEY_LOCAL_MACHINE\Software\Microsoft\MediaPlayer\Setup]
"Progress_CurrentDialog" = dword:value
"Progress_MaxDialog" = dword:value
"Progress_CurrentInstall" = dword:value
"Progress_MaxInstall" = dword:value
```



<span data-ttu-id="6ebc6-116">Na sintaxe de registro anterior, *Value* é um espaço reservado para um valor inteiro.</span><span class="sxs-lookup"><span data-stu-id="6ebc6-116">In the preceding registry syntax, *value* is a placeholder for an integer value.</span></span>

<span data-ttu-id="6ebc6-117">O progresso \_ CurrentDialog indica qual caixa de diálogo a instalação do Windows Media Player está exibindo no momento.</span><span class="sxs-lookup"><span data-stu-id="6ebc6-117">Progress\_CurrentDialog indicates which dialog box Windows Media Player setup is currently displaying.</span></span> <span data-ttu-id="6ebc6-118">O \_ MaxDialog de progresso indica o número total de caixas de diálogo que o Windows Media exibirá.</span><span class="sxs-lookup"><span data-stu-id="6ebc6-118">Progress\_MaxDialog indicates the total number of dialog boxes that Windows Media will display.</span></span> <span data-ttu-id="6ebc6-119">Por exemplo, se Progress \_ CurrentDialog = 2 e Progress \_ MaxDialog = 5, o Windows Media Player está atualmente exibindo a segunda caixa de diálogo em uma sequência de cinco.</span><span class="sxs-lookup"><span data-stu-id="6ebc6-119">For example, if Progress\_CurrentDialog = 2 and Progress\_MaxDialog = 5, Windows Media Player is currently displaying the second dialog box in a sequence of five.</span></span>

<span data-ttu-id="6ebc6-120">Progresso \_ CurrentInstall e MaxInstall de progresso \_ , em conjunto, indicam a porcentagem de conclusão da caixa de diálogo atual.</span><span class="sxs-lookup"><span data-stu-id="6ebc6-120">Progress\_CurrentInstall and Progress\_MaxInstall, taken together, indicate the percent of completion of the current dialog.</span></span> <span data-ttu-id="6ebc6-121">Por exemplo, se Progress \_ CurrentInstall = 6 e Progress \_ MaxInstall = 25, a caixa de diálogo atual será 6/25 (ou seja, 24%) concluí.</span><span class="sxs-lookup"><span data-stu-id="6ebc6-121">For example, if Progress\_CurrentInstall = 6 and Progress\_MaxInstall = 25, the current dialog is 6/25 (that is, 24%) complete.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6ebc6-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6ebc6-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6ebc6-123">**Configurações do registro**</span><span class="sxs-lookup"><span data-stu-id="6ebc6-123">**Registry Settings**</span></span>](registry-settings.md)
</dt> </dl>

 

 




