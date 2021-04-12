---
title: Funções de curva e superfície de portabilidade
description: Funções de curva e superfície de portabilidade
ms.assetid: 2e80f742-6665-4e7c-a8a1-c43c4764ccc8
keywords:
- Portabilidade do íris GL, curvas
- portando do íris GL, curvas
- portando para OpenGL do íris GL, curvas
- Portabilidade OpenGL do íris GL, curvas
- Portabilidade do íris GL, patches da superfície
- portando do íris GL, patches de superfície
- portando para OpenGL do íris GL, patches de superfície
- Portabilidade OpenGL do íris GL, patches de superfície
- curvas
- patches da superfície
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3caedc89697d1c83325a00b3dc1cb55c34612e64
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104291896"
---
# <a name="porting-curve-and-surface-functions"></a>Funções de curva e superfície de portabilidade

O OpenGL não dá suporte a equivalentes às funções da íris GL para as curvas e os patches de superfície. Você precisará reescrever seu código se ele incluir qualquer uma das seguintes chamadas:

-   **defbasis**
-   **curvebasis**, **curveprecision**, **CRV**, **crvn**, **rcrv**, **rcrvn** e **curveit**
-   **patchbasis**, **patchcurves**, **patchprecision**, **patch** e **rpatch**

Este tópico inclui informações sobre o seguinte.

-   [Portando objetos NURBS](porting-nurbs-objects.md)
-   [Portando curvas NURBS](porting-nurbs-curves.md)
-   [Transportando curvas de corte](porting-trimming-curves.md)
-   [Portando superfícies NURBS](porting-nurbs-surfaces.md)

 

 




