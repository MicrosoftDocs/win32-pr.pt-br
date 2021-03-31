---
title: Transformando em coordenadas da janela
description: Antes que as coordenadas do clipe sejam convertidas em coordenadas da janela, elas são divididas pelo valor de w para produzir coordenadas de dispositivo normalizadas.
ms.assetid: 4c2d0bf6-89e8-485a-9080-c0599f989943
keywords:
- Pipeline de processamento OpenGL, convertendo para coordenadas de janela
- convertendo em coordenadas de janela OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8ec3d8922890cfa3a79c5dacd94e93a06c53a73
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103637043"
---
# <a name="transforming-to-window-coordinates"></a><span data-ttu-id="297f7-105">Transformando em coordenadas da janela</span><span class="sxs-lookup"><span data-stu-id="297f7-105">Transforming to Window Coordinates</span></span>

<span data-ttu-id="297f7-106">Antes que as coordenadas do clipe sejam convertidas em coordenadas da janela, elas são divididas pelo valor de *w* para produzir coordenadas de dispositivo normalizadas.</span><span class="sxs-lookup"><span data-stu-id="297f7-106">Before clip coordinates are converted to window coordinates, they are divided by the value of *w* to yield normalized device coordinates.</span></span> <span data-ttu-id="297f7-107">A transformação viewport aplicada a essas coordenadas normalizadas produz coordenadas de janela.</span><span class="sxs-lookup"><span data-stu-id="297f7-107">The viewport transformation applied to these normalized coordinates produces window coordinates.</span></span> <span data-ttu-id="297f7-108">Você controla o visor, que determina a área da janela na tela que exibe uma imagem, com [**glDepthRange**](gldepthrange.md) e [**glViewport**](glviewport.md).</span><span class="sxs-lookup"><span data-stu-id="297f7-108">You control the viewport, which determines the area of the on-screen window that displays an image, with [**glDepthRange**](gldepthrange.md) and [**glViewport**](glviewport.md).</span></span>

 

 




