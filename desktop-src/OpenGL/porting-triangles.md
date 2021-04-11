---
title: Coângulos de portabilidade
description: Você pode desenhar três tipos de triângulos nos triângulos separados do OpenGL, nas faixas de triângulo e nos ventiladores de triângulo.
ms.assetid: 48617892-c9a0-4c67-b42e-afa4243023e7
keywords:
- Portabilidade do íris GL, triângulos
- portando do íris GL, triângulos
- portando para OpenGL do íris GL, triângulos
- Portabilidade do OpenGL do íris GL, triângulos
- funções de desenho, triângulos
- triângulos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad0c7a0af4b538bb951cf0d1c5f2e12b2e1badda
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292436"
---
# <a name="porting-triangles"></a>Coângulos de portabilidade

Você pode desenhar três tipos de triângulos em OpenGL: triângulos separados, faixas de triângulo e ventiladores de triângulo.

O OpenGL não tem nenhum equivalente para a função **swaptmesh** do íris GL. Você pode obter o mesmo efeito usando uma combinação de triângulos, faixas de triângulo e ventiladores de triângulo.

A tabela a seguir lista as funções do íris GL para desenhar triângulos e suas funções OpenGL equivalentes.



| Função GL de íris           | Parâmetro glBegin equivalente | Significado                                       |
|----------------------------|------------------------------|-----------------------------------------------|
|                            | \_TRIângulos GL                | As corridas de vértices interpretadas como triângulos. |
| **bgntmesh**, **endtmesh** | \_faixa de triângulo GL \_          | Faixas vinculadas de triângulos.                   |
|                            | \_ \_ ventilador do triângulo GL            | Ventiladores vinculados de triângulos.                     |



 

??

 

 




