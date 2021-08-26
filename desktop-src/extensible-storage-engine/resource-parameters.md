---
description: 'Saiba mais sobre: Parâmetros de recurso'
title: Parâmetros do recurso
TOCTitle: Resource Parameters
ms:assetid: 1f61845a-ffa5-4894-9fe0-a58737b3b54e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269201(v=EXCHG.10)
ms:contentKeyID: 32765504
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
ms.openlocfilehash: ac1a6aba2eda729c3e705cf5acdda837c2670564
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122472442"
---
# <a name="resource-parameters"></a>Parâmetros do recurso


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="resource-parameters"></a>Parâmetros do recurso

Este tópico contém parâmetros que são usados para recursos.

*JET_paramCachedClosedTables*  
125  

Esse parâmetro controla o número de recursos de árvore B+ armazenados em cache pela instância depois que as tabelas que elas representam foram fechadas pelo aplicativo.

Valores grandes para esse parâmetro fará com que o mecanismo de banco de dados use mais memória, mas aumentará a velocidade com a qual um grande número de tabelas pode ser aberto aleatoriamente pelo aplicativo. Isso é útil para aplicativos que têm um esquema com um número muito grande de tabelas.


| | | <p>Valor padrão:</p> | <p>64</p> | | <p>Tipo:</p> | <p>Inteiro</p> | | <p>Intervalo válido:</p> | <p>1 – 2147483647</p> | | <p>Escopo:</p> | <p>Instância</p> | | <p>Definido após <a href="gg269354(v=exchg.10).md">JetCreateInstance:</a></p> | <p>Sim</p> | | <p>Definido após <a href="gg294068(v=exchg.10).md">JetInit:</a></p> | <p>Não</p> | | <p>Afeta o layout físico:</p> | <p>Não</p> | | <p>Afeta a confiabilidade:</p> | <p>Não</p> | | <p>Afeta o desempenho:</p> | <p>Sim</p> | | <p>Afeta recursos:</p> | <p>Sim</p> | | <p>Disponibilidade:</p> | <p>Windows Vista e versões posteriores</p> | 



*JET_paramDisablePerfmon*  
107  

Esse parâmetro pode ser usado para impedir que o mecanismo de banco de dados publice dados sobre seu desempenho para Windows. Isso pode ser feito para reduzir a atividade de thread de serviço do mecanismo de banco de dados.


| | | <p>Valor padrão:</p> | <p>Falso</p> | | <p>Tipo:</p> | <p>Boolean</p> | | <p>Intervalo válido:</p> | <p>False, True</p> | | <p>Escopo:</p> | <p>Global</p> | | <p>Definido após <a href="gg269354(v=exchg.10).md">JetCreateInstance:</a></p> | <p>Não</p> | | <p>Definido após <a href="gg294068(v=exchg.10).md">JetInit:</a></p> | <p>Não</p> | | <p>Afeta o layout físico:</p> | <p>Não</p> | | <p>Afeta a confiabilidade:</p> | <p>Não</p> | | <p>Afeta o desempenho:</p> | <p>Não</p> | | <p>Afeta recursos:</p> | <p>Sim</p> | | <p>Disponibilidade:</p> | <p>Windows Vista e versões posteriores</p> | 



*JET_paramGlobalMinVerPages*  
81  

Esse parâmetro permite que os aplicativos que operam no modo de várias instâncias pré-alocam memória para páginas de versão em um pool global para emular o comportamento mais antigo. Isso é útil caso o aplicativo deseje garantir que as transações de um determinado tamanho possam ser bem-sucedidas posteriormente, mesmo que a memória se torne ruim.

**Windows 2000:**  Memória suficiente para fazer o back de todas as páginas de versão sempre é reservada no [momento do JetInit.](./jetinit-function.md)

**Windows XP:**  A partir Windows XP, isso ainda é verdadeiro quando está no modo de instância única. No entanto, a memória da página de versão é alocada dinamicamente quando está no modo de várias instâncias.


| | | <p>Valor padrão:</p> | <p>64</p> | | <p>Tipo:</p> | <p>Inteiro</p> | | <p>Intervalo válido:</p> | <p>1 – 2147483647</p> | | <p>Escopo:</p> | <p>Global</p> | | <p>Definido após <a href="gg269354(v=exchg.10).md">JetCreateInstance:</a></p> | <p>Não</p> | | <p>Definido após <a href="gg294068(v=exchg.10).md">JetInit:</a></p> | <p>Não</p> | | <p>Afeta o layout físico:</p> | <p>Não</p> | | <p>Afeta a confiabilidade:</p> | <p>Sim</p> | | <p>Afeta o desempenho:</p> | <p>Não</p> | | <p>Afeta recursos:</p> | <p>Sim</p> | | <p>Disponibilidade:</p> | <p>Windows XP e versões posteriores</p> | 



*JET_paramMaxCursors*  
8  

Esse parâmetro reserva o número solicitado de recursos de cursor para uso por uma instância. Um recurso de cursor corresponde diretamente a um [tipo JET_TABLEID](./jet-tableid.md) dados. Essa configuração afetará quantos cursores podem ser usados ao mesmo tempo. Um recurso de cursor não pode ser compartilhado por sessões diferentes, portanto, esse parâmetro deve ser definido com um valor grande o suficiente para que cada sessão possa usar tantos cursores quantos necessários.

**Windows 2000, Windows XP e Windows Server 2003:**  Valores grandes para esse parâmetro consumirão espaço de endereço e poderão aumentar o uso de memória.


| | | <p>Valor padrão:</p> | <p>1024</p> | | <p>Tipo:</p> | <p>Inteiro</p> | | <p>Intervalo válido:</p> | <p>0 a 2147483647</p> | | <p>Escopo:</p> | <p>Instância</p> | | <p>Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Sim</p> | | <p>Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>Não</p> | | <p>Afeta o layout físico:</p> | <p>Não</p> | | <p>Afeta a confiabilidade:</p> | <p>Não</p> | | <p>Afeta o desempenho:</p> | <p>Não</p> | | <p>Afeta os recursos:</p> | <p>Sim</p> | | <p>Disponibilidade:</p> | <p>Tudo</p> | 



*JET_paramMaxInstances*  
104  

Esse parâmetro controla o número máximo de instâncias que podem ser criadas em um único processo.


| | | <p>Valor padrão:</p> | <p>16</p> | | <p>Tipo:</p> | <p>Inteiro</p> | | <p>Intervalo válido:</p> | <p>1-1024</p> | | <p>Escopo:</p> | <p>Global</p> | | <p>Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Não</p> | | <p>Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>Não</p> | | <p>Afeta o layout físico:</p> | <p>Não</p> | | <p>Afeta a confiabilidade:</p> | <p>Não</p> | | <p>Afeta o desempenho:</p> | <p>Sim</p> | | <p>Afeta os recursos:</p> | <p>Sim</p> | | <p>Disponibilidade:</p> | <p>Windows XP e versões posteriores</p> | 



*JET_paramMaxOpenTables*  
6  

Esse parâmetro reserva o número solicitado de recursos da árvore B + para uso por uma instância. Essa configuração afetará quantas tabelas podem ser usadas ao mesmo tempo. Esse parâmetro precisa ser definido em relação ao esquema físico dos bancos de dados em uso pelo mecanismo de banco de dados, portanto, essa configuração não é tão simples quanto poderia ser.

Em geral, você precisará de dois recursos mais um recurso por índice secundário por tabela no uso simultâneo do aplicativo.

**Windows 2000, Windows XP e Windows Server 2003:**  Valores grandes para esse parâmetro consumirão espaço de endereço e poderão aumentar o uso de memória.


| | | <p>Valor padrão:</p> | <p>300</p> | | <p>Tipo:</p> | <p>Inteiro</p> | | <p>Intervalo válido:</p> | <p>0 a 2147483647</p> | | <p>Escopo:</p> | <p>Instância</p> | | <p>Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Sim</p> | | <p>Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>Não</p> | | <p>Afeta o layout físico:</p> | <p>Não</p> | | <p>Afeta a confiabilidade:</p> | <p>Não</p> | | <p>Afeta o desempenho:</p> | <p>Não</p> | | <p>Afeta os recursos:</p> | <p>Sim</p> | | <p>Disponibilidade:</p> | <p>Tudo</p> | 



*JET_paramMaxSessions*  
5  

Esse parâmetro reserva o número solicitado de recursos de sessão para uso por uma instância. Um recurso de sessão corresponde diretamente a um tipo de dados [JET_SESID](./jet-sesid.md) . Essa configuração afetará quantas sessões podem ser usadas ao mesmo tempo.

**Windows 2000, Windows XP e Windows Server 2003:**  Valores grandes para esse parâmetro consumirão espaço de endereço e poderão aumentar o uso de memória.


| | | <p>Valor padrão:</p> | <p>16</p> | | <p>Tipo:</p> | <p>Inteiro</p> | | <p>Intervalo válido:</p> | <p>0 a 30000</p> | | <p>Escopo:</p> | <p>Instância</p> | | <p>Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Sim</p> | | <p>Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>Não</p> | | <p>Afeta o layout físico:</p> | <p>Não</p> | | <p>Afeta a confiabilidade:</p> | <p>Não</p> | | <p>Afeta o desempenho:</p> | <p>Não</p> | | <p>Afeta os recursos:</p> | <p>Sim</p> | | <p>Disponibilidade:</p> | <p>Tudo</p> | 



*JET_paramMaxTemporaryTables*  
10  

Esse parâmetro reserva o número solicitado de recursos de tabela temporária para uso por uma instância. Essa configuração afetará quantas tabelas temporárias podem ser usadas ao mesmo tempo.

**Windows 2000, Windows XP e Windows Server 2003:**  Valores grandes para esse parâmetro consumirão espaço de endereço e poderão aumentar o uso de memória.

**Windows XP e posterior:**  Se esse parâmetro de sistema for definido como zero, nenhum banco de dados temporário será criado e qualquer atividade que exija o uso do banco de dados temporário falhará. Essa configuração pode ser útil para evitar a e/s necessária para criar o banco de dados temporário se for conhecido que ele não será usado.

**Observação**  O uso de uma tabela temporária também requer um recurso de cursor.


| | | <p>Valor padrão:</p> | <p>20</p> | | <p>Tipo:</p> | <p>Inteiro</p> | | <p>Intervalo válido:</p> | <p>0 a 2147483647</p> | | <p>Escopo:</p> | <p>Instância</p> | | <p>Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Sim</p> | | <p>Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>Não</p> | | <p>Afeta o layout físico:</p> | <p>Sim</p> | | <p>Afeta a confiabilidade:</p> | <p>Não</p> | | <p>Afeta o desempenho:</p> | <p>Não</p> | | <p>Afeta os recursos:</p> | <p>Sim</p> | | <p>Disponibilidade:</p> | <p>Tudo</p> | 



*JET_paramMaxVerPages*  
9  

Esse parâmetro reserva o número solicitado de páginas de repositório de versão para uso por uma instância. O repositório de versão mantém um registro ao vivo de todas as diferentes versões de cada registro ou entrada de índice no banco de dados que pode ser visto por todas as transações ativas. Essas versões são usadas para dar suporte ao controle de simultaneidade de várias versões em uso pelo mecanismo de banco de dados para dar suporte a transações usando o isolamento de instantâneo. Essa configuração afetará quantas atualizações podem ser mantidas na memória por vez. Isso, por sua vez, afetará o número máximo de atualizações que uma única transação pode executar, a duração máxima que uma transação pode ser mantida aberta, a carga simultânea máxima de transações de atualização no sistema ou uma combinação delas.

Cada página de repositório de versão conforme configurada por esse parâmetro é 16 KB em tamanho em computadores de 32 bits e 32 KB em computadores de 64 bits.

**Windows Vista e posterior:**  O tamanho da página de repositório de versão pode ser lido e alterado via JET_paramVerPageSize.

**Windows 2000, Windows XP e Windows Server 2003:**  Valores grandes para esse parâmetro consumirão espaço de endereço e poderão aumentar o uso de memória.

**Observação**  Isso é, de longe, o recurso mais comum a ser esgotado pelo mecanismo de banco de dados. A atenção deve ser paga à configuração do parâmetro System e à carga transacional do aplicativo para evitar esgotar esse recurso em operação normal. Quando esse recurso estiver esgotado, as atualizações para o banco de dados serão rejeitadas com JET_errVersionStoreOutOfMemory. Para liberar alguns desses recursos, a transação pendente mais antiga deve ser anulada.


| | | <p>Valor padrão:</p> | <p>64</p> | | <p>Tipo:</p> | <p>Inteiro</p> | | <p>Intervalo válido:</p> | <p>1 a 2147483647</p> | | <p>Escopo:</p> | <p>Instância</p> | | <p>Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Sim</p> | | <p>Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>Não</p> | | <p>Afeta o layout físico:</p> | <p>Não</p> | | <p>Afeta a confiabilidade:</p> | <p>Sim</p> | | <p>Afeta o desempenho:</p> | <p>Não</p> | | <p>Afeta os recursos:</p> | <p>Sim</p> | | <p>Disponibilidade:</p> | <p>Tudo</p> | 



*JET_paramPageHintCacheSize*  
101  

Esse parâmetro controla o tamanho de um cache especial usado para acelerar a pesquisa de ponteiros de página filho da árvore B + no cache de página do banco de dados. O tamanho do cache está em bytes.


| | | <p>Valor padrão:</p> | <p>262144</p> | | <p>Tipo:</p> | <p>Inteiro</p> | | <p>Intervalo válido:</p> | <p>0 a 2147483647</p> | | <p>Escopo:</p> | <p>Global</p> | | <p>Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Sim</p> | | <p>Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>Sim</p> | | <p>Afeta o layout físico:</p> | <p>Não</p> | | <p>Afeta a confiabilidade:</p> | <p>Não</p> | | <p>Afeta o desempenho:</p> | <p>Sim</p> | | <p>Afeta os recursos:</p> | <p>Sim</p> | | <p>Disponibilidade:</p> | <p>Windows XP e versões posteriores</p> | 



*JET_paramPreferredMaxOpenTables*  
7  

Esse parâmetro tenta manter o número de recursos da árvore B em uso abaixo do limite especificado.

Se esse parâmetro for definido como zero, ele usará como padrão 100% de **JET_paramMaxOpenTables**.

**Windows Vista e posterior:**  Esse parâmetro é obsoleto e não afeta a operação do mecanismo de banco de dados. Os aplicativos devem usar JET_paramMaxCachedClosedTables em vez disso.


| | | <p>Valor padrão:</p> | <p>0 (100% de <strong>JET_paramMaxOpenTables</strong>)</p> | | <p>Tipo:</p> | <p>Inteiro</p> | | <p>Intervalo válido:</p> | <p>0 a 2147483647</p> | | <p>Escopo:</p> | <p>Instância</p> | | <p>Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Sim</p> | | <p>Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>Não</p> | | <p>Afeta o layout físico:</p> | <p>Não</p> | | <p>Afeta a confiabilidade:</p> | <p>Não</p> | | <p>Afeta o desempenho:</p> | <p>Sim</p> | | <p>Afeta os recursos:</p> | <p>Sim</p> | | <p>Disponibilidade:</p> | <p>Tudo</p> | 



*JET_paramPreferredVerPages*  
63  

Esse parâmetro representa um limite relativo a **JET_paramMaxVerPages** que controla o uso discricionário de páginas de versão pelo mecanismo de banco de dados. Se o tamanho do repositório de versão exceder esse limite, todas as informações usadas apenas para tarefas em segundo plano opcionais, como a recuperação de espaço excluído no banco de dados, serão sacrificadas para preservar espaço para informações transacionais.

**Windows 2000, Windows XP e Windows Server 2003:**  Definir esse parâmetro como zero definiria o limite como 90% de **JET_paramMaxVerPages**.

**Windows Vista e posterior:**  Não há mais suporte para isso e o valor padrão desse parâmetro foi alterado para esclarecer seu comportamento.

Cada página de repositório de versão conforme configurada por esse parâmetro é 16 KB em tamanho em computadores de 32 bits e 32 KB em computadores de 64 bits.

**Windows Vista e posterior:**  O tamanho da página de repositório de versão pode ser lido e alterado via JET_paramVerPageSize.

**Observação**  Se o mecanismo de banco de dados operar acima desse limite com muita frequência, é possível que o banco de dados diminua no desempenho. Isso acontece porque os processos em segundo plano que limpam o banco de dados não podem funcionar sem as informações opcionais que são geradas nesse cenário. A desfragmentação online ou offline irá neutralizar esse efeito.


| | | <p>Valor padrão:</p> | <p><strong>Windows 2000, Windows XP e Windows Server 2003:</strong> 0 (90% do JET_paramMaxVerPages)</p><p><strong>Windows Vista:</strong> 58</p> | | <p>Tipo:</p> | <p>Inteiro</p> | | <p>Intervalo válido:</p> | <p>1 a 2147483647</p> | | <p>Escopo:</p> | <p>Instância</p> | | <p>Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Sim</p> | | <p>Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>Sim</p> | | <p>Afeta o layout físico:</p> | <p>Não</p> | | <p>Afeta a confiabilidade:</p> | <p>Sim</p> | | <p>Afeta o desempenho:</p> | <p>Sim</p> | | <p>Afeta os recursos:</p> | <p>Sim</p> | | <p>Disponibilidade:</p> | <p>Tudo</p> | 



*JET_paramVerPageSize*  
128  

Esse parâmetro controla o tamanho das páginas de repositório de versão usadas pelo mecanismo de banco de dados para manter informações transacionais. O valor desse parâmetro é o tamanho da unidade para todos os outros parâmetros do sistema que estão em termos de páginas de versão (por exemplo, JET_paramMaxVerPages).

O mecanismo de banco de dados pode optar por usar um tamanho de página de repositório de versão maior do que o solicitado.


| | | <p>Valor padrão:</p> | <p>16384</p> | | <p>Tipo:</p> | <p>Inteiro</p> | | <p>Intervalo válido:</p> | <p>1024, 2048, 4096, 8192, 16384, 32768, 65536</p> | | <p>Escopo:</p> | <p>Global</p> | | <p>Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Não</p> | | <p>Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>Não</p> | | <p>Afeta o layout físico:</p> | <p>Não</p> | | <p>Afeta a confiabilidade:</p> | <p>Não</p> | | <p>Afeta o desempenho:</p> | <p>Não</p> | | <p>Afeta os recursos:</p> | <p>Sim</p> | | <p>Disponibilidade:</p> | <p>Windows Vista e posterior</p> | 



*JET_paramVersionStoreTaskQueueMax*  
105  

Esse parâmetro controla o número de itens de trabalho de limpeza em segundo plano que podem ser enfileirados no pool de threads do mecanismo de banco de dados a qualquer momento.


| | | <p>Valor padrão:</p> | <p>32</p> | | <p>Tipo:</p> | <p>Inteiro</p> | | <p>Intervalo válido:</p> | <p><strong>Windows XP e Windows Server 2003:</strong> 1 a 63</p><p><strong>Windows Vista:</strong> 1 a 127</p> | | <p>Escopo:</p> | <p>Instância</p> | | <p>Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Sim</p> | | <p>Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p><strong>Windows XP e Windows Server 2003:</strong>  Não</p><p><strong>Windows Vista:</strong>  Ok</p> | | <p>Afeta o layout físico:</p> | <p>Não</p> | | <p>Afeta a confiabilidade:</p> | <p>Não</p> | | <p>Afeta o desempenho:</p> | <p>Sim</p> | | <p>Afeta recursos:</p> | <p>Sim</p> | | <p>Disponibilidade:</p> | <p>Windows XP e versões posteriores</p> | 



### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requer Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>Requer Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</p> | | <p><strong>Cabeçalho</strong></p> | <p>Declarado em Esent.h.</p> | 



### <a name="see-also"></a>Consulte Também

[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)
