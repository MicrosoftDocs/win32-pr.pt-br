---
title: Serviços em buffer
description: Serviços em buffer
ms.assetid: 4816ab05-42fc-4c22-b753-8fd153d88c27
keywords:
- e/s de arquivo de multimídia, serviços em buffer
- e/s de arquivo, serviços em buffer
- entrada e saída (e/s), serviços em buffer
- E/s (entrada e saída), serviços em buffer
- e/s em buffer
- função mmioOpen
- buffer de e/s interno
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d014ed765609dd43886cc7b33987f8fd5ac7e65a
ms.sourcegitcommit: 7ef31bf778e76ce4196205d4c4c632fbdc649805
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/05/2021
ms.locfileid: "103923028"
---
# <a name="buffered-services"></a>Serviços em buffer

A maior parte da sobrecarga na e/s de arquivo ocorre ao acessar o dispositivo de mídia. Se você estiver lendo ou escrevendo muitos blocos de informações pequenos, o dispositivo poderá passar muito tempo migrando para o local físico na mídia para cada operação de leitura ou gravação. Nesse caso, você pode obter um melhor desempenho usando os serviços de e/s de arquivo em buffer. Com e/s em buffer, o Gerenciador de e/s de arquivos mantém um buffer intermediário maior do que os blocos de informações que você está lendo ou gravando. Ele acessa o dispositivo somente quando o buffer deve ser preenchido ou gravado no disco.

Antes de configurar e usar a e/s de arquivo em buffer, você deve decidir se deseja que o Gerenciador de e/s de arquivo ou o aplicativo aloque o buffer. É mais simples permitir que o Gerenciador de e/s de arquivos aloque o buffer. No entanto, você pode permitir que o aplicativo aloque o buffer se desejar acessar diretamente o buffer ou abrir um arquivo de memória. Para obter mais informações sobre como usar arquivos de memória, consulte [executando a e/s de arquivo de memória](performing-memory-file-i-o.md). Para obter um exemplo de acesso direto a um buffer de e/s, consulte [acessando um buffer de e/s de arquivo](accessing-a-file-i-o-buffer.md)

Um buffer alocado pelo Gerenciador de e/s de arquivos é chamado de buffer de e/s interno. Para abrir um arquivo para e/s armazenada em buffer usando um buffer interno, especifique o \_ sinalizador MMIO ALLOCBUF ao abrir o arquivo com a função [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) . A ilustração a seguir mostra o estado inicial do buffer de e/s de arquivo depois que um arquivo é aberto para uma operação de leitura em buffer. O buffer é transparente — você lê e busca como se estivesse usando e/s sem buffer. A função **mmioOpen** definiu PchNext e *pchEndRead* para apontar para o início do buffer de e/s de arquivo.

![Captura de tela que mostra ' pchEndRead ' e ' pchNext ' apontando para o início do buffer de e/s de arquivo.](images/mmio7.gif)

A ilustração a seguir mostra o estado inicial do buffer de e/s de arquivo depois que um arquivo é aberto para uma operação de gravação em buffer. A função **mmioOpen** definiu **pchNext** para apontar para o início do buffer de e/s de arquivo e **pchEndWrite** para apontar para o final do buffer.

![Captura de tela que mostra ' pchNext ' no início do buffer de e/s de arquivo e ' pchEndWrite ' no final.](images/mmio11.gif)

O tamanho padrão do buffer de e/s interno é 8K. Se esse tamanho não for adequado, você poderá usar a função [**mmioSetBuffer**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosetbuffer) para alterar o tamanho do buffer. Você também pode usar essa função para habilitar o armazenamento em buffer em um arquivo aberto para e/s não armazenada em buffer, ou para fornecer seu próprio buffer para uso como um arquivo de memória.

Você pode forçar o conteúdo de um buffer de e/s a ser gravado no disco usando a função [**mmioFlush**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioflush) . No entanto, quando você fecha um arquivo usando a função [**mmioClose**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioclose) , não é necessário chamar **mmioFlush** para liberar um buffer de e/s — a função **mmioClose** o libera automaticamente. Se você ficar sem espaço em disco, o **mmioFlush** poderá falhar, mesmo se as chamadas anteriores à função [**mmioWrite**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiowrite) tiverem sido bem-sucedidas. Da mesma forma, **mmioClose** poderia falhar quando estiver liberando seu buffer de e/s.

Os aplicativos que são sensíveis ao desempenho, como aqueles que transmitem dados em tempo real de um CD-ROM, podem otimizar o desempenho de e/s de arquivo acessando diretamente o buffer de e/s. Você deve ter cuidado se optar por fazer isso, pois você ignora algumas das proteções e verificação de erros fornecidas pelo Gerenciador de e/s de arquivos.

O Gerenciador de e/s de arquivos de multimídia usa a estrutura [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) para manter informações de estado sobre um arquivo aberto. Você usa três membros nessa estrutura para ler e gravar o buffer de e/s: **pchNext**, **pchEndRead** e **pchEndWrite**. O membro **pchNext** aponta para o próximo local no buffer para leitura ou gravação. Você deve incrementar esse membro enquanto lê e grava o buffer. O membro **pchEndRead** identifica o último caractere válido que você pode ler do buffer. Da mesma forma, esse membro identifica o último local no buffer que você pode escrever. Mais precisamente, **pchEndRead** e **pchEndWrite** apontam para o local da memória que segue os últimos dados válidos no buffer. Use as funções [**mmioGetInfo**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiogetinfo) e [**mmioSetInfo**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosetinfo) para recuperar e definir informações de estado sobre o buffer de e/s de arquivo. A ilustração a seguir mostra o estado do buffer de e/s depois que o aplicativo chama **mmioAdvance** durante uma operação de leitura. A função **mmioAdvance** preenche o buffer e define o ponteiro **pchEndRead** para o final do buffer.

![Captura de tela que mostra ' pchNext ' no início do buffer de e/s de arquivo e ' pchEndRead ' no final.](images/mmio8.gif)

Na ilustração a seguir, o aplicativo lê o buffer de e/s no local especificado por **pchNext** e avança o ponteiro.

![Captura de tela que mostra ' pchNext ' no meio do buffer de e/s de arquivo e ' pchEndRead ' no final.](images/mmio9.gif)

Da mesma forma, para uma operação de gravação, o aplicativo grava no buffer de e/s e avança o ponteiro **pchNext** , conforme mostrado na ilustração a seguir.

![Captura de tela que mostra ' pchNext ' no meio do buffer de e/s de arquivo e ' pchEndWrite ' no final.](images/mmio12.gif)

Depois que o aplicativo preenche o buffer, ele chama **mmioAdvance** para liberar o buffer para o disco. A função **mmioAdvance** redefine **pchNext** para apontar para o início do buffer, conforme mostrado na ilustração a seguir.

![Captura de tela que mostra ' pchNext ' no início do buffer de e/s de arquivo, o buffer no meio do E o F e ' pchEndWrite ' no final do buffer.](images/mmio13.gif)

Quando você chegar ao final do buffer de e/s, deverá avançar o buffer para preenchê-lo a partir do disco, se você estiver lendo, ou liberá-lo para o disco, se você estiver escrevendo. Use a função [**mmioAdvance**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioadvance) para avançar um buffer de e/s. Para preencher um buffer de e/s do disco, use **mmioAdvance** com o \_ sinalizador de leitura MMIO. Se não houver dados suficientes restantes no arquivo para preencher o buffer, o membro **pchEndRead** da estrutura **MMIOINFO** apontará para o local após o último byte válido no buffer. Para liberar um buffer para o disco, defina o \_ sinalizador sujo MMIO no membro **dwFlags** da estrutura **MMIOINFO** e, em seguida, chame **MMIOADVANCE** com o sinalizador de \_ gravação MMIO.

Por exemplo, durante uma operação de leitura, a função **mmioAdvance** define **pchEndRead** para apontar para o final de dados válidos no buffer, conforme mostrado na ilustração a seguir.

![Captura de tela que mostra ' pchNext ' no início do buffer de e/s de arquivo, o buffer no final do E o F e ' pchEndRead ' no final do buffer.](images/mmio10.gif)

Da mesma forma, durante uma operação de gravação, o aplicativo chama **mmioAdvance** para liberar o buffer e avançar **pchNext** para o final dos dados válidos no buffer, conforme mostrado na ilustração a seguir.

![imagem de buffer de e/s de arquivo](images/mmio14.gif)

 

 