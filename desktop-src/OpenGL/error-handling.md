---
title: Tratamento de erro (OpenGL)
description: Quando o OpenGL detecta um erro, ele registra um código de erro atual.
ms.assetid: 8e40e382-14fd-44df-8e1c-ebceb34af19c
keywords:
- tratamento de erro openGL
- Tratamento de erros do OpenGL
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

Quando o OpenGL detecta um erro, ele registra um código de erro atual. A função que causou o erro é ignorada, portanto, não tem nenhum efeito no estado OpenGL ou no conteúdo do framebuffer. (Se o erro registrado foi GL \_ SEM \_ \_ MEMÓRIA, no entanto, os resultados da função são indefinido.) Depois de registrado, o código de erro atual não é limpo até que você chame a função de consulta [**glGetError,**](glgeterror.md) que retorna o código de erro atual.

Implementações do OpenGL podem retornar vários códigos de erro atuais, cada um deles permanece definido até ser consultado. A **função glGetError** retorna GL NO ERROR depois de você ter consultado todos os códigos de erro atuais ou \_ se não houver nenhum \_ erro. Portanto, se você obtiver um código de erro, chame **glGetError** até que GL NO ERROR seja retornado para ter certeza de que você descobriu \_ todos os \_ erros. Para ver a lista de códigos de erro, consulte [Códigos de erro openGL.](opengl-error-codes.md)

Você pode usar a [**função gluErrorString**](gluerrorstring.md) GLU para obter uma cadeia de caracteres descritiva correspondente ao código de erro passado. Para obter mais informações sobre **gluErrorString,** consulte [Tratamento de erros](handling-errors.md).

> [!Note]  
> As funções GLU geralmente retornam valores de erro se um erro é detectado. Além disso, a biblioteca do Utilitário OpenGL define os códigos de erro GLU INVALID ENUM, GLU INVALID VALUE e GLU OUT OF MEMORY, que têm o mesmo significado que os códigos de erro \_ \_ do \_ \_ \_ \_ \_ OpenGL relacionados.

 

 

 




