---
title: Portando triângulos
description: Você pode desenhar três tipos de triângulos em triângulos separados openGL, faixas de triângulo e ventiladores de triângulo.
ms.assetid: 48617892-c9a0-4c67-b42e-afa4243023e7
keywords:
- Portação IRIS GL, triângulos
- portando de IRIS GL, triângulos
- portando para OpenGL de IRIS GL, triângulos
- Portação openGL de IRIS GL, triângulos
- funções de desenho, triângulos
- triângulos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85acc650a709650495b93cdd00176400f00168cc8fe6445a23505f12b332abf9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011994"
---
# <a name="porting-triangles"></a>Portando triângulos

Você pode desenhar três tipos de triângulos no OpenGL: triângulos separados, faixas de triângulo e ventiladores de triângulo.

O OpenGL não tem equivalente para a função IRIS GL **swaptmesh.** Você pode obter o mesmo efeito usando uma combinação de triângulos, faixas de triângulo e ventiladores de triângulo.

A tabela a seguir lista as funções IRIS GL para desenhar triângulos e suas funções Equivalentes do OpenGL.



| Função IRIS GL           | Parâmetro glBegin equivalente | Significado                                       |
|----------------------------|------------------------------|-----------------------------------------------|
|                            | TRIÂNGULOS \_ GL                | Triplos de vértices interpretados como triângulos. |
| **bgntmesh**, **endtmesh** | FAIXA \_ DE TRIÂNGULO \_ GL          | Faixas vinculadas de triângulos.                   |
|                            | VENTILADOR \_ DE TRIÂNGULO \_ GL            | Ventiladores vinculados de triângulos.                     |



 

??

 

 




