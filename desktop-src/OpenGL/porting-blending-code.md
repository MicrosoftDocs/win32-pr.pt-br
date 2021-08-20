---
title: Portando o código de mesclagem
description: No íris GL, ao desenhar em buffers de frente e para trás, a mesclagem é feita com a leitura de um dos buffers, a mesclagem com essa cor e a gravação do resultado em ambos os buffers. No entanto, no OpenGL, cada buffer é lido por vez, mesclado e gravado.
ms.assetid: 18334c6b-586d-44a3-aa95-d10589ba99f4
keywords:
- Portabilidade do íris GL, mesclagem
- portando do íris GL, mesclagem
- portando para OpenGL do íris GL, mesclagem
- Portabilidade do OpenGL do íris GL, mesclagem
- combinação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13548a2f08821e4f80bf63230077f9a39540ba9b8a37763e7935d211ef0dcdc0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119485906"
---
# <a name="porting-blending-code"></a>Portando o código de mesclagem

No íris GL, ao desenhar em buffers de frente e para trás, a mesclagem é feita com a leitura de um dos buffers, a mesclagem com essa cor e a gravação do resultado em ambos os buffers. No entanto, no OpenGL, cada buffer é lido por vez, mesclado e gravado.

A tabela a seguir lista as funções de mesclagem íris GL e suas funções OpenGL equivalentes.



| Função GL de íris  | Função OpenGL                            | Significado                     |
|-------------------|--------------------------------------------|-----------------------------|
|                   | [**glEnable**](glenable.md) (GL \_ Blend) | Ativa a mesclagem.          |
| **blendfunction** | [**glBlendFunc**](glblendfunc.md)         | Especifica uma função de mistura. |



 

A função OpenGL **glBlendFunc** e a função **BLENDFUNCTION** do íris GL são quase idênticas. A tabela a seguir lista os fatores de combinação do íris GL e seus equivalentes em OpenGL.



| ÍRIS GL          | OpenGL                     | Observações             |
|------------------|----------------------------|-------------------|
| BF \_ zero         | GL \_ zero                   |                   |
| BF \_ um          | GL \_ um                    |                   |
| \_SA BF           | \_origem GL \_ alfa             |                   |
| MSA do BF \_          | GL \_ um \_ menos \_ src \_ Alpha |                   |
| BF \_ da           | GL \_ DST \_ Alpha             |                   |
| MDA do BF \_          | GL \_ um \_ menos o \_ DST \_ Alpha |                   |
| BF \_ SC           | \_cor de src GL \_             |                   |
| BF \_ msc          | GL \_ um \_ menos \_ cor de src \_ | Somente destino. |
| BF \_ DC           | \_cor de DST do GL \_             | Somente origem.      |
| BF \_ MDC          | GL \_ um \_ menos \_ cor do DST \_ | Somente origem.      |
| \_ \_ MDA SA mínimo de BF \_ | GL \_ src \_ alfa \_ saturado   |                   |



 

??

 

 




