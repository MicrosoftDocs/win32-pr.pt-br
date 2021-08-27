---
description: 'Saiba mais sobre: parâmetros de banco de dados'
title: Parâmetros de Banco de Dados
TOCTitle: Database Parameters
ms:assetid: 8fb68748-8718-4393-9fd6-0d9adaa34844
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269337(v=EXCHG.10)
ms:contentKeyID: 32765626
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
ms.openlocfilehash: cdccfca7e7a68ea997c9b564939f89799634e344
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122471832"
---
# <a name="database-parameters"></a>Parâmetros de Banco de Dados


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="database-parameters"></a>Parâmetros de Banco de Dados

Este tópico contém parâmetros que são usados para o banco de dados.

*JET_paramCheckFormatWhenOpenFail*  
44  

Esse parâmetro, quando definido, fará com que o [JetInit](./jetinit-function.md) retorne um erro especial quando um banco de dados ou log de transações de uma versão anterior do mecanismo de banco de dados for aberto. Esses erros são:


| <p>Erro do</p> | <p>Descrição</p> | 
|--------------|--------------------|
| <p>JET_errDatabase200Format</p> | <p>o banco de dados e/ou os arquivos de log de transações foram criados com o mecanismo de banco de dados no Windows NT 3,51.</p> | 
| <p>JET_errDatabase400Format</p> | <p>o banco de dados e/ou os arquivos de log de transações foram criados com o mecanismo de banco de dados em uma versão de teste anterior ao Windows NT Server 4,0.</p> | 
| <p>JET_errDatabase500Format</p> | <p>o banco de dados e/ou os arquivos de log de transações foram criados com o mecanismo de banco de dados no Windows NT Server 4,0.</p> | 



**Windows Vista:**  para o Windows Vista e posterior, esse parâmetro é obsoleto e não afeta a operação do mecanismo de banco de dados.


| | | <p>Valor padrão:</p> | <p>Verdadeiro</p> | | <p>Tipo:</p> | <p>Boolean</p> | | <p>Intervalo válido:</p> | <p>Falso, verdadeiro</p> | | <p>Escopo:</p> | <p>Instância</p> | | <p>Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Sim</p> | | <p>Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>Não</p> | | <p>Afeta o layout físico:</p> | <p>Não</p> | | <p>Afeta a confiabilidade:</p> | <p>Não</p> | | <p>Afeta o desempenho:</p> | <p>Não</p> | | <p>Afeta os recursos:</p> | <p>Não</p> | | <p>Disponibilidade:</p> | <p>Tudo</p> | 



*JET_paramDatabasePageSize*  
64  

Esse parâmetro configura o tamanho da página para o banco de dados. O tamanho da página é a menor unidade de alocação de espaço possível para um arquivo de banco de dados. O tamanho da página do banco de dados também é muito importante porque ele define o limite superior do tamanho de um registro individual no banco de dados.

**Observação** Há suporte para apenas um tamanho de página de banco de dados por processo no momento. Isso significa que, se você estiver em um único processo que contém diferentes aplicativos que usam o mecanismo de banco de dados, todos eles deverão concordar em um tamanho de página de banco de dados.


| | | <p>Valor padrão:</p> | <p>4096</p> | | <p>Tipo:</p> | <p>Inteiro</p> | | <p>Intervalo válido:</p> | <p>2048, 4096, 8192</p> | | <p>Escopo:</p> | <p>Global</p> | | <p>Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Não</p> | | <p>Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>Não</p> | | <p>Afeta o layout físico:</p> | <p>Sim</p> | | <p>Afeta a confiabilidade:</p> | <p>Não</p> | | <p>Afeta o desempenho:</p> | <p>Sim</p> | | <p>Afeta os recursos:</p> | <p>Sim</p> | | <p>Disponibilidade:</p> | <p>Tudo</p> | 



*JET_paramDbExtensionSize*  
18  

Esse parâmetro controla a quantidade de espaço que é adicionada a um arquivo de banco de dados cada vez que ele precisa aumentar para acomodar mais informações. O tamanho está em páginas de banco de dados.


| | | <p>Valor padrão:</p> | <p>256</p> | | <p>Tipo:</p> | <p>Inteiro</p> | | <p>Intervalo válido:</p> | <p>1 a 2147483647</p> | | <p>Escopo:</p> | <p>Instância</p> | | <p>Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Sim</p> | | <p>Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>Não</p><p><strong>Windows Vista:</strong>  para Windows Vista e posterior: sim</p> | | <p>Afeta o layout físico:</p> | <p>Não</p> | | <p>Afeta a confiabilidade:</p> | <p>Não</p> | | <p>Afeta o desempenho:</p> | <p>Sim</p> | | <p>Afeta os recursos:</p> | <p>Sim</p> | | <p>Disponibilidade:</p> | <p>Tudo</p> | 



*JET_paramEnableIndexChecking*  
45  

Quando esse parâmetro for true, todos os bancos de dados serão verificados em [JetAttachDatabase](./jetattachdatabase-function.md) tempo para índices em colunas de chave Unicode que foram criadas usando uma versão mais antiga da biblioteca NLS no sistema operacional. Isso deve ser feito porque o mecanismo de banco de dados persiste as chaves de classificação geradas por [LCMapStringW](/windows/win32/api/winnls/nf-winnls-lcmapstringa) e o valor dessas chaves de classificação muda de versão para versão.

Se for detectado que um índice primário está nesse estado, [JetAttachDatabase](./jetattachdatabase-function.md) sempre falhará com JET_errPrimaryIndexCorrupted.

Se algum índice secundário for detectado como nesse estado, haverá dois resultados possíveis. Se JET_bitDbDeleteCorruptIndexes foi passado para [JetAttachDatabase,](./jetattachdatabase-function.md) esses índices serão excluídos e JET_wrnCorruptIndexDeleted serão retornados de [JetAttachDatabase](./jetattachdatabase-function.md). Esses índices precisarão ser recriados pelo seu aplicativo. Se JET_bitDbDeleteCorruptIndexes foi passado para [JetAttachDatabase,](./jetattachdatabase-function.md) a chamada falhará com JET_errSecondaryIndexCorrupted.

**Observação** É altamente recomendável que esse parâmetro seja definido como True pelo seu aplicativo.

**Observação** É altamente recomendável que os aplicativos evitem o uso de colunas de chave Unicode em seus índices de chave primária (clustered).


| | | <p>Valor padrão:</p> | <p>Falso</p> | | <p>Tipo:</p> | <p>Boolean</p> | | <p>Intervalo válido:</p> | <p>False, True</p> | | <p>Escopo:</p> | <p>Global</p><p><strong>Windows Vista:</strong>  Para Windows Vista e posterior: Instância</p> | | <p>Definido após <a href="gg269354(v=exchg.10).md">JetCreateInstance:</a></p> | <p>Não</p> | | <p>Definido após <a href="gg294068(v=exchg.10).md">JetInit:</a></p> | <p>Não</p> | | <p>Afeta o layout físico:</p> | <p>Não</p> | | <p>Afeta a confiabilidade:</p> | <p>Sim</p> | | <p>Afeta o desempenho:</p> | <p>Não</p> | | <p>Afeta recursos:</p> | <p>Não</p> | | <p>Disponibilidade:</p> | <p>Tudo</p> | 



*JET_paramEnableIndexCleanup*  
54  

Quando esse parâmetro é definido como true, o mecanismo de banco de dados pode limpar automaticamente os índices em colunas de chave Unicode no momento [do JetInit,](./jetinit-function.md) conforme necessário, para evitar alterações de formato de banco de dados causadas por alterações na biblioteca NLS no Windows. Essas alterações são feitas rotineiramente na biblioteca NLS para adicionar suporte a novos idiomas, para adicionar caracteres ausentes a um idioma, para adicionar uma ordem de collação a um idioma ou para corrigir bugs na ordem de collação de um idioma. Essas alterações afetam as chaves de classificação produzidas pelo [LCMapStringW,](/windows/win32/api/winnls/nf-winnls-lcmapstringa) que são persistentes pelo mecanismo de banco de dados como componentes de chaves de índice.

É importante perceber que é possível que as alterações no índice sejam tão ótimas que uma limpeza incremental não seja possível. Nesse caso, o índice será tratado conforme prescrito **pelo JET_paramEnableIndexChecking**.

**Observação** É altamente recomendável que esse parâmetro e **JET_paramEnableIndexChecking** definido como **True** pelo seu aplicativo.


| | | <p>Valor padrão:</p> | <p>Verdadeiro</p> | | <p>Tipo:</p> | <p>Boolean</p> | | <p>Intervalo válido:</p> | <p>False, True</p> | | <p>Escopo:</p> | <p>Instância</p> | | <p>Definido após <a href="gg269354(v=exchg.10).md">JetCreateInstance:</a></p> | <p>Sim</p> | | <p>Definido após <a href="gg294068(v=exchg.10).md">JetInit:</a></p> | <p>Não</p><p><strong>Windows Vista:</strong>  Para Windows Vista e posterior: Sim</p> | | <p>Afeta o layout físico:</p> | <p>Não</p> | | <p>Afeta a confiabilidade:</p> | <p>Não</p> | | <p>Afeta o desempenho:</p> | <p>Não</p> | | <p>Afeta recursos:</p> | <p>Não</p> | | <p>Disponibilidade:</p> | <p>Windows Server 2003 e versões posteriores</p> | 



*JET_paramOneDatabasePerSession*  
102  

Quando esse parâmetro for true, somente um banco de dados poderá ser aberto usando [JetOpenDatabase](./jetopendatabase-function.md) por uma determinada sessão ao mesmo tempo. O banco de dados temporário é excluído dessa restrição.

**Windows XP e Windows Server 2003:**  Esse parâmetro é escrito somente no Windows XP e Windows Server 2003.

**Windows Vista:**  Esse parâmetro se comporta normalmente a partir Windows Vista.

**Observação**  Esse parâmetro é somente gravação.


| | | <p>Valor padrão:</p> | <p>Falso</p> | | <p>Tipo:</p> | <p>Boolean</p> | | <p>Intervalo válido:</p> | <p>False, True</p> | | <p>Escopo:</p> | <p>Global</p> | | <p>Definido após <a href="gg269354(v=exchg.10).md">JetCreateInstance:</a></p> | <p>Não</p><p><strong>Windows Vista:</strong>  Para Windows Vista e posterior: Sim</p> | | <p>Definido após <a href="gg294068(v=exchg.10).md">JetInit:</a></p> | <p>Não</p> | | <p>Afeta o layout físico:</p> | <p>Não</p> | | <p>Afeta a confiabilidade:</p> | <p>Não</p> | | <p>Afeta o desempenho:</p> | <p>Não</p> | | <p>Afeta recursos:</p> | <p>Não</p> | | <p>Disponibilidade:</p> | <p>Windows XP e versões posteriores</p> | 



*JET_paramEnableOnlineDefrag*  
35  

Esse parâmetro controla o comportamento da desfragmentação online quando iniciado usando [JetDefragment](./jetdefragment-function.md). Consulte [JetDefragment para](./jetdefragment-function.md) obter mais informações.

Windows 2000: no Windows 2000, esse parâmetro era um boolano simples que poria a desfragmentação online quando iniciada pelo [JetDefragment](./jetdefragment-function.md). Quando definido como **TRUE,** a desfragmentação online será executada nos registros de cada tabela no banco de dados.

**Windows XP:**  No Windows XP e versões posteriores, esse parâmetro pode ser definido como uma ou mais das seguintes opções:


| <p>Opção</p> | <p>Descrição</p> | 
|---------------|--------------------|
| <p>JET_OnlineDefragDisable</p> | <p>Não execute a desfragmentação online. esse é o equivalente binário à configuração Windows 2000 de False para esse parâmetro.</p> | 
| <p>JET_OnlineDefragAllOBSOLETE</p> | <p>Execute a desfragmentação online completa. esse é o equivalente binário à configuração Windows 2000 de True para esse parâmetro.</p> | 
| <p>JET_OnlineDefragDatabases</p> | <p>Execute a desfragmentação online dos registros de cada tabela no banco de dados.</p> | 
| <p>JET_OnlineDefragSpaceTrees</p> | <p>Execute a desfragmentação online das árvores de espaço de cada tabela no banco de dados.</p> | 
| <p>JET_OnlineDefragStreamingFiles</p> | <p>esse parâmetro é usado para dar suporte à infraestrutura de Exchange da Microsoft e não se destina a ser usado em seu aplicativo.</p> | 
| <p>JET_OnlineDefragAll</p> | <p>Execute a desfragmentação online completa. esse é o equivalente conceitual para a configuração Windows 2000 de True para esse parâmetro.</p> | 




| | | <p>Valor padrão:</p> | <p><strong>Windows 2000:</strong>  True</p><p><strong>Windows xp: para o Windows xp e posterior:</strong> JET_OnlineDefragAll</p> | | <p>Tipo:</p> | <p><strong>Windows 2000:</strong>  Boolean</p><p><strong>Windows XP e posterior:</strong>  JET_GRBIT (inteiro)</p> | | <p>Intervalo válido:</p> | <p><strong>Windows 2000:</strong>  Falso, verdadeiro</p><p><strong>Windows XP e posterior:</strong> 0 – JET_OnlineDefragAll</p> | | <p>Escopo:</p> | <p>Instância</p> | | <p>Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Sim</p> | | <p>Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>Sim</p> | | <p>Afeta o layout físico:</p> | <p>Não</p> | | <p>Afeta a confiabilidade:</p> | <p>Sim</p> | | <p>Afeta o desempenho:</p> | <p>Sim</p> | | <p>Afeta os recursos:</p> | <p>Não</p> | | <p>Disponibilidade:</p> | <p>Tudo</p> | 



*JET_paramPageFragment*  
20  

Esse parâmetro é o limite que o mecanismo de banco de dados usa para controlar a fragmentação de espaço livre. O tamanho está em páginas de banco de dados.


| | | <p>Valor padrão:</p> | <p>8</p> | | <p>Tipo:</p> | <p>Inteiro</p> | | <p>Intervalo válido:</p> | <p>0 a 2147483647</p> | | <p>Escopo:</p> | <p>Instância</p> | | <p>Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Sim</p> | | <p>Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>Não</p> | | <p>Afeta o layout físico:</p> | <p>Não</p> | | <p>Afeta a confiabilidade:</p> | <p>Não</p> | | <p>Afeta o desempenho:</p> | <p>Sim</p> | | <p>Afeta os recursos:</p> | <p>Sim</p> | | <p>Disponibilidade:</p> | <p>Tudo</p> | 



*JET_paramRecordUpgradeDirtyLevel*  
78

Esse parâmetro controla a agressividade com que o Gerenciador de cache de página de banco de dados gravará uma página de banco de dados que passou por uma conversão de formato in-loco. essas conversões de formato ocorrem imediatamente conforme as páginas são carregadas de um banco de dados criado com o mecanismo de banco de dados Windows 2000, mas usadas por uma versão Windows XP ou posterior do mecanismo de banco de dados.


| | | <p>Valor padrão:</p> | <p>1</p> | | <p>Tipo:</p> | <p>Inteiro</p> | | <p>Intervalo válido:</p> | <p>0-3</p> | | <p>Escopo:</p> | <p>Global</p> | | <p>Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Sim</p> | | <p>Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>Sim</p> | | <p>Afeta o layout físico:</p> | <p>Sim</p> | | <p>Afeta a confiabilidade:</p> | <p>Não</p> | | <p>Afeta o desempenho:</p> | <p>Sim</p> | | <p>Afeta os recursos:</p> | <p>Não</p> | | <p>Disponibilidade:</p> | <p>Windows XP e versões posteriores</p> | 



*JET_paramWaypointLatency*  
153  

A latência (em logs) por trás da dica/log confirmado mais alto para adiar liberações de página do banco de dados. A habilitação dessa latência pode permitir a recuperação do banco de dados no caso de perda catastrófica do arquivo de log mais recente. Consulte JET_bitReplayIgnoreLostLogs.


| | | <p>Valor padrão:</p> | <p>0</p> | | <p>Tipo:</p> | <p>Inteiro</p> | | <p>Intervalo válido:</p> | <p>0-1023</p> | | <p>Escopo:</p> | <p>Instância</p> | | <p>Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Sim</p> | | <p>Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>Não</p> | | <p>Afeta o layout físico:</p> | <p>Não</p> | | <p>Afeta a confiabilidade:</p> | <p>Sim</p> | | <p>Afeta o desempenho:</p> | <p>Sim</p> | | <p>Afeta os recursos:</p> | <p>Não</p> | | <p>Disponibilidade:</p> | <p>Windows 7</p> | 



*JET_paramDefragmentSequentialBTrees*  
160  

Ativar/desativar a desfragmentação de árvore B sequencial automática.


| | | <p>Valor padrão:</p> | <p>1</p> | | <p>Tipo:</p> | <p>Boolean</p> | | <p>Intervalo válido:</p> | <p>0-1</p> | | <p>Escopo:</p> | <p>Instância</p> | | <p>Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Sim</p> | | <p>Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>Não</p> | | <p>Afeta o layout físico:</p> | <p>Sim</p> | | <p>Afeta a confiabilidade:</p> | <p>Não</p> | | <p>Afeta o desempenho:</p> | <p>Sim</p> | | <p>Afeta os recursos:</p> | <p>Não</p> | | <p>Disponibilidade:</p> | <p>Windows 7</p> | 



*JET_paramDefragmentSequentialBTreesDensityCheckFrequency*  
161  

Determina com que frequência a densidade da árvore B é verificada.


| | | <p>Valor padrão:</p> | <p>10</p> | | <p>Tipo:</p> | <p>Inteiro</p> | | <p>Intervalo válido:</p> | <p>0-inteiro máx.</p> | | <p>Escopo:</p> | <p>Instância</p> | | <p>Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Sim</p> | | <p>Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>Não</p> | | <p>Afeta o layout físico:</p> | <p>Sim</p> | | <p>Afeta a confiabilidade:</p> | <p>Não</p> | | <p>Afeta o desempenho:</p> | <p>Sim</p> | | <p>Afeta os recursos:</p> | <p>Não</p> | | <p>Disponibilidade:</p> | <p>Windows 7</p> | 



*JET_paramIOThrottlingTimeQuanta*  
162  

Tempo máximo, em milissegundos, que o mecanismo de limitação de e/s fornece uma tarefa a ser executada para que ela seja considerada ' concluída '.


| | | <p>Valor padrão:</p> | <p>125</p> | | <p>Tipo:</p> | <p>Inteiro</p> | | <p>Intervalo válido:</p> | <p>0-10000</p> | | <p>Escopo:</p> | <p>Global</p> | | <p>Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Sim</p> | | <p>Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>Não</p> | | <p>Afeta o layout físico:</p> | <p>Não</p> | | <p>Afeta a confiabilidade:</p> | <p>Não</p> | | <p>Afeta o desempenho:</p> | <p>Sim</p> | | <p>Afeta os recursos:</p> | <p>Não</p> | | <p>Disponibilidade:</p> | <p>Windows 7</p> | 



### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>requer o Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>requer o Windows server 2008, Windows server 2003 ou Windows servidor 2000.</p> | | <p><strong>Cabeçalho</strong></p> | <p>Declarado em Esent.h.</p> | 



### <a name="see-also"></a>Consulte Também

[JetAttachDatabase](./jetattachdatabase-function.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetDefragment](./jetdefragment-function.md)  
[JetInit](./jetinit-function.md)
