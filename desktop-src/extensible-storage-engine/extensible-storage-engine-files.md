---
description: 'Saiba mais sobre: arquivos do mecanismo de armazenamento extensível'
title: Arquivos do mecanismo de armazenamento extensível
TOCTitle: Extensible Storage Engine Files
ms:assetid: b89a8f78-f2c4-4cbf-a000-a95c34589033
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294069(v=EXCHG.10)
ms:contentKeyID: 32765684
ms.date: 09/22/2016
ms.topic: article
ms.openlocfilehash: c27bb0104c5923496c5dd7962ef4a9bacdc90af4
ms.sourcegitcommit: 70f39ec77d19d3c32c376ee2831753d2cafae41a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105785214"
---
# <a name="extensible-storage-engine-files"></a>Arquivos do mecanismo de armazenamento extensível


_**Aplica-se a:** Windows | Windows Server_

## <a name="extensible-storage-engine-files"></a>Arquivos do mecanismo de armazenamento extensível

O mecanismo de armazenamento extensível usa os seguintes tipos de arquivos:

- [Arquivos de log de transações](#transaction-log-files)

- [Arquivos de log de transações temporários](#temporary-transaction-log-files)

- [Arquivos de log de transações reservados](#reserved-transaction-log-files)

- [Arquivos de ponto de verificação](#checkpoint-files)

- [Arquivos do banco de dados](#database-files)

- [Bancos de dados temporários](#temporary-databases)

- [Liberar arquivos de mapa](#flush-map-files)

Esta tabela contém uma visão geral dos nomes de arquivo de dados que são gerenciados pelo ESE. Para o Windows Vista e posterior, a configuração JET_paramLegacyNames Impacta os nomes de arquivo usados.

<table xmlns="https://www.w3.org/1999/xhtml">
  <tr>
    <th>
      <p>Sistema operacional</p>
    </th>
    <th>
      <p>Windows Server 2003 e anterior<br /><br /></p>
    </th>
    <th colspan="2">
      <p></p>
      <p>Windows Vista e posterior (cliente) <br />
Windows Server 2008 e posterior (servidor)
</p>
    </th>
    <th>
      <p>Atualização de aniversário do Windows 10 e posterior (cliente) <br />
Windows Server 2016 e posterior (servidor)
</p>
    </th>
  </tr>
  <tr>
    <td>
      <p>
        <strong>JET_paramLegacyNames configuração</strong>
      </p>
    </td>
    <td>
      <p>
        <strong>N/A</strong>
      </p>
    </td>
    <td>
      <p>
        <strong>Nenhum</strong>
      </p>
    </td>
    <td>
      <p>
        <strong>JET_bitESE98FileNames</strong>
      </p>
    </td>
    <td>
      <p>
        <strong>O mesmo que o Windows Vista/Server 2008</strong>
      </p>
    </td>
  </tr>
  <tr>
    <td>
      <p>Log atual</p>
    </td>
    <td>
      <p>&lt;Inst &gt; . log</p>
    </td>
    <td>
      <p>&lt;Inst &gt; . jtx</p>
    </td>
    <td>
      <p>&lt;Inst &gt; . log</p>
    </td>
    <td></td>
  </tr>
  <tr>
    <td>
      <p>Log de pré-inicialização</p>
    </td>
    <td>
      <p>&lt;Inst &gt; tmp. log</p>
    </td>
    <td>
      <p>&lt;Inst &gt; tmp. jtx</p>
    </td>
    <td>
      <p>&lt;Inst &gt; tmp. log</p>
    </td>
    <td></td>
  </tr>
  <tr>
    <td>
      <p>Logs girados</p>
    </td>
    <td>
      <p>&lt;Inst &gt; xxxxx. log</p>
    </td>
    <td>
      <p>&lt;Inst &gt; xxxxx. jtx após FFFFF mudar para &lt; Inst &gt; xxxxxxxx. jtx</p>
    </td>
    <td>
      <p>&lt;Inst &gt; xxxxx. log após FFFFF mudar para &lt; Inst &gt; xxxxxxxx. log.</p>
    </td>
    <td></td>
  </tr>
  <tr>
    <td>
      <p>
        <a href="gg294069(v=exchg.10).md">Arquivos de ponto de verificação</a>
      </p>
    </td>
    <td>
      <p>&lt;Inst &gt; . chk</p>
    </td>
    <td>
      <p>&lt;Inst &gt; . JCP</p>
    </td>
    <td>
      <p>&lt;Inst &gt; . chk</p>
    </td>
    <td rowspan="2"></td>
  </tr>
  <tr>
    <td>
      <p>
        <a href="gg294069(v=exchg.10).md">Bancos de dados temporários</a>
      </p>
    </td>
    <td>
      <p>&lt;padrão de nome de arquivo do BD temp &gt; : tmp. edb</p>
    </td>
    <td>
      <p>&lt;padrão de nome de arquivo do BD temp &gt; : tmp. edb</p>
    </td>
    <td>
      <p>&lt;padrão de nome de arquivo do BD temp &gt; : tmp. edb</p>
    </td>
  </tr>
  <tr>
    <td>
      <p>
        <a href="gg294069(v=exchg.10).md">Arquivos de log de transações reservados</a>
      </p>
    </td>
    <td>
      <p>res1. log &amp; res2. log</p>
    </td>
    <td>
      <p>&lt;Inst &gt; RESXXXXX. jrs</p>
    </td>
    <td colspan="2">
      <p>&lt;Inst &gt; RESXXXXX. jrs</p>
    </td>
  </tr>
  <tr>
    <td>
      <p>
        <a href="gg294069(v=exchg.10).md">Arquivos de banco de dados</a>
      </p>
    </td>
    <td>
      <p>&lt;nome do arquivo de BD&gt;</p>
    </td>
    <td>
      <p>&lt;nome do arquivo de BD&gt;</p>
    </td>
    <td>
      <p>&lt;nome do arquivo de BD&gt;</p>
    </td>
    <td></td>
  </tr>
  <tr>
    <td>
      <p>
        <a href="gg294069(v=exchg.10).md">Liberar arquivos de mapa</a>
      </p>
    </td>
    <td>
      <p>N/D</p>
    </td>
    <td>
      <p>N/D</p>
    </td>
    <td>
      <p>N/D</p>
    </td>
    <td>
      <p>&lt;nome do arquivo de BD sem extensão &gt; . JFM</p>
    </td>
  </tr>
</table>


### <a name="transaction-log-files"></a>Arquivos de log de transações

Os arquivos de log de transações contêm operações em arquivos de banco de dados. Elas contêm informações suficientes para colocar um banco de dados em um estado logicamente consistente após uma terminação de processo inesperada ou um desligamento do sistema.

Os nomes dos arquivos de log dependem de um nome de base de três letras, que pode ser definido com [JET_paramBaseName](./transaction-log-parameters.md). Os exemplos a seguir usam um nome de base de "edb", porque esse é o nome de base padrão. A extensão dos arquivos de log de transações será. log ou. jtx, dependendo se o JET_bitESE98FileNames está definido no parâmetro JET_paramLegacyFileNames. Para obter mais informações, consulte [parâmetros do sistema do mecanismo de armazenamento extensível](./extensible-storage-engine-system-parameters.md).

Os arquivos de log de transações são nomeados \<base\> \<generation-number\> . log, começando com 1. O número de geração de log está em formato hexadecimal. Por exemplo, edb00001. log é o primeiro log, e edb000ff. log é o log 255th. Os arquivos de log têm cinco dígitos hexadecimais no nome do arquivo de log, até o arquivo de log 1048576th, no ponto em que os arquivos de log começam a ser nomeados em um formato 11,3 (por exemplo, edb00100000. log). \<base\>. log é sempre o arquivo de log que está sendo usado no momento. Se o mecanismo de banco de dados não estiver ativo, a geração de edb. log poderá ser identificada usando o seguinte comando: **esentutl.exe-ml edb. log**.

Embora os arquivos de log de transações tenham o. Extensão de LOG normalmente associada a arquivos de texto, os arquivos de log de transações estão em um formato binário e nunca devem ser editados por um usuário. As operações de banco de dados são gravadas primeiro no log. Os dados podem ser gravados no arquivo de banco de dado mais tarde; possivelmente de imediato, possivelmente muito mais tarde. No caso de um processo inesperado ou encerramento do sistema, as operações ainda estão presentes nos arquivos de log, e as transações incompletas podem ser revertidas. O ato de reproduzir arquivos de log de transações é chamado de *recuperação simples* e é feito automaticamente quando [JetInit](./jetinit-function.md) ou [JetInit2](./jetinit2-function.md) é chamado. A recuperação simples também pode ser executada manualmente com a opção "-r" do programa Esentutl.exe. O ato de reproduzir arquivos de log de transações em um banco de dados restaurado de um backup é chamado de *recuperação complexa*.

Os arquivos de log têm um tamanho fixo, personalizável com [JET_paramLogFileSize](./transaction-log-parameters.md). Quando o arquivo de log atual (ou seja, edb. log) é preenchido, ele é renomeado para \<base\> \<generation-number\> . log e um novo arquivo de log de transações é necessário no fluxo do log de transações.

Cada instância de banco de dados tem uma única sequência de arquivo de log associada a ela. O Windows XP introduziu o [JetCreateInstance](./jetcreateinstance-function.md), permitindo que várias sequências de arquivos de log de transações sejam usadas por um único processo. No entanto, várias sequências do arquivo de log de transações não podem existir no mesmo diretório.

Os arquivos de log de transações quase nunca devem ser manipulados manualmente, renomeados, movidos ou excluídos porque os dados corrompidos podem resultar.

Os arquivos de log de transações serão excluídos pelo mecanismo de banco de dados durante um backup completo (consulte [JetBackup](./jetbackup-function.md), [JetTruncateLog](./jettruncatelog-function.md), [JetTruncateLogInstance](./jettruncateloginstance-function.md)) ou durante operações normais, se o log circular estiver habilitado.

Depois que um arquivo de log de transações é preenchido, o mecanismo de banco de dados precisa criar um novo arquivo de log. O log circular é um meio pelo qual os arquivos de log podem ser limpos automaticamente pelo mecanismo de banco de dados quando não são mais necessários para a recuperação de falhas. Esse processo é uma alternativa à remoção de arquivos de log como um produto de execução de um backup. O log circular pode ser controlado com o parâmetro do sistema [JET_paramCircularLog](./transaction-log-parameters.md) . Os arquivos de log de transações não devem ser excluídos usando qualquer outro método.

### <a name="temporary-transaction-log-files"></a>Arquivos de log de transações temporários

Quando o edb. log é preenchido, o ESE precisa criar um novo arquivo. O novo arquivo de transação de log é conhecido como um arquivo de log de transações temporário antes de seu uso pelo ESE.

Enquanto um novo arquivo de log é criado e seu tamanho estendido, ele será chamado de \<base\> tmp. log. A criação de um novo arquivo pode ser uma operação potencialmente dispendiosa, portanto, o ESE criará o próximo arquivo de log proativamente como uma tarefa em segundo plano.

Como o arquivo de log de transações temporários é criado na antecipação de necessidade de um novo arquivo de log de transações, ele não contém informações úteis.

### <a name="reserved-transaction-log-files"></a>Arquivos de log de transações reservados

Os arquivos de log de transações reservados são criados quando o mecanismo começa a permitir que operações importantes sejam registradas para obter um desligamento normal.

**Windows Vista:** No Windows Vista e posterior, os arquivos de log de transações reservados são nomeados \<base\> RESXXXXX. jrs.

**Windows Server 2003:** No Windows Server 2003 e versões anteriores, os arquivos de log de transações reservados são nomeados res1. log e res2. log.

Quando o mecanismo de banco de dados fica sem espaço em disco, ele não pode criar um novo arquivo de log. A coisa mais segura a fazer é desligar corretamente, mas algumas operações (como operações de reversão) ainda devem ser registradas em log. A maioria das operações de banco de dados falhará durante esse estágio.

Como os arquivos de log de transações reservados são criados na antecipação de necessidade de arquivos de log de transações em um cenário de fora de disco, eles não contêm nenhuma informação útil.

### <a name="checkpoint-files"></a>arquivos de ponto de verificação

O arquivo de ponto de verificação armazena o ponto de verificação para uma sequência de arquivo de log de transação específica. O arquivo de ponto de verificação é chamado \<base\> . chk ou \<base\> . JCP, dependendo se o JET_bitESE98FileNames está definido no parâmetro JET_paramLegacyFileNames e sua localização é fornecida por [JET_paramSystemPath](./transaction-log-parameters.md).

As operações de banco de dados são primeiro gravadas nos arquivos de log e, em seguida, armazenadas em cache na memória. Em algum momento posterior, as operações são gravadas no arquivo de banco de dados, mas por motivos de desempenho, a ordem na qual as operações são gravadas no arquivo de banco de dados pode não corresponder à ordem em que foram registradas originalmente. As operações gravadas no arquivo de log de transações estarão em um dos dois Estados:

  - Gravado no arquivo de log de transações e no arquivo de banco de dados.

  - Gravado no arquivo de log de transações e ainda não gravados no arquivo de banco de dados.

Muitas operações de banco de dados podem ser armazenadas em um único arquivo de log de transações. Um determinado arquivo de log pode consistir nos seguintes itens:

  - Todas as operações gravadas no arquivo de banco de dados.

  - Nenhuma operação gravada no arquivo de banco de dados

  - Uma mistura de operações gravadas no arquivo de banco de dados e operações ainda não gravadas no arquivo de banco de dados.

O ponto de verificação refere-se ao ponto no tempo no fluxo de log de transações, em que todas as operações anteriores ao ponto de verificação foram gravadas no arquivo de banco de dados. Não há nenhuma garantia sobre as operações que ocorrem após o ponto de verificação; Alguns podem estar na memória e alguns podem ser gravados no banco de dados.

Como todas as operações nos arquivos de log antes do ponto de verificação são representadas no arquivo de banco de dados, somente os arquivos de log de transações após o ponto de verificação são necessários para a recuperação simples para colocar um determinado banco de dados em um estado limpo.

### <a name="database-files"></a>Arquivos do banco de dados

O arquivo de banco de dados contém o esquema para todas as tabelas no banco de dados, os registros de todas as tabelas no banco de dados e os índices nas tabelas. Seu local é fornecido usando [JetCreateDatabase](./jetcreatedatabase-function.md), [JetCreateDatabase2](./jetcreatedatabase2-function.md), [JetAttachDatabase](./jetattachdatabase-function.md)ou [JetAttachDatabase2](./jetattachdatabase2-function.md).

Um banco de dados é desligado corretamente somente após uma chamada bem-sucedida para [JetTerm](./jetterm-function.md) ou [JetTerm2](./jetterm2-function.md).

O programa Esentutl.exe pode detectar se um banco de dados é desligado corretamente com a opção "-MH". Por exemplo, "esentutl.exe-MH Sample. edb" lerá o cabeçalho do banco de dados de um banco de dados chamado Sample. edb e imprimirá o estado de Sample. edb. Ele pode imprimir "Estado: limpar desligamento" ou "Estado: desligamento anormal".

Um banco de dados que não foi desligado corretamente está em um estado de desligamento anormal. Antes do Windows XP, esse estado era chamado *inconsistente*. Um banco de dados sujo (inconsistente) pode ser levado a um estado limpo com a recuperação simples. Um banco de dados corrompido não é o mesmo que um banco de dados sujo ("inconsistente").

Um banco de dados corrompido refere-se a uma corrupção física ou lógica e não pode ser corrigido com a recuperação simples. As corrupções físicas podem ser invertidas de bits, que frequentemente serão detectadas pelas somas de verificação nas páginas do banco de dados. Uma soma de verificação com falha em um arquivo de banco de dados se manifesta como um erro JET_errReadVerifyFailure.

Somente os bancos de dados desligados de forma limpa podem ser movidos com segurança ou renomeados. Se um banco de dados não tiver sido desligado corretamente, ele não poderá ser movido ou renomeado automaticamente.

Vários bancos de dados podem ser associados a uma única sequência de arquivos de log de transações.

### <a name="temporary-databases"></a>Bancos de dados temporários

O banco de dados temporário é usado como um repositório de backup para temptables e também é usado durante a criação de índices.

O nome e o local são configurados com [JET_paramTempPath](./temporary-database-parameters.md).

Temptables são criados com [JetOpenTempTable](./jetopentemptable-function.md), [JetOpenTempTable2](./jetopentemptable2-function.md), [JetOpenTempTable3](./jetopentemptable3-function.md), [JetOpenTemporaryTable](./jetopentemporarytable-function.md). Eles também são criados por algumas chamadas à API e usados para retornar informações de esquema (como [JetGetIndexInfo](./jetgetindexinfo-function.md)).

## <a name="flush-map-files"></a>Liberar arquivos de mapa

A partir da atualização de aniversário do Windows 10 (cliente) e do Windows Server 2016 (servidor), o ESE adicionou um nível adicional de proteção contra gravações perdidas (ou liberações perdidas) 1, permitindo que ele detecte tais eventos de reinitialization2ção entre processos. Esse recurso requer a persistência de metadados em um arquivo separado chamado de arquivo de "mapa de liberação".

Um arquivo de mapa de liberação é criado para cada arquivo de banco de dados e está localizado no mesmo diretório. O arquivo é nomeado de forma semelhante ao arquivo de banco de dados, mas com uma extensão diferente. Por exemplo, se o aplicativo cliente criar um banco de dados com o caminho completo C: \\ mydirectory \\ MyDabatase. edb, seu arquivo de mapa de liberação correspondente será C: \\ mydirectory \\ MyDabatase. JFM.

Esse aprimoramento apresenta dois requisitos de como os arquivos de banco de dados devem ser nomeados:

  - Dois bancos de dados no mesmo diretório não devem ter o mesmo nome de arquivo com extensões diferentes. Por exemplo: C: \\ mydirectory \\ MyDabatase. db1 e C: \\ mydirectory \\ MyDabatase. DB2.

  - 2 \. Um banco de dados não deve ter uma extensão. JFM.

Quando você copia ou move um arquivo de banco de dados manualmente, seu arquivo de mapa de liberação correspondente também deve ser, respectivamente, copiado ou movido para o mesmo diretório de destino. Se um arquivo de mapa de liberação não estiver presente no momento de um novo anexo de banco de dados (via [JetAttachDatabase](./jetattachdatabase-function.md), um novo será criado e preenchido novamente sob demanda, pois as páginas são lidas no banco de dados. Misturar bancos de dados incompatíveis e arquivos de mapa de liberação é manipulado pelo ESE e força o mapa de liberação incompatível a ser excluído e recriado do zero.

O tamanho de um arquivo de mapa de liberação é diretamente proporcional ao seu arquivo de banco de dados associado e aproximadamente igual a (todos os tamanhos em bytes, o resultado deve ser arredondado para o próximo múltiplo de 8.192):

`8,192 + ((<database file size> / <database page size>) / 4)`

Por exemplo: para um banco de dados de 1,5 GB usando um tamanho de página 32 KB, o tamanho aproximado do mapa de liberação é 24.576 bytes (ou 24KB).

O arquivo do mapa de liberação precisa ser atualizado, pois as páginas do banco de dados são liberadas. Se o registro em log transacional estiver habilitado (por exemplo, [JET_paramRecovery](./transaction-log-parameters.md) definido como "ativado", o padrão), a atualização do mapa de liberação será executada à medida que o aplicativo cliente fizer modificações no banco de dados. Em média, todo o mapa de liberação é gravado na mídia não volátil uma vez para cada 20% de [JET_paramCheckpointDepthMax](./database-cache-parameters.md) (em bytes) de logs transacionais gerados. O número de operações de gravação depende de quão distribuído em todo o banco de dados as modificações são. Mas é, no máximo, aproximadamente (todos os tamanhos em bytes):

`<flush map file size> / JET_paramMaxCoalesceWriteSize`

Se o registro em log transacional estiver desabilitado (por exemplo, [JET_paramRecovery](./transaction-log-parameters.md) definido como "desativado"), o mapa de liberação será atualizado apenas uma vez quando o banco de dados for explicitamente desanexado (via [JetDetachDatabase](./jetdetachdatabase-function.md), ou desanexado implicitamente, encerrando sua instância do ESE associada (por meio de qualquer uma das funções de [JetTerm](./jetterm-function.md) , desde que [JET_bitTermDirty](./jetterm2-function.md) não seja passado).

1 uma gravação perdida (ou liberação perdida) é definida como uma operação de gravação que retorna com êxito do sistema operacional para o mecanismo de banco de dados ESE, mas os dados reais nunca são mantidos no arquivo de banco de dados na mídia não volátil. Geralmente, isso é causado por uma pilha de armazenamento mal configurada ou defeituosa (software ou hardware). Os aplicativos cliente podem receber um erro [JET_errReadLostFlushVerifyFailure](./extensible-storage-engine-error-codes.md) de funções do ESE que exigem a leitura de dados do banco de dados se eles estiverem localizados em uma região que sofreu um evento de gravação perdido.

2 a capacidade de detectar gravações perdidas no tempo de vida de um processo vem presente desde o Windows 8 (cliente) e o Windows Server 2012 (Server).
