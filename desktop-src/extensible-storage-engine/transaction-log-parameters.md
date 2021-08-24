---
description: 'Saiba mais sobre: Parâmetros de log de transações'
title: Parâmetros de Log de Transação
TOCTitle: Transaction Log Parameters
ms:assetid: 41ade693-2bae-4c84-9339-a68a1b7c23e6
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269235(v=EXCHG.10)
ms:contentKeyID: 32765537
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 24c8665b42aad5c94db18e3a30a2b5ea09974627
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122465073"
---
# <a name="transaction-log-parameters"></a>Parâmetros de Log de Transação


_**Aplica-se a:** Windows | Windows Servidor_

**Neste artigo**  
Parâmetros de Log de Transação  
Requisitos  
Consulte Também  

## <a name="transaction-log-parameters"></a>Parâmetros de Log de Transação

Este tópico contém parâmetros que são usados para logs de transações.

*JET_paramBaseName*  
3  

Esse parâmetro define o prefixo de três letras usado para muitos dos arquivos usados pelo mecanismo de banco de dados. Por exemplo, o arquivo de ponto de verificação é chamado de EDB. CHK por padrão porque EDB é o nome base padrão. O nome base pode ser usado para distinguir facilmente entre conjuntos de arquivos que pertencem a instâncias diferentes ou a aplicativos diferentes.


| | | <p>Valor padrão:</p> | <p>"edb"</p> | | <p>Tipo:</p> | <p>String</p> | | <p>Intervalo válido:</p> | <p>3 caracteres</p> | | <p>Escopo:</p> | <p>Instância</p> | | <p>Definido após <a href="gg269354(v=exchg.10).md">JetCreateInstance:</a></p> | <p>Sim</p> | | <p>Definido após <a href="gg294068(v=exchg.10).md">JetInit:</a></p> | <p>Não</p> | | <p>Afeta o layout físico:</p> | <p>Sim</p> | | <p>Afeta a confiabilidade:</p> | <p>Não</p> | | <p>Afeta o desempenho:</p> | <p>Não</p> | | <p>Afeta recursos:</p> | <p>Não</p> | | <p>Disponibilidade:</p> | <p>Tudo</p> | 



*JET_paramCircularLog*  
17  

Esse parâmetro configura como os arquivos de log de transações são gerenciados pelo mecanismo de banco de dados.

Quando o log circular estiver desligado, todos os arquivos de log de transações gerados serão retidos no disco até que não sejam mais necessários porque um backup completo do banco de dados foi executado. Nesse modo, é possível restaurar de um backup mais antigo e reproduzir por meio de todos os arquivos de log de transações retidos, de modo que nenhum dado seja perdido como resultado do desastre que força a restauração. Backups completos regulares são necessários para impedir que o disco preencha com arquivos de log de transações.

Quando o log circular estiver, somente os arquivos de log de transações menores que o ponto de verificação atual serão retidos no disco. O benefício desse modo é que os backups não são necessários para retirar arquivos de log de transações antigos. A recompensa é que uma restauração de perda de dados zero não é mais possível.


| | | <p>Valor padrão:</p> | <p>Falso</p> | | <p>Tipo:</p> | <p>Boolean</p> | | <p>Intervalo válido:</p> | <p>False, True</p> | | <p>Escopo:</p> | <p>Instância</p> | | <p>Definido após <a href="gg269354(v=exchg.10).md">JetCreateInstance:</a></p> | <p>Sim</p> | | <p>Definido após <a href="gg294068(v=exchg.10).md">JetInit:</a></p> | <p>Não</p> | | <p>Afeta o layout físico:</p> | <p>Sim</p> | | <p>Afeta a confiabilidade:</p> | <p>Sim</p> | | <p>Afeta o desempenho:</p> | <p>Não</p> | | <p>Afeta recursos:</p> | <p>Sim</p> | | <p>Disponibilidade:</p> | <p>Tudo</p> | 



*JET_paramCommitDefault*  
16  

Esse parâmetro controla a ação padrão tomada quando a transação mais externa é comprometida em uma sessão. Qualquer opção válida que possa ser passada para [JetCommitTransaction](./jetcommittransaction-function.md) também pode ser feita para ser o padrão para todas as sessões em uma instância e/ou para uma sessão específica. Consulte [JetCommitTransaction](./jetcommittransaction-function.md) para obter mais detalhes sobre essas opções.

Esse parâmetro tem um impacto sobre a confiabilidade e o desempenho das transações. Consulte [JetCommitTransaction para](./jetcommittransaction-function.md) obter mais detalhes.


| | | <p>Valor padrão:</p> | <p>0</p> | | <p>Tipo:</p> | <p>JET_GRBIT (inteiro)</p> | | <p>Intervalo válido:</p> | <p>Uma opção válida para JetCommitTransaction</p> | | <p>Escopo:</p> | <p>Instância ou sessão</p> | | <p>Definido após <a href="gg269354(v=exchg.10).md">JetCreateInstance:</a></p> | <p>Sim</p> | | <p>Definido após <a href="gg294068(v=exchg.10).md">JetInit:</a></p> | <p>Sim</p> | | <p>Afeta o layout físico:</p> | <p>Não</p> | | <p>Afeta a confiabilidade:</p> | <p>Sim</p> | | <p>Afeta o desempenho:</p> | <p>Sim</p> | | <p>Afeta recursos:</p> | <p>Não</p> | | <p>Disponibilidade:</p> | <p>Tudo</p> | 



*JET_paramDeleteOldLogs*  
48  

Quando esse parâmetro for true e os arquivos de log de transações apontados pelo caminho do arquivo de log (**JET_paramLogFilePath**) são de uma versão obsoleta, esses arquivos de log de transações serão excluídos automaticamente.

**Windows 2000:**  deve-se ter cuidado com o uso desse parâmetro ao atualizar um banco de dados de Windows NT para Windows 2000. Se o banco de dados não estiver em um estado consistente e os arquivos de log antigos forem excluídos, o conteúdo do banco de dados será perdido.


| | | <p>Valor padrão:</p> | <p><strong>Windows 2000:</strong>  For</p><p><strong>Windows XP:</strong>  True</p> | | <p>Tipo:</p> | <p>Boolean</p> | | <p>Intervalo válido:</p> | <p>Falso, verdadeiro</p> | | <p>Escopo:</p> | <p>Instância</p> | | <p>Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Sim</p> | | <p>Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>Não</p> | | <p>Afeta o layout físico:</p> | <p>Sim</p> | | <p>Afeta a confiabilidade:</p> | <p>Sim</p> | | <p>Afeta o desempenho:</p> | <p>Não</p> | | <p>Afeta os recursos:</p> | <p>Não</p> | | <p>Disponibilidade:</p> | <p>Tudo</p> | 



*JET_paramIgnoreLogVersion*  
47  

Se esse parâmetro for true, o mecanismo de banco de dados não validará o número de versão do arquivo de log de transações durante [JetInit](./jetinit-function.md).

**Windows XP:**  a partir do Windows XP, esse parâmetro é obsoleto e não afeta a operação do mecanismo de banco de dados.


| | | <p>Valor padrão:</p> | <p>Falso</p> | | <p>Tipo:</p> | <p>Boolean</p> | | <p>Intervalo válido:</p> | <p>Falso, verdadeiro</p> | | <p>Escopo:</p> | <p>Instância</p> | | <p>Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Sim</p> | | <p>Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>Não</p> | | <p>Afeta o layout físico:</p> | <p>Não</p> | | <p>Afeta a confiabilidade:</p> | <p>Sim</p> | | <p>Afeta o desempenho:</p> | <p>Não</p> | | <p>Afeta os recursos:</p> | <p>Não</p> | | <p>Disponibilidade:</p> | <p>Tudo</p> | 



*JET_paramLegacyFileNames*  
136  

Esse parâmetro fornece compatibilidade com versões anteriores do mecanismo de banco de dados para as convenções de nomenclatura do arquivo.

Atualmente, há suporte para as seguintes opções:

JET_bitESE98FileNames

Quando essa opção estiver presente, o mecanismo de banco de dados usará as seguintes convenções de nomenclatura para seus arquivos:

  - Os arquivos de log de transações usarão. LOG para sua extensão de arquivo

  - Os arquivos de ponto de verificação usarão. CHK para sua extensão de arquivo


| | | <p>Valor padrão:</p> | <p>JET_bitESE98FileNames</p> | | <p>Tipo:</p> | <p>JET_GRBIT (inteiro)</p> | | <p>Intervalo válido:</p> | <p>0, JET_bitESE98FileNames</p> | | <p>Escopo:</p> | <p>Instância</p> | | <p>Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Sim</p> | | <p>Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>Não</p> | | <p>Afeta o layout físico:</p> | <p>Sim</p> | | <p>Afeta a confiabilidade:</p> | <p>Não</p> | | <p>Afeta o desempenho:</p> | <p>Não</p> | | <p>Afeta os recursos:</p> | <p>Não</p> | | <p>Disponibilidade:</p> | <p>Windows Vista e versões posteriores</p> | 



*JET_paramLogBuffers*  
12  

Esse parâmetro irá configurar a quantidade de memória usada para armazenar em cache os registros de log antes que eles sejam gravados no arquivo de log de transações. A unidade para esse parâmetro é o tamanho do setor do volume que contém os arquivos de log de transações. O tamanho do setor quase sempre é de 512 bytes, portanto, é seguro assumir esse tamanho para a unidade.

Esse parâmetro tem um impacto no desempenho. Quando o mecanismo de banco de dados está sob carga de atualização pesada, esse buffer pode se tornar completo com muita rapidez. Um tamanho de cache maior para o arquivo de log de transações é essencial para um bom desempenho de atualização sob uma condição de alta carga. O padrão é conhecido como muito pequeno para esse caso.

**Windows XP e Windows 2000:**  no Windows XP e versões anteriores, não é recomendável definir esse parâmetro como um número de buffers maior (em bytes) que metade do tamanho de um arquivo de log de transações.


| | | <p>Valor padrão:</p> | <p><strong>Windows 2000, Windows XP e Windows Server 2003:</strong> 80</p><p><strong>Windows Vista:</strong> 126</p> | | <p>Tipo:</p> | <p>Inteiro</p> | | <p>Intervalo válido:</p> | <p><strong>Windows 2000, Windows XP e Windows Server 2003:</strong> 80 – 2147483647</p><p><strong>Windows Vista:</strong> 1 a 2147483647</p> | | <p>Escopo:</p> | <p>Instância</p> | | <p>Definido após <a href="gg269354(v=exchg.10).md">JetCreateInstance:</a></p> | <p>Sim</p> | | <p>Definido após <a href="gg294068(v=exchg.10).md">JetInit:</a></p> | <p>Não</p> | | <p>Afeta o layout físico:</p> | <p>Não</p> | | <p>Afeta a confiabilidade:</p> | <p>Não</p> | | <p>Afeta o desempenho:</p> | <p>Sim</p> | | <p>Afeta recursos:</p> | <p>Sim</p> | | <p>Disponibilidade:</p> | <p>Tudo</p> | 



*JET_paramLogCheckpointPeriod*  
14  

Esse parâmetro configura o mecanismo de banco de dados para fazer um ponto de verificação quando o número especificado de setores de arquivo de log tiver sido gerado.

**Windows XP:**  A partir Windows XP, esse parâmetro está obsoleto e não afeta a operação do mecanismo de banco de dados.


| | | <p>Valor padrão:</p> | <p>1024</p> | | <p>Tipo:</p> | <p>Inteiro</p> | | <p>Intervalo válido:</p> | <p>0 – 2147483647</p> | | <p>Escopo:</p> | <p>Instância</p> | | <p>Definido após <a href="gg269354(v=exchg.10).md">JetCreateInstance:</a></p> | <p>Sim</p> | | <p>Definido após <a href="gg294068(v=exchg.10).md">JetInit:</a></p> | <p>Não</p> | | <p>Afeta o layout físico:</p> | <p>Não</p> | | <p>Afeta a confiabilidade:</p> | <p>Sim</p> | | <p>Afeta o desempenho:</p> | <p>Sim</p> | | <p>Afeta recursos:</p> | <p>Não</p> | | <p>Disponibilidade:</p> | <p>Tudo</p> | 



*JET_paramLogFileCreateAsynch*  
69  

Quando esse parâmetro for definido como true, o mecanismo de banco de dados criará o próximo arquivo de log de transações conforme o arquivo de log de transações atual for consumido. A intenção é minimizar o tempo gasto alternando de um arquivo de log de transações para o próximo sob uma carga de atualização pesada.


| | | <p>Valor padrão:</p> | <p>Verdadeiro</p> | | <p>Tipo:</p> | <p>Boolean</p> | | <p>Intervalo válido:</p> | <p>False, True</p> | | <p>Escopo:</p> | <p>Instância</p> | | <p>Definido após <a href="gg269354(v=exchg.10).md">JetCreateInstance:</a></p> | <p>Sim</p> | | <p>Definido após <a href="gg294068(v=exchg.10).md">JetInit:</a></p> | <p>Não</p> | | <p>Afeta o layout físico:</p> | <p>Sim</p> | | <p>Afeta a confiabilidade:</p> | <p>Não</p> | | <p>Afeta o desempenho:</p> | <p>Sim</p> | | <p>Afeta recursos:</p> | <p>Sim</p> | | <p>Disponibilidade:</p> | <p>Windows XP e versões posteriores</p> | 



*JET_paramLogFilePath*  
2 

Esse parâmetro indica o caminho do sistema de arquivos relativo ou absoluto da pasta que conterá os logs de transações para a instância. O caminho deve ser encerrado com um caractere de faixa invertida, o que indica que o caminho de destino é uma pasta. Os arquivos de log de transações contêm as informações necessárias para colocar os arquivos de banco de dados em um estado consistente após uma falha. Normalmente, eles são nomeados como \* EDB. LOG. O conteúdo dos arquivos de log de transações é tão importante (se não mais) do que os próprios arquivos de banco de dados. Todos os esforços devem ser feitos para protegê-los.

Também haverá arquivos de log de reserva adicionais chamados RES1. LOG e RES2. LOG armazenado junto com os arquivos de log comuns. O conteúdo desses arquivos não é importante, pois sua única finalidade é reservar espaço em disco para permitir que o mecanismo seja desligado normalmente em um cenário de disco baixo. Eles também serão um arquivo de log temporário normalmente chamado EDBTMP. FAÇA LOGOFF nessa mesma pasta. O conteúdo desse arquivo também não é importante. Esse arquivo é um novo arquivo de log que está sendo preparado para uso.

As propriedades do volume de host dos arquivos de log de transações e seu posicionamento em relação aos outros arquivos usados pelo mecanismo de banco de dados podem afetar drasticamente o desempenho.

**Observação**  Se um caminho relativo for especificado, ele será relativo ao diretório de trabalho atual do processo que hospeda o aplicativo que está usando o mecanismo de banco de dados.


| | | <p>Valor padrão:</p> | <p>".\"</p> | | <p>Tipo:</p> | <p>Caminho da Pasta (cadeia de caracteres)</p> | | <p>Intervalo válido:</p> | <p>0 – 246 caracteres</p> | | <p>Escopo:</p> | <p>Instância</p> | | <p>Definido após <a href="gg269354(v=exchg.10).md">JetCreateInstance:</a></p> | <p>Sim</p> | | <p>Definido após <a href="gg294068(v=exchg.10).md">JetInit:</a></p> | <p>Não</p> | | <p>Afeta o layout físico:</p> | <p>Sim</p> | | <p>Afeta a confiabilidade:</p> | <p>Sim</p> | | <p>Afeta o desempenho:</p> | <p>Sim</p> | | <p>Afeta recursos:</p> | <p>Não</p> | | <p>Disponibilidade:</p> | <p>Tudo</p> | 



*JET_paramLogFileSize*  
11  

Esse parâmetro configurará o tamanho dos arquivos de log de transações. Cada arquivo de log de transações tem um tamanho fixo. O tamanho é igual à configuração desse parâmetro do sistema em unidades de 1024 bytes.

Esse parâmetro tem um impacto sobre a confiabilidade. Se a configuração for muito pequena, o número máximo de arquivos de log (1048575) será atingido muito mais rapidamente. Quando isso acontece, a instância deve ser desligado corretamente, os arquivos de log existentes devem ser excluídos e a instância deve ser reiniciada. Essa ação não apenas reduzirá a disponibilidade do aplicativo, mas também invalidará todos os backups anteriores do banco de dados do aplicativo.

Esse parâmetro tem um impacto sobre o desempenho. Se a configuração for muito grande, [o JetInit](./jetinit-function.md) ficará lento porque o mecanismo de banco de dados deve ler o arquivo de log mais novo (no mínimo) quando for inicializado. Se a configuração for muito grande, também levará mais tempo para alternar entre arquivos de log. Se a configuração for muito pequena, mais arquivos de log precisarão ser criados para um determinado número de atualizações, o que adicionará mais sobrecarga.


| | | <p>Valor padrão:</p> | <p>5120</p> | | <p>Tipo:</p> | <p>Inteiro</p> | | <p>Intervalo válido:</p> | <p><strong>Windows 2000, Windows XP e Windows Server 2003:</strong> 128 – 32768</p><p><strong>Windows Vista:</strong> 64 – 32768</p> | | <p>Escopo:</p> | <p>Instância</p> | | <p>Definido após <a href="gg269354(v=exchg.10).md">JetCreateInstance:</a></p> | <p>Sim</p> | | <p>Definido após <a href="gg294068(v=exchg.10).md">JetInit:</a></p> | <p>Não</p> | | <p>Afeta o layout físico:</p> | <p>Sim</p> | | <p>Afeta a confiabilidade:</p> | <p>Sim</p> | | <p>Afeta o desempenho:</p> | <p>Sim</p> | | <p>Afeta recursos:</p> | <p>Sim</p> | | <p>Disponibilidade:</p> | <p>Tudo</p> | 



*JET_paramLogWaitingUserMax*  
15  

Esse parâmetro tenta otimizar a liberação do buffer de log causada por uma confirmação durável aguardando um número especificado de sessões aguardar uma confirmação durável antes de forçar uma liberação a ocorrer na espera de que outra transação compartilhe a liberação.

**Windows XP:**  A partir Windows XP, esse parâmetro está obsoleto e não afeta a operação do mecanismo de banco de dados.


| | | <p>Valor padrão:</p> | <p>3</p> | | <p>Tipo:</p> | <p>Inteiro</p> | | <p>Intervalo válido:</p> | <p>0 – 2147483647</p> | | <p>Escopo:</p> | <p>Instância</p> | | <p>Definido após <a href="gg269354(v=exchg.10).md">JetCreateInstance:</a></p> | <p>Sim</p> | | <p>Definido após <a href="gg294068(v=exchg.10).md">JetInit:</a></p> | <p>Não</p> | | <p>Afeta o layout físico:</p> | <p>Não</p> | | <p>Afeta a confiabilidade:</p> | <p>Não</p> | | <p>Afeta o desempenho:</p> | <p>Sim</p> | | <p>Afeta recursos:</p> | <p>Não</p> | | <p>Disponibilidade:</p> | <p>Tudo</p> | 



*JET_paramRecovery*  
34  

Esse parâmetro é a opção mestra que controla a recuperação de falhas de uma instância. Se esse parâmetro for definido como "On", a recuperação de estilo ARIES será usada para colocar todos os bancos de dados na instância em um estado consistente no caso de um processo ou falha do computador. Se esse parâmetro for definido como "Off", todos os bancos de dados na instância serão gerenciados sem o benefício da recuperação de falhas. Ou seja, se a instância não for fechada corretamente usando [JetTerm](./jetterm-function.md) antes do processo de saída ou desligamento do computador, o conteúdo de todos os bancos de dados nessa instância será corrompido.

Desabilitar a recuperação é útil em circunstâncias especiais em que se sabe que o conteúdo de um banco de dados não é útil em caso de falha. A recuperação deve ser habilitada para todos os outros casos.


| | | <p>Valor padrão:</p> | <p>"On"</p> | | <p>Tipo:</p> | <p>String</p> | | <p>Intervalo válido:</p> | <p>0 – 259 caracteres</p> | | <p>Escopo:</p> | <p>Instância</p> | | <p>Definido após <a href="gg269354(v=exchg.10).md">JetCreateInstance:</a></p> | <p>Sim</p> | | <p>Definido após <a href="gg294068(v=exchg.10).md">JetInit:</a></p> | <p>Não</p> | | <p>Afeta o layout físico:</p> | <p>Sim</p> | | <p>Afeta a confiabilidade:</p> | <p>Sim</p> | | <p>Afeta o desempenho:</p> | <p>Sim</p> | | <p>Afeta recursos:</p> | <p>Sim</p> | | <p>Disponibilidade:</p> | <p>Tudo</p> | 



*JET_paramSystemPath*  
0  

Esse parâmetro indica o caminho do sistema de arquivos relativo ou absoluto da pasta que conterá o arquivo de ponto de verificação para a instância. O caminho deve ser encerrado com um caractere de faixa invertida, o que indica que o caminho de destino é uma pasta. O arquivo de ponto de verificação é um arquivo simples mantido por instância que se lembra do arquivo de log de transações mais antigo que deve ser replayado para colocar todos os bancos de dados nessa instância em um estado consistente após uma falha. O arquivo de ponto de verificação normalmente é chamado de EDB. CHK.

**Observação**  Se um caminho relativo for especificado, ele será relativo ao diretório de trabalho atual do processo que hospeda o aplicativo que está usando o mecanismo de banco de dados.


| | | <p>Valor padrão:</p> | <p>".\"</p> | | <p>Tipo:</p> | <p>Caminho da pasta (cadeia de caracteres)</p> | | <p>Intervalo válido:</p> | <p>0 a 246 caracteres</p> | | <p>Escopo:</p> | <p>Instância</p> | | <p>Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Sim</p> | | <p>Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>Não</p> | | <p>Afeta o layout físico:</p> | <p>Sim</p> | | <p>Afeta a confiabilidade:</p> | <p>Não</p> | | <p>Afeta o desempenho:</p> | <p>Não</p> | | <p>Afeta os recursos:</p> | <p>Não</p> | | <p>Disponibilidade:</p> | <p>Tudo</p> | 



*JET_paramWaitLogFlush*  
13 

Esse parâmetro tenta otimizar a liberação do buffer de log causado por uma confirmação durável aguardando um período de tempo especificado antes de forçar uma liberação a ocorrer na esperança de que outra transação compartilhará a liberação.

**Windows XP:**  a partir do Windows XP, esse parâmetro é obsoleto e não afeta a operação do mecanismo de banco de dados.


| | | <p>Valor padrão:</p> | <p>0</p> | | <p>Tipo:</p> | <p>Inteiro</p> | | <p>Intervalo válido:</p> | <p>0 a 2147483647</p> | | <p>Escopo:</p> | <p>Instância ou sessão</p> | | <p>Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Sim</p> | | <p>Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>Sim</p> | | <p>Afeta o layout físico:</p> | <p>Não</p> | | <p>Afeta a confiabilidade:</p> | <p>Não</p> | | <p>Afeta o desempenho:</p> | <p>Sim</p> | | <p>Afeta os recursos:</p> | <p>Não</p> | | <p>Disponibilidade:</p> | <p>Tudo</p> | 



*JET_paramLegacyFileNames*  
136  

esse parâmetro é usado para especificar os recursos de compatibilidade de nomenclatura de arquivo a serem mantidos com o Windows Server 2003 e o esquema de nomenclatura de arquivo anterior. para obter mais informações sobre os diferentes arquivos e sua nomenclatura, consulte [arquivos do mecanismo de Armazenamento extensível](./extensible-storage-engine-files.md).

o JET_bitESE98FileNames garante que a extensão de arquivo usada nos arquivos de log de transações e o arquivo de ponto de verificação sejam os mesmos usados no Windows Server 2003. observação: se estiver atualizando do Windows Server 2003, esse bit ainda não precisará ser especificado, pois o mecanismo atualizará automaticamente as extensões de arquivo se JET_paramCircularLog estiver definido como **true** ou manterá a extensão de log mais antiga se JET_paramCircularLog for **false**.

**Observação**  Para definir um bit, o valor deve primeiro ser recuperado e, em seguida, "ou" no bit de compatibilidade desejado.


| | | <p>Valor padrão:</p> | <p>JET_bitESE98FileNames</p> | | <p>Tipo:</p> | <p>JET_GRBIT (inteiro)</p> | | <p>Intervalo válido:</p> | <p>JET_bitESE98FileNames</p> | | <p>Escopo:</p> | <p>Instância</p> | | <p>Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Sim</p> | | <p>Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>Não</p> | | <p>Afeta o layout físico:</p> | <p>Sim</p> | | <p>Afeta a confiabilidade:</p> | <p>Não</p> | | <p>Afeta o desempenho:</p> | <p>Não</p> | | <p>Afeta os recursos:</p> | <p>Não</p> | | <p>Disponibilidade:</p> | <p>a partir do Windows Server 2008 e Windows Vista</p> | 



## <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>requer o Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>requer o Windows server 2008, Windows server 2003 ou Windows servidor 2000.</p> | | <p><strong>Cabeçalho</strong></p> | <p>Declarado em ESENT. h.</p> | 



## <a name="see-also"></a>Consulte Também

[arquivos do mecanismo de Armazenamento extensível](./extensible-storage-engine-files.md)  
[JetCommitTransaction](./jetcommittransaction-function.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)  
[JetTerm](./jetterm-function.md)
