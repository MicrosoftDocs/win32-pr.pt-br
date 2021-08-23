---
title: Portando curvas de corte
description: As curvas de corte openGL são muito semelhantes às curvas de corte IRIS GL. A tabela a seguir lista as funções IRIS GL para definir curvas de corte e suas funções equivalentes do OpenGL.
ms.assetid: 9aeea9ca-5ecd-4be1-853d-45b1566b263b
keywords:
- Portação IRIS GL, curvas de corte
- portando de IRIS GL, recortando curvas
- portando para OpenGL do IRIS GL, recortando curvas
- Portação openGL de IRIS GL, curvas de corte
- curvas de corte
- curvas
- Portação IRIS GL, curvas
- portando de IRIS GL, curvas
- portando para OpenGL de IRIS GL, curvas
- Portação openGL de IRIS GL, curvas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad544431adaa7f0b049341ec7314e3e53ae60752d633a48c760ca09334f79d33
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119553856"
---
# <a name="porting-trimming-curves"></a>Portando curvas de corte

As curvas de corte openGL são muito semelhantes às curvas de corte IRIS GL. A tabela a seguir lista as funções IRIS GL para definir curvas de corte e suas funções equivalentes do OpenGL.



| Função IRIS GL | Função OpenGL                        | Significado                              |
|------------------|----------------------------------------|--------------------------------------|
| **bgntrim**      | [**gluBeginTrim**](glubegintrim.md)   | Começa a definição de curva de corte.    |
| **pwlcurve**     | [**gluPwlCurve**](glupwlcurve.md)     | Define uma curva linear por parte.    |
| **niascurve**   | [**gluNagisCurve**](glunurbscurve.md) | Especifica atributos de curva de corte. |
| **endtrim**      | [**gluEndTrim**](gluendtrim.md)       | Termina a definição de curva de corte.      |



 

??

 

 




