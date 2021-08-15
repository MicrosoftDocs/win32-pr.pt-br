---
description: 'Saiba mais sobre: Função JetCreateDatabase'
title: Função JetCreateDatabase
TOCTitle: JetCreateDatabase Function
ms:assetid: 2b13b038-1694-46d8-b903-9be64384cb06
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269212(v=EXCHG.10)
ms:contentKeyID: 32765515
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCreateDatabase
- JetCreateDatabaseA
- JetCreateDatabaseW
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 788c8e9fcc97d834843f42752d59cd6c8754fd49b99eac829ed5a68ae18cf287
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119358295"
---
# <a name="jetcreatedatabase-function"></a>Função JetCreateDatabase


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetcreatedatabase-function"></a>Função JetCreateDatabase

A **função JetCreateDatabase** cria e anexa um arquivo de banco de dados a ser usado com o mecanismo de banco de dados ESE. Chamar [JetCreateDatabase2](./jetcreatedatabase2-function.md) com *cpgDatabaseSizeMax* definido como zero é idêntico a chamar **JetCreateDatabase** com *szConnect* definido como NULL. Atualmente, até sete bancos de dados podem ser criados por instância.

```cpp
    JET_ERR JET_API JetCreateDatabase(
      __in          JET_SESID sesid,
      __in          JET_PCSTR szFilename,
      __in_opt      JET_PCSTR szConnect,
      __out         JET_DBID* pdbid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parâmetros

*sesid*

O contexto de sessão do banco de dados a ser usado para a chamada à API.

*szFilename*

O nome do banco de dados a ser criado.

*szConnect*

Reservado para uso futuro. Definido como NULL.

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
<td><p>Por padrão, se <strong>JetCreateDatabase</strong> for chamado e o banco de dados já existir, a chamada à API falhará e o banco de dados original não será substituído. JET_bitDbOverwriteExisting altera esse comportamento e o banco de dados antigo será substituído por um novo. Windows XP e posterior.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitDbRecoveryOff</p></td>
<td><p>JET_bitDbRecoveryOff o registro em log. Definir esse bit perde a capacidade de repetir arquivos de log e recuperar o banco de dados para um estado acessível consistente após um evento catastrófico.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitDbShadowingOff</p></td>
<td><p>Definir JET_bitDbShadowingOff desabilitará a duplicação de algumas estruturas de banco de dados internas (sombreamento). A duplicação dessas estruturas é feita para resiliência, portanto, definir JET_bitDbShadowingOff removerá essa resiliência.</p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a>Valor Retornado

Essa função retorna o [JET_ERR](./jet-err.md) tipo de dados com um dos códigos de retorno a seguir. Para obter mais informações sobre os possíveis erros de ESE, consulte [Extensible Armazenamento Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Código de retorno</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_errSuccess</p></td>
<td><p>A operação foi concluída com sucesso.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseDuplicate</p></td>
<td><p>O banco de dados chamado <em>em szFilename</em> já existe. Quando esse erro é retornado, o banco de dados não é anexado.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseInUse</p></td>
<td><p>Poderá ser retornado se o acesso exclusivo tiver sido solicitado, mas não puder ser concedido ou se outra sessão já tiver aberto o banco de dados exclusivamente.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseInvalidPages</p></td>
<td><p>Retornado quando <em>cpgDatabaseSizeMax</em> é maior que o número máximo de páginas permitidas em um banco de dados. O máximo atual é 2147483646 (0x7ffffffe).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseInvalidPath</p></td>
<td><p>Um caminho inválido foi dado em <em>szFilename.</em> <em>szFilename</em> deve ser não NULL. Por padrão, <em>szFilename</em> deve apontar para um diretório existente. O caminho será criado se <em>JET_paramCreatePathIfNotExist</em> estiver definido (consulte <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a>).</p></td>
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
<td><p>Foi feita uma tentativa de abrir mais de um banco de dados e JET_paramOneDatabasePerSession foi definido. Consulte <a href="gg269337(v=exchg.10).md">Parâmetros de banco de dados</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errOutOfMemory</p></td>
<td><p>A operação falhou porque não foi possível alocar memória.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTooManyAttachedDatabases</p></td>
<td><p>Somente um número finito de banco de dados pode ser anexado por instância. Atualmente, o limite é de sete bancos de dados por instância.</p></td>
</tr>
<tr class="even">
<td><p>JET_wrnDatabaseAttached</p></td>
<td><p>Um aviso nãofatal que indica que o arquivo de banco de dados já foi anexado por esta sessão.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnFileOpenReadOnly</p></td>
<td><p>JET_wrnFileOpenReadOnly indica que o arquivo foi anexado somente leitura, mas <strong>JetCreateDatabase</strong> não passou JET_bitDbReadOnly. O banco de dados ainda é aberto com acesso somente leitura.</p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a>Comentários

Se o banco de dados especificado *em szFilename* existir e JET_bitDbOverwriteExisting não tiver sido passado, a chamada à API falhará. Se JET_bitDbOverwriteExisting foi passado, o arquivo de banco de dados antigo será excluído primeiro.

Se a API criar um arquivo de banco de dados e, em seguida, ocorrer outro erro, ela limpará e excluirá o arquivo.

**JetCreateDatabase abrirá** implicitamente o banco de dados. Não é necessariamente chamar [JetOpenDatabase subsequentemente.](./jetopendatabase-function.md)

#### <a name="requirements"></a>Requisitos

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
<tr class="even">
<td><p><strong>Biblioteca</strong></p></td>
<td><p>Use ESENT.lib.</p></td>
</tr>
<tr class="odd">
<td><p><strong>DLL</strong></p></td>
<td><p>Requer ESENT.dll.</p></td>
</tr>
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Implementado como <strong>JetCreateDatabaseW</strong> (Unicode) e <strong>JetCreateDatabaseA</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Consulte Também

[Arquivos extensíveis Armazenamento mecanismo](./extensible-storage-engine-files.md)  
[JET_ERR](./jet-err.md)  
[JET_DBID](./jet-dbid.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JetAttachDatabase](./jetattachdatabase-function.md)  
[JetCloseDatabase](./jetclosedatabase-function.md)  
[JetCreateDatabase2](./jetcreatedatabase2-function.md)  
[JetOpenDatabase](./jetopendatabase-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[Parâmetros do sistema](./extensible-storage-engine-system-parameters.md)
