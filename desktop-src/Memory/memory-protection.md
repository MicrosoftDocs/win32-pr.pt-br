---
description: A memória que pertence a um processo é protegida implicitamente pelo seu espaço de endereço virtual privado.
ms.assetid: 70ded07a-7be6-4189-a1ae-281917f42a1e
title: Proteção de memória
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd30df8084c91a62c28414f4a8142397ee777e52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104091814"
---
# <a name="memory-protection"></a>Proteção de memória

A memória que pertence a um processo é protegida implicitamente pelo seu espaço de endereço virtual privado. Além disso, o Windows fornece proteção de memória usando o hardware de memória virtual. A implementação dessa proteção varia de acordo com o processador, por exemplo, as páginas de código no espaço de endereço de um processo podem ser marcadas como somente leitura e protegidas contra modificações feitas por threads de modo de usuário.

Para obter a lista completa de atributos, consulte [constantes de proteção de memória](memory-protection-constants.md).

## <a name="copy-on-write-protection"></a>Proteção de cópia em gravação

A proteção de cópia em gravação é uma otimização que permite que vários processos mapeiem seus espaços de endereço virtual, de forma que eles compartilhem uma página física até que um dos processos modifique a página. Isso faz parte de uma técnica chamada *avaliação lenta*, que permite ao sistema conservar a memória física e o tempo, não executando uma operação até que seja absolutamente necessário.

Por exemplo, suponha que dois processos carreguem páginas da mesma DLL em seus espaços de memória virtual. Essas páginas de memória virtual são mapeadas para as mesmas páginas de memória física para ambos os processos. Desde que nenhum processo grave nessas páginas, eles poderão mapear e compartilhar, as mesmas páginas físicas, conforme mostrado no diagrama a seguir.

![caixas e setas das páginas do processo 1 e 2 mapeadas para a mesma memória física](images/mem1.png)

Se o processo 1 gravar em uma dessas páginas, o conteúdo da página física será copiado para outra página física e o mapa de memória virtual será atualizado para o processo 1. Ambos os processos agora têm sua própria instância da página na memória física. Portanto, não é possível que um processo grave em uma página física compartilhada e que o outro processo Veja as alterações.

![caixas e setas de processos e remapeamento de memória física](images/mem2.png)

## <a name="loading-applications-and-dlls"></a>Carregando aplicativos e DLLs

Quando várias instâncias do mesmo aplicativo baseado no Windows são carregadas, cada instância é executada em seu próprio espaço de endereço virtual protegido. No entanto, seus identificadores de instância (*HINSTANCE*) normalmente têm o mesmo valor. Esse valor representa o endereço base do aplicativo em seu espaço de endereço virtual. Se cada instância puder ser carregada em seu endereço base padrão, ela poderá mapear e compartilhar as mesmas páginas físicas com as outras instâncias, usando a proteção de cópia em gravação. O sistema permite que essas instâncias compartilhem as mesmas páginas físicas até que uma delas modifique uma página. Se, por algum motivo, uma dessas instâncias não puder ser carregada no endereço base desejado, ela receberá suas próprias páginas físicas.

DLLs são criadas com um endereço base padrão. Cada processo que usa uma DLL tentará carregar a DLL em seu próprio espaço de endereço no endereço virtual padrão para a DLL. Se vários aplicativos puderem carregar uma DLL em seu endereço virtual padrão, eles poderão compartilhar as mesmas páginas físicas para a DLL. Se por algum motivo um processo não puder carregar a DLL no endereço padrão, ele carregará a DLL em outro lugar. A proteção de cópia em gravação força algumas das páginas da DLL a serem copiadas em páginas físicas diferentes para esse processo, pois as correções para instruções de salto são gravadas nas páginas da DLL e serão diferentes para esse processo. Se a seção de código contiver muitas referências à seção de dados, isso poderá fazer com que a seção de código inteira seja copiada para novas páginas físicas.

 

 



