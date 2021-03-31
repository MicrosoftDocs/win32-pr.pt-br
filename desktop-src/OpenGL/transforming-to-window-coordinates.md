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
# <a name="transforming-to-window-coordinates"></a>Transformando em coordenadas da janela

Antes que as coordenadas do clipe sejam convertidas em coordenadas da janela, elas são divididas pelo valor de *w* para produzir coordenadas de dispositivo normalizadas. A transformação viewport aplicada a essas coordenadas normalizadas produz coordenadas de janela. Você controla o visor, que determina a área da janela na tela que exibe uma imagem, com [**glDepthRange**](gldepthrange.md) e [**glViewport**](glviewport.md).

 

 




