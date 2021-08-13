---
title: Serviços em buffer
description: Serviços em buffer
ms.assetid: 4816ab05-42fc-4c22-b753-8fd153d88c27
keywords:
- E/S de arquivo multimídia, serviços armazenados em buffer
- E/S de arquivo, serviços armazenados em buffer
- entrada e saída (E/S), serviços armazenados em buffer
- E/S (entrada e saída), serviços armazenados em buffer
- E/S em buffer
- Função mmioOpen
- buffer interno de E/S
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67f8e7c11dbc90f7090bc8fcee114ebfac79f9bd54d834203f4b8e7bf893f591
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117989355"
---
# <a name="buffered-services"></a>Serviços em buffer

A maior parte da sobrecarga na E/S de arquivo ocorre ao acessar o dispositivo de mídia. Se você estiver lendo ou escrevendo muitos blocos pequenos de informações, o dispositivo poderá gastar muito tempo mudando para o local físico na mídia para cada operação de leitura ou gravação. Nesse caso, você pode obter um melhor desempenho usando serviços de E/S de arquivo armazenado em buffer. Com a E/S em buffer, o gerenciador de E/S de arquivo mantém um buffer intermediário maior do que os blocos de informações que você está lendo ou escrevendo. Ele acessa o dispositivo somente quando o buffer deve ser preenchido ou gravado no disco.

Antes de configurar e usar a E/S de arquivo em buffer, você deve decidir se deseja que o gerenciador de E/S de arquivo ou o aplicativo aloce o buffer. É mais simples permitir que o gerenciador de E/S de arquivo aloce o buffer. No entanto, você pode permitir que o aplicativo aloce o buffer se quiser acessar diretamente o buffer ou abrir um arquivo de memória. Para obter mais informações sobre como usar arquivos de memória, consulte [Executando E/S de arquivo de memória](performing-memory-file-i-o.md). Para ver um exemplo de acesso direto a um buffer de E/S, consulte [Acessando um buffer de E/S de arquivo](accessing-a-file-i-o-buffer.md)

Um buffer alocado pelo gerenciador de E/S de arquivo é chamado de buffer de E/S interno. Para abrir um arquivo para E/S em buffer usando um buffer interno, especifique o sinalizador MMIO ALLOCBUF ao abrir o arquivo com a \_ [**função mmioOpen.**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) A ilustração a seguir mostra o estado inicial do buffer de E/S do arquivo depois que um arquivo é aberto para uma operação de leitura em buffer. O buffer é transparente – você lê e busca como se estivesse usando E/S sem buffer. A **função mmioOpen** definiu pchNext e *pchEndRead* para apontar para o início do buffer de E/S do arquivo.

![Captura de tela que mostra 'pchEndRead' e 'pchNext' apontando para o início do Buffer de E/S de Arquivo.](images/mmio7.gif)

A ilustração a seguir mostra o estado inicial do buffer de E/S do arquivo depois que um arquivo é aberto para uma operação de gravação em buffer. A **função mmioOpen** definiu **pchNext** para apontar para o início do buffer de E/S do arquivo e **pchEndWrite** para apontar para o final do buffer.

![Captura de tela que mostra 'pchNext' no início do Buffer de E/S de Arquivo e 'pchEndWrite' no final.](images/mmio11.gif)

O tamanho padrão do buffer de E/S interno é 8K. Se esse tamanho não for adequado, você poderá usar a [**função mmioSetBuffer**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosetbuffer) para alterar o tamanho do buffer. Você também pode usar essa função para habilitar o buffer em um arquivo aberto para E/S sem buffer ou para fornecer seu próprio buffer para uso como um arquivo de memória.

Você pode forçar o conteúdo de um buffer de E/S a ser gravado no disco usando a [**função mmioFlush.**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioflush) No entanto, ao fechar um arquivo usando a função [**mmioClose,**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioclose) você não precisa chamar **mmioFlush** para liberar um buffer de E/S – a **função mmioClose** o libera automaticamente. Se você ficar sem espaço em disco, **mmioFlush** poderá falhar, mesmo que as chamadas anteriores à [**função mmioWrite**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiowrite) foram bem-sucedidas. Da mesma forma, **mmioClose** pode falhar ao liberar seu buffer de E/S.

Aplicativos sensíveis ao desempenho, como aqueles que transmitem dados em tempo real de um CD-ROM, podem otimizar o desempenho de E/S de arquivo acessando diretamente o buffer de E/S. Você deve ter cuidado se optar por fazer isso, pois ignora algumas das proteções e verificação de erros fornecidas pelo gerenciador de E/S de arquivo.

O gerenciador de E/S de arquivo multimídia usa a [**estrutura MMIOINFO**](/previous-versions//dd757322(v=vs.85)) para manter informações de estado sobre um arquivo aberto. Você usa três membros nessa estrutura para ler e gravar o buffer de E/S: **pchNext,** **pchEndRead** e **pchEndWrite**. O **membro pchNext** aponta para o próximo local no buffer a ser lido ou escrito. Você deve incrementar esse membro conforme lê e escreve o buffer. O **membro pchEndRead** identifica o último caractere válido que você pode ler do buffer. Da mesma forma, esse membro identifica o último local no buffer que você pode gravar. Mais precisamente, **pchEndRead e** **pchEndWrite** apontam para o local de memória que segue os últimos dados válidos no buffer. Use as [**funções mmioGetInfo**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiogetinfo) e [**mmioSetInfo**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosetinfo) para recuperar e definir informações de estado sobre o buffer de E/S do arquivo. A ilustração a seguir mostra o estado do buffer de E/S depois que o aplicativo chama **mmioAdvance** durante uma operação de leitura. A **função mmioAdvance** preenche o buffer e define o **ponteiro pchEndRead** para o final do buffer.

![Captura de tela que mostra 'pchNext' no início do Buffer de E/S de Arquivo e 'pchEndRead' no final.](images/mmio8.gif)

Na ilustração a seguir, o aplicativo lê do buffer de E/S no local especificado por **pchNext** e avança o ponteiro.

![Captura de tela que mostra 'pchNext' no meio do Buffer de E/S de Arquivo e 'pchEndRead' no final.](images/mmio9.gif)

Da mesma forma, para uma operação de gravação, o aplicativo grava no buffer de E/S e avança o ponteiro **pchNext,** conforme mostrado na ilustração a seguir.

![Captura de tela que mostra 'pchNext' no meio do Buffer de E/S de Arquivo e 'pchEndWrite' no final.](images/mmio12.gif)

Depois que o aplicativo preencher o buffer, ele **chamará mmioAdvance** para liberar o buffer para o disco. A **função mmioAdvance** redefine **pchNext** para apontar para o início do buffer, conforme mostrado na ilustração a seguir.

![Captura de tela que mostra 'pchNext' no início do Buffer de E/S de Arquivo, o buffer no meio do E O F e 'pchEndWrite' no final do buffer.](images/mmio13.gif)

Ao chegar ao final do buffer de E/S, você deve avançar o buffer para preenchê-lo do disco, se estiver lendo ou liberar para o disco, se estiver escrevendo. Use a [**função mmioAdvance**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioadvance) para avançar um buffer de E/S. Para preencher um buffer de E/S do disco, use **mmioAdvance** com o sinalizador MMIO \_ READ. Se não houver dados suficientes restantes no arquivo para preencher o buffer, o membro **pchEndRead** da estrutura **MMIOINFO** aponta para o local após o último byte válido no buffer. Para liberar um buffer para o disco, defina o sinalizador MMIO DIRTY no membro \_ **dwFlags** da estrutura **MMIOINFO** e, em seguida, chame **mmioAdvance** com o sinalizador MMIO \_ WRITE.

Por exemplo, durante uma operação de leitura, a função **mmioAdvance** define **pchEndRead** para apontar para o final de dados válidos no buffer, conforme mostrado na ilustração a seguir.

![Captura de tela que mostra 'pchNext' no início do Buffer de E/S de Arquivo, o buffer no final do E O F e 'pchEndRead' no final do buffer.](images/mmio10.gif)

Da mesma forma, durante uma operação de gravação, o aplicativo chama **mmioAdvance** para liberar o buffer e avançar **pchNext** ao final dos dados válidos no buffer, conforme mostrado na ilustração a seguir.

![imagem de buffer de e/s de arquivo](images/mmio14.gif)

 

 