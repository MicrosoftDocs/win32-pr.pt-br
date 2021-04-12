---
title: Portando funções de anti-aliasing
description: Portando funções de anti-aliasing
ms.assetid: 7f79f0fa-4a08-4678-bc73-8611e8d9e91a
keywords:
- Portabilidade do íris GL, anti-aliasing
- portando do íris GL, antialiasing
- portando para OpenGL do íris GL, antialiasing
- Portabilidade OpenGL do íris GL, antialiasing
- suavização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ec2fcae4fe7b6909e00efb0fb892821a5c12765
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364422"
---
# <a name="porting-antialiasing-functions"></a>Portando funções de anti-aliasing

No OpenGL, o modo de subpixel é sempre ativado, consequentemente, o **subpixel** da função de Engl da íris (**true**) não é necessário e não tem equivalente a OpenGL. Os tópicos a seguir descrevem os aspectos do código de anti-aliasing do íris GL.

-   [Portando o código de mesclagem](porting-blending-code.md)
-   [Portando funções de teste do aFunction](porting-afunction-test-functions.md)
-   [Usando funções de anti-aliasing](using-antialiasing-functions.md)

 

 




