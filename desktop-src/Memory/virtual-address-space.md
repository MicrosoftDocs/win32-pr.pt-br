---
description: O espaço de endereço virtual para um processo é o conjunto de endereços de memória virtual que ele pode usar. O espaço de endereço para cada processo é privado e não pode ser acessado por outros processos, a menos que ele seja compartilhado.
ms.assetid: 747f9f53-a595-4f4b-8b81-3123d59edb2f
title: Espaço de endereço virtual (gerenciamento de memória)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a5c9b6aa7fce3be508cae2afd67767f9deaa25e1fe4aa38c4530529f64d7df7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120040068"
---
# <a name="virtual-address-space-memory-management"></a>Espaço de endereço virtual (gerenciamento de memória)

O espaço de endereço virtual para um processo é o conjunto de endereços de memória virtual que ele pode usar. O espaço de endereço para cada processo é privado e não pode ser acessado por outros processos, a menos que ele seja compartilhado.

Um endereço virtual não representa o local físico real de um objeto na memória; em vez disso, o sistema mantém uma *tabela de página* para cada processo, que é uma estrutura de dados interna usada para converter endereços virtuais em seus endereços físicos correspondentes. Cada vez que um thread faz referência a um endereço, o sistema converte o endereço virtual em um endereço físico.

o espaço de endereço virtual para Windows de 32 bits é de 4 gigabytes (GB) de tamanho e dividido em duas partições: uma para uso pelo processo e a outra reservada para uso pelo sistema. para obter mais informações sobre o espaço de endereço virtual no Windows de 64 bits, consulte [espaço de endereço virtual no Windows de 64 bits](../winprog64/virtual-address-space.md).

Para obter mais informações sobre memória virtual, consulte os seguintes tópicos:

-   [espaço de endereço Virtual e Armazenamento físico](virtual-address-space-and-physical-storage.md)
-   [Conjunto de Trabalho](working-set.md)
-   [Estado da página](page-state.md)
-   [Escopo da memória alocada](scope-of-allocated-memory.md)
-   [Prevenção de Execução de Dados](data-execution-prevention.md)
-   [Proteção de memória](memory-protection.md)
-   [limites de memória para versões de Windows](memory-limits-for-windows-releases.md)

## <a name="default-virtual-address-space-for-32-bit-windows"></a>Espaço de endereço virtual padrão para Windows de 32 bits

A tabela a seguir mostra o intervalo de memória padrão para cada partição.



| Intervalo de memória                             | Uso                |
|------------------------------------------|----------------------|
| 2 GB baixos (0x00000000 a 0x7FFFFFFF)  | Usado pelo processo. |
| Alto GB (0x80000000 a 0xFFFFFFFF) | Usado pelo sistema.  |



 

## <a name="virtual-address-space-for-32-bit-windows-with-4gt"></a>espaço de endereço Virtual para Windows de 32 bits com 4gt

Se o [ajuste de 4 gigabytes](4-gigabyte-tuning.md) (4GT) estiver habilitado, o intervalo de memória para cada partição será o seguinte.



| Intervalo de memória                             | Uso                |
|------------------------------------------|----------------------|
| 3GB baixos (0x00000000 a 0xBFFFFFFF)  | Usado pelo processo. |
| Alta 1GB (0xC0000000 a 0xFFFFFFFF) | Usado pelo sistema.  |



 

Depois que 4GT estiver habilitado, um processo que tem o sinalizador de [**\_ \_ \_ \_ reconhecimento de endereço grande de arquivo de imagem**](/windows/win32/api/dbghelp/ns-dbghelp-loaded_image) definido em seu cabeçalho de imagem terá acesso a 1 GB de memória adicional acima dos 2 GB baixos.

## <a name="adjusting-the-virtual-address-space-for-32-bit-windows"></a>Ajustando o espaço de endereço virtual para Windows de 32 bits

Você pode usar o comando a seguir para definir uma opção de entrada de inicialização que configura o tamanho da partição que está disponível para uso pelo processo para um valor entre 2048 (2 GB) e 3072 (3 GB):

[Bcdedit/set](/windows-hardware/drivers/devtest/bcdedit--set) **IncreaseUserVa** *megabytes*

Depois que a opção de entrada de inicialização é definida, o intervalo de memória para cada partição é o seguinte.



| Intervalo de memória                            | Uso                |
|-----------------------------------------|----------------------|
| Baixa (0x00000000 a *megabytes*)    | Usado pelo processo. |
| Alta (*megabytes*+ 1 a 0xFFFFFFFF) | Usado pelo sistema.  |



 

**Windows Server 2003:** Defina a opção **/USERVA** em boot.ini como um valor entre 2048 e 3072.

 

 
