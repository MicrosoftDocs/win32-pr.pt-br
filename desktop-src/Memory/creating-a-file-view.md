---
description: Para mapear os dados de um arquivo para a memória virtual de um processo, você deve criar uma exibição do arquivo.
ms.assetid: b1ebd9a4-cde4-4c0c-80d2-5ccb655cd3a4
title: Criando uma exibição de arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eadae741e9f74e8a3e1cd68006100d6acf82aad5019a8d31b18a7761c5620b69
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067876"
---
# <a name="creating-a-file-view"></a>Criando uma exibição de arquivo

Para mapear os dados de um arquivo para a memória virtual de um processo, você deve criar uma exibição do arquivo. As funções [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) e [**MapViewOfFileEx**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffileex) usam o identificador de objeto de mapeamento de arquivo retornado pelo [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) para criar uma exibição do arquivo ou uma parte do arquivo no espaço de endereço virtual do processo. Essas funções falharão se os sinalizadores de acesso entrarem em conflito com aqueles especificados quando **CreateFileMapping** criou o objeto de mapeamento de arquivo.

A função [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) retorna um ponteiro para a exibição de arquivo. Ao desreferenciar um ponteiro no intervalo de endereços especificado em **MapViewOfFile**, um aplicativo pode ler dados do arquivo e gravar dados no arquivo. Gravar na exibição de arquivo resulta em alterações no objeto de mapeamento de arquivo. A gravação real no arquivo no disco é tratada pelo sistema. Os dados não são realmente transferidos no momento em que o objeto de mapeamento de arquivo é gravado. Em vez disso, grande parte da entrada e saída (e/s) do arquivo é armazenada em cache para melhorar o desempenho geral do sistema. Os aplicativos podem substituir esse comportamento chamando a função [**FlushViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-flushviewoffile) para forçar o sistema a executar transações de disco imediatamente.

A função [**MapViewOfFileEx**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffileex) funciona exatamente como a função [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) , exceto que ela permite que um processo especifique o endereço base da exibição do arquivo no espaço de endereço virtual do processo no parâmetro *lpvBase* . Se não houver espaço suficiente no endereço especificado, a chamada falhará. Portanto, se você precisar mapear um arquivo para o mesmo endereço em vários processos, os processos devem negociar um endereço apropriado: o parâmetro *lpvBase* deve ser um múltiplo integral da granularidade de alocação de memória do sistema ou a chamada falhará. Para obter a granularidade de alocação de memória do sistema, use a função [**GetSystemInfo**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsysteminfo) , que preenche os membros de uma estrutura de [**\_ informações do sistema**](/windows/win32/api/sysinfoapi/ns-sysinfoapi-system_info) .

Um aplicativo pode criar várias exibições de arquivo do mesmo objeto de mapeamento de arquivo. Uma exibição de arquivo pode ter um tamanho diferente do objeto de mapeamento de arquivo do qual é derivado, mas deve ser menor do que o objeto de mapeamento de arquivo. O deslocamento especificado pelos parâmetros *dwOffsetHigh* e *dwOffsetLow* de [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) deve ser um múltiplo da granularidade de alocação do sistema.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando uma exibição dentro de um arquivo](creating-a-view-within-a-file.md)
</dt> </dl>

 

 
