---
description: 'Saiba mais sobre: Parâmetros de banco de dados'
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
ms.openlocfilehash: 13de02c7d322933f64361cfdabcb8f95ead837ad915ad69c3961a8b8874d5b9a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119117556"
---
# <a name="database-parameters"></a>Parâmetros de Banco de Dados


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="database-parameters"></a>Parâmetros de Banco de Dados

Este tópico contém parâmetros que são usados para o banco de dados.

*JET_paramCheckFormatWhenOpenFail*  
44  

Esse parâmetro, quando definido, fará com que [o JetInit](./jetinit-function.md) retorne um erro especial quando um banco de dados ou log de transações de uma versão anterior do mecanismo de banco de dados for aberto. Esses erros são:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Erro</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_errDatabase200Format</p></td>
<td><p>Os arquivos de log de transações e/ou de banco de dados foram criados com o mecanismo de banco de dados Windows NT 3.51.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabase400Format</p></td>
<td><p>Os arquivos de log de transações e/ou de banco de dados foram criados com o mecanismo de banco de dados em uma versão de teste antes Windows NT Server 4.0.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabase500Format</p></td>
<td><p>Os arquivos de log de transações e/ou de banco de dados foram criados com o mecanismo de banco de dados Windows NT Server 4.0.</p></td>
</tr>
</tbody>
</table>


**Windows Vista:**  Por Windows Vista e posterior, esse parâmetro está obsoleto e não afeta a operação do mecanismo de banco de dados.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valor padrão:</p></td>
<td><p>Verdadeiro</p></td>
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
<td><p>Não</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilidade:</p></td>
<td><p>Tudo</p></td>
</tr>
</tbody>
</table>


*JET_paramDatabasePageSize*  
64  

Esse parâmetro configura o tamanho da página para o banco de dados. O tamanho da página é a menor unidade de alocação de espaço possível para um arquivo de banco de dados. O tamanho da página do banco de dados também é muito importante porque define o limite superior do tamanho de um registro individual no banco de dados.

**Observação** No momento, há suporte para apenas um tamanho de página de banco de dados por processo. Isso significa que, se você estiver em um único processo que contém diferentes aplicativos que usam o mecanismo de banco de dados, todos eles deverão concordar com o tamanho da página do banco de dados.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valor padrão:</p></td>
<td><p>4096</p></td>
</tr>
<tr class="even">
<td><p>Tipo:</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Intervalo válido:</p></td>
<td><p>2048, 4096, 8192</p></td>
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
<td><p>Sim</p></td>
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


*JET_paramDbExtensionSize*  
18  

Esse parâmetro controla a quantidade de espaço que é adicionada a um arquivo de banco de dados sempre que precisa crescer para acomodar mais dados. O tamanho está nas páginas do banco de dados.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valor padrão:</p></td>
<td><p>256</p></td>
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
<td><p>Não</p>
<p><strong>Windows Vista:</strong>  Para Windows Vista e posterior: Sim</p></td>
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


*JET_paramEnableIndexChecking*  
45  

Quando esse parâmetro é true, cada banco de dados é verificado no horário [jetAttachDatabase](./jetattachdatabase-function.md) para índices em colunas de chave Unicode que foram criadas usando uma versão mais antiga da biblioteca NLS no sistema operacional. Isso deve ser feito porque o mecanismo de banco de dados persiste as chaves de classificação geradas por [LCMapStringW](/windows/win32/api/winnls/nf-winnls-lcmapstringa) e o valor dessas chaves de classificação muda de Release para Release.

Se for detectado que um índice primário está nesse estado, [JetAttachDatabase](./jetattachdatabase-function.md) sempre falhará com JET_errPrimaryIndexCorrupted.

Se algum índice secundário for detectado para estar nesse estado, haverá dois resultados possíveis. Se JET_bitDbDeleteCorruptIndexes foi passado para [JetAttachDatabase](./jetattachdatabase-function.md) , esses índices serão excluídos e JET_wrnCorruptIndexDeleted serão retornados de [JetAttachDatabase](./jetattachdatabase-function.md). Esses índices precisarão ser recriados pelo seu aplicativo. Se JET_bitDbDeleteCorruptIndexes não foi passado para [JetAttachDatabase](./jetattachdatabase-function.md) , a chamada falhará com JET_errSecondaryIndexCorrupted.

**Observação** É altamente recomendável que esse parâmetro seja definido como true pelo seu aplicativo.

**Observação** É altamente recomendável que os aplicativos evitem o uso de colunas de chave Unicode em seus índices de chave primária (clusterizados).

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
<td><p>Falso, verdadeiro</p></td>
</tr>
<tr class="even">
<td><p>Escopo:</p></td>
<td><p>Global</p>
<p><strong>Windows Vista:</strong>  para Windows Vista e posterior: instância</p></td>
</tr>
<tr class="odd">
<td><p>Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>Não</p></td>
</tr>
<tr class="even">
<td><p>Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
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
<td><p>Afeta os recursos:</p></td>
<td><p>Não</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilidade:</p></td>
<td><p>Tudo</p></td>
</tr>
</tbody>
</table>


*JET_paramEnableIndexCleanup*  
54  

Quando esse parâmetro é definido como true, o mecanismo de banco de dados pode limpar automaticamente os índices em colunas de chave Unicode em [JetInit](./jetinit-function.md) , conforme necessário, para evitar alterações no formato de banco de dados causados por alterações na biblioteca NLS no Windows. Essas alterações são feitas rotineiramente na biblioteca NLS para adicionar suporte a novos idiomas, para adicionar caracteres ausentes a um idioma, para adicionar uma ordem de agrupamento a um idioma ou para corrigir bugs na ordem de agrupamento de um idioma. Essas alterações afetam as chaves de classificação produzidas por [LCMapStringW](/windows/win32/api/winnls/nf-winnls-lcmapstringa) que são mantidas pelo mecanismo de banco de dados como componentes de chaves de índice.

É importante perceber que é possível que as alterações no índice sejam tão ótimas que uma limpeza incremental não é possível. Nesse caso, o índice será manipulado conforme prescrito pelo **JET_paramEnableIndexChecking**.

**Observação** É altamente recomendável que esse parâmetro e **JET_paramEnableIndexChecking** sejam definidos como **true** pelo seu aplicativo.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valor padrão:</p></td>
<td><p>Verdadeiro</p></td>
</tr>
<tr class="even">
<td><p>Tipo:</p></td>
<td><p>Boolean</p></td>
</tr>
<tr class="odd">
<td><p>Intervalo válido:</p></td>
<td><p>Falso, verdadeiro</p></td>
</tr>
<tr class="even">
<td><p>Escopo:</p></td>
<td><p>Instância</p></td>
</tr>
<tr class="odd">
<td><p>Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>Sim</p></td>
</tr>
<tr class="even">
<td><p>Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>Não</p>
<p><strong>Windows Vista:</strong>  para Windows Vista e posterior: sim</p></td>
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
<td><p>Afeta os recursos:</p></td>
<td><p>Não</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilidade:</p></td>
<td><p>Windows Server 2003 e versões posteriores</p></td>
</tr>
</tbody>
</table>


*JET_paramOneDatabasePerSession*  
102  

Quando esse parâmetro for true, somente um banco de dados poderá ser aberto usando [JetOpenDatabase](./jetopendatabase-function.md) por uma determinada sessão ao mesmo tempo. O banco de dados temporário é excluído dessa restrição.

**Windows XP e Windows Server 2003:**  esse parâmetro é somente gravação no Windows XP e no Windows Server 2003.

**Windows Vista:**  esse parâmetro se comporta normalmente a partir do Windows Vista.

**Observação**  Esse parâmetro é somente gravação.

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
<td><p>Falso, verdadeiro</p></td>
</tr>
<tr class="even">
<td><p>Escopo:</p></td>
<td><p>Global</p></td>
</tr>
<tr class="odd">
<td><p>Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>Não</p>
<p><strong>Windows Vista:</strong>  para Windows Vista e posterior: sim</p></td>
</tr>
<tr class="even">
<td><p>Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
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
<td><p>Afeta os recursos:</p></td>
<td><p>Não</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilidade:</p></td>
<td><p>Windows XP e versões posteriores</p></td>
</tr>
</tbody>
</table>


*JET_paramEnableOnlineDefrag*  
35  

Esse parâmetro controla o comportamento da desfragmentação online quando iniciado usando [JetDefragment](./jetdefragment-function.md). Consulte [JetDefragment](./jetdefragment-function.md) para obter mais informações.

Windows 2000: On Windows 2000, esse parâmetro era um booliano simples que faria a desfragmentação online quando iniciado por [JetDefragment](./jetdefragment-function.md). Quando definido como **true**, a desfragmentação online será executada nos registros de cada tabela no banco de dados.

**Windows XP:**  no Windows XP e versões posteriores, esse parâmetro pode ser definido como uma ou mais das seguintes opções:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Opção</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_OnlineDefragDisable</p></td>
<td><p>Não execute a desfragmentação online. Esse é o equivalente binário à configuração Windows 2000 de False para esse parâmetro.</p></td>
</tr>
<tr class="even">
<td><p>JET_OnlineDefragAllOBSOLETE</p></td>
<td><p>Execute a desfragmentação online completa. Esse é o equivalente binário à configuração Windows 2000 de True para esse parâmetro.</p></td>
</tr>
<tr class="odd">
<td><p>JET_OnlineDefragDatabases</p></td>
<td><p>Execute a desfragmentação online dos registros de cada tabela no banco de dados.</p></td>
</tr>
<tr class="even">
<td><p>JET_OnlineDefragSpaceTrees</p></td>
<td><p>Execute a desfragmentação online das árvores de espaço de cada tabela no banco de dados.</p></td>
</tr>
<tr class="odd">
<td><p>JET_OnlineDefragStreamingFiles</p></td>
<td><p>Esse parâmetro é usado para dar suporte à infraestrutura do Microsoft Exchange e não se destina a ser usado em seu aplicativo.</p></td>
</tr>
<tr class="even">
<td><p>JET_OnlineDefragAll</p></td>
<td><p>Execute a desfragmentação online completa. Esse é o equivalente conceitual à configuração Windows 2000 de True para esse parâmetro.</p></td>
</tr>
</tbody>
</table>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valor padrão:</p></td>
<td><p><strong>Windows 2000:</strong>  Verdade</p>
<p><strong>Windows XP: para Windows XP e posterior:</strong> JET_OnlineDefragAll</p></td>
</tr>
<tr class="even">
<td><p>Tipo:</p></td>
<td><p><strong>Windows 2000:</strong>  Boolean</p>
<p><strong>Windows XP e posterior:</strong>  JET_GRBIT (inteiro)</p></td>
</tr>
<tr class="odd">
<td><p>Intervalo válido:</p></td>
<td><p><strong>Windows 2000:</strong>  False, True</p>
<p><strong>Windows XP e posterior:</strong> 0 – JET_OnlineDefragAll</p></td>
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
<td><p>Não</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilidade:</p></td>
<td><p>Tudo</p></td>
</tr>
</tbody>
</table>


*JET_paramPageFragment*  
20  

Esse parâmetro é o limite que o mecanismo de banco de dados usa para controlar a fragmentação de espaço livre. O tamanho está nas páginas do banco de dados.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valor padrão:</p></td>
<td><p>8</p></td>
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


*JET_paramRecordUpgradeDirtyLevel*  
78

Esse parâmetro controla o quão agressivamente o gerenciador de cache de página do banco de dados gravará uma página de banco de dados que passou por uma conversão de formato in-loque. Essas conversões de formato ocorrem em tempo real conforme as páginas são carregadas de um banco de dados que foi criado com o mecanismo de banco de dados do Windows 2000, mas usado por um Windows XP ou versão posterior do mecanismo de banco de dados.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valor padrão:</p></td>
<td><p>1</p></td>
</tr>
<tr class="even">
<td><p>Tipo:</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Intervalo válido:</p></td>
<td><p>0-3</p></td>
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
<td><p>Sim</p></td>
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
<td><p>Não</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilidade:</p></td>
<td><p>Windows XP e versões posteriores</p></td>
</tr>
</tbody>
</table>


*JET_paramWaypointLatency*  
153  

A latência (em logs) por trás da dica/log confirmado mais alto para adiar liberações de página do banco de dados. A habilitação dessa latência pode permitir a recuperação de banco de dados no caso de perda catastrófica do logfile mais recente. Consulte JET_bitReplayIgnoreLostLogs.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valor padrão:</p></td>
<td><p>0</p></td>
</tr>
<tr class="even">
<td><p>Tipo:</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Intervalo válido:</p></td>
<td><p>0-1023</p></td>
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
<td><p>Sim</p></td>
</tr>
<tr class="even">
<td><p>Afeta recursos:</p></td>
<td><p>Não</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilidade:</p></td>
<td><p>Windows 7</p></td>
</tr>
</tbody>
</table>


*JET_paramDefragmentSequentialBTrees*  
160  

Ativar/desativar a desfragmentação de árvore B sequencial automática.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valor padrão:</p></td>
<td><p>1</p></td>
</tr>
<tr class="even">
<td><p>Tipo:</p></td>
<td><p>Boolean</p></td>
</tr>
<tr class="odd">
<td><p>Intervalo válido:</p></td>
<td><p>0-1</p></td>
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
<td><p>Sim</p></td>
</tr>
<tr class="even">
<td><p>Afeta recursos:</p></td>
<td><p>Não</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilidade:</p></td>
<td><p>Windows 7</p></td>
</tr>
</tbody>
</table>


*JET_paramDefragmentSequentialBTreesDensityCheckFrequency*  
161  

Determina com que frequência a densidade da árvore B é verificada.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valor padrão:</p></td>
<td><p>10</p></td>
</tr>
<tr class="even">
<td><p>Tipo:</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Intervalo válido:</p></td>
<td><p>Inteiro máximo de 0</p></td>
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
<td><p>Sim</p></td>
</tr>
<tr class="even">
<td><p>Afeta recursos:</p></td>
<td><p>Não</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilidade:</p></td>
<td><p>Windows 7</p></td>
</tr>
</tbody>
</table>


*JET_paramIOThrottlingTimeQuanta*  
162  

Tempo máximo, em milissegundos, que o mecanismo de avaliação de E/S fornece uma tarefa a ser executado para que ela seja considerada "concluída".

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valor padrão:</p></td>
<td><p>125</p></td>
</tr>
<tr class="even">
<td><p>Tipo:</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Intervalo válido:</p></td>
<td><p>0-10000</p></td>
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
<td><p>Não</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilidade:</p></td>
<td><p>Windows 7</p></td>
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
<td><p>Declarado em ESENT. h.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Consulte Também

[JetAttachDatabase](./jetattachdatabase-function.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetDefragment](./jetdefragment-function.md)  
[JetInit](./jetinit-function.md)
