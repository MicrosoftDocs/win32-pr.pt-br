---
description: 'Saiba mais sobre: membros da API'
title: Membros da API
TOCTitle: Api members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.Api
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api_members(v=EXCHG.10)
ms:contentKeyID: 55100778
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: e1debc551dc644d71568772761cb14500d2fd546
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370552"
---
# <a name="api-members"></a>Membros da API

Incluir membros protegidos  
Incluir membros herdados  

Versões gerenciadas da API ESENT. Essa classe contém métodos estáticos que correspondem à API ESENT não gerenciada. Esses métodos geram exceções quando são retornados erros. Métodos auxiliares para a API ESENT. Eles encapsulam JetMakeKey. Métodos somente internos da API. Métodos auxiliares para a API ESENT. Isso faz a conversão de dados para JetMakeKey. Métodos auxiliares para a API ESENT. Esses métodos lidam com metadados de banco de dados. Métodos auxiliares para a API ESENT. Essas não são versões de interoperabilidade da API, mas encapsulam usos muito comuns das funções. Membros da API que são marcados como obsoletos. Métodos auxiliares para a API ESENT. Essas não são versões de interoperabilidade da API, mas encapsulam usos muito comuns das funções. Métodos auxiliares para a API ESENT. Isso faz a conversão de dados para a configuração de colunas.

O tipo de [API](./api-class.md) expõe os membros a seguir.

## <a name="methods"></a>Métodos

<table>
<thead>
<tr class="header">
<th> </th>
<th>Nome</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn292138(v=exchg.10).md">DeserializeObjectFromColumn (JET_SESID, JET_TABLEID, JET_COLUMNID)</a></td>
<td>Desserializar um objeto de uma coluna.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn292115(v=exchg.10).md">DeserializeObjectFromColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)</a></td>
<td>Desserializar um objeto de uma coluna.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn292114(v=exchg.10).md">EscrowUpdate</a></td>
<td>Executar adição atômica em uma coluna. A coluna deve ser do tipo <a href="hh577895(v=exchg.10).md">Long</a>. Essa função permite que várias sessões atualizem o mesmo registro simultaneamente sem conflitos.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn292099(v=exchg.10).md">GetBookmark</a></td>
<td>Recupera o indicador para o registro que está associado à entrada de índice na posição atual de um cursor. Esse indicador pode então ser usado para reposicionar esse cursor de volta para o mesmo registro usando JetGotoBookmark.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn292098(v=exchg.10).md">GetColumnDictionary</a></td>
<td>Cria um dicionário que mapeia nomes de coluna para suas IDs de coluna.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn292101(v=exchg.10).md">GetTableColumnid</a></td>
<td>Obtém o columnid da coluna especificada.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn292090(v=exchg.10).md">GetTableColumns (JET_SESID, JET_TABLEID)</a></td>
<td>Itera sobre todas as colunas na tabela, retornando informações sobre cada uma delas.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn292089(v=exchg.10).md">GetTableColumns (JET_SESID, JET_DBID, Cadeia de caracteres)</a></td>
<td>Itera sobre todas as colunas na tabela, retornando informações sobre cada uma delas.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn292093(v=exchg.10).md">GetTableIndexes (JET_SESID, JET_TABLEID)</a></td>
<td>Itera em todos os índices na tabela, retornando informações sobre cada um.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn292092(v=exchg.10).md">GetTableIndexes (JET_SESID, JET_DBID, Cadeia de caracteres)</a></td>
<td>Itera em todos os índices na tabela, retornando informações sobre cada um.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn292095(v=exchg.10).md">Gettablenamenames</a></td>
<td>Retorna os nomes das tabelas no banco de dados.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn292094(v=exchg.10).md">IntersectIndexes</a></td>
<td>Intersecte um grupo de intervalos de índice e retorne os indicadores dos registros que são encontrados em todos os intervalos de índice. Consulte também <a href="dn292212(v=exchg.10).md">JetIntersectIndexes (JET_SESID, [], Int32, JET_RECORDLIST, IntersectIndexesGrbit)</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn292097(v=exchg.10).md">JetAddColumn</a></td>
<td>Adicione uma nova coluna a uma tabela existente.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn292096(v=exchg.10).md">JetAttachDatabase</a></td>
<td>Anexa um arquivo de banco de dados para uso com uma instância de banco de dados. Para usar o banco de dados, será necessário abri-lo subsequentemente com <a href="dn292219(v=exchg.10).md">JetOpenDatabase (JET_SESID, String, String, JET_DBID, OpenDatabaseGrbit)</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn292100(v=exchg.10).md">JetAttachDatabase2</a></td>
<td>Anexa um arquivo de banco de dados para uso com uma instância de banco de dados. Para usar o banco de dados, será necessário abri-lo subsequentemente com <a href="dn292219(v=exchg.10).md">JetOpenDatabase (JET_SESID, String, String, JET_DBID, OpenDatabaseGrbit)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn292102(v=exchg.10).md">JetBackupInstance</a></td>
<td>Executa um backup de streaming de uma instância do, incluindo todos os bancos de dados anexados, em um diretório. Com vários métodos de backup com suporte no mecanismo, essa é a função mais simples e encapsulada.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn292104(v=exchg.10).md">JetBeginExternalBackupInstance</a></td>
<td>Inicia um backup externo enquanto o mecanismo e o banco de dados estão online e ativos.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn292103(v=exchg.10).md">JetBeginSession</a></td>
<td>Inicializar uma nova sessão ESENT.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn292105(v=exchg.10).md">JetBeginTransaction</a></td>
<td>Faz com que uma sessão Insira uma transação ou crie um novo ponto de salvamento em uma transação existente.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn292106(v=exchg.10).md">JetBeginTransaction2</a></td>
<td>Faz com que uma sessão Insira uma transação ou crie um novo ponto de salvamento em uma transação existente.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn292107(v=exchg.10).md">JetCloseDatabase</a></td>
<td>Fecha um arquivo de banco de dados que foi aberto anteriormente com <a href="dn292219(v=exchg.10).md">JetOpenDatabase (JET_SESID, String, String, JET_DBID, OpenDatabaseGrbit)</a> ou criado com <a href="dn292118(v=exchg.10).md">JetCreateDatabase (JET_SESID, String, String, JET_DBID, CreateDatabaseGrbit)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn292108(v=exchg.10).md">JetCloseFileInstance</a></td>
<td>Fecha um arquivo que foi aberto com JetOpenFileInstance depois que os dados desse arquivo foram extraídos usando JetReadFileInstance.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn292109(v=exchg.10).md">JetCloseTable</a></td>
<td>Fechar uma tabela aberta.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn292110(v=exchg.10).md">JetCommitTransaction</a></td>
<td>Confirma as alterações feitas no estado do banco de dados durante o ponto de salvamento atual e os migra para o ponto de salvamento anterior. Se o ponto de salvamento mais externo for confirmado, as alterações feitas durante esse ponto de salvamento serão confirmadas no estado do banco de dados e a sessão sairá da transação.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn292112(v=exchg.10).md">JetCompact</a></td>
<td>Faz uma cópia de um banco de dados existente. A cópia é compactada para um estado ideal para uso. Os dados nos dados copiados serão empacotados de acordo com as medidas escolhidas para os índices na criação do índice. Dessa forma, os dados compactados podem ser armazenados da maneira mais densa possível. Como alternativa, os dados compactados podem reservar espaço para o aumento de registro subsequente ou inserções de índice.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn292113(v=exchg.10).md">JetComputeStats</a></td>
<td>Percorre cada índice de uma tabela para calcular exatamente o número de entradas em um índice e o número de chaves distintas em um índice. Essas informações, junto com o número de páginas de banco de dados alocadas para um índice e a hora atual da computação, são armazenadas em metadados de índice no banco de dados. Esses dados podem ser recuperados posteriormente com operações de informações.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn292118(v=exchg.10).md">JetCreateDatabase</a></td>
<td>Cria e anexa um arquivo de banco de dados.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn292120(v=exchg.10).md">JetCreateDatabase2</a></td>
<td>Cria e anexa um arquivo de banco de dados com um tamanho máximo de banco de dados especificado.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn292121(v=exchg.10).md">JetCreateIndex</a></td>
<td>Cria um índice sobre os dados em um banco de dado ESE. Um índice pode ser usado para localizar dados específicos rapidamente.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn292123(v=exchg.10).md">JetCreateIndex2</a></td>
<td>Cria índices em dados em um banco de dado ESE.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn292122(v=exchg.10).md">JetCreateInstance</a></td>
<td>Aloca uma nova instância do mecanismo de banco de dados.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn292126(v=exchg.10).md">JetCreateInstance2</a></td>
<td>Aloque uma nova instância do mecanismo de banco de dados para uso em um único processo, com um nome de exibição especificado.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn292127(v=exchg.10).md">JetCreateTable</a></td>
<td>Crie uma tabela vazia. A tabela recém-criada é aberta exclusivamente.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn292129(v=exchg.10).md">JetCreateTableColumnIndex3</a></td>
<td>Cria uma tabela, adiciona colunas e índices nessa tabela.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn292130(v=exchg.10).md">JetDefragment</a></td>
<td>Inicia e interrompe as tarefas de desfragmentação do banco de dados que aprimoram a organização em um banco de dado.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn292145(v=exchg.10).md">JetDefragment2</a></td>
<td>Inicia e interrompe as tarefas de desfragmentação do banco de dados que aprimoram a organização em um banco de dado.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn292131(v=exchg.10).md">JetDelete</a></td>
<td>Exclui o registro atual em uma tabela de banco de dados.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn292133(v=exchg.10).md">JetDeleteColumn</a></td>
<td>Exclui uma coluna de uma tabela de banco de dados.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn292132(v=exchg.10).md">JetDeleteColumn2</a></td>
<td>Exclui uma coluna de uma tabela de banco de dados.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn292135(v=exchg.10).md">JetDeleteIndex</a></td>
<td>Exclui um índice de uma tabela de banco de dados.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn292134(v=exchg.10).md">JetDeleteTable</a></td>
<td>Exclui uma tabela de um banco de dados.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn292139(v=exchg.10).md">JetDetachDatabase</a></td>
<td>Libera um arquivo de banco de dados que foi anexado anteriormente a uma sessão de banco de dados.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn292136(v=exchg.10).md">JetDetachDatabase2</a></td>
<td>Libera um arquivo de banco de dados que foi anexado anteriormente a uma sessão de banco de dados.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn292137(v=exchg.10).md">JetDupCursor</a></td>
<td>Duplica um cursor Open e retorna um identificador para o cursor duplicado. Se o cursor que foi duplicado era um cursor somente leitura, o cursor duplicado também é um cursor somente leitura. Qualquer estado relacionado à construção de uma chave de pesquisa ou à atualização de um registro não é copiado para o cursor duplicado. Além disso, o local do cursor original não é duplicado no cursor duplicado. O cursor duplicado sempre é aberto no índice clusterizado e seu local está sempre na primeira linha da tabela.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn292140(v=exchg.10).md">JetDupSession</a></td>
<td>Inicialize uma nova sessão do ESE na mesma instância do sesid fornecido.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn292142(v=exchg.10).md">JetEndExternalBackupInstance</a></td>
<td>Encerra uma sessão de backup externo. Essa API é a última API em uma série de APIs que devem ser chamadas para executar um backup online (não baseado em VSS) com êxito.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn292143(v=exchg.10).md">JetEndExternalBackupInstance2</a></td>
<td>Encerra uma sessão de backup externo. Essa API é a última API em uma série de APIs que devem ser chamadas para executar um backup online (não baseado em VSS) com êxito.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn292144(v=exchg.10).md">JetEndSession</a></td>
<td>Encerra uma sessão.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn292148(v=exchg.10).md">JetEnumerateColumns</a></td>
<td>Recupera com eficiência um conjunto de colunas e seus valores do registro atual de um cursor ou o buffer de cópia desse cursor. As colunas e os valores recuperados podem ser restringidos por uma lista de IDs de coluna, números de itagSequence e outras características. Essa API de recuperação de coluna é exclusiva, pois retorna informações na memória alocada dinamicamente que é obtida usando um retorno de chamada compatível de realocação fornecido pelo usuário. Essa nova flexibilidade permite a recuperação eficiente de dados de coluna com características específicas (como tamanho e multiplicidade) que são desconhecidos para o chamador. Isso elimina a necessidade de usar os modos de descoberta de JetRetrieveColumn para determinar essas características a fim de configurar uma chamada final para JetRetrieveColumn que recuperará com êxito os dados desejados.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn292150(v=exchg.10).md">JetEscrowUpdate</a></td>
<td>Executa uma operação de adição atômica em uma coluna. Essa função permite que várias sessões atualizem o mesmo registro simultaneamente sem conflitos. Consulte também <a href="dn292114(v=exchg.10).md">EscrowUpdate (JET_SESID, JET_TABLEID, JET_COLUMNID, Int32)</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn292147(v=exchg.10).md">JetFreeBuffer</a></td>
<td>Libera a memória que foi alocada por uma chamada do mecanismo de banco de dados.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn292154(v=exchg.10).md">JetGetAttachInfoInstance</a></td>
<td>Usado durante um backup iniciado por <a href="dn292104(v=exchg.10).md">JetBeginExternalBackupInstance (JET_INSTANCE, BeginExternalBackupGrbit)</a> para consultar uma instância para obter os nomes dos arquivos de banco de dados que devem se tornar parte do conjunto de arquivos de backup. Somente os bancos de dados atualmente anexados à instância usando <a href="dn292096(v=exchg.10).md">JetAttachDatabase (JET_SESID, String, AttachDatabaseGrbit)</a> serão considerados. Esses arquivos podem ser abertos subsequentemente usando <a href="dn292230(v=exchg.10).md">JetOpenFileInstance (JET_INSTANCE, String, JET_HANDLE, Int64, Int64)</a> e Read usando <a href="dn332987(v=exchg.10).md">JetReadFileInstance (JET_INSTANCE, JET_HANDLE, [], Int32, Int32)</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn292149(v=exchg.10).md">JetGetBookmark</a></td>
<td>Recupera o indicador para o registro que está associado à entrada de índice na posição atual de um cursor. Esse indicador pode então ser usado para reposicionar esse cursor de volta para o mesmo registro usando <a href="dn292200(v=exchg.10).md">JetGotoBookmark (JET_SESID, JET_TABLEID, [], Int32)</a>. O indicador não terá mais do que <a href="dn351215(v=exchg.10).md">BookmarkMost</a> bytes. Consulte também <a href="dn292099(v=exchg.10).md">GetBookmark (JET_SESID, JET_TABLEID)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn292158(v=exchg.10).md">JetGetColumnInfo (JET_SESID, JET_DBID, String, String JET_COLUMNBASE)</a></td>
<td>Recupera informações sobre uma coluna em uma tabela.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn292151(v=exchg.10).md">JetGetColumnInfo (JET_SESID, JET_DBID, String, String JET_COLUMNDEF)</a></td>
<td>Recupera informações sobre uma coluna de tabela.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn292152(v=exchg.10).md">JetGetColumnInfo (JET_SESID, JET_DBID, String, String JET_COLUMNLIST)</a></td>
<td>Recupera informações sobre todas as colunas em uma tabela.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn292153(v=exchg.10).md">JetGetCurrentIndex</a></td>
<td>Ddetermines o nome do índice atual de um determinado cursor. Esse nome também é usado posteriormente para selecionar novamente esse índice como o índice atual usando <a href="dn334011(v=exchg.10).md">JetSetCurrentIndex (JET_SESID, JET_TABLEID, String)</a>. Ele também pode ser usado para descobrir as propriedades desse índice usando JetGetTableIndexInfo.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn292155(v=exchg.10).md">JetGetCursorInfo</a></td>
<td>Determine se uma atualização do registro atual de um cursor resultará em um conflito de gravação, com base no status de atualização atual do registro. É possível que um conflito de gravação será retornado, mesmo se JetGetCursorInfo retornar com êxito. Porque outra sessão pode atualizar o registro antes que a sessão atual seja capaz de atualizar o mesmo registro.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn292159(v=exchg.10).md">JetGetDatabaseFileInfo (cadeia de caracteres, JET_DBINFOMISC JET_DbInfo)</a></td>
<td>Recupera determinadas informações sobre o banco de dados especificado.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn292161(v=exchg.10).md">JetGetDatabaseFileInfo (cadeia de caracteres, Int32, JET_DbInfo)</a></td>
<td>Recupera determinadas informações sobre o banco de dados especificado.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn292160(v=exchg.10).md">JetGetDatabaseFileInfo (cadeia de caracteres, Int64, JET_DbInfo)</a></td>
<td>Recupera determinadas informações sobre o banco de dados especificado.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn292162(v=exchg.10).md">JetGetDatabaseInfo (JET_SESID, JET_DBID, JET_DBINFOMISC JET_DbInfo)</a></td>
<td>Recupera determinadas informações sobre o banco de dados especificado.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn292164(v=exchg.10).md">JetGetDatabaseInfo (JET_SESID, JET_DBID, Int32, JET_DbInfo)</a></td>
<td>Recupera determinadas informações sobre o banco de dados especificado.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn292167(v=exchg.10).md">JetGetDatabaseInfo (JET_SESID, JET_DBID, Cadeia de caracteres JET_DbInfo)</a></td>
<td>Recupera determinadas informações sobre o banco de dados especificado.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn292168(v=exchg.10).md">JetGetIndexInfo (JET_SESID, JET_DBID, String, String JET_INDEXLIST)</a></td>
<td><strong>Obsoleto.</strong> Recupera informações sobre índices em uma tabela.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn292172(v=exchg.10).md">JetGetIndexInfo (JET_SESID, JET_DBID, String, String, JET_INDEXID, JET_IdxInfo)</a></td>
<td>Recupera informações sobre índices em uma tabela.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn292166(v=exchg.10).md">JetGetIndexInfo (JET_SESID, JET_DBID, String, String, JET_INDEXLIST, JET_IdxInfo)</a></td>
<td>Recupera informações sobre índices em uma tabela.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn292171(v=exchg.10).md">JetGetIndexInfo (JET_SESID, JET_DBID, String, String, Int32, JET_IdxInfo)</a></td>
<td>Recupera informações sobre índices em uma tabela.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn292169(v=exchg.10).md">JetGetIndexInfo (JET_SESID, JET_DBID, Cadeia de caracteres, Cadeia de caracteres, JET_IdxInfo)</a></td>
<td>Recupera informações sobre índices em uma tabela.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn292173(v=exchg.10).md">JetGetIndexInfo (JET_SESID, JET_DBID, String, String, UInt16, JET_IdxInfo)</a></td>
<td>Recupera informações sobre índices em uma tabela.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn292170(v=exchg.10).md">JetGetInstanceInfo</a></td>
<td>Recupera informações sobre as instâncias que estão em execução.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn292175(v=exchg.10).md">JetGetLock</a></td>
<td>Reserve explicitamente a capacidade de atualizar uma linha, bloqueio de gravação ou impedir explicitamente que uma linha seja atualizada por qualquer outra sessão, bloqueio de leitura. Normalmente, os bloqueios de gravação de linha são adquiridos implicitamente como resultado da atualização de linhas. Os bloqueios de leitura geralmente não são necessários devido ao controle de versão de registro. No entanto, em alguns casos, uma transação pode desejar bloquear explicitamente uma linha para impor a serialização ou para garantir que uma operação subsequente terá sucesso.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn292174(v=exchg.10).md">JetGetLogInfoInstance</a></td>
<td>Usado durante um backup iniciado por <a href="dn292104(v=exchg.10).md">JetBeginExternalBackupInstance (JET_INSTANCE, BeginExternalBackupGrbit)</a> para consultar uma instância para obter os nomes dos arquivos de patch de banco de dados e dos LogFiles que devem se tornar parte do conjunto de arquivos de backup. Esses arquivos podem ser abertos subsequentemente usando <a href="dn292230(v=exchg.10).md">JetOpenFileInstance (JET_INSTANCE, String, JET_HANDLE, Int64, Int64)</a> e Read usando <a href="dn332987(v=exchg.10).md">JetReadFileInstance (JET_INSTANCE, JET_HANDLE, [], Int32, Int32)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn292177(v=exchg.10).md">JetGetLS</a></td>
<td>Permite que o aplicativo recupere o identificador de contexto conhecido como armazenamento local associado a um cursor ou à tabela associada a esse cursor. Esse identificador de contexto deve ter sido definido anteriormente usando <a href="dn334015(v=exchg.10).md">JetSetLS (JET_SESID, JET_TABLEID, JET_LS, LsGrbit)</a>. JetGetLS também pode ser usado para buscar simultaneamente o identificador de contexto atual para um cursor ou uma tabela e redefinir esse identificador de contexto.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn292179(v=exchg.10).md">JetGetObjectInfo (JET_SESID, JET_DBID, JET_OBJECTLIST)</a></td>
<td>Recupera informações sobre objetos de banco de dados.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn292178(v=exchg.10).md">JetGetObjectInfo (JET_SESID, JET_DBID, JET_objtyp, Cadeia de caracteres JET_OBJECTINFO)</a></td>
<td>Recupera informações sobre objetos de banco de dados.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn292181(v=exchg.10).md">JetGetRecordPosition</a></td>
<td>Retorna a posição fracionária do registro atual no índice atual na forma de uma estrutura de <a href="dn335256(v=exchg.10).md">JET_RECPOS</a> . Consulte também <a href="dn292207(v=exchg.10).md">JetGotoPosition (JET_SESID, JET_TABLEID, JET_RECPOS)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn292180(v=exchg.10).md">JetGetSecondaryIndexBookmark</a></td>
<td>Recupera um indicador especial para a entrada de índice secundário na posição atual de um cursor. Esse indicador pode então ser usado para reposicionar com eficiência esse cursor de volta para a mesma entrada de índice usando JetGotoSecondaryIndexBookmark. Isso é mais útil ao reposicionar em um índice secundário que contém chaves duplicadas ou que contém várias entradas de índice para o mesmo registro.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn292182(v=exchg.10).md">JetGetSystemParameter (JET_INSTANCE, JET_SESID, JET_param, Int32, Cadeia de caracteres, Int32)</a></td>
<td>Obtém as opções de configuração do banco de dados.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn292185(v=exchg.10).md">JetGetSystemParameter (JET_INSTANCE, JET_SESID, JET_param, IntPtr, Cadeia de caracteres, Int32)</a></td>
<td>Obtém as opções de configuração do banco de dados.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn292186(v=exchg.10).md">JetGetTableColumnInfo (JET_SESID, JET_TABLEID, JET_COLUMNID JET_COLUMNDEF)</a></td>
<td>Recupera informações sobre uma coluna de tabela.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn292187(v=exchg.10).md">JetGetTableColumnInfo (JET_SESID, JET_TABLEID, Cadeia de caracteres JET_COLUMNDEF)</a></td>
<td>Recupera informações sobre uma coluna de tabela.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn292189(v=exchg.10).md">JetGetTableColumnInfo (JET_SESID, JET_TABLEID, Cadeia de caracteres JET_COLUMNLIST)</a></td>
<td>Recupera informações sobre todas as colunas na tabela.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn292191(v=exchg.10).md">JetGetTableIndexInfo (JET_SESID, JET_TABLEID, Cadeia de caracteres JET_INDEXLIST)</a></td>
<td><strong>Obsoleto.</strong> Recupera informações sobre índices em uma tabela.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn292190(v=exchg.10).md">JetGetTableIndexInfo (JET_SESID, JET_TABLEID, Cadeia de caracteres, JET_INDEXID JET_IdxInfo)</a></td>
<td>Recupera informações sobre índices em uma tabela.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn292196(v=exchg.10).md">JetGetTableIndexInfo (JET_SESID, JET_TABLEID, Cadeia de caracteres, JET_INDEXLIST JET_IdxInfo)</a></td>
<td>Recupera informações sobre índices em uma tabela.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn292193(v=exchg.10).md">JetGetTableIndexInfo (JET_SESID, JET_TABLEID, Cadeia de caracteres, Int32, JET_IdxInfo)</a></td>
<td>Recupera informações sobre índices em uma tabela.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn292192(v=exchg.10).md">JetGetTableIndexInfo (JET_SESID, JET_TABLEID, String, String JET_IdxInfo)</a></td>
<td>Recupera informações sobre índices em uma tabela.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn292195(v=exchg.10).md">JetGetTableIndexInfo (JET_SESID, JET_TABLEID, Cadeia de caracteres, UInt16, JET_IdxInfo)</a></td>
<td>Recupera informações sobre índices em uma tabela.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn292197(v=exchg.10).md">JetGetTableInfo (JET_SESID, JET_TABLEID, JET_DBID JET_TblInfo)</a></td>
<td>Recupera várias partes de informações sobre uma tabela em um banco de dados.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn292198(v=exchg.10).md">JetGetTableInfo (JET_SESID, JET_TABLEID, JET_OBJECTINFO JET_TblInfo)</a></td>
<td>Recupera várias partes de informações sobre uma tabela em um banco de dados.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn292201(v=exchg.10).md">JetGetTableInfo (JET_SESID, JET_TABLEID, Int32, JET_TblInfo)</a></td>
<td>Recupera várias partes de informações sobre uma tabela em um banco de dados.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn292202(v=exchg.10).md">JetGetTableInfo (JET_SESID, JET_TABLEID, [], JET_TblInfo)</a></td>
<td>Recupera várias partes de informações sobre uma tabela em um banco de dados.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn292204(v=exchg.10).md">JetGetTableInfo (JET_SESID, JET_TABLEID, Cadeia de caracteres JET_TblInfo)</a></td>
<td>Recupera várias partes de informações sobre uma tabela em um banco de dados.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn292199(v=exchg.10).md">JetGetTruncateLogInfoInstance</a></td>
<td>Usado durante um backup iniciado por <a href="dn292104(v=exchg.10).md">JetBeginExternalBackupInstance (JET_INSTANCE, BeginExternalBackupGrbit)</a> para consultar uma instância para obter os nomes dos arquivos de log de transações que podem ser excluídos com segurança depois que o backup for concluído com êxito.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn292203(v=exchg.10).md">JetGetVersion</a></td>
<td>Recupera a versão do mecanismo de banco de dados.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn292200(v=exchg.10).md">JetGotoBookmark</a></td>
<td>Posiciona um cursor para uma entrada de índice para o registro que está associado ao indicador especificado. O indicador pode ser usado com qualquer índice definido em uma tabela. O indicador de um registro pode ser recuperado usando <a href="dn292149(v=exchg.10).md">JetGetBookmark (JET_SESID, JET_TABLEID, [], Int32, Int32)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn292207(v=exchg.10).md">JetGotoPosition</a></td>
<td>Move um cursor para um novo local que é uma fração do caminho por meio do índice atual. Consulte também <a href="dn292181(v=exchg.10).md">JetGetRecordPosition (JET_SESID, JET_TABLEID, JET_RECPOS)</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn292205(v=exchg.10).md">JetGotoSecondaryIndexBookmark</a></td>
<td>Posiciona um cursor para uma entrada de índice que está associada ao indicador de índice secundário especificado. O indicador de índice secundário deve ser usado com o mesmo índice na mesma tabela da qual ele foi recuperado originalmente. O indicador de índice secundário para uma entrada de índice pode ser recuperado usando <a href="dn292205(v=exchg.10).md">JetGotoSecondaryIndexBookmark (JET_SESID, JET_TABLEID, [], Int32, [], Int32, GotoSecondaryIndexBookmarkGrbit)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn292206(v=exchg.10).md">JetGrowDatabase</a></td>
<td>Estende o tamanho de um banco de dados que está aberto no momento.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn292208(v=exchg.10).md">JetIdle</a></td>
<td>Executa tarefas de limpeza ociosas ou verifica o status do repositório de versão no ESE.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn292209(v=exchg.10).md">JetIndexRecordCount</a></td>
<td>Conta o número de entradas no índice atual a partir da posição atual para frente. A posição atual é incluída na contagem. A contagem pode ser maior que o número total de registros na tabela se o índice atual estiver sobre uma coluna de valores múltiplos e as instâncias da coluna tiverem vários valores. Se a tabela estiver vazia, 0 será retornado para a contagem.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn292210(v=exchg.10).md">JetInit</a></td>
<td>Inicialize o mecanismo de banco de dados ESENT.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn292214(v=exchg.10).md">JetInit2</a></td>
<td>Inicialize o mecanismo de banco de dados ESENT.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn292212(v=exchg.10).md">JetIntersectIndexes</a></td>
<td>Computa a interseção entre vários conjuntos de entradas de índice de índices secundários diferentes na mesma tabela. Essa operação é útil para localizar o conjunto de registros em uma tabela que corresponde a dois ou mais critérios que podem ser expressos usando intervalos de índice. Consulte também <a href="dn292094(v=exchg.10).md">IntersectIndexes (JET_SESID, [])</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn292216(v=exchg.10).md">JetMakeKey</a></td>
<td>Constrói chaves de pesquisa que podem ser usadas por <a href="dn334003(v=exchg.10).md">JetSeek (JET_SESID, JET_TABLEID, SeekGrbit)</a> e <a href="dn334024(v=exchg.10).md">JetSetIndexRange (JET_SESID, JET_TABLEID, SetIndexRangeGrbit)</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn292218(v=exchg.10).md">JetMove (JET_SESID, JET_TABLEID, JET_Move, MoveGrbit)</a></td>
<td>Navegar por um índice. O cursor pode ser posicionado no início ou no final do índice e movido para trás e encaminhado por um número especificado de entradas de índice. Consulte também <a href="dn334150(v=exchg.10).md">TryMoveFirst (JET_SESID, JET_TABLEID)</a>, <a href="dn334140(v=exchg.10).md">TryMoveLast (JET_SESID, JET_TABLEID)</a>, <a href="dn334095(v=exchg.10).md">TryMoveNext (JET_SESID, JET_TABLEID)</a>, <a href="dn334144(v=exchg.10).md">TryMovePrevious (JET_SESID, JET_TABLEID)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn292217(v=exchg.10).md">JetMove (JET_SESID, JET_TABLEID, Int32, MoveGrbit)</a></td>
<td>Navegar por um índice. O cursor pode ser posicionado no início ou no final do índice e movido para trás e encaminhado por um número especificado de entradas de índice. Consulte também <a href="dn334150(v=exchg.10).md">TryMoveFirst (JET_SESID, JET_TABLEID)</a>, <a href="dn334140(v=exchg.10).md">TryMoveLast (JET_SESID, JET_TABLEID)</a>, <a href="dn334095(v=exchg.10).md">TryMoveNext (JET_SESID, JET_TABLEID)</a>, <a href="dn334144(v=exchg.10).md">TryMovePrevious (JET_SESID, JET_TABLEID)</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn292219(v=exchg.10).md">JetOpenDatabase</a></td>
<td>Abre um banco de dados anexado anteriormente com <a href="dn292096(v=exchg.10).md">JetAttachDatabase (JET_SESID, String, AttachDatabaseGrbit)</a>para uso com uma sessão de banco de dados. Essa função pode ser chamada várias vezes para o mesmo banco de dados.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn292230(v=exchg.10).md">JetOpenFileInstance</a></td>
<td>Abre um banco de dados anexado, um arquivo de patch de banco de dados ou um arquivo de log de transações de uma instância ativa com a finalidade de executar um backup difuso de streaming. Os dados desses arquivos podem, subsequentemente, ser lidos por meio do identificador retornado usando JetReadFileInstance. O identificador retornado deve ser fechado usando JetCloseFileInstance. Um backup externo da instância deve ter sido iniciado anteriormente usando JetBeginExternalBackupInstance.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn292234(v=exchg.10).md">JetOpenTable</a></td>
<td>Abre um cursor em uma tabela criada anteriormente.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn292231(v=exchg.10).md">JetOpenTempTable</a></td>
<td>Cria uma tabela temporária com um único índice. Uma tabela temporária armazena e recupera registros, assim como uma tabela comum criada usando JetCreateTableColumnIndex. No entanto, as tabelas temporárias são muito mais rápidas do que as tabelas comuns devido à sua natureza volátil. Eles também podem ser usados para classificar e executar com muita rapidez a remoção de duplicidades em conjuntos de registros quando acessados de forma puramente sequencial. Consulte também <a href="dn292233(v=exchg.10).md">JetOpenTempTable3 (JET_SESID, [], Int32, JET_UNICODEINDEX, TempTableGrbit, JET_TABLEID, [])</a>. <a href="dn335326(v=exchg.10).md">JetOpenTemporaryTable (JET_SESID, JET_OPENTEMPORARYTABLE)</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn292232(v=exchg.10).md">JetOpenTempTable2</a></td>
<td>Cria uma tabela temporária com um único índice. Uma tabela temporária armazena e recupera registros, assim como uma tabela comum criada usando JetCreateTableColumnIndex. No entanto, as tabelas temporárias são muito mais rápidas do que as tabelas comuns devido à sua natureza volátil. Eles também podem ser usados para classificar e executar com muita rapidez a remoção de duplicidades em conjuntos de registros quando acessados de forma puramente sequencial. Consulte também <a href="dn292231(v=exchg.10).md">JetOpenTempTable (JET_SESID, [], Int32, TempTableGrbit, JET_TABLEID, [])</a>, <a href="dn292233(v=exchg.10).md">JetOpenTempTable3 (JET_SESID, [], Int32, JET_UNICODEINDEX, TempTableGrbit, JET_TABLEID, [])</a>. <a href="dn335326(v=exchg.10).md">JetOpenTemporaryTable (JET_SESID, JET_OPENTEMPORARYTABLE)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn292233(v=exchg.10).md">JetOpenTempTable3</a></td>
<td>Cria uma tabela temporária com um único índice. Uma tabela temporária armazena e recupera registros, assim como uma tabela comum criada usando JetCreateTableColumnIndex. No entanto, as tabelas temporárias são muito mais rápidas do que as tabelas comuns devido à sua natureza volátil. Eles também podem ser usados para classificar e executar com muita rapidez a remoção de duplicidades em conjuntos de registros quando acessados de forma puramente sequencial. Consulte também <a href="dn292231(v=exchg.10).md">JetOpenTempTable (JET_SESID, [], Int32, TempTableGrbit, JET_TABLEID, [])</a>, <a href="dn335326(v=exchg.10).md">JetOpenTemporaryTable (JET_SESID, JET_OPENTEMPORARYTABLE)</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn332998(v=exchg.10).md">JetOSSnapshotFreeze</a></td>
<td>Inicia um instantâneo. Enquanto o instantâneo está em andamento, nenhuma atividade de gravação em disco pelo mecanismo pode ocorrer.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn292235(v=exchg.10).md">JetOSSnapshotPrepare</a></td>
<td>Inicia a preparação para uma sessão de instantâneo. Uma sessão de instantâneo é um intervalo de tempo curto no qual o mecanismo não emite nenhum IOs de gravação para o disco, para que o mecanismo possa participar de uma sessão de instantâneo de volume (quando controlada por um gravador de instantâneo).</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn332986(v=exchg.10).md">JetOSSnapshotThaw</a></td>
<td>Notifica o mecanismo de que ele pode retomar as operações de e/s normais após um período de congelamento e um instantâneo bem-sucedido.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn332988(v=exchg.10).md">JetPrepareUpdate</a></td>
<td>Prepare um cursor para atualização.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn332987(v=exchg.10).md">JetReadFileInstance</a></td>
<td>Recupera o conteúdo de um arquivo aberto com <a href="dn292230(v=exchg.10).md">JetOpenFileInstance (JET_INSTANCE, String, JET_HANDLE, Int64, Int64)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn332989(v=exchg.10).md">JetRegisterCallback</a></td>
<td>Permite que o aplicativo configure o mecanismo de banco de dados para emitir notificações para o aplicativo para eventos específicos. Essas notificações são associadas a uma tabela específica e permanecem em vigor somente até que a instância que contém a tabela seja desligada usando <a href="dn334020(v=exchg.10).md">JetTerm (JET_INSTANCE)</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn332990(v=exchg.10).md">JetRenameColumn</a></td>
<td>Altera o nome de uma coluna existente.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn332993(v=exchg.10).md">JetRenameTable</a></td>
<td>Altera o nome de uma tabela existente.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn332991(v=exchg.10).md">JetResetSessionContext</a></td>
<td>Desassocia uma sessão do thread atual. Isso deve ser usado em conjunto com <a href="dn334027(v=exchg.10).md">JetSetSessionContext (JET_SESID, IntPtr)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn332994(v=exchg.10).md">JetResetTableSequential</a></td>
<td>Notifica o mecanismo de banco de dados de que o aplicativo não está mais verificando o índice inteiro no qual o cursor está posicionado. Essa chamada reverte uma notificação enviada por <a href="dn334018(v=exchg.10).md">JetSetTableSequential (JET_SESID, JET_TABLEID, SetTableSequentialGrbit)</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn332992(v=exchg.10).md">JetRestoreInstance</a></td>
<td>Restaura e recupera um backup de streaming de uma instância do, incluindo todos os bancos de dados anexados. Ele foi projetado para funcionar com um backup criado com a função <a href="dn292102(v=exchg.10).md">JetBackupInstance (JET_INSTANCE, String, BackupGrbit, JET_PFNSTATUS)</a> . Essa é a função de restauração mais simples e encapsulada.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn332995(v=exchg.10).md">JetRetrieveColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, [], Int32, Int32, RetrieveColumnGrbit, JET_RETINFO)</a></td>
<td>Recupera um valor de coluna única do registro atual. O registro é aquele associado à entrada de índice na posição atual do cursor. Como alternativa, essa função pode recuperar uma coluna de um registro que está sendo criado no buffer de cópia do cursor. Essa função também pode recuperar dados de coluna de uma entrada de índice que faz referência ao registro atual. Além de recuperar o valor real da coluna, JetRetrieveColumn também pode ser usado para recuperar o tamanho de uma coluna, antes de recuperar os dados da coluna em si, para que os buffers de aplicativo possam ser dimensionados adequadamente.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn332997(v=exchg.10).md">JetRetrieveColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, [], Int32, Int32, Int32, RetrieveColumnGrbit, JET_RETINFO)</a></td>
<td>Recupera um valor de coluna única do registro atual. O registro é aquele associado à entrada de índice na posição atual do cursor. Como alternativa, essa função pode recuperar uma coluna de um registro que está sendo criado no buffer de cópia do cursor. Essa função também pode recuperar dados de coluna de uma entrada de índice que faz referência ao registro atual. Além de recuperar o valor real da coluna, JetRetrieveColumn também pode ser usado para recuperar o tamanho de uma coluna, antes de recuperar os dados da coluna em si, para que os buffers de aplicativo possam ser dimensionados adequadamente.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn334004(v=exchg.10).md">JetRetrieveColumns</a></td>
<td>Recupera vários valores de coluna do registro atual em uma única operação. Uma matriz de estruturas de JET_RETRIEVECOLUMN é usada para descrever o conjunto de valores de coluna a serem recuperados e para descrever os buffers de saída para cada valor de coluna a ser recuperado.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn334002(v=exchg.10).md">JetRetrieveKey</a></td>
<td>Recupera a chave da entrada de índice na posição atual de um cursor. Consulte também <a href="dn334085(v=exchg.10).md">RetrieveKey (JET_SESID, JET_TABLEID, RetrieveKeyGrbit)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn334001(v=exchg.10).md">JetRollback</a></td>
<td>Desfaz as alterações feitas no estado do banco de dados e retorna ao último ponto de salvamento. O JetRollback também fechará todos os cursores abertos durante o ponto de salvamento. Se o ponto de salvamento mais externo for desfeito, a sessão sairá da transação.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn334003(v=exchg.10).md">JetSeek</a></td>
<td>Posiciona com eficiência um cursor para uma entrada de índice que corresponda aos critérios de pesquisa especificados pela chave de pesquisa nesse cursor e à desigualdade especificada. Uma chave de pesquisa deve ter sido construída anteriormente usando <a href="dn292216(v=exchg.10).md">JetMakeKey (JET_SESID, JET_TABLEID, [], Int32, MakeKeyGrbit)</a>. Consulte também <a href="dn334145(v=exchg.10).md">TrySeek (JET_SESID, JET_TABLEID, SeekGrbit)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn334009(v=exchg.10).md">JetSetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, [], Int32, SetColumnGrbit, JET_SETINFO)</a></td>
<td>A função JetSetColumn modifica um valor de coluna única em um registro modificado a ser inserido ou para atualizar o registro atual. Ele pode substituir um valor existente, adicionar um novo valor a uma sequência de valores em uma coluna com vários valores, remover um valor de uma sequência de valores em uma coluna com vários valores ou atualizar todo ou parte de um valor longo (uma coluna do tipo <a href="hh577895(v=exchg.10).md">LONGTEXT</a> ou <a href="hh577895(v=exchg.10).md">LongBinary</a>).</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn334008(v=exchg.10).md">JetSetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, [], Int32, Int32, SetColumnGrbit, JET_SETINFO)</a></td>
<td>A função JetSetColumn modifica um valor de coluna única em um registro modificado a ser inserido ou para atualizar o registro atual. Ele pode substituir um valor existente, adicionar um novo valor a uma sequência de valores em uma coluna com vários valores, remover um valor de uma sequência de valores em uma coluna com vários valores ou atualizar todo ou parte de um valor longo (uma coluna do tipo <a href="hh577895(v=exchg.10).md">LONGTEXT</a> ou <a href="hh577895(v=exchg.10).md">LongBinary</a>).</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn334010(v=exchg.10).md">JetSetColumnDefaultValue</a></td>
<td>Altera o valor padrão de uma coluna existente.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn334006(v=exchg.10).md">JetSetColumns</a></td>
<td>Permite que um aplicativo defina vários valores de coluna em uma única operação. Uma matriz de estruturas de <a href="dn335260(v=exchg.10).md">JET_SETCOLUMN</a> é usada para descrever o conjunto de valores de coluna a ser definido e para descrever os buffers de entrada para cada valor de coluna a ser definido.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn334011(v=exchg.10).md">JetSetCurrentIndex</a></td>
<td>Define o índice atual de um cursor.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn334005(v=exchg.10).md">JetSetCurrentIndex2</a></td>
<td>Define o índice atual de um cursor.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn334012(v=exchg.10).md">JetSetCurrentIndex3</a></td>
<td>Define o índice atual de um cursor.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn334013(v=exchg.10).md">JetSetCurrentIndex4</a></td>
<td>Define o índice atual de um cursor.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn334014(v=exchg.10).md">JetSetDatabaseSize</a></td>
<td>Define o tamanho de um arquivo de banco de dados não aberto.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn334024(v=exchg.10).md">JetSetIndexRange</a></td>
<td>Limita temporariamente o conjunto de entradas de índice que o cursor pode percorrer usando <a href="dn292217(v=exchg.10).md">JetMove (JET_SESID, JET_TABLEID, Int32, MoveGrbit)</a> para aqueles que começam da entrada de índice atual e terminam na entrada de índice que corresponde aos critérios de pesquisa especificados pela chave de pesquisa no cursor e nos critérios de associação especificados. Uma chave de pesquisa deve ter sido construída anteriormente usando <a href="dn292216(v=exchg.10).md">JetMakeKey (JET_SESID, JET_TABLEID, [], Int32, MakeKeyGrbit)</a>. Consulte também <a href="dn334099(v=exchg.10).md">TrySetIndexRange (JET_SESID, JET_TABLEID, SetIndexRangeGrbit)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn334015(v=exchg.10).md">JetSetLS</a></td>
<td>Permite que o aplicativo associe um identificador de contexto conhecido como armazenamento local com um cursor ou a tabela associada a esse cursor. Esse identificador de contexto pode ser usado pelo aplicativo para armazenar dados auxiliares associados a um cursor ou tabela. O aplicativo é notificado posteriormente usando um retorno de chamada de tempo de execução quando o identificador de contexto deve ser liberado. Isso torna possível associar o estado alocado dinamicamente a um cursor ou tabela.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn334027(v=exchg.10).md">JetSetSessionContext</a></td>
<td>Associa uma sessão com o thread atual usando o identificador de contexto fornecido. Essa associação substitui o requisito de mecanismo padrão que uma transação para uma determinada sessão deve ocorrer inteiramente no mesmo thread. Use <a href="dn332991(v=exchg.10).md">JetResetSessionContext (JET_SESID)</a> para remover a associação.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn334028(v=exchg.10).md">JetSetSystemParameter (JET_INSTANCE, JET_SESID, JET_param, JET_CALLBACK, Cadeia de caracteres)</a></td>
<td>Define opções de configuração do banco de dados.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn334017(v=exchg.10).md">JetSetSystemParameter (JET_INSTANCE, JET_SESID, JET_param, Int32, Cadeia de caracteres)</a></td>
<td>Define opções de configuração do banco de dados.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn334029(v=exchg.10).md">JetSetSystemParameter (JET_INSTANCE, JET_SESID, JET_param, IntPtr, Cadeia de caracteres)</a></td>
<td>Define opções de configuração do banco de dados.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn334018(v=exchg.10).md">JetSetTableSequential</a></td>
<td>Notifica o mecanismo de banco de dados de que o aplicativo está verificando o índice inteiro no qual o cursor está posicionado. Consequentemente, os métodos usados para acessar os dados do índice serão ajustados para tornar esse cenário o mais rápido possível. Consulte também <a href="dn332994(v=exchg.10).md">JetResetTableSequential (JET_SESID, JET_TABLEID, ResetTableSequentialGrbit)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn334032(v=exchg.10).md">JetStopBackupInstance</a></td>
<td>Impede que a atividade relacionada ao backup de streaming continue em uma instância em execução específica, encerrando assim o backup de streaming de forma previsível.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn334035(v=exchg.10).md">JetStopServiceInstance</a></td>
<td>Prepara uma instância para encerramento.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn334020(v=exchg.10).md">JetTerm</a></td>
<td>Finalize uma instância que foi criada com <a href="dn292210(v=exchg.10).md">JetInit (JET_INSTANCE)</a> ou <a href="dn292122(v=exchg.10).md">JetCreateInstance (JET_INSTANCE, String)</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn334037(v=exchg.10).md">JetTerm2</a></td>
<td>Finalize uma instância que foi criada com <a href="dn292210(v=exchg.10).md">JetInit (JET_INSTANCE)</a> ou <a href="dn292122(v=exchg.10).md">JetCreateInstance (JET_INSTANCE, String)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn334022(v=exchg.10).md">JetTruncateLogInstance</a></td>
<td>Usado durante um backup iniciado pelo JetBeginExternalBackup para excluir qualquer arquivo de log de transações que não será mais necessário depois que o backup atual for concluído com êxito.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn334019(v=exchg.10).md">JetUnregisterCallback</a></td>
<td>Configura o mecanismo de banco de dados para parar de emitir notificações para o aplicativo conforme solicitado anteriormente por meio <a href="dn332989(v=exchg.10).md">de JetRegisterCallback (JET_SESID, JET_TABLEID, JET_cbtyp, JET_CALLBACK, IntPtr, JET_HANDLE)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn334036(v=exchg.10).md">JetUpdate (JET_SESID, JET_TABLEID)</a></td>
<td>A função JetUpdate executa uma operação de atualização, incluindo a inserção de uma nova linha em uma tabela ou a atualização de uma linha existente. A exclusão de uma linha de tabela é executada chamando <a href="dn292131(v=exchg.10).md">JetDelete (JET_SESID, JET_TABLEID)</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn334023(v=exchg.10).md">JetUpdate (JET_SESID, JET_TABLEID, [], Int32, Int32)</a></td>
<td>A função JetUpdate executa uma operação de atualização, incluindo a inserção de uma nova linha em uma tabela ou a atualização de uma linha existente. A exclusão de uma linha de tabela é executada chamando <a href="dn292131(v=exchg.10).md">JetDelete (JET_SESID, JET_TABLEID)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn334042(v=exchg.10).md">MakeKey (JET_SESID, JET_TABLEID, booliano, MakeKeyGrbit)</a></td>
<td>Constrói uma chave de pesquisa que pode ser usada por <a href="dn334003(v=exchg.10).md">JetSeek (JET_SESID, JET_TABLEID, SeekGrbit)</a> e <a href="dn334024(v=exchg.10).md">JetSetIndexRange (JET_SESID, JET_TABLEID, SetIndexRangeGrbit)</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn334026(v=exchg.10).md">MakeKey (JET_SESID, JET_TABLEID, byte, MakeKeyGrbit)</a></td>
<td>Constrói uma chave de pesquisa que pode ser usada por <a href="dn334003(v=exchg.10).md">JetSeek (JET_SESID, JET_TABLEID, SeekGrbit)</a> e <a href="dn334024(v=exchg.10).md">JetSetIndexRange (JET_SESID, JET_TABLEID, SetIndexRangeGrbit)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn334044(v=exchg.10).md">MakeKey (JET_SESID, JET_TABLEID, [], MakeKeyGrbit)</a></td>
<td>Constrói uma chave de pesquisa que pode ser usada por <a href="dn334003(v=exchg.10).md">JetSeek (JET_SESID, JET_TABLEID, SeekGrbit)</a> e <a href="dn334024(v=exchg.10).md">JetSetIndexRange (JET_SESID, JET_TABLEID, SetIndexRangeGrbit)</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn334025(v=exchg.10).md">MakeKey (JET_SESID, JET_TABLEID, DateTime, MakeKeyGrbit)</a></td>
<td>Constrói uma chave de pesquisa que pode ser usada por <a href="dn334003(v=exchg.10).md">JetSeek (JET_SESID, JET_TABLEID, SeekGrbit)</a> e <a href="dn334024(v=exchg.10).md">JetSetIndexRange (JET_SESID, JET_TABLEID, SetIndexRangeGrbit)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn334046(v=exchg.10).md">MakeKey (JET_SESID, JET_TABLEID, Double, MakeKeyGrbit)</a></td>
<td>Constrói uma chave de pesquisa que pode ser usada por <a href="dn334003(v=exchg.10).md">JetSeek (JET_SESID, JET_TABLEID, SeekGrbit)</a> e <a href="dn334024(v=exchg.10).md">JetSetIndexRange (JET_SESID, JET_TABLEID, SetIndexRangeGrbit)</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn334030(v=exchg.10).md">MakeKey (JET_SESID, JET_TABLEID, GUID, MakeKeyGrbit)</a></td>
<td>Constrói uma chave de pesquisa que pode ser usada por <a href="dn334003(v=exchg.10).md">JetSeek (JET_SESID, JET_TABLEID, SeekGrbit)</a> e <a href="dn334024(v=exchg.10).md">JetSetIndexRange (JET_SESID, JET_TABLEID, SetIndexRangeGrbit)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn334048(v=exchg.10).md">MakeKey (JET_SESID, JET_TABLEID, Int16, MakeKeyGrbit)</a></td>
<td>Constrói uma chave de pesquisa que pode ser usada por <a href="dn334003(v=exchg.10).md">JetSeek (JET_SESID, JET_TABLEID, SeekGrbit)</a> e <a href="dn334024(v=exchg.10).md">JetSetIndexRange (JET_SESID, JET_TABLEID, SetIndexRangeGrbit)</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn334031(v=exchg.10).md">MakeKey (JET_SESID, JET_TABLEID, Int32, MakeKeyGrbit)</a></td>
<td>Constrói uma chave de pesquisa que pode ser usada por <a href="dn334003(v=exchg.10).md">JetSeek (JET_SESID, JET_TABLEID, SeekGrbit)</a> e <a href="dn334024(v=exchg.10).md">JetSetIndexRange (JET_SESID, JET_TABLEID, SetIndexRangeGrbit)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn334050(v=exchg.10).md">MakeKey (JET_SESID, JET_TABLEID, Int64, MakeKeyGrbit)</a></td>
<td>Constrói uma chave de pesquisa que pode ser usada por <a href="dn334003(v=exchg.10).md">JetSeek (JET_SESID, JET_TABLEID, SeekGrbit)</a> e <a href="dn334024(v=exchg.10).md">JetSetIndexRange (JET_SESID, JET_TABLEID, SetIndexRangeGrbit)</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn334033(v=exchg.10).md">MakeKey (JET_SESID, JET_TABLEID, única, MakeKeyGrbit)</a></td>
<td>Constrói uma chave de pesquisa que pode ser usada por <a href="dn334003(v=exchg.10).md">JetSeek (JET_SESID, JET_TABLEID, SeekGrbit)</a> e <a href="dn334024(v=exchg.10).md">JetSetIndexRange (JET_SESID, JET_TABLEID, SetIndexRangeGrbit)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn334052(v=exchg.10).md">MakeKey (JET_SESID, JET_TABLEID, UInt16, MakeKeyGrbit)</a></td>
<td>Constrói uma chave de pesquisa que pode ser usada por <a href="dn334003(v=exchg.10).md">JetSeek (JET_SESID, JET_TABLEID, SeekGrbit)</a> e <a href="dn334024(v=exchg.10).md">JetSetIndexRange (JET_SESID, JET_TABLEID, SetIndexRangeGrbit)</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn334054(v=exchg.10).md">MakeKey (JET_SESID, JET_TABLEID, UInt32, MakeKeyGrbit)</a></td>
<td>Constrói uma chave de pesquisa que pode ser usada por <a href="dn334003(v=exchg.10).md">JetSeek (JET_SESID, JET_TABLEID, SeekGrbit)</a> e <a href="dn334024(v=exchg.10).md">JetSetIndexRange (JET_SESID, JET_TABLEID, SetIndexRangeGrbit)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn334034(v=exchg.10).md">MakeKey (JET_SESID, JET_TABLEID, UInt64, MakeKeyGrbit)</a></td>
<td>Constrói uma chave de pesquisa que pode ser usada por <a href="dn334003(v=exchg.10).md">JetSeek (JET_SESID, JET_TABLEID, SeekGrbit)</a> e <a href="dn334024(v=exchg.10).md">JetSetIndexRange (JET_SESID, JET_TABLEID, SetIndexRangeGrbit)</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn334038(v=exchg.10).md">MakeKey (JET_SESID, JET_TABLEID, Cadeia de caracteres, codificação, MakeKeyGrbit)</a></td>
<td>Constrói uma chave de pesquisa que pode ser usada por <a href="dn334003(v=exchg.10).md">JetSeek (JET_SESID, JET_TABLEID, SeekGrbit)</a> e <a href="dn334024(v=exchg.10).md">JetSetIndexRange (JET_SESID, JET_TABLEID, SetIndexRangeGrbit)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn334058(v=exchg.10).md">MoveAfterLast</a></td>
<td>Posicionar o cursor após o último registro na tabela. Uma movimentação subsequente anterior posicionará o cursor no último registro.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn334057(v=exchg.10).md">MoveBeforeFirst</a></td>
<td>Posicionar o cursor antes do primeiro registro na tabela. Em seguida, uma movimentação subsequente posicionará o cursor no primeiro registro.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn334040(v=exchg.10).md">ResetIndexRange</a></td>
<td>Remove um intervalo de índice criado com <a href="dn334024(v=exchg.10).md">JetSetIndexRange (JET_SESID, JET_TABLEID, SetIndexRangeGrbit)</a> ou <a href="dn334099(v=exchg.10).md">TrySetIndexRange (JET_SESID, JET_TABLEID, SetIndexRangeGrbit)</a>. Se nenhum intervalo de índice estiver presente, esse método não fará nada.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn334041(v=exchg.10).md">RetrieveColumn (JET_SESID, JET_TABLEID, JET_COLUMNID)</a></td>
<td>Recupera um valor de coluna única do registro atual. O registro é aquele associado à entrada de índice na posição atual do cursor.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn334060(v=exchg.10).md">RetrieveColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit, JET_RETINFO)</a></td>
<td>Recupera um valor de coluna única do registro atual. O registro é aquele associado à entrada de índice na posição atual do cursor. Como alternativa, essa função pode recuperar uma coluna de um registro que está sendo criado no buffer de cópia do cursor. Essa função também pode recuperar dados de coluna de uma entrada de índice que faz referência ao registro atual. Além de recuperar o valor real da coluna, JetRetrieveColumn também pode ser usado para recuperar o tamanho de uma coluna, antes de recuperar os dados da coluna em si, para que os buffers de aplicativo possam ser dimensionados adequadamente.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn334045(v=exchg.10).md">RetrieveColumnAsBoolean (JET_SESID, JET_TABLEID, JET_COLUMNID)</a></td>
<td>Recupera um valor de coluna booliana do registro atual. O registro é aquele associado à entrada de índice na posição atual do cursor.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn334078(v=exchg.10).md">RetrieveColumnAsBoolean (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)</a></td>
<td>Recupera um valor de coluna booliana do registro atual. O registro é aquele associado à entrada de índice na posição atual do cursor.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn334047(v=exchg.10).md">RetrieveColumnAsByte (JET_SESID, JET_TABLEID, JET_COLUMNID)</a></td>
<td>Recupera um valor de coluna de byte do registro atual. O registro é aquele associado à entrada de índice na posição atual do cursor.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn334074(v=exchg.10).md">RetrieveColumnAsByte (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)</a></td>
<td>Recupera um valor de coluna de byte do registro atual. O registro é aquele associado à entrada de índice na posição atual do cursor.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn334077(v=exchg.10).md">RetrieveColumnAsDateTime (JET_SESID, JET_TABLEID, JET_COLUMNID)</a></td>
<td>Recupera um valor de coluna datetime do registro atual. O registro é aquele associado à entrada de índice na posição atual do cursor.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn334051(v=exchg.10).md">RetrieveColumnAsDateTime (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)</a></td>
<td>Recupera um valor de coluna datetime do registro atual. O registro é aquele associado à entrada de índice na posição atual do cursor.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn334053(v=exchg.10).md">RetrieveColumnAsDouble (JET_SESID, JET_TABLEID, JET_COLUMNID)</a></td>
<td>Recupera um valor de coluna dupla do registro atual. O registro é aquele associado à entrada de índice na posição atual do cursor.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn334084(v=exchg.10).md">RetrieveColumnAsDouble (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)</a></td>
<td>Recupera um valor de coluna dupla do registro atual. O registro é aquele associado à entrada de índice na posição atual do cursor.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn334056(v=exchg.10).md">RetrieveColumnAsFloat (JET_SESID, JET_TABLEID, JET_COLUMNID)</a></td>
<td>Recupera um valor de coluna float do registro atual. O registro é aquele associado à entrada de índice na posição atual do cursor.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn334092(v=exchg.10).md">RetrieveColumnAsFloat (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)</a></td>
<td>Recupera um valor de coluna float do registro atual. O registro é aquele associado à entrada de índice na posição atual do cursor.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn334093(v=exchg.10).md">RetrieveColumnAsGuid (JET_SESID, JET_TABLEID, JET_COLUMNID)</a></td>
<td>Recupera um valor de coluna GUID do registro atual. O registro é aquele associado à entrada de índice na posição atual do cursor.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn334061(v=exchg.10).md">RetrieveColumnAsGuid (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)</a></td>
<td>Recupera um valor de coluna GUID do registro atual. O registro é aquele associado à entrada de índice na posição atual do cursor.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn334062(v=exchg.10).md">RetrieveColumnAsInt16 (JET_SESID, JET_TABLEID, JET_COLUMNID)</a></td>
<td>Recupera um valor de coluna única do registro atual. O registro é aquele associado à entrada de índice na posição atual do cursor.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn334098(v=exchg.10).md">RetrieveColumnAsInt16 (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)</a></td>
<td>Recupera um valor de coluna Int16 do registro atual. O registro é aquele associado à entrada de índice na posição atual do cursor.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn334100(v=exchg.10).md">RetrieveColumnAsInt32 (JET_SESID, JET_TABLEID, JET_COLUMNID)</a></td>
<td>Recupera um valor de coluna única do registro atual. O registro é aquele associado à entrada de índice na posição atual do cursor.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn334068(v=exchg.10).md">RetrieveColumnAsInt32 (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)</a></td>
<td>Recupera um valor de coluna Int32 do registro atual. O registro é aquele associado à entrada de índice na posição atual do cursor.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn334066(v=exchg.10).md">RetrieveColumnAsInt64 (JET_SESID, JET_TABLEID, JET_COLUMNID)</a></td>
<td>Recupera um valor de coluna única do registro atual. O registro é aquele associado à entrada de índice na posição atual do cursor.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn334091(v=exchg.10).md">RetrieveColumnAsInt64 (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)</a></td>
<td>Recupera um valor de coluna única do registro atual. O registro é aquele associado à entrada de índice na posição atual do cursor.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn334067(v=exchg.10).md">RetrieveColumnAsString (JET_SESID, JET_TABLEID, JET_COLUMNID)</a></td>
<td>Recupera um valor de coluna única do registro atual. O registro é aquele associado à entrada de índice na posição atual do cursor. A codificação Unicode é usada.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn334103(v=exchg.10).md">RetrieveColumnAsString (JET_SESID, JET_TABLEID, JET_COLUMNID, codificação)</a></td>
<td>Recupera um valor de coluna de cadeia de caracteres do registro atual. O registro é aquele associado à entrada de índice na posição atual do cursor.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn334070(v=exchg.10).md">RetrieveColumnAsString (JET_SESID, JET_TABLEID, JET_COLUMNID, codificação, RetrieveColumnGrbit)</a></td>
<td>Recupera um valor de coluna de cadeia de caracteres do registro atual. O registro é aquele associado à entrada de índice na posição atual do cursor.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn334069(v=exchg.10).md">RetrieveColumnAsUInt16 (JET_SESID, JET_TABLEID, JET_COLUMNID)</a></td>
<td>Recupera um valor de coluna UInt16 do registro atual. O registro é aquele associado à entrada de índice na posição atual do cursor.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn334106(v=exchg.10).md">RetrieveColumnAsUInt16 (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)</a></td>
<td>Recupera um valor de coluna UInt16 do registro atual. O registro é aquele associado à entrada de índice na posição atual do cursor.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn334108(v=exchg.10).md">RetrieveColumnAsUInt32 (JET_SESID, JET_TABLEID, JET_COLUMNID)</a></td>
<td>Recupera um valor de coluna UInt32 do registro atual. O registro é aquele associado à entrada de índice na posição atual do cursor.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn334073(v=exchg.10).md">RetrieveColumnAsUInt32 (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)</a></td>
<td>Recupera um valor de coluna UInt32 do registro atual. O registro é aquele associado à entrada de índice na posição atual do cursor.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn334072(v=exchg.10).md">RetrieveColumnAsUInt64 (JET_SESID, JET_TABLEID, JET_COLUMNID)</a></td>
<td>Recupera um valor de coluna UInt64 do registro atual. O registro é aquele associado à entrada de índice na posição atual do cursor.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn334113(v=exchg.10).md">RetrieveColumnAsUInt64 (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)</a></td>
<td>Recupera um valor de coluna UInt64 do registro atual. O registro é aquele associado à entrada de índice na posição atual do cursor.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn334075(v=exchg.10).md">RetrieveColumns</a></td>
<td>Recupera colunas em objetos Columnvalue.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn334076(v=exchg.10).md">RetrieveColumnSize (JET_SESID, JET_TABLEID, JET_COLUMNID)</a></td>
<td>Recupera o tamanho de um valor de coluna única do registro atual. O registro é aquele associado à entrada de índice na posição atual do cursor. Como alternativa, essa função pode recuperar uma coluna de um registro que está sendo criado no buffer de cópia do cursor. Essa função também pode recuperar dados de coluna de uma entrada de índice que faz referência ao registro atual.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn334117(v=exchg.10).md">RetrieveColumnSize (JET_SESID, JET_TABLEID, JET_COLUMNID, Int32, RetrieveColumnGrbit)</a></td>
<td>Recupera o tamanho de um valor de coluna única do registro atual. O registro é aquele associado à entrada de índice na posição atual do cursor. Como alternativa, essa função pode recuperar uma coluna de um registro que está sendo criado no buffer de cópia do cursor. Essa função também pode recuperar dados de coluna de uma entrada de índice que faz referência ao registro atual.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn334085(v=exchg.10).md">RetrieveKey</a></td>
<td>Recupera a chave da entrada de índice na posição atual de um cursor.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn334120(v=exchg.10).md">SerializeObjectToColumn</a></td>
<td>Gravar uma forma serializada de um objeto em uma coluna.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn334123(v=exchg.10).md">SetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, booliano)</a></td>
<td>Modifica um valor de coluna única em um registro modificado a ser inserido ou para atualizar o registro atual.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn334080(v=exchg.10).md">SetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, Byte)</a></td>
<td>Modifica um valor de coluna única em um registro modificado a ser inserido ou para atualizar o registro atual.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn334121(v=exchg.10).md">SetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, [])</a></td>
<td>Modifica um valor de coluna única em um registro modificado a ser inserido ou para atualizar o registro atual.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn334082(v=exchg.10).md">SetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, DateTime)</a></td>
<td>Modifica um valor de coluna única em um registro modificado a ser inserido ou para atualizar o registro atual.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn334125(v=exchg.10).md">SetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, duplo)</a></td>
<td>Modifica um valor de coluna única em um registro modificado a ser inserido ou para atualizar o registro atual.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn334081(v=exchg.10).md">SetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, GUID)</a></td>
<td>Modifica um valor de coluna única em um registro modificado a ser inserido ou para atualizar o registro atual.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn334127(v=exchg.10).md">SetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, Int16)</a></td>
<td>Modifica um valor de coluna única em um registro modificado a ser inserido ou para atualizar o registro atual.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn334083(v=exchg.10).md">SetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, Int32)</a></td>
<td>Modifica um valor de coluna única em um registro modificado a ser inserido ou para atualizar o registro atual.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn334130(v=exchg.10).md">SetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, Int64)</a></td>
<td>Modifica um valor de coluna única em um registro modificado a ser inserido ou para atualizar o registro atual.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn334087(v=exchg.10).md">SetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, única)</a></td>
<td>Modifica um valor de coluna única em um registro modificado a ser inserido ou para atualizar o registro atual.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn334132(v=exchg.10).md">SetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, UInt16)</a></td>
<td>Modifica um valor de coluna única em um registro modificado a ser inserido ou para atualizar o registro atual.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn334086(v=exchg.10).md">SetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, UInt32)</a></td>
<td>Modifica um valor de coluna única em um registro modificado a ser inserido ou para atualizar o registro atual.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn334135(v=exchg.10).md">SetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, UInt64)</a></td>
<td>Modifica um valor de coluna única em um registro modificado a ser inserido ou para atualizar o registro atual.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn334089(v=exchg.10).md">SetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, [], SetColumnGrbit)</a></td>
<td>Modifica um valor de coluna única em um registro modificado a ser inserido ou para atualizar o registro atual.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn334136(v=exchg.10).md">SetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, Cadeia de caracteres, codificação)</a></td>
<td>Modifica um valor de coluna única em um registro modificado a ser inserido ou para atualizar o registro atual.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn334090(v=exchg.10).md">SetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, Cadeia de caracteres, codificação, SetColumnGrbit)</a></td>
<td>Modifica um valor de coluna única em um registro modificado a ser inserido ou para atualizar o registro atual.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn334138(v=exchg.10).md">Colunas</a></td>
<td>Define colunas de objetos Columnvalue.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn334139(v=exchg.10).md">TryGetLock</a></td>
<td>Reserve explicitamente a capacidade de atualizar uma linha, bloqueio de gravação ou impedir explicitamente que uma linha seja atualizada por qualquer outra sessão, bloqueio de leitura. Normalmente, os bloqueios de gravação de linha são adquiridos implicitamente como resultado da atualização de linhas. Os bloqueios de leitura geralmente não são necessários devido ao controle de versão de registro. No entanto, em alguns casos, uma transação pode desejar bloquear explicitamente uma linha para impor a serialização ou para garantir que uma operação subsequente terá sucesso.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn334094(v=exchg.10).md">TryMove</a></td>
<td>Tente navegar por um índice. Se a navegação for realizada com sucesso, esse método retornará true. Se não houver registro para navegar para esse método retornará false; uma exceção será lançada para outros erros.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn334150(v=exchg.10).md">TryMoveFirst</a></td>
<td>Tente mover para o primeiro registro na tabela. Se a tabela estiver vazia, isso retornará false, se um erro diferente for encontrado, uma exceção será lançada.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn334140(v=exchg.10).md">TryMoveLast</a></td>
<td>Tente mover para o último registro na tabela. Se a tabela estiver vazia, isso retornará false, se um erro diferente for encontrado, uma exceção será lançada.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn334095(v=exchg.10).md">TryMoveNext</a></td>
<td>Tente mover para o próximo registro na tabela. Se não houver um próximo registro, isso retornará false, se um erro diferente for encontrado, uma exceção será lançada.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn334144(v=exchg.10).md">TryMovePrevious</a></td>
<td>Tente mover para o registro anterior na tabela. Se não houver um registro anterior, isso retornará false, se um erro diferente for encontrado, uma exceção será lançada.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn334096(v=exchg.10).md">TryOpenTable</a></td>
<td>Tente abrir uma tabela.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn334145(v=exchg.10).md">TrySeek</a></td>
<td>Posiciona com eficiência um cursor para uma entrada de índice que corresponda aos critérios de pesquisa especificados pela chave de pesquisa nesse cursor e à desigualdade especificada. Uma chave de pesquisa deve ter sido construída anteriormente usando JetMakeKey.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro estático" alt="Static member" /></td>
<td><a href="dn334099(v=exchg.10).md">TrySetIndexRange</a></td>
<td>Limita temporariamente o conjunto de entradas de índice que o cursor pode percorrer usando JetMove para aqueles que começam da entrada de índice atual e terminam na entrada de índice que corresponde aos critérios de pesquisa especificados pela chave de pesquisa nesse cursor e os critérios de associação especificados. Uma chave de pesquisa deve ter sido construída anteriormente usando JetMakeKey. Retorna true se o intervalo de índice não estiver vazio; caso contrário, false.</td>
</tr>
</tbody>
</table>


Parte superior

## <a name="see-also"></a>Confira também

#### <a name="reference"></a>Referência

[Classe de API](./api-class.md)

[Namespace Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
