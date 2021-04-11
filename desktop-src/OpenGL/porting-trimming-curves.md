---
title: Transportando curvas de corte
description: As curvas de corte de OpenGL são muito semelhantes às curvas de corte do íris GL. A tabela a seguir lista as funções do íris GL para definir curvas de corte e suas funções OpenGL equivalentes.
ms.assetid: 9aeea9ca-5ecd-4be1-853d-45b1566b263b
keywords:
- Portagem do íris GL, curvas de corte
- portando do íris GL, aparando curvas
- portando para OpenGL do íris GL, aparando curvas
- Portabilidade do OpenGL do íris GL, corte de curvas
- aparando curvas
- curvas
- Portabilidade do íris GL, curvas
- portando do íris GL, curvas
- portando para OpenGL do íris GL, curvas
- Portabilidade OpenGL do íris GL, curvas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cc82822b2e0b9e66729f0cb1a0e939d2775999c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104160202"
---
# <a name="porting-trimming-curves"></a>Transportando curvas de corte

As curvas de corte de OpenGL são muito semelhantes às curvas de corte do íris GL. A tabela a seguir lista as funções do íris GL para definir curvas de corte e suas funções OpenGL equivalentes.



| Função GL de íris | Função OpenGL                        | Significado                              |
|------------------|----------------------------------------|--------------------------------------|
| **bgntrim**      | [**gluBeginTrim**](glubegintrim.md)   | Começa a definição da curva de corte.    |
| **pwlcurve**     | [**gluPwlCurve**](glupwlcurve.md)     | Define uma curva linear piecewise.    |
| **nurbscurve**   | [**gluNurbsCurve**](glunurbscurve.md) | Especifica os atributos de curva de corte. |
| **endtrim**      | [**gluEndTrim**](gluendtrim.md)       | Encerra a definição de curva de corte.      |



 

??

 

 




