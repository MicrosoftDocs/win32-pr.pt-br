---
title: Tratamento de erro (OpenGL)
description: Quando o OpenGL detecta um erro, ele registra um código de erro atual.
ms.assetid: 8e40e382-14fd-44df-8e1c-ebceb34af19c
keywords:
- erro ao manipular o OpenGL
- Tratamento de erro de OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 064330859b4e6b6d2d0bb9985e9f24d968a7daa5062215c64e82f89563ae06ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118361376"
---
# <a name="error-handling-opengl"></a>Tratamento de erro (OpenGL)

Quando o OpenGL detecta um erro, ele registra um código de erro atual. A função que causou o erro é ignorada, portanto, não tem nenhum efeito sobre o estado do OpenGL ou sobre o conteúdo do framebuffer. (Se o erro registrado foi GL \_ SEM \_ \_ memória, no entanto, os resultados da função são indefinidos.) Depois de registrado, o código de erro atual não é limpo até que você chame a função de consulta [**glGetError**](glgeterror.md) , que retorna o código de erro atual.

As implementações do OpenGL podem retornar vários códigos de erro atuais, cada um deles permanece definido até a consulta. A função **glGetError** retornará GL \_ sem \_ erro depois que você tiver consultado todos os códigos de erro atuais ou se não houver erro. Portanto, se você obtiver um código de erro, chame **glGetError** até o GL \_ nenhum \_ erro será retornado para certificar-se de que você descobriu todos os erros. Para obter a lista de códigos de erro, confira [códigos de erro OpenGL](opengl-error-codes.md).

Você pode usar a função [**gluErrorString**](gluerrorstring.md) Glu para obter uma cadeia de caracteres descritiva correspondente ao código de erro passado. Para obter mais informações sobre o **gluErrorString**, consulte [tratamento de erros](handling-errors.md).

> [!Note]  
> As funções GLU geralmente retornam valores de erro se um erro for detectado. Além disso, a biblioteca do utilitário OpenGL define os códigos de erro GLU \_ Enumeração inválida \_ , glu \_ \_ valor inválido e Glu \_ memória insuficiente \_ \_ , que têm o mesmo significado que os códigos de erro OpenGL relacionados.

 

 

 




