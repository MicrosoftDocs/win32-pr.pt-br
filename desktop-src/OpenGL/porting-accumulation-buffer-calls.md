---
title: Portando chamadas de buffer de acumulação
description: Você deve alocar seu buffer de acumulação solicitando o formato de pixel apropriado com a função OpenGL auxInitDisplayMode ou ChoosePixelFormat.
ms.assetid: 523728ce-4aae-4247-a3dc-23864231cad1
keywords:
- Portabilidade do íris GL, buffers de acumulação
- portando do íris GL, buffers de acumulação
- portando para OpenGL do íris GL, buffers de acumulação
- Portabilidade OpenGL do íris GL, buffers de acumulação
- buffers de acumulação OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91ca91cb3ba35535ba2470297070dffc932a1c33
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104160465"
---
# <a name="porting-accumulation-buffer-calls"></a>Portando chamadas de buffer de acumulação

Você deve alocar seu buffer de acumulação solicitando o formato de pixel apropriado com a função OpenGL **auxInitDisplayMode** ou [**ChoosePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat) . A tabela a seguir lista as funções do íris GL que afetam o buffer de acumulação e suas funções OpenGL equivalentes.



| Função GL de íris       | Função OpenGL                                       | Significado                                                                       |
|------------------------|-------------------------------------------------------|-------------------------------------------------------------------------------|
| **acsize**             | **auxInitDisplayMode** ou **ChoosePixelFormat**       | Especifica o número de bitplanes por componente de cor no buffer de acumulação. |
| **acbuf**              | [**glAccum**](glaccum.md)                            | Opera no buffer de acumulação.                                          |
|                        | [**glClearAccum**](glclearaccum.md)                  | Define valores claros para o buffer de acumulação.                                    |
| **acbuf**(AC \_ limpa) | [**glClear**](glclear.md) (bit de buffer do GL \_ Accum \_ \_ ) | Limpa o buffer de acumulação.                                               |



 

A tabela a seguir lista os parâmetros **acbuf** do íris GL juntamente com os parâmetros equivalentes do OpenGL [**glAccum**](glaccum.md) .



| Parâmetro do íris GL     | Parâmetro OpenGL |
|-----------------------|------------------|
| \_acumulação de AC        | GL \_ Accum        |
| \_desacumular AC limpar \_ | \_carga GL         |
| retorno de AC \_            | retorno do GL \_       |
| \_mult AC              | \_mult GL         |
| adição de AC \_               | adição de GL \_          |



 

 

 




