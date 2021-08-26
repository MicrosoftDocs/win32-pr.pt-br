---
title: Transformando em coordenadas de janela
description: Antes que as coordenadas de clipe sejam convertidas em coordenadas de janela, elas são divididas pelo valor de w para produzir coordenadas de dispositivo normalizadas.
ms.assetid: 4c2d0bf6-89e8-485a-9080-c0599f989943
keywords:
- Pipeline de processamento openGL, convertendo em coordenadas de janela
- convertendo em coordenadas de janela OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fa74b42457349b14e151099a3c4238e855ad0001e1b8f9416808a1279b82345
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119887986"
---
# <a name="transforming-to-window-coordinates"></a>Transformando em coordenadas de janela

Antes que as coordenadas de clipe sejam convertidas em coordenadas de janela, elas são divididas pelo valor *de w* para produzir coordenadas de dispositivo normalizadas. A transformação do viewport aplicada a essas coordenadas normalizadas produz coordenadas de janela. Você controla o visor, que determina a área da janela na tela que exibe uma imagem, com [**glDepthRange**](gldepthrange.md) e [**glViewport**](glviewport.md).

 

 




