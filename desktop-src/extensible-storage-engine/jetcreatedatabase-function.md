---
description: 'Saiba mais sobre: função JetCreateDatabase'
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
ms.openlocfilehash: b7b3998d25d4f54d5150ad2a7a7d523f943d2eb7
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122465063"
---
# <a name="jetcreatedatabase-function"></a>Função JetCreateDatabase


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetcreatedatabase-function"></a>Função JetCreateDatabase

A função **JetCreateDatabase** cria e anexa um arquivo de banco de dados a ser usado com o mecanismo de banco de dados ESE. Chamar [JetCreateDatabase2](./jetcreatedatabase2-function.md) com *cpgDatabaseSizeMax* definido como zero é idêntico a chamar **JETCREATEDATABASE** com *szConnect* definido como nulo. Atualmente, até sete bancos de dados podem ser criados por instância.

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

O contexto da sessão de banco de dados a ser usado para a chamada à API.

*szFilename*

O nome do banco de dados a ser criado.

*szConnect*

Reservado para uso futuro. Definido como NULL.

*pdbid*

Ponteiro para um buffer que, em uma chamada bem-sucedida, contém o identificador do banco de dados. Em caso de falha, o valor é indefinido.

*grbit*

Um grupo de bits que especifica zero ou mais das opções a seguir.


| <p>Valor</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_bitDbOverwriteExisting</p> | <p>Por padrão, se <strong>JetCreateDatabase</strong> for chamado e o banco de dados já existir, a chamada à API falhará e o banco de dados original não será substituído. JET_bitDbOverwriteExisting altera esse comportamento e o banco de dados antigo será substituído por um novo. Windows XP e posterior.</p> | 
| <p>JET_bitDbRecoveryOff</p> | <p>JET_bitDbRecoveryOff desativa o registro em log. A definição desse bit perde a capacidade de reproduzir arquivos de log e recuperar o banco de dados para um estado utilizável consistente após um evento catastrófico.</p> | 
| <p>JET_bitDbShadowingOff</p> | <p>A configuração JET_bitDbShadowingOff desabilitará a duplicação de algumas estruturas de banco de dados internas (sombreamento). A duplicação dessas estruturas é feita para manter a resiliência. portanto, a configuração JET_bitDbShadowingOff removerá essa resiliência.</p> | 



### <a name="return-value"></a>Valor Retornado

Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir. para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de Armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).


| <p>Código de retorno</p> | <p>Descrição</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>A operação foi concluída com sucesso.</p> | 
| <p>JET_errDatabaseDuplicate</p> | <p>O banco de dados nomeado em <em>szFilename</em> já existe. Quando esse erro é retornado, o banco de dados não é anexado.</p> | 
| <p>JET_errDatabaseInUse</p> | <p>Pode ser retornado se o acesso exclusivo tiver sido solicitado, mas não puder ser concedido ou se outra sessão já tiver aberto o banco de dados exclusivamente.</p> | 
| <p>JET_errDatabaseInvalidPages</p> | <p>Retornado quando <em>cpgDatabaseSizeMax</em> é maior do que o número máximo de páginas permitido em um banco de dados. O máximo atual é 2147483646 (0x7FFFFFFE).</p> | 
| <p>JET_errDatabaseInvalidPath</p> | <p>Um caminho inválido foi fornecido em <em>szFilename</em>. <em>szFilename</em> deve ser não nulo. Por padrão, <em>szFilename</em> deve apontar para um diretório existente. O caminho será criado se <em>JET_paramCreatePathIfNotExist</em> estiver definido (consulte <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a>).</p> | 
| <p>JET_errDatabaseLocked</p> | <p>Indica que outra sessão já abriu o banco de dados exclusivamente (usando JET_bitDbExclusive).</p> | 
| <p>JET_errDatabaseNotFound</p> | <p>O banco de dados não foi anexado anteriormente (consulte <a href="gg294074(v=exchg.10).md">JetAttachDatabase</a>).</p> | 
| <p>JET_errDatabaseSharingViolation</p> | <p>O arquivo de banco de dados já foi anexado por uma sessão diferente.</p> | 
| <p>JET_errInTransaction</p> | <p>Foi feita uma tentativa de criar um banco de dados em uma transação.</p> | 
| <p>JET_errInvalidDatabase</p> | <p>Foi feita uma tentativa de abrir um arquivo que não é um arquivo de banco de dados válido.</p> | 
| <p>JET_errOneDatabasePerSession</p> | <p>Foi feita uma tentativa de abrir mais de um banco de dados e JET_paramOneDatabasePerSession foi definido. Consulte <a href="gg269337(v=exchg.10).md">parâmetros de banco de dados</a>.</p> | 
| <p>JET_errOutOfMemory</p> | <p>A operação falhou porque não foi possível alocar memória.</p> | 
| <p>JET_errTooManyAttachedDatabases</p> | <p>Somente um número finito de banco de dados pode ser anexado por instância. Atualmente, o limite é de sete bancos de dados por instância.</p> | 
| <p>JET_wrnDatabaseAttached</p> | <p>Um aviso não fatal que indica que o arquivo de banco de dados já foi anexado por esta sessão.</p> | 
| <p>JET_wrnFileOpenReadOnly</p> | <p>JET_wrnFileOpenReadOnly indica que o arquivo foi anexado somente leitura, mas <strong>JetCreateDatabase</strong> não passou JET_bitDbReadOnly. O banco de dados ainda está aberto com acesso somente leitura.</p> | 



#### <a name="remarks"></a>Comentários

Se o banco de dados especificado em *szFilename* existir e JET_bitDbOverwriteExisting não tiver sido passado, a chamada à API falhará. Se JET_bitDbOverwriteExisting foi passado, o arquivo de banco de dados antigo será excluído primeiro.

Se a API criar um arquivo de banco de dados e, em seguida, atingir outro erro, ele limpará e excluirá o arquivo.

**JetCreateDatabase** irá abrir implicitamente o banco de dados. Não é necessariamente chamar [JetOpenDatabase](./jetopendatabase-function.md).

#### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>requer o Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>requer o Windows server 2008, Windows server 2003 ou Windows servidor 2000.</p> | | <p><strong>Cabeçalho</strong></p> | <p>Declarado em ESENT. h.</p> | | <p><strong>Biblioteca</strong></p> | <p>Use ESENT. lib.</p> | | <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | | <p><strong>Unicode</strong></p> | <p>Implementado como <strong>JetCreateDatabaseW</strong> (Unicode) e <strong>JetCreateDatabaseA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Consulte Também

[arquivos do mecanismo de Armazenamento extensível](./extensible-storage-engine-files.md)  
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
