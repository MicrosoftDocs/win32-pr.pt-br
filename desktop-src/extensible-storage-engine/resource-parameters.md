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
ms.openlocfilehash: 87c8c93e70950aca360e4aa9bad62b8280611c6713156dec80e4d11414f346d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118978596"
---
# <a name="resource-parameters"></a>Parâmetros do recurso


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="resource-parameters"></a>Parâmetros do recurso

Este tópico contém parâmetros que são usados para recursos.

*JET_paramCachedClosedTables*  
125  

Esse parâmetro controla o número de recursos de árvore B+ armazenados em cache pela instância depois que as tabelas que elas representam foram fechadas pelo aplicativo.

Valores grandes para esse parâmetro fará com que o mecanismo de banco de dados use mais memória, mas aumentará a velocidade com a qual um grande número de tabelas pode ser aberto aleatoriamente pelo aplicativo. Isso é útil para aplicativos que têm um esquema com um número muito grande de tabelas.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valor padrão:</p></td>
<td><p>64</p></td>
</tr>
<tr class="even">
<td><p>Tipo:</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Intervalo válido:</p></td>
<td><p>1 – 2147483647</p></td>
</tr>
<tr class="even">
<td><p>Escopo:</p></td>
<td><p>Instância</p></td>
</tr>
<tr class="odd">
<td><p>Definido após <a href="gg269354(v=exchg.10).md">JetCreateInstance:</a></p></td>
<td><p>Sim</p></td>
</tr>
<tr class="even">
<td><p>Definido após <a href="gg294068(v=exchg.10).md">JetInit:</a></p></td>
<td><p>Não</p></td>
</tr>
<tr class="odd">
<td><p>Afeta o layout físico:</p></td>
<td><p>Não</p></td>
</tr>
<tr class="even">
<td><p>Afeta a confiabilidade:</p></td>
<td><p>Não</p></td>
</tr>
<tr class="odd">
<td><p>Afeta o desempenho:</p></td>
<td><p>Sim</p></td>
</tr>
<tr class="even">
<td><p>Afeta recursos:</p></td>
<td><p>Sim</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilidade:</p></td>
<td><p>Windows Vista e versões posteriores</p></td>
</tr>
</tbody>
</table>


*JET_paramDisablePerfmon*  
107  

Esse parâmetro pode ser usado para impedir que o mecanismo de banco de dados publice dados sobre seu desempenho para Windows. Isso pode ser feito para reduzir a atividade de thread de serviço do mecanismo de banco de dados.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valor padrão:</p></td>
<td><p>Falso</p></td>
</tr>
<tr class="even">
<td><p>Tipo:</p></td>
<td><p>Boolean</p></td>
</tr>
<tr class="odd">
<td><p>Intervalo válido:</p></td>
<td><p>False, True</p></td>
</tr>
<tr class="even">
<td><p>Escopo:</p></td>
<td><p>Global</p></td>
</tr>
<tr class="odd">
<td><p>Definido após <a href="gg269354(v=exchg.10).md">JetCreateInstance:</a></p></td>
<td><p>Não</p></td>
</tr>
<tr class="even">
<td><p>Definido após <a href="gg294068(v=exchg.10).md">JetInit:</a></p></td>
<td><p>Não</p></td>
</tr>
<tr class="odd">
<td><p>Afeta o layout físico:</p></td>
<td><p>Não</p></td>
</tr>
<tr class="even">
<td><p>Afeta a confiabilidade:</p></td>
<td><p>Não</p></td>
</tr>
<tr class="odd">
<td><p>Afeta o desempenho:</p></td>
<td><p>Não</p></td>
</tr>
<tr class="even">
<td><p>Afeta recursos:</p></td>
<td><p>Sim</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilidade:</p></td>
<td><p>Windows Vista e versões posteriores</p></td>
</tr>
</tbody>
</table>


*JET_paramGlobalMinVerPages*  
81  

Esse parâmetro permite que os aplicativos que operam no modo de várias instâncias pré-alocam memória para páginas de versão em um pool global para emular o comportamento mais antigo. Isso é útil caso o aplicativo deseje garantir que as transações de um determinado tamanho possam ser bem-sucedidas posteriormente, mesmo que a memória se torne ruim.

**Windows 2000:**  Memória suficiente para fazer o back de todas as páginas de versão sempre é reservada no [momento do JetInit.](./jetinit-function.md)

**Windows XP:**  A partir Windows XP, isso ainda é verdadeiro quando está no modo de instância única. No entanto, a memória da página de versão é alocada dinamicamente quando está no modo de várias instâncias.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valor padrão:</p></td>
<td><p>64</p></td>
</tr>
<tr class="even">
<td><p>Tipo:</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Intervalo válido:</p></td>
<td><p>1 – 2147483647</p></td>
</tr>
<tr class="even">
<td><p>Escopo:</p></td>
<td><p>Global</p></td>
</tr>
<tr class="odd">
<td><p>Definido após <a href="gg269354(v=exchg.10).md">JetCreateInstance:</a></p></td>
<td><p>Não</p></td>
</tr>
<tr class="even">
<td><p>Definido após <a href="gg294068(v=exchg.10).md">JetInit:</a></p></td>
<td><p>Não</p></td>
</tr>
<tr class="odd">
<td><p>Afeta o layout físico:</p></td>
<td><p>Não</p></td>
</tr>
<tr class="even">
<td><p>Afeta a confiabilidade:</p></td>
<td><p>Sim</p></td>
</tr>
<tr class="odd">
<td><p>Afeta o desempenho:</p></td>
<td><p>Não</p></td>
</tr>
<tr class="even">
<td><p>Afeta recursos:</p></td>
<td><p>Sim</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilidade:</p></td>
<td><p>Windows XP e versões posteriores</p></td>
</tr>
</tbody>
</table>


*JET_paramMaxCursors*  
8  

Esse parâmetro reserva o número solicitado de recursos de cursor para uso por uma instância. Um recurso de cursor corresponde diretamente a um [tipo JET_TABLEID](./jet-tableid.md) dados. Essa configuração afetará quantos cursores podem ser usados ao mesmo tempo. Um recurso de cursor não pode ser compartilhado por sessões diferentes, portanto, esse parâmetro deve ser definido com um valor grande o suficiente para que cada sessão possa usar tantos cursores quantos necessários.

**Windows 2000, Windows XP e Windows Server 2003:**  Valores grandes para esse parâmetro consumirão espaço de endereço e poderão aumentar o uso de memória.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valor padrão:</p></td>
<td><p>1024</p></td>
</tr>
<tr class="even">
<td><p>Tipo:</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Intervalo válido:</p></td>
<td><p>0 – 2147483647</p></td>
</tr>
<tr class="even">
<td><p>Escopo:</p></td>
<td><p>Instância</p></td>
</tr>
<tr class="odd">
<td><p>Definido após <a href="gg269354(v=exchg.10).md">JetCreateInstance:</a></p></td>
<td><p>Sim</p></td>
</tr>
<tr class="even">
<td><p>Definido após <a href="gg294068(v=exchg.10).md">JetInit:</a></p></td>
<td><p>Não</p></td>
</tr>
<tr class="odd">
<td><p>Afeta o layout físico:</p></td>
<td><p>Não</p></td>
</tr>
<tr class="even">
<td><p>Afeta a confiabilidade:</p></td>
<td><p>Não</p></td>
</tr>
<tr class="odd">
<td><p>Afeta o desempenho:</p></td>
<td><p>Não</p></td>
</tr>
<tr class="even">
<td><p>Afeta recursos:</p></td>
<td><p>Sim</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilidade:</p></td>
<td><p>Tudo</p></td>
</tr>
</tbody>
</table>


*JET_paramMaxInstances*  
104  

Esse parâmetro controla o número máximo de instâncias que podem ser criadas em um único processo.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valor padrão:</p></td>
<td><p>16</p></td>
</tr>
<tr class="even">
<td><p>Tipo:</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Intervalo válido:</p></td>
<td><p>1-1024</p></td>
</tr>
<tr class="even">
<td><p>Escopo:</p></td>
<td><p>Global</p></td>
</tr>
<tr class="odd">
<td><p>Definido após <a href="gg269354(v=exchg.10).md">JetCreateInstance:</a></p></td>
<td><p>Não</p></td>
</tr>
<tr class="even">
<td><p>Definido após <a href="gg294068(v=exchg.10).md">JetInit:</a></p></td>
<td><p>Não</p></td>
</tr>
<tr class="odd">
<td><p>Afeta o layout físico:</p></td>
<td><p>Não</p></td>
</tr>
<tr class="even">
<td><p>Afeta a confiabilidade:</p></td>
<td><p>Não</p></td>
</tr>
<tr class="odd">
<td><p>Afeta o desempenho:</p></td>
<td><p>Sim</p></td>
</tr>
<tr class="even">
<td><p>Afeta recursos:</p></td>
<td><p>Sim</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilidade:</p></td>
<td><p>Windows XP e versões posteriores</p></td>
</tr>
</tbody>
</table>


*JET_paramMaxOpenTables*  
6  

Esse parâmetro reserva o número solicitado de recursos de árvore B+ para uso por uma instância. Essa configuração afetará quantas tabelas podem ser usadas ao mesmo tempo. Esse parâmetro precisa ser definido em relação ao esquema físico dos bancos de dados em uso pelo mecanismo de banco de dados, portanto, essa configuração não é tão simples quanto poderia ser.

Em geral, você precisará de dois recursos mais um recurso por índice secundário por tabela em uso simultâneo pelo aplicativo.

**Windows 2000, Windows XP e Windows Server 2003:**  Valores grandes para esse parâmetro consumirão espaço de endereço e poderão aumentar o uso de memória.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valor padrão:</p></td>
<td><p>300</p></td>
</tr>
<tr class="even">
<td><p>Tipo:</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Intervalo válido:</p></td>
<td><p>0 – 2147483647</p></td>
</tr>
<tr class="even">
<td><p>Escopo:</p></td>
<td><p>Instância</p></td>
</tr>
<tr class="odd">
<td><p>Definido após <a href="gg269354(v=exchg.10).md">JetCreateInstance:</a></p></td>
<td><p>Sim</p></td>
</tr>
<tr class="even">
<td><p>Definido após <a href="gg294068(v=exchg.10).md">JetInit:</a></p></td>
<td><p>Não</p></td>
</tr>
<tr class="odd">
<td><p>Afeta o layout físico:</p></td>
<td><p>Não</p></td>
</tr>
<tr class="even">
<td><p>Afeta a confiabilidade:</p></td>
<td><p>Não</p></td>
</tr>
<tr class="odd">
<td><p>Afeta o desempenho:</p></td>
<td><p>Não</p></td>
</tr>
<tr class="even">
<td><p>Afeta recursos:</p></td>
<td><p>Sim</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilidade:</p></td>
<td><p>Tudo</p></td>
</tr>
</tbody>
</table>


*JET_paramMaxSessions*  
5  

Esse parâmetro reserva o número solicitado de recursos de sessão para uso por uma instância do . Um recurso de sessão corresponde diretamente a um [tipo JET_SESID](./jet-sesid.md) dados. Essa configuração afetará quantas sessões podem ser usadas ao mesmo tempo.

**Windows 2000, Windows XP e Windows Server 2003:**  Valores grandes para esse parâmetro consumirão espaço de endereço e poderão aumentar o uso de memória.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valor padrão:</p></td>
<td><p>16</p></td>
</tr>
<tr class="even">
<td><p>Tipo:</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Intervalo válido:</p></td>
<td><p>0 – 30000</p></td>
</tr>
<tr class="even">
<td><p>Escopo:</p></td>
<td><p>Instância</p></td>
</tr>
<tr class="odd">
<td><p>Definido após <a href="gg269354(v=exchg.10).md">JetCreateInstance:</a></p></td>
<td><p>Sim</p></td>
</tr>
<tr class="even">
<td><p>Definido após <a href="gg294068(v=exchg.10).md">JetInit:</a></p></td>
<td><p>Não</p></td>
</tr>
<tr class="odd">
<td><p>Afeta o layout físico:</p></td>
<td><p>Não</p></td>
</tr>
<tr class="even">
<td><p>Afeta a confiabilidade:</p></td>
<td><p>Não</p></td>
</tr>
<tr class="odd">
<td><p>Afeta o desempenho:</p></td>
<td><p>Não</p></td>
</tr>
<tr class="even">
<td><p>Afeta recursos:</p></td>
<td><p>Sim</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilidade:</p></td>
<td><p>Tudo</p></td>
</tr>
</tbody>
</table>


*JET_paramMaxTemporaryTables*  
10  

Esse parâmetro reserva o número solicitado de recursos de tabela temporários para uso por uma instância do . Essa configuração afetará quantas tabelas temporárias podem ser usadas ao mesmo tempo.

**Windows 2000, Windows XP e Windows Server 2003:**  Valores grandes para esse parâmetro consumirão espaço de endereço e poderão aumentar o uso de memória.

**Windows XP e posterior:**  Se esse parâmetro do sistema for definido como zero, nenhum banco de dados temporário será criado e qualquer atividade que exija o uso do banco de dados temporário falhará. Essa configuração pode ser útil para evitar a E/S necessária para criar o banco de dados temporário se for conhecido que ele não será usado.

**Observação**  O uso de uma tabela temporária também requer um recurso de cursor.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valor padrão:</p></td>
<td><p>20</p></td>
</tr>
<tr class="even">
<td><p>Tipo:</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Intervalo válido:</p></td>
<td><p>0 – 2147483647</p></td>
</tr>
<tr class="even">
<td><p>Escopo:</p></td>
<td><p>Instância</p></td>
</tr>
<tr class="odd">
<td><p>Definido após <a href="gg269354(v=exchg.10).md">JetCreateInstance:</a></p></td>
<td><p>Sim</p></td>
</tr>
<tr class="even">
<td><p>Definido após <a href="gg294068(v=exchg.10).md">JetInit:</a></p></td>
<td><p>Não</p></td>
</tr>
<tr class="odd">
<td><p>Afeta o layout físico:</p></td>
<td><p>Sim</p></td>
</tr>
<tr class="even">
<td><p>Afeta a confiabilidade:</p></td>
<td><p>Não</p></td>
</tr>
<tr class="odd">
<td><p>Afeta o desempenho:</p></td>
<td><p>Não</p></td>
</tr>
<tr class="even">
<td><p>Afeta recursos:</p></td>
<td><p>Sim</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilidade:</p></td>
<td><p>Tudo</p></td>
</tr>
</tbody>
</table>


*JET_paramMaxVerPages*  
9  

Esse parâmetro reserva o número solicitado de páginas do armazenamento de versão para uso por uma instância. O armazenamento de versão contém um registro ativo de todas as diferentes versões de cada registro ou entrada de índice no banco de dados que pode ser visto por todas as transações ativas. Essas versões são usadas para dar suporte ao controle de concurreência com várias versões em uso pelo mecanismo de banco de dados para dar suporte a transações usando isolamento de instantâneo. Essa configuração afetará quantas atualizações podem ser mantidas na memória por vez. Isso, por sua vez, afetará o número máximo de atualizações que uma única transação pode executar, a duração máxima que uma transação pode ser mantida aberta, a carga máxima simultânea de transações de atualização no sistema ou uma combinação delas.

Cada página do armazenamento de versão, conforme configurado por esse parâmetro, tem 16KB em máquinas de 32 bits e 32KB em máquinas de 64 bits.

**Windows Vista e posterior:**  O tamanho da página do armazenamento de versão pode ser lido e alterado por meio JET_paramVerPageSize.

**Windows 2000, Windows XP e Windows Server 2003:**  Valores grandes para esse parâmetro consumirão espaço de endereço e poderão aumentar o uso de memória.

**Observação**  Esse é, de longe, o recurso mais comum a ser esgotado pelo mecanismo de banco de dados. É necessário ter cuidado com a configuração do parâmetro do sistema e com a carga transacional do aplicativo para evitar esgotar esse recurso em operação normal. Quando esse recurso for esgotado, as atualizações do banco de dados serão rejeitadas com JET_errVersionStoreOutOfMemory. Para liberar alguns desses recursos, a transação pendente mais antiga deve ser anulada.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valor padrão:</p></td>
<td><p>64</p></td>
</tr>
<tr class="even">
<td><p>Tipo:</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Intervalo válido:</p></td>
<td><p>1 – 2147483647</p></td>
</tr>
<tr class="even">
<td><p>Escopo:</p></td>
<td><p>Instância</p></td>
</tr>
<tr class="odd">
<td><p>Definido após <a href="gg269354(v=exchg.10).md">JetCreateInstance:</a></p></td>
<td><p>Sim</p></td>
</tr>
<tr class="even">
<td><p>Definido após <a href="gg294068(v=exchg.10).md">JetInit:</a></p></td>
<td><p>Não</p></td>
</tr>
<tr class="odd">
<td><p>Afeta o layout físico:</p></td>
<td><p>Não</p></td>
</tr>
<tr class="even">
<td><p>Afeta a confiabilidade:</p></td>
<td><p>Sim</p></td>
</tr>
<tr class="odd">
<td><p>Afeta o desempenho:</p></td>
<td><p>Não</p></td>
</tr>
<tr class="even">
<td><p>Afeta recursos:</p></td>
<td><p>Sim</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilidade:</p></td>
<td><p>Tudo</p></td>
</tr>
</tbody>
</table>


*JET_paramPageHintCacheSize*  
101  

Esse parâmetro controla o tamanho de um cache especial usado para acelerar a busca de ponteiros de página filho da Árvore B+ no cache de página do banco de dados. O tamanho do cache é em bytes.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valor padrão:</p></td>
<td><p>262144</p></td>
</tr>
<tr class="even">
<td><p>Tipo:</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Intervalo válido:</p></td>
<td><p>0 – 2147483647</p></td>
</tr>
<tr class="even">
<td><p>Escopo:</p></td>
<td><p>Global</p></td>
</tr>
<tr class="odd">
<td><p>Definido após <a href="gg269354(v=exchg.10).md">JetCreateInstance:</a></p></td>
<td><p>Sim</p></td>
</tr>
<tr class="even">
<td><p>Definido após <a href="gg294068(v=exchg.10).md">JetInit:</a></p></td>
<td><p>Sim</p></td>
</tr>
<tr class="odd">
<td><p>Afeta o layout físico:</p></td>
<td><p>Não</p></td>
</tr>
<tr class="even">
<td><p>Afeta a confiabilidade:</p></td>
<td><p>Não</p></td>
</tr>
<tr class="odd">
<td><p>Afeta o desempenho:</p></td>
<td><p>Sim</p></td>
</tr>
<tr class="even">
<td><p>Afeta recursos:</p></td>
<td><p>Sim</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilidade:</p></td>
<td><p>Windows XP e versões posteriores</p></td>
</tr>
</tbody>
</table>


*JET_paramPreferredMaxOpenTables*  
7  

Esse parâmetro tenta manter o número de recursos de árvore B+ em uso abaixo do limite especificado.

Se esse parâmetro for definido como zero, o padrão será 100% do **JET_paramMaxOpenTables**.

**Windows Vista e posterior:**  Esse parâmetro é obsoleto e não afeta a operação do mecanismo de banco de dados. Os aplicativos devem usar JET_paramMaxCachedClosedTables em vez disso.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valor padrão:</p></td>
<td><p>0 (100% de <strong>JET_paramMaxOpenTables</strong>)</p></td>
</tr>
<tr class="even">
<td><p>Tipo:</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Intervalo válido:</p></td>
<td><p>0 – 2147483647</p></td>
</tr>
<tr class="even">
<td><p>Escopo:</p></td>
<td><p>Instância</p></td>
</tr>
<tr class="odd">
<td><p>Definido após <a href="gg269354(v=exchg.10).md">JetCreateInstance:</a></p></td>
<td><p>Sim</p></td>
</tr>
<tr class="even">
<td><p>Definido após <a href="gg294068(v=exchg.10).md">JetInit:</a></p></td>
<td><p>Não</p></td>
</tr>
<tr class="odd">
<td><p>Afeta o layout físico:</p></td>
<td><p>Não</p></td>
</tr>
<tr class="even">
<td><p>Afeta a confiabilidade:</p></td>
<td><p>Não</p></td>
</tr>
<tr class="odd">
<td><p>Afeta o desempenho:</p></td>
<td><p>Sim</p></td>
</tr>
<tr class="even">
<td><p>Afeta recursos:</p></td>
<td><p>Sim</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilidade:</p></td>
<td><p>Tudo</p></td>
</tr>
</tbody>
</table>


*JET_paramPreferredVerPages*  
63  

Esse parâmetro representa um limite relativo a **JET_paramMaxVerPages** que controla o uso discricionário de páginas de versão pelo mecanismo de banco de dados. Se o tamanho do armazenamento de versões exceder esse limite, todas as informações usadas apenas para tarefas opcionais em segundo plano, como recuperar espaço excluído no banco de dados, serão, em vez disso, preservadas para preservar espaço para informações transacionais.

**Windows 2000, Windows XP e Windows Server 2003:**  Definir esse parâmetro como zero definiria o limite como 90% de **JET_paramMaxVerPages**.

**Windows Vista e posterior:**  Não há mais suporte para isso e o valor padrão desse parâmetro foi alterado para esclarecer seu comportamento.

Cada página do armazenamento de versão, conforme configurado por esse parâmetro, tem 16KB em máquinas de 32 bits e 32KB em máquinas de 64 bits.

**Windows Vista e posterior:**  O tamanho da página do armazenamento de versão pode ser lido e alterado por meio JET_paramVerPageSize.

**Observação**  Se o mecanismo de banco de dados opera acima desse limite com muita frequência, é possível que o banco de dados seja degradado no desempenho. Isso acontece porque os processos em segundo plano que limpam o banco de dados não podem funcionar sem as informações opcionais que são lançadas nesse cenário. A desfragmentação online ou offline vai combater esse efeito.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valor padrão:</p></td>
<td><p><strong>Windows 2000, Windows XP e Windows Server 2003:</strong> 0 (90% do JET_paramMaxVerPages)</p>
<p><strong>Windows Vista:</strong> 58</p></td>
</tr>
<tr class="even">
<td><p>Tipo:</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Intervalo válido:</p></td>
<td><p>1 – 2147483647</p></td>
</tr>
<tr class="even">
<td><p>Escopo:</p></td>
<td><p>Instância</p></td>
</tr>
<tr class="odd">
<td><p>Definido após <a href="gg269354(v=exchg.10).md">JetCreateInstance:</a></p></td>
<td><p>Sim</p></td>
</tr>
<tr class="even">
<td><p>Definido após <a href="gg294068(v=exchg.10).md">JetInit:</a></p></td>
<td><p>Sim</p></td>
</tr>
<tr class="odd">
<td><p>Afeta o layout físico:</p></td>
<td><p>Não</p></td>
</tr>
<tr class="even">
<td><p>Afeta a confiabilidade:</p></td>
<td><p>Sim</p></td>
</tr>
<tr class="odd">
<td><p>Afeta o desempenho:</p></td>
<td><p>Sim</p></td>
</tr>
<tr class="even">
<td><p>Afeta recursos:</p></td>
<td><p>Sim</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilidade:</p></td>
<td><p>Tudo</p></td>
</tr>
</tbody>
</table>


*JET_paramVerPageSize*  
128  

Esse parâmetro controla o tamanho das páginas do armazenamento de versão usadas pelo mecanismo de banco de dados para armazenar informações transacionais. O valor desse parâmetro é o tamanho da unidade para todos os outros parâmetros do sistema que estão em termos de páginas de versão (por exemplo, JET_paramMaxVerPages).

O mecanismo de banco de dados pode optar por usar um tamanho de página de armazenamento de versão maior do que o solicitado.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valor padrão:</p></td>
<td><p>16384</p></td>
</tr>
<tr class="even">
<td><p>Tipo:</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Intervalo válido:</p></td>
<td><p>1024, 2048, 4096, 8192, 16384, 32768, 65536</p></td>
</tr>
<tr class="even">
<td><p>Escopo:</p></td>
<td><p>Global</p></td>
</tr>
<tr class="odd">
<td><p>Definido após <a href="gg269354(v=exchg.10).md">JetCreateInstance:</a></p></td>
<td><p>Não</p></td>
</tr>
<tr class="even">
<td><p>Definido após <a href="gg294068(v=exchg.10).md">JetInit:</a></p></td>
<td><p>Não</p></td>
</tr>
<tr class="odd">
<td><p>Afeta o layout físico:</p></td>
<td><p>Não</p></td>
</tr>
<tr class="even">
<td><p>Afeta a confiabilidade:</p></td>
<td><p>Não</p></td>
</tr>
<tr class="odd">
<td><p>Afeta o desempenho:</p></td>
<td><p>Não</p></td>
</tr>
<tr class="even">
<td><p>Afeta recursos:</p></td>
<td><p>Sim</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilidade:</p></td>
<td><p>Windows Vista e posterior</p></td>
</tr>
</tbody>
</table>


*JET_paramVersionStoreTaskQueueMax*  
105  

Esse parâmetro controla o número de itens de trabalho de limpeza em segundo plano que podem ser enfocados no pool de threads do mecanismo de banco de dados a qualquer momento.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valor padrão:</p></td>
<td><p>32</p></td>
</tr>
<tr class="even">
<td><p>Tipo:</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Intervalo válido:</p></td>
<td><p><strong>Windows XP e Windows Server 2003:</strong> 1 a 63</p>
<p><strong>Windows Vista:</strong> 1 a 127</p></td>
</tr>
<tr class="even">
<td><p>Escopo:</p></td>
<td><p>Instância</p></td>
</tr>
<tr class="odd">
<td><p>Definido após <a href="gg269354(v=exchg.10).md">JetCreateInstance:</a></p></td>
<td><p>Sim</p></td>
</tr>
<tr class="even">
<td><p>Definido após <a href="gg294068(v=exchg.10).md">JetInit:</a></p></td>
<td><p><strong>Windows XP e Windows Server 2003:</strong>  Não</p>
<p><strong>Windows Vista:</strong>  Sim</p></td>
</tr>
<tr class="odd">
<td><p>Afeta o layout físico:</p></td>
<td><p>Não</p></td>
</tr>
<tr class="even">
<td><p>Afeta a confiabilidade:</p></td>
<td><p>Não</p></td>
</tr>
<tr class="odd">
<td><p>Afeta o desempenho:</p></td>
<td><p>Sim</p></td>
</tr>
<tr class="even">
<td><p>Afeta recursos:</p></td>
<td><p>Sim</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilidade:</p></td>
<td><p>Windows XP e versões posteriores</p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Cliente</strong></p></td>
<td><p>Requer Windows Vista, Windows XP ou Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p><strong>Servidor</strong></p></td>
<td><p>Requer Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Cabeçalho</strong></p></td>
<td><p>Declarado em Esent.h.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Consulte Também

[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)
