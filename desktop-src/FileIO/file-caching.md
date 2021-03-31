---
description: O Windows armazena em cache os dados de arquivo que são lidos de discos e gravados em discos.
ms.assetid: 0865c741-63e3-4246-ba69-801b02153e4a
title: Cache de arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a14fb668af16cfb8a4e42b59b25b73ecefbb7cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837004"
---
# <a name="file-caching"></a>Cache de arquivo

Por padrão, o Windows armazena em cache os dados de arquivo que são lidos em discos e gravados em discos. Isso implica que as operações de leitura lêem dados de arquivo de uma área na memória do sistema conhecida como cache de arquivos do sistema, e não do disco físico. Do mesmo modo, as operações de gravação gravam dados de arquivo no cache de arquivo do sistema em vez de no disco, e esse tipo de cache é conhecido como um cache de write-back. O armazenamento em cache é gerenciado por um objeto de arquivo.

O Caching ocorre sob a direção do *Gerenciador de cache*, que opera continuamente enquanto o Windows está em execução. Os dados de arquivo no cache de arquivos do sistema são gravados no disco em intervalos determinados pelo sistema operacional e a memória usada anteriormente por esses dados de arquivo é liberada – isso é conhecido como *liberação* do cache. A política de atrasar a gravação dos dados no arquivo e armazená-lo no cache até que o cache seja liberado é chamada de gravação lenta e é disparada pelo Gerenciador de cache em um intervalo de tempo determinável. A hora na qual um bloco de dados de arquivo é liberado tem base em parte na quantidade de tempo que ele ficou armazenado no cache e na quantidade de tempo desde que os dados foram acessados pela última vez em uma operação de leitura. Isso garante que os dados de arquivos lidos com frequência permaneçam acessíveis no cache de arquivo do sistema pelo máximo de tempo.

Esse processo de cache de dados de arquivo é ilustrado na figura a seguir.

![processo de cache de dados de arquivo](images/fig3.png)

Conforme descrito pelas setas sólidas na figura anterior, uma região de dados de 256 KB é lida em um "slot" de cache de 256 KB no espaço de endereço do sistema quando ele é solicitado pela primeira vez pelo Gerenciador de cache durante uma operação de leitura de arquivo. Em seguida, um processo do modo de usuário copia os dados deste slot em seu próprio espaço de endereço. Após a conclusão do acesso a dados pelo processo, ele grava os dados alterados de volta ao mesmo slot no cache do sistema, como mostrado a seta pontilhada entre o espaço de endereço do processo e o cache do sistema. Quando o Gerenciador de cache determinar que os dados não serão mais necessários por um determinado período de tempo, ele gravará os dados alterados de volta no arquivo no disco, conforme mostrado pela seta pontilhada entre o cache do sistema e o disco.

A quantidade de melhorias de desempenho de e/s oferecidas pelo cache de dados de arquivo depende do tamanho do bloco de dados de arquivo que está sendo lido ou gravado. Quando grandes blocos de dados de arquivo são lidos e gravados, é mais provável que as leituras e gravações de disco sejam necessárias para concluir a operação de e/s. O desempenho de e/s será cada vez mais prejudicado à medida que mais desse tipo de operação de e/s ocorrer.

Nessas situações, o Caching pode ser desativado. Isso é feito no momento em que o arquivo é aberto passando **o \_ sinalizador de arquivo \_ sem \_ buffer** como um valor para o parâmetro *dwFlagsAndAttributes* de [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea). Quando o Caching está desabilitado, todas as operações de leitura e gravação acessam diretamente o disco físico. No entanto, os metadados de arquivo ainda podem ser armazenados em cache. Para liberar os metadados para o disco, use a função [**FlushFileBuffers**](/windows/desktop/api/FileAPI/nf-fileapi-flushfilebuffers) .

A frequência na qual a liberação ocorre é uma consideração importante que equilibra o desempenho do sistema com a confiabilidade do sistema. Se o sistema liberar o cache com muita frequência, o número de grandes operações de gravação que liberam incorreções diminuirá significativamente o desempenho do sistema. Se o sistema não for liberado com frequência suficiente, a probabilidade é maior que a memória do sistema será esgotada pelo cache ou uma falha repentina do sistema (como perda de energia para o computador) ocorrerá antes da liberação. Na última instância, os dados armazenados em cache serão perdidos.

Para garantir que a quantidade certa de liberação ocorra, o Gerenciador de cache gera um processo a cada segundo chamado de gravador lento. O processo de gravador lento enfileira um oitavo das páginas que não foram liberadas recentemente para serem gravadas no disco. Ele reavalia constantemente a quantidade de dados que estão sendo liberados para o desempenho ideal do sistema e, se mais dados precisarem ser gravados, ele colocará em fila mais dados. Os gravadores lentos não liberam arquivos temporários, pois a suposição é que eles serão excluídos pelo aplicativo ou sistema.

Alguns aplicativos, como software de verificação de vírus, exigem que suas operações de gravação sejam liberadas para o disco imediatamente; O Windows fornece essa capacidade por meio de cache de gravação. Um processo permite o cache de write-through para uma operação de e/s específica, passando o sinalizador de gravação do sinalizador de arquivo para sua chamada para [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea). **\_ \_ \_** Com o cache de gravação habilitado, os dados ainda são gravados no cache, mas o Gerenciador de cache grava os dados imediatamente em disco, em vez de incorrer em um atraso usando o gravador lento. Um processo também pode forçar uma liberação de um arquivo que foi aberto chamando a função [**FlushFileBuffers**](/windows/desktop/api/FileAPI/nf-fileapi-flushfilebuffers) .

Os metadados do sistema de arquivos são sempre armazenados em cache. Portanto, para armazenar quaisquer alterações de metadados no disco, o arquivo deve ser liberado ou aberto com a **gravação do \_ sinalizador \_ \_ de arquivo**.

 

 



