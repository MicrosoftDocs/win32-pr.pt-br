---
title: Processando funções de contexto
description: Cinco funções WGL gerenciam contextos de renderização, conforme descrito na tabela a seguir.
ms.assetid: e03ec03d-2a85-49de-a2be-fe81a5ec5f7f
keywords:
- Funções WGL, contextos de renderização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad8d3a8ea0333154d3145711829ab23e262fa485
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917637"
---
# <a name="rendering-context-functions"></a>Processando funções de contexto

Cinco funções WGL gerenciam contextos de renderização, conforme descrito na tabela a seguir.



| Função WGL                                         | Descrição                                                                                  |
|------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [**wglCreateContext**](/windows/desktop/api/wingdi/nf-wingdi-wglcreatecontext)         | Cria um novo contexto de renderização.                                                             |
| [**WglMakeCurrent**](/windows/desktop/api/wingdi/nf-wingdi-wglmakecurrent)             | Define o contexto de renderização atual de um thread.                                                   |
| [**WglGetCurrentContext**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentcontext) | Obtém um identificador para o contexto de renderização atual de um thread.                                    |
| [**WglGetCurrentDC**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentdc)           | Obtém um identificador para o contexto do dispositivo associado ao contexto de renderização atual de um thread. |
| [**WglDeleteContext**](/windows/desktop/api/wingdi/nf-wingdi-wgldeletecontext)         | Exclui um contexto de renderização.                                                                 |



 

A função [**wglCreateContext**](/windows/desktop/api/wingdi/nf-wingdi-wglcreatecontext) usa um identificador de contexto de dispositivo como seu parâmetro e retorna um identificador de contexto de renderização. O contexto de renderização criado é adequado para desenhar no dispositivo referenciado pelo identificador de contexto do dispositivo. Em particular, seu formato de pixel é o mesmo que o formato de pixel do contexto do dispositivo. Depois de criar um contexto de renderização, você pode liberar ou descartar o contexto do dispositivo. Consulte [contextos de dispositivo](/windows/desktop/gdi/device-contexts) para obter mais detalhes sobre como criar, obter, liberar e descartar um contexto de dispositivo.

> [!Note]  
> O contexto do dispositivo enviado para [**wglCreateContext**](/windows/desktop/api/wingdi/nf-wingdi-wglcreatecontext) deve ser um contexto de dispositivo de exibição, um contexto de dispositivo de memória ou um contexto de dispositivo de impressora colorida que usa quatro ou mais bits por pixel. O contexto do dispositivo não pode ser um contexto de dispositivo de impressora monocromática.

 

A função [**wglMakeCurrent**](/windows/desktop/api/wingdi/nf-wingdi-wglmakecurrent) usa um identificador de contexto de renderização e um identificador de contexto de dispositivo como parâmetros. Todas as chamadas OpenGL subsequentes feitas pelo thread são feitas por meio desse contexto de renderização e são desenhadas no dispositivo referenciado por esse contexto de dispositivo. O contexto do dispositivo não precisa ser o mesmo passado para **wglCreateContext** quando o contexto de renderização foi criado, mas ele deve estar no mesmo dispositivo e ter o mesmo formato de pixel. A chamada para **wglMakeCurrent** cria uma associação entre o contexto de renderização fornecido e o contexto do dispositivo. Você não pode liberar ou descartar o contexto do dispositivo associado a um contexto de renderização atual até que você faça com que o contexto de renderização não seja atual.

Depois que um thread tem um contexto de renderização atual, ele pode fazer chamadas de elementos gráficos OpenGL. Todas as chamadas devem passar por um contexto de renderização. Nada acontece se você fizer chamadas de elementos gráficos OpenGL de um thread que não tem um contexto de renderização atual.

A função [**wglGetCurrentContext**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentcontext) não usa parâmetros e retorna um identificador para o contexto de renderização atual do thread de chamada. Se o thread não tiver um contexto de renderização atual, o valor de retorno será **nulo**.

Quando você obtém um identificador para o contexto do dispositivo associado ao contexto de renderização atual de um thread chamando [**wglGetCurrentDC**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentdc), a associação é criada quando um contexto de renderização é tornado atual.

Você pode interromper a associação entre um contexto de renderização atual e um thread chamando [**wglMakeCurrent**](/windows/desktop/api/wingdi/nf-wingdi-wglmakecurrent) com um dos dois identificadores:

-   Um identificador de contexto de renderização **nulo**
-   Um identificador diferente daquele originalmente chamado

Depois de chamar [**wglMakeCurrent**](/windows/desktop/api/wingdi/nf-wingdi-wglmakecurrent) com o parâmetro de identificador de contexto de renderização definido como **NULL**, o thread de chamada não tem nenhum contexto de renderização atual. O contexto de renderização é liberado de sua conexão com o thread e a associação do contexto de renderização a um contexto de dispositivo termina. O OpenGL libera todos os comandos de desenho e pode liberar alguns recursos. Nenhum desenho OpenGL será feito até a próxima chamada para **wglMakeCurrent**, porque o thread pode não fazer chamadas gráficas OpenGL até recuperar um contexto de renderização atual.

A segunda maneira de quebrar a associação entre um contexto de renderização e um thread é chamar **wglMakeCurrent** com um contexto de renderização diferente. Após essa chamada, o thread de chamada tem um novo contexto de renderização atual, o antigo contexto de renderização atual é liberado de sua conexão com o thread e a associação do contexto de renderização atual anterior a um contexto de dispositivo termina.

A função [**wglDeleteContext**](/windows/desktop/api/wingdi/nf-wingdi-wgldeletecontext) usa um único parâmetro, o identificador para o contexto de renderização a ser excluído. Antes de chamar **wglDeleteContext**, torne o contexto de renderização não atual chamando [**wglMakeCurrent**](/windows/desktop/api/wingdi/nf-wingdi-wglmakecurrent)e exclua ou libere o contexto do dispositivo associado chamando [DeleteDC](/windows/desktop/api/wingdi/nf-wingdi-deletedc) ou [ReleaseDC](/windows/desktop/api/winuser/nf-winuser-releasedc) conforme apropriado.

É um erro para um thread excluir um contexto de renderização que é o contexto de renderização atual de outro thread. No entanto, se um contexto de renderização for o contexto de renderização atual do thread de chamada, o **wglDeleteContext** liberará todos os comandos OpenGL Drawing e tornará o contexto de renderização não atual antes de excluí-lo. Nesse caso, depender de **wglDeleteContext** para fazer com que um contexto de renderização não atual exige que o programador exclua ou libere o contexto do dispositivo associado.

 

 