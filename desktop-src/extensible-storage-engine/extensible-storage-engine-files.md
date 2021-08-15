---
description: 'Saiba mais sobre: Extensible Armazenamento Engine Files'
title: Arquivos extensíveis Armazenamento mecanismo
TOCTitle: Extensible Storage Engine Files
ms:assetid: b89a8f78-f2c4-4cbf-a000-a95c34589033
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294069(v=EXCHG.10)
ms:contentKeyID: 32765684
ms.date: 09/22/2016
ms.topic: article
ms.openlocfilehash: a955da455cb2a2397010fd7869f6320970ef9f85ac1e1602f4439239dc56b167
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118256291"
---
# <a name="extensible-storage-engine-files"></a>Arquivos extensíveis Armazenamento mecanismo


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="extensible-storage-engine-files"></a>Arquivos extensíveis Armazenamento mecanismo

O mecanismo Armazenamento extensível usa os seguintes tipos de arquivos:

- [Arquivos de log de transações](#transaction-log-files)

- [Arquivos de log de transações temporários](#temporary-transaction-log-files)

- [Arquivos de log de transações reservadas](#reserved-transaction-log-files)

- [Arquivos de ponto de verificação](#checkpoint-files)

- [Arquivos do banco de dados](#database-files)

- [Bancos de dados temporários](#temporary-databases)

- [Liberar arquivos de mapa](#flush-map-files)

Esta tabela contém uma visão geral dos nomes de arquivo de dados gerenciados pelo ESE. Por Windows Vista e posterior, a configuração JET_paramLegacyNames afeta os nomes de arquivo usados.

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
Windows Servidor 2008 e posterior (servidor)
</p>
    </th>
    <th>
      <p>Windows 10 Atualização de aniversário e posterior (cliente) <br />
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
        <strong>O mesmo Windows Vista/Server 2008</strong>
      </p>
    </td>
  </tr>
  <tr>
    <td>
      <p>Log Atual</p>
    </td>
    <td>
      <p>&lt;inst &gt; .log</p>
    </td>
    <td>
      <p>&lt;inst &gt; .jtx</p>
    </td>
    <td>
      <p>&lt;inst &gt; .log</p>
    </td>
    <td></td>
  </tr>
  <tr>
    <td>
      <p>Log de pré-entrada</p>
    </td>
    <td>
      <p>&lt;inst &gt; tmp.log</p>
    </td>
    <td>
      <p>&lt;inst &gt; tmp.jtx</p>
    </td>
    <td>
      <p>&lt;inst &gt; tmp.log</p>
    </td>
    <td></td>
  </tr>
  <tr>
    <td>
      <p>Logs girados</p>
    </td>
    <td>
      <p>&lt;inst &gt; XXXXX.log</p>
    </td>
    <td>
      <p>&lt;inst &gt; XXXXX.jtx após fFFFF mudar para &lt; inst &gt; XXXXXXXX.jtx</p>
    </td>
    <td>
      <p>&lt;inst &gt; XXXXX.log após a mudança de FFFFF para &lt; inst &gt; XXXXXXXX.log.</p>
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
      <p>&lt;inst &gt; .chk</p>
    </td>
    <td>
      <p>&lt;inst &gt; .jcp</p>
    </td>
    <td>
      <p>&lt;inst &gt; .chk</p>
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
      <p>&lt;temp db file name &gt; Default: tmp.edb</p>
    </td>
    <td>
      <p>&lt;temp db file name &gt; Default: tmp.edb</p>
    </td>
    <td>
      <p>&lt;temp db file name &gt; Default: tmp.edb</p>
    </td>
  </tr>
  <tr>
    <td>
      <p>
        <a href="gg294069(v=exchg.10).md">Arquivos de log de transações reservadas</a>
      </p>
    </td>
    <td>
      <p>res1.log &amp; res2.log</p>
    </td>
    <td>
      <p>&lt;inst &gt; RESXXXXX.jrs</p>
    </td>
    <td colspan="2">
      <p>&lt;inst &gt; RESXXXXX.jrs</p>
    </td>
  </tr>
  <tr>
    <td>
      <p>
        <a href="gg294069(v=exchg.10).md">Arquivos de banco de dados</a>
      </p>
    </td>
    <td>
      <p>&lt;nome do arquivo de banco de dados&gt;</p>
    </td>
    <td>
      <p>&lt;nome do arquivo de banco de dados&gt;</p>
    </td>
    <td>
      <p>&lt;nome do arquivo de banco de dados&gt;</p>
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
      <p>&lt;db file name without extension &gt; .jfm</p>
    </td>
  </tr>
</table>


### <a name="transaction-log-files"></a>Arquivos de log de transações

Arquivos de log de transações contêm operações em arquivos de banco de dados. Eles contêm informações suficientes para colocar um banco de dados em um estado logicamente consistente após um encerramento inesperado de processo ou desligamento do sistema.

Os nomes dos arquivos de log dependem de um nome base de três letras, que pode ser definido com [JET_paramBaseName](./transaction-log-parameters.md). Os exemplos a seguir usam um nome base de "edb", porque esse é o nome base padrão. A extensão para os arquivos de log de transações será .log ou .jtx, dependendo se o JET_bitESE98FileNames está definido no parâmetro JET_paramLegacyFileNames. Para obter mais informações, consulte [Extensible Armazenamento System Parameters .](./extensible-storage-engine-system-parameters.md)

Os arquivos de log de transações \<base\> \<generation-number\> são denominados .log, começando com 1. O número de geração de log está em formato hexadecimal. Por exemplo, edb00001.log é o primeiro log e edb000ff.log é o 255º log. Os arquivos de log têm cinco dígitos hexadecimais no nome do arquivo de log até o 1048576º arquivo de log, quando os arquivos de log começam a ser nomeados em um formato 11.3 (por exemplo, edb00100000.log). \<base\>.log é sempre o arquivo de log que está sendo usado no momento. Se o mecanismo de banco de dados não estiver ativo, a geração de edb.log poderá ser identificada usando o seguinte comando: **esentutl.exe -ml edb.log**.

Embora os arquivos de log de transações tenham o . A extensão LOG normalmente associada a arquivos de texto, os arquivos de log de transações estão em um formato binário e nunca devem ser editados por um usuário. As operações de banco de dados são escritas no log primeiro. Os dados podem ser gravados no arquivo de banco de dados posteriormente; possivelmente imediatamente, potencialmente muito mais tarde. No caso de um processo inesperado ou encerramento do sistema, as operações ainda estão presentes nos arquivos de log e transações incompletas podem ser recompodas. O ato de repetir arquivos de log de transações é chamado de recuperação suave e é feito automaticamente quando [JetInit](./jetinit-function.md) ou [JetInit2](./jetinit2-function.md) é chamado. A recuperação suave também pode ser executada manualmente com a opção "-r" do programa Esentutl.exe. O ato de repetir arquivos de log de transações em um banco de dados que é restaurado de um backup é chamado *de recuperação de disco rígido.*

Os arquivos de log são de um tamanho fixo, personalizáveis [com JET_paramLogFileSize](./transaction-log-parameters.md). Quando o arquivo de log atual (ou seja, edb.log) é preenchido, ele é renomeado para .log e um novo arquivo de log de transações é necessário no fluxo de \<base\> \<generation-number\> log de transações.

Cada instância de banco de dados tem uma única sequência de arquivos de log associada a ela. Windows O XP [introduziu JetCreateInstance](./jetcreateinstance-function.md), permitindo que várias sequências de arquivos de log de transações sejam usadas por um único processo. No entanto, não é possível existir várias sequências de arquivo de log de transações no mesmo diretório.

Os arquivos de log de transações quase nunca devem ser manipulados manualmente, renomeados, movidos ou excluídos porque podem resultar em corrupção de dados.

Os arquivos de log de transações serão excluídos pelo mecanismo de banco de dados durante um backup completo (consulte [JetBackup,](./jetbackup-function.md) [JetTruncateLog](./jettruncatelog-function.md), [JetTruncateLogInstance](./jettruncateloginstance-function.md)) ou durante operações normais, se o log circular estiver habilitado.

Depois que um arquivo de log de transações é preenchido, o mecanismo de banco de dados precisa criar um novo arquivo de log. O log circular é um meio pelo qual os arquivos de log podem ser limpos automaticamente pelo mecanismo de banco de dados quando não são mais necessários para a recuperação de falhas. Esse processo é uma alternativa à remoção de arquivos de log como um by-product da execução de um backup. O registro em log circular pode ser controlado com o [JET_paramCircularLog](./transaction-log-parameters.md) do sistema. Os arquivos de log de transações não devem ser excluídos usando qualquer outro método.

### <a name="temporary-transaction-log-files"></a>Arquivos de log de transações temporários

Quando edb.log é preenchida, o ESE precisa criar um novo arquivo. O novo arquivo de transação de log é conhecido como um arquivo de log de transações temporário antes de seu uso pelo ESE.

Embora um novo arquivo de log seja criado e seu tamanho seja estendido, ele será \<base\> chamado de tmp.log. A criação de um novo arquivo pode ser uma operação potencialmente cara, portanto, o ESE criará o próximo arquivo de log proativamente como uma tarefa em segundo plano.

Como o arquivo de log de transações temporárias é criado antecipando a necessidade de um novo arquivo de log de transações, ele não contém nenhuma informação útil.

### <a name="reserved-transaction-log-files"></a>Arquivos de log de transações reservadas

Os arquivos de log de transações reservados são criados quando o mecanismo começa a permitir que operações importantes sejam registradas para obter um desligamento limpo.

**Windows Vista:** No Windows Vista e posterior, os Arquivos de Log de Transações Reservadas são \<base\> denominados RESXXXXX.jrs.

**Windows Server 2003:** No Windows Server 2003 e anteriores, os Arquivos de Log de Transações Reservadas são chamados res1.log e res2.log.

Quando o mecanismo de banco de dados fica sem espaço em disco, ele não pode criar um novo arquivo de log. O mais seguro a fazer é desligar corretamente, mas algumas operações (como operações de reação) ainda devem ser registradas. A maioria das operações de banco de dados falhará durante esse estágio.

Como os arquivos de log de transações reservados são criados em antecipação à necessidade de arquivos de log de transações em um cenário fora do disco, eles não contêm nenhuma informação útil.

### <a name="checkpoint-files"></a>arquivos de ponto de verificação

O arquivo de ponto de verificação armazena o ponto de verificação para uma sequência de arquivos de log de transações específica. O arquivo de ponto de verificação é denominado \<base\> .chk ou \<base\> .jcp, dependendo se o JET_bitESE98FileNames está [](./transaction-log-parameters.md)definido no parâmetro JET_paramLegacyFileNames e seu local é dado por JET_paramSystemPath .

As operações de banco de dados são primeiro escritas nos arquivos de log e, em seguida, armazenadas em cache na memória. Em algum momento posterior, as operações são escritas no arquivo de banco de dados, mas, por motivos de desempenho, a ordem na qual as operações são escritas no arquivo de banco de dados pode não corresponder à ordem em que foram registradas originalmente. As operações escritas no arquivo de log de transações estarão em um dos dois estados:

  - Gravado no arquivo de log de transações e no arquivo de banco de dados.

  - Gravado no arquivo de log de transações e ainda não gravado no arquivo de banco de dados.

Muitas operações de banco de dados podem ser armazenadas em um único arquivo de log de transações. Um determinado arquivo de log pode consistir nos seguintes itens:

  - Todas as operações escritas no arquivo de banco de dados.

  - Nenhuma operação é escrita no arquivo de banco de dados

  - Uma combinação de operações escritas no arquivo de banco de dados e operações que ainda não foram escritas no arquivo de banco de dados.

O ponto de verificação refere-se ao ponto no tempo no fluxo de log de transações em que todas as operações anteriores ao ponto de verificação foram escritas no arquivo de banco de dados. Não há nenhuma garantia sobre as operações que ocorrem após o ponto de verificação; alguns podem estar na memória e outros podem ser gravados no banco de dados.

Como todas as operações nos arquivos de log anteriores ao ponto de verificação são representadas no arquivo de banco de dados, somente os arquivos de log de transações após o ponto de verificação são necessários para a recuperação suave para colocar um banco de dados específico em um estado limpo.

### <a name="database-files"></a>Arquivos do banco de dados

O arquivo de banco de dados contém o esquema para todas as tabelas no banco de dados, os registros de todas as tabelas no banco de dados e os índices nas tabelas. Seu local é dado usando [JetCreateDatabase,](./jetcreatedatabase-function.md) [JetCreateDatabase2,](./jetcreatedatabase2-function.md) [JetAttachDatabase ou](./jetattachdatabase-function.md) [JetAttachDatabase2](./jetattachdatabase2-function.md).

Um banco de dados é desligado corretamente somente após uma chamada bem-sucedida para [JetTerm](./jetterm-function.md) ou [JetTerm2.](./jetterm2-function.md)

O Esentutl.exe pode detectar se um banco de dados é desligado corretamente com a opção "-mh". Por exemplo, "esentutl.exe -mh sample.edb" lerá o header do banco de dados de um banco de dados chamado sample.edb e imprimirá o estado de sample.edb. Ele pode imprimir "Estado: Desligamento Limpo" ou "Estado: Desligamento Sujo".

Um banco de dados que não foi desligado corretamente está em um estado de desligamento sujo. Antes de Windows XP, esse estado era chamado *de inconsistente.* Um banco de dados sujo (inconsistente) pode ser levado para um estado limpo com recuperação suave. Um banco de dados corrompido não é o mesmo que um banco de dados sujo ("inconsistente").

Um banco de dados corrompido refere-se a uma corrupção física ou lógica e não pode ser corrigido com recuperação suave. As corrupçãos físicas podem ser invasões de bits, que frequentemente serão capturadas pelas verificações nas páginas do banco de dados. Uma verificação com falha em um arquivo de banco de dados se manifesta como JET_errReadVerifyFailure erro.

Somente os bancos de dados desligados corretamente podem ser movidos com segurança ou renomeados. Se um banco de dados não tiver sido desligado corretamente, ele não poderá ser movido ou renomeado automaticamente com segurança.

Vários bancos de dados podem ser associados a uma única sequência de arquivos de log de transações.

### <a name="temporary-databases"></a>Bancos de dados temporários

O banco de dados temporário é usado como um armazenamento de back-back para temptables e também é usado ao criar índices.

O nome e o local são configurados [com JET_paramTempPath](./temporary-database-parameters.md).

Temptables são criados com [JetOpenTempTable,](./jetopentemptable-function.md) [JetOpenTempTable2,](./jetopentemptable2-function.md) [JetOpenTempTable3,](./jetopentemptable3-function.md) [JetOpenTemporaryTable](./jetopentemporarytable-function.md). Eles também são criados por algumas chamadas à API e usados para retornar informações de esquema (como [JetGetIndexInfo](./jetgetindexinfo-function.md)).

## <a name="flush-map-files"></a>Liberar arquivos de mapa

A partir da Atualização de Aniversário do Windows 10 (cliente) e do Windows Server 2016 (servidor), o ESE adicionou um nível adicional de proteção contra gravações perdidas (ou liberações perdidas) 1, permitindo que ele detecte esses eventos entre processos de inicialização2. Esse recurso requer metadados persistentes para um arquivo separado chamado de "mapa de liberação".

Um arquivo de mapa de liberação é criado para cada arquivo de banco de dados e está localizado no mesmo diretório. O arquivo é nomeado de forma semelhante ao arquivo de banco de dados, mas com uma extensão diferente. Por exemplo, se o aplicativo cliente criar um banco de dados com o caminho completo C: MyDirectory MyDabatase.edb, seu arquivo de mapa de liberação correspondente será \\ \\ C: \\ MyDirectory \\ MyDabatase.jfm.

Essa melhoria apresenta dois requisitos de como os arquivos de banco de dados devem ser nomeados:

  - Dois bancos de dados no mesmo diretório não devem ter o mesmo nome de arquivo com extensões diferentes. Por exemplo: C: \\ MyDirectory \\ MyDabatase.db1 e C: \\ MyDirectory \\ MyDabatase.db2.

  - 2\. Um banco de dados não deve ter uma extensão .jfm.

Quando você copia ou move manualmente um arquivo de banco de dados, seu arquivo de mapa de liberação correspondente também deve ser, respectivamente, copiado ou movido para o mesmo diretório de destino. Se um arquivo de mapa de liberação não estiver presente no momento de um novo anexo de banco de dados (por meio de [JetAttachDatabase),](./jetattachdatabase-function.md)um novo será criado e preenchido sob demanda conforme as páginas são lidas do banco de dados. A combinação de arquivos de banco de dados e de mapa de liberação incompatibilidade é manipulada pelo ESE e força o mapa de liberação sem-compatibilidade a ser excluído e criado do zero.

O tamanho de um arquivo de mapa de liberação é diretamente proporcional ao seu arquivo de banco de dados associado e aproximadamente igual a (todos os tamanhos em bytes, o resultado deve ser arredondado para o próximo múltiplo de 8.192):

`8,192 + ((<database file size> / <database page size>) / 4)`

Por exemplo: para um banco de dados de 1,5 GB usando um tamanho de página de 32KB, o tamanho aproximado do mapa de liberação é de 24.576 bytes (ou 24KB).

O arquivo de mapa de liberação precisa ser atualizado à medida que as páginas do banco de dados são liberados. Se o log transacional estiver habilitado (por exemplo, [JET_paramRecovery](./transaction-log-parameters.md) definido como "ativado", o padrão), a atualização do mapa de liberação será executada à medida que o aplicativo cliente fizer modificações no banco de dados. Em média, todo o mapa de liberação é gravado na mídia não volátil uma vez para cada 20% de JET_paramCheckpointDepthMax [-worth](./database-cache-parameters.md) (em bytes) de logs transacionais gerados. O número de operações de gravação depende de como são distribuídas em todo o banco de dados as modificações. Mas é, no máximo, aproximadamente (todos os tamanhos em bytes):

`<flush map file size> / JET_paramMaxCoalesceWriteSize`

Se o registro em log transacional estiver desabilitado (por [exemplo,](./transaction-log-parameters.md) JET_paramRecovery definido como "desativado"), o mapa de liberação será atualizado apenas uma vez quando o banco de dados for explicitamente desvinculado corretamente (por meio de [JetDetachDatabase](./jetdetachdatabase-function.md)ou desvinculado implicitamente corretamente, encerrando sua instância ESE associada (por meio de qualquer uma das funções [JetTerm,](./jetterm-function.md) desde que [JET_bitTermDirty](./jetterm2-function.md) não seja passado).

1 Uma gravação perdida (ou liberação perdida) é definida como uma operação de gravação que retorna com êxito do sistema operacional para o mecanismo de banco de dados ESE, mas os dados reais nunca são persistentes para o arquivo de banco de dados na mídia não volátil. Geralmente, isso é causado por uma pilha de armazenamento mal-configurada ou mal configurada (software ou hardware). Os aplicativos cliente podem receber [um JET_errReadLostFlushVerifyFailure](./extensible-storage-engine-error-codes.md) erro de funções ESE que exigem a leitura de dados do banco de dados se os dados estão localizados em uma região que subescodizou um evento de gravação perdido.

2 A capacidade de detectar gravações perdidas dentro do tempo de vida de um processo está presente desde Windows 8 (cliente) e Windows Server 2012 (servidor).
