---
description: Um processo pai pode especificar propriedades associadas à janela principal de seu processo filho.
ms.assetid: 12547da4-8d41-48c5-8efc-f0423f64caa7
title: Definindo propriedades de janela usando STARTUPINFO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 637e8fc9c76694a468b4b8fa6d5d2bd8a3432bbb7dad078d616df753244af358
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119517376"
---
# <a name="setting-window-properties-using-startupinfo"></a>Definindo propriedades de janela usando STARTUPINFO

Um processo pai pode especificar propriedades associadas à janela principal de seu processo filho. A função [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) usa um ponteiro para uma estrutura [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) como um de seus parâmetros. Use os membros desta estrutura para especificar características da janela principal do processo filho. O membro **dwFlags** contém um campo de bits que determina quais outros membros da estrutura são usados. Isso permite que você especifique valores para qualquer subconjunto das propriedades da janela. O sistema usa valores padrão para as propriedades que você não especificar. O membro **dwFlags** também pode forçar um cursor de comentários a ser exibido durante a inicialização do novo processo.

Para processos de GUI, a estrutura [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) especifica os valores padrão a serem usados na primeira vez que o novo processo chama as funções [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) e de [**janela**](/windows/win32/api/winuser/nf-winuser-showwindow) para criar e exibir uma janela sobreposta. Os seguintes valores padrão podem ser especificados:

-   A largura e a altura, em pixels, da janela criada pela [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa).
-   O local, em coordenadas de tela da janela criada pela [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa).
-   O parâmetro *nCmdShow* de [**janela**](/windows/win32/api/winuser/nf-winuser-showwindow).

Para processos de console, use a estrutura [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) para especificar as propriedades da janela somente ao criar um novo console (usando [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) com criar \_ novo \_ console ou com a função [**AllocConsole**](/windows/console/allocconsole) ). A estrutura **STARTUPINFO** pode ser usada para especificar as seguintes propriedades da janela do console:

-   O tamanho da nova janela do console, em células de caractere.
-   O local da nova janela do console, em coordenadas da tela.
-   O tamanho, em células de caracteres, do buffer de tela do novo console.
-   Os atributos de cor de plano de fundo e texto do buffer de tela do novo console.
-   O título da janela do novo console.

 

 
