---
description: 'Saiba mais sobre: Função JetCreateDatabase2'
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
ms.openlocfilehash: b362b7ada2c0cc2924ce178adda2368faef770bf
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479202"
---
# <a name="jetcreatedatabase2-function"></a>Função JetCreateDatabase2


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetcreatedatabase2-function"></a>Função JetCreateDatabase2

A **função JetCreateDatabase2** cria e anexa um arquivo de banco de dados a ser usado com o mecanismo de banco de dados ESE com um tamanho máximo de banco de dados especificado. Chamar **JetCreateDatabase2** com *cpgDatabaseSizeMax* definido como zero é idêntico a chamar [JetCreateDatabase](./jetcreatedatabase-function.md) com *szConnect* definido como NULL. Atualmente, até sete bancos de dados podem ser criados por instância.

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

O contexto de sessão do banco de dados a ser usado para a chamada à API.

*szFilename*

O nome do banco de dados a ser criado.

*cpgDatabaseSizeMax*

O tamanho máximo, em páginas de banco de dados, para o banco de dados. O tamanho da página do banco de dados padrão é de 4 quilobytes e pode ser alterado com [JetSetSystemParameter](./jetsetsystemparameter-function.md) antes de criar um banco de dados.

Passar zero significa que não há nenhum máximo imposto pelo mecanismo de banco de dados.

*pdbid*

Ponteiro para um buffer que, em uma chamada bem-sucedida, contém o identificador do banco de dados. Em caso de falha, o valor é indefinido.

*grbit*

Um grupo de bits que especifica zero ou mais das opções a seguir.


| <p>Valor</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_bitDbOverwriteExisting</p> | <p>Por padrão, se <a href="gg269212(v=exchg.10).md">JetCreateDatabase</a> ou <strong>JetCreateDatabase2</strong> for chamado e o banco de dados já existir, a chamada à API falhará e o banco de dados original não será substituído. JET_bitDbOverwriteExisting altera esse comportamento e o banco de dados antigo será substituído por um novo. Windows XP e posterior.</p> | 
| <p>JET_bitDbRecoveryOff</p> | <p>JET_bitDbRecoveryOff o registro em log. Definir esse bit perde a capacidade de repetir arquivos de log e recuperar o banco de dados para um estado acessível consistente após um evento catastrófico.</p> | 
| <p>JET_bitDbShadowingOff</p> | <p>Definir JET_bitDbShadowingOff desabilitará a duplicação de algumas estruturas de banco de dados internas (sombreamento). A duplicação dessas estruturas é feita para resiliência, portanto, definir JET_bitDbShadowingOff removerá essa resiliência.</p> | 



### <a name="return-value"></a>Valor Retornado

Essa função retorna o [JET_ERR](./jet-err.md) de dados com um dos códigos de retorno a seguir. Para obter mais informações sobre os possíveis erros de ESE, consulte [Extensible Armazenamento Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Código de retorno</p> | <p>Descrição</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>A operação foi concluída com sucesso.</p> | 
| <p>JET_errDatabaseDuplicate</p> | <p>O banco de dados chamado <em>em szFilename</em> já existe. Quando esse erro é retornado, o banco de dados não é anexado.</p> | 
| <p>JET_errDatabaseInUse</p> | <p>Poderá ser retornado se o acesso exclusivo tiver sido solicitado, mas não puder ser concedido ou se outra sessão já tiver aberto o banco de dados exclusivamente.</p> | 
| <p>JET_errDatabaseInvalidPages</p> | <p>Retornado quando <em>cpgDatabaseSizeMax</em> é maior que o número máximo de páginas permitidas em um banco de dados. O máximo atual é 2147483646 (0x7ffffffe).</p> | 
| <p>JET_errDatabaseInvalidPath</p> | <p>Um caminho inválido foi dado em <em>szFilename.</em> <em>szFilename</em> deve ser não NULL. Por padrão, <em>szFilename</em> deve apontar para um diretório existente. O caminho será criado se <em>JET_paramCreatePathIfNotExist</em> estiver definido (consulte <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a>).</p> | 
| <p>JET_errDatabaseLocked</p> | <p>Indica que outra sessão já abriu o banco de dados exclusivamente (usando JET_bitDbExclusive).</p> | 
| <p>JET_errDatabaseNotFound</p> | <p>O banco de dados não foi anexado anteriormente (consulte <a href="gg294074(v=exchg.10).md">JetAttachDatabase</a>).</p> | 
| <p>JET_errDatabaseSharingViolation</p> | <p>O arquivo de banco de dados já foi anexado por uma sessão diferente.</p> | 
| <p>JET_errInTransaction</p> | <p>Foi feita uma tentativa de criar um banco de dados em uma transação.</p> | 
| <p>JET_errInvalidDatabase</p> | <p>Foi feita uma tentativa de abrir um arquivo que não é um arquivo de banco de dados válido.</p> | 
| <p>JET_errOneDatabasePerSession</p> | <p>Foi feita uma tentativa de abrir mais de um banco de dados e JET_paramOneDatabasePerSession foi definido. Consulte <a href="gg294139(v=exchg.10).md">Parâmetros do sistema</a>.</p> | 
| <p>JET_errOutOfMemory</p> | <p>O sistema ficou sem recursos.</p> | 
| <p>JET_errTooManyAttachedDatabases</p> | <p>Somente um número finito de banco de dados pode ser anexado por instância. Atualmente, o limite é de sete bancos de dados por instância.</p> | 
| <p>JET_wrnDatabaseAttached</p> | <p>Um aviso nãofatal que indica que o arquivo de banco de dados já foi anexado por esta sessão.</p> | 
| <p>JET_wrnFileOpenReadOnly</p> | <p>JET_wrnFileOpenReadOnly indica que o arquivo foi anexado somente leitura, mas <a href="gg269212(v=exchg.10).md">JetCreateDatabase</a> não passou JET_bitDbReadOnly. O banco de dados ainda é aberto com acesso somente leitura.</p> | 



#### <a name="remarks"></a>Comentários

Se o banco de dados especificado *em szFilename* existir e JET_bitDbOverwriteExisting não tiver sido passado, a chamada à API falhará. Se JET_bitDbOverwriteExisting foi passado, o arquivo de banco de dados antigo será excluído primeiro.

Se a API criar um arquivo de banco de dados e, em seguida, receber outro erro, ela limpará e excluirá o arquivo.

**JetCreateDatabase2** abrirá implicitamente o banco de dados. Não é necessário chamar [JetOpenDatabase posteriormente.](./jetopendatabase-function.md)

#### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requer Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>Requer Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</p> | | <p><strong>Cabeçalho</strong></p> | <p>Declarado em Esent.h.</p> | | <p><strong>Biblioteca</strong></p> | <p>Use ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | | <p><strong>Unicode</strong></p> | <p>Implementado como <strong>JetCreateDatabase2W</strong> (Unicode) e <strong>JetCreateDatabase2A</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Consulte Também

[Arquivos extensíveis Armazenamento mecanismo](./extensible-storage-engine-files.md)  
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
