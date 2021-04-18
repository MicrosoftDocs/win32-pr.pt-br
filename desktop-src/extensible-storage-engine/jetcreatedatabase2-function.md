---
description: 'Saiba mais sobre: função JetCreateDatabase2'
title: Função JetCreateDatabase2
TOCTitle: JetCreateDatabase2 Function
ms:assetid: 267ac69f-49d3-4741-b324-d8510d7a36d3
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269208(v=EXCHG.10)
ms:contentKeyID: 32765511
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCreateDatabase2A
- JetCreateDatabase2W
- JetCreateDatabase2
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a370f88f95a2eb8217dc06124b50c9ed165eb679
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105780346"
---
# <a name="jetcreatedatabase2-function"></a>Função JetCreateDatabase2


_**Aplica-se a:** Windows | Windows Server_

## <a name="jetcreatedatabase2-function"></a>Função JetCreateDatabase2

A função **JetCreateDatabase2** cria e anexa um arquivo de banco de dados a ser usado com o mecanismo de banco de dados ESE com um tamanho máximo de banco de dados especificado. Chamar **JetCreateDatabase2** com *cpgDatabaseSizeMax* definido como zero é idêntico a chamar [JETCREATEDATABASE](./jetcreatedatabase-function.md) com *szConnect* definido como nulo. Atualmente, até sete bancos de dados podem ser criados por instância.

```cpp
    JET_ERR JET_API JetCreateDatabase2(
      __in          JET_SESID sesid,
      __in          const tchar* szFilename,
      __in          const unsigned long cpgDatabaseSizeMax,
      __out         JET_DBID* pdbid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parâmetros

*sesid*

O contexto da sessão de banco de dados a ser usado para a chamada à API.

*szFilename*

O nome do banco de dados a ser criado.

*cpgDatabaseSizeMax*

O tamanho máximo, em páginas de banco de dados, para o banco de dados. O tamanho da página do banco de dados padrão é 4 quilobytes e pode ser alterado com [JetSetSystemParameter](./jetsetsystemparameter-function.md) antes de criar um banco de dados.

Passar zero significa que não há nenhum máximo imposto pelo mecanismo de banco de dados.

*pdbid*

Ponteiro para um buffer que, em uma chamada bem-sucedida, contém o identificador do banco de dados. Em caso de falha, o valor é indefinido.

*grbit*

Um grupo de bits que especifica zero ou mais das opções a seguir.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Valor</p></th>
<th><p>Significado</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_bitDbOverwriteExisting</p></td>
<td><p>Por padrão, se <a href="gg269212(v=exchg.10).md">JetCreateDatabase</a> ou <strong>JetCreateDatabase2</strong> for chamado e o banco de dados já existir, a chamada à API falhará e o banco de dados original não será substituído. JET_bitDbOverwriteExisting altera esse comportamento e o banco de dados antigo será substituído por um novo. Windows XP e posterior.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitDbRecoveryOff</p></td>
<td><p>JET_bitDbRecoveryOff desativa o registro em log. A definição desse bit perde a capacidade de reproduzir arquivos de log e recuperar o banco de dados para um estado utilizável consistente após um evento catastrófico.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitDbShadowingOff</p></td>
<td><p>A configuração JET_bitDbShadowingOff desabilitará a duplicação de algumas estruturas de banco de dados internas (sombreamento). A duplicação dessas estruturas é feita para manter a resiliência. portanto, a configuração JET_bitDbShadowingOff removerá essa resiliência.</p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a>Valor Retornado

Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir. Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Código de retorno</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_errSuccess</p></td>
<td><p>A operação foi concluída com sucesso.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseDuplicate</p></td>
<td><p>O banco de dados nomeado em <em>szFilename</em> já existe. Quando esse erro é retornado, o banco de dados não é anexado.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseInUse</p></td>
<td><p>Pode ser retornado se o acesso exclusivo tiver sido solicitado, mas não puder ser concedido ou se outra sessão já tiver aberto o banco de dados exclusivamente.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseInvalidPages</p></td>
<td><p>Retornado quando <em>cpgDatabaseSizeMax</em> é maior do que o número máximo de páginas permitido em um banco de dados. O máximo atual é 2147483646 (0x7FFFFFFE).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseInvalidPath</p></td>
<td><p>Um caminho inválido foi fornecido em <em>szFilename</em>. <em>szFilename</em> deve ser não nulo. Por padrão, <em>szFilename</em> deve apontar para um diretório existente. O caminho será criado se <em>JET_paramCreatePathIfNotExist</em> estiver definido (consulte <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a>).</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseLocked</p></td>
<td><p>Indica que outra sessão já abriu o banco de dados exclusivamente (usando JET_bitDbExclusive).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseNotFound</p></td>
<td><p>O banco de dados não foi anexado anteriormente (consulte <a href="gg294074(v=exchg.10).md">JetAttachDatabase</a>).</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseSharingViolation</p></td>
<td><p>O arquivo de banco de dados já foi anexado por uma sessão diferente.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInTransaction</p></td>
<td><p>Foi feita uma tentativa de criar um banco de dados em uma transação.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidDatabase</p></td>
<td><p>Foi feita uma tentativa de abrir um arquivo que não é um arquivo de banco de dados válido.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOneDatabasePerSession</p></td>
<td><p>Foi feita uma tentativa de abrir mais de um banco de dados e JET_paramOneDatabasePerSession foi definido. Consulte <a href="gg294139(v=exchg.10).md">parâmetros do sistema</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOutOfMemory</p></td>
<td><p>O sistema ficou com poucos recursos.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTooManyAttachedDatabases</p></td>
<td><p>Somente um número finito de banco de dados pode ser anexado por instância. Atualmente, o limite é de sete bancos de dados por instância.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnDatabaseAttached</p></td>
<td><p>Um aviso não fatal que indica que o arquivo de banco de dados já foi anexado por esta sessão.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnFileOpenReadOnly</p></td>
<td><p>JET_wrnFileOpenReadOnly indica que o arquivo foi anexado somente leitura, mas <a href="gg269212(v=exchg.10).md">JetCreateDatabase</a> não passou JET_bitDbReadOnly. O banco de dados ainda está aberto com acesso somente leitura.</p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a>Comentários

Se o banco de dados especificado em *szFilename* existir e JET_bitDbOverwriteExisting não tiver sido passado, a chamada à API falhará. Se JET_bitDbOverwriteExisting foi passado, o arquivo de banco de dados antigo será excluído primeiro.

Se a API criar um arquivo de banco de dados e, em seguida, atingir outro erro, ele limpará e excluirá o arquivo.

**JetCreateDatabase2** irá abrir implicitamente o banco de dados. Não é necessário, subsequentemente, chamar [JetOpenDatabase](./jetopendatabase-function.md).

#### <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Cliente</strong></p></td>
<td><p>Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p><strong>Servidor</strong></p></td>
<td><p>Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Cabeçalho</strong></p></td>
<td><p>Declarado em ESENT. h.</p></td>
</tr>
<tr class="even">
<td><p><strong>Biblioteca</strong></p></td>
<td><p>Use ESENT. lib.</p></td>
</tr>
<tr class="odd">
<td><p><strong>DLL</strong></p></td>
<td><p>Requer ESENT.dll.</p></td>
</tr>
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Implementado como <strong>JetCreateDatabase2W</strong> (Unicode) e <strong>JetCreateDatabase2A</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Consulte Também

[Arquivos do mecanismo de armazenamento extensível](./extensible-storage-engine-files.md)  
[JET_ERR](./jet-err.md)  
[JET_DBID](./jet-dbid.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JetAttachDatabase](./jetattachdatabase-function.md)  
[JetCloseDatabase](./jetclosedatabase-function.md)  
[JetCreateDatabase](./jetcreatedatabase-function.md)  
[JetOpenDatabase](./jetopendatabase-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[Parâmetros do sistema](./extensible-storage-engine-system-parameters.md)
