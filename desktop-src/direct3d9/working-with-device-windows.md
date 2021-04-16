---
description: Esta seção lista um problema que você pode encontrar ao trabalhar com janelas de dispositivos em aplicativos Direct3D.
ms.assetid: 7cfd2ad6-fb85-4303-9fa4-6fe7d16d9951
title: Trabalhando com dispositivos Windows (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b56352ef0ec66def620a0ae0995d92d8b421722e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105808285"
---
# <a name="working-with-device-windows-direct3d-9"></a><span data-ttu-id="62677-103">Trabalhando com dispositivos Windows (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="62677-103">Working with Device Windows (Direct3D 9)</span></span>

<span data-ttu-id="62677-104">Esta seção lista um problema que você pode encontrar ao trabalhar com janelas de dispositivos em aplicativos Direct3D.</span><span class="sxs-lookup"><span data-stu-id="62677-104">This section lists an issue that you might encounter when working with device windows in Direct3D applications.</span></span>

-   <span data-ttu-id="62677-105">O Direct3D só conecta as janelas de foco em vez da janela do dispositivo com a função de processamento de mensagens do Direct3D e processa apenas as mensagens da janela de foco.</span><span class="sxs-lookup"><span data-stu-id="62677-105">Direct3D only hooks up the focus windows instead of the device window with the Direct3D message processing function, and only processes the focus window messages.</span></span> <span data-ttu-id="62677-106">Portanto, a janela de foco deve ser o pai de qualquer janela do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="62677-106">So, the focus window should be the parent of any device window.</span></span>

## <a name="related-topics"></a><span data-ttu-id="62677-107">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="62677-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="62677-108">Dicas de programação</span><span class="sxs-lookup"><span data-stu-id="62677-108">Programming Tips</span></span>](programming-tips.md)
</dt> </dl>

 

 



