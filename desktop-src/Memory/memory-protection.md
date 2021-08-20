---
description: A memória que pertence a um processo é implicitamente protegida por seu espaço de endereço virtual privado.
ms.assetid: 70ded07a-7be6-4189-a1ae-281917f42a1e
title: Proteção de memória
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4421b07ee4ed88dffe0e46d1121d5d4117b471a84ffcf4f85738bd8be912f09c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117809057"
---
# <a name="memory-protection"></a>Proteção de memória

A memória que pertence a um processo é implicitamente protegida por seu espaço de endereço virtual privado. Além disso, Windows fornece proteção de memória usando o hardware de memória virtual. A implementação dessa proteção varia de acordo com o processador, por exemplo, páginas de código no espaço de endereço de um processo podem ser marcadas como somente leitura e protegidas contra modificação por threads de modo de usuário.

Para ver a lista completa de atributos, consulte [Constantes de proteção de memória.](memory-protection-constants.md)

## <a name="copy-on-write-protection"></a>Proteção de cópia na gravação

A proteção de cópia na gravação é uma otimização que permite que vários processos mapeiem seus espaços de endereço virtual, de forma que eles compartilhem uma página física até que um dos processos modifice a página. Isso faz parte de uma técnica chamada avaliação *lento,* que permite ao sistema conservar memória física e tempo, não executando uma operação até que seja absolutamente necessário.

Por exemplo, suponha que dois processos carreguem páginas da mesma DLL em seus espaços de memória virtual. Essas páginas de memória virtual são mapeadas para as mesmas páginas de memória física para ambos os processos. Desde que nenhum dos processos seja gravado nessas páginas, eles podem mapear e compartilhar as mesmas páginas físicas, conforme mostrado no diagrama a seguir.

![caixas e setas do processo 1 e 2 páginas mapeadas para a mesma memória física](images/mem1.png)

Se o Processo 1 grava em uma dessas páginas, o conteúdo da página física é copiado para outra página física e o mapa de memória virtual é atualizado para o Processo 1. Ambos os processos agora têm sua própria instância da página na memória física. Portanto, não é possível que um processo seja escrito em uma página física compartilhada e que o outro processo veja as alterações.

![caixas e setas de processos e remapeamento de memória física](images/mem2.png)

## <a name="loading-applications-and-dlls"></a>Carregando aplicativos e DLLs

Quando várias instâncias do mesmo aplicativo Windows são carregadas, cada instância é executado em seu próprio espaço de endereço virtual protegido. No entanto, suas alças de instância (*hInstance*) normalmente têm o mesmo valor. Esse valor representa o endereço base do aplicativo em seu espaço de endereço virtual. Se cada instância puder ser carregada em seu endereço base padrão, ela poderá mapear e compartilhar as mesmas páginas físicas com as outras instâncias, usando a proteção de cópia na gravação. O sistema permite que essas instâncias compartilhem as mesmas páginas físicas até que uma delas modifica uma página. Se, por algum motivo, uma dessas instâncias não puder ser carregada no endereço base desejado, ela receberá suas próprias páginas físicas.

As DLLs são criadas com um endereço base padrão. Cada processo que usa uma DLL tentará carregar a DLL em seu próprio espaço de endereço no endereço virtual padrão para a DLL. Se vários aplicativos puderem carregar uma DLL em seu endereço virtual padrão, eles poderão compartilhar as mesmas páginas físicas para a DLL. Se, por algum motivo, um processo não puder carregar a DLL no endereço padrão, ele carregará a DLL em outro lugar. A proteção de cópia na gravação força algumas das páginas da DLL a serem copiadas em páginas físicas diferentes para esse processo, pois as correções para instruções de salto são escritas nas páginas da DLL e serão diferentes para esse processo. Se a seção de código contiver muitas referências à seção de dados, isso poderá fazer com que toda a seção de código seja copiada para novas páginas físicas.

 

 



