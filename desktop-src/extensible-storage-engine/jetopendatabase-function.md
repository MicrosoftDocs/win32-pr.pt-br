---
description: 'Saiba mais sobre: função JetOpenDatabase'
title: Função JetOpenDatabase
TOCTitle: JetOpenDatabase Function
ms:assetid: 7764f0c2-6795-4b93-be3d-f6830cdce369
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269299(v=EXCHG.10)
ms:contentKeyID: 32765591
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOpenDatabase
- JetOpenDatabaseW
- JetOpenDatabaseA
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3fc7f484921dab0967ea991ac4060e5af7d78ec0
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122988489"
---
# <a name="jetopendatabase-function"></a>Função JetOpenDatabase


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetopendatabase-function"></a>Função JetOpenDatabase

A função **JetOpenDatabase** abre um banco de dados anexado anteriormente, usando as funções [JetAttachDatabase](./jetattachdatabase-function.md) ou [JetAttachDatabase2](./jetattachdatabase2-function.md) , para uso com uma sessão de banco de dados. Essa função pode ser chamada várias vezes para o mesmo banco de dados.

```cpp
    JET_ERR JET_API JetOpenDatabase(
      __in          JET_SESID sesid,
      __in          const tchar* szFilename,
      __in_opt      const tchar* szConnect,
      __out         JET_DBID* pdbid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parâmetros

*sesid*

O contexto da sessão de banco de dados a ser usado para a chamada à API.

*szFilename*

O nome do banco de dados a ser aberto.

*szConnect*

Reservado. Definido como NULL.

*pdbid*

Ponteiro para um buffer que, em uma chamada bem-sucedida, contém o identificador do banco de dados. Se a chamada falhar, o valor será indefinido.

*grbit*

Um grupo de bits que especifica zero ou mais das opções a seguir.


| <p>Valor</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_bitDbExclusive</p> | <p>Permite que apenas uma única sessão anexe um banco de dados. Normalmente, várias sessões podem abrir um banco de dados.</p> | 
| <p>JET_bitDbReadOnly</p> | <p>Impede modificações no banco de dados.</p> | 



### <a name="return-value"></a>Valor Retornado

Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir. para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de Armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).


| <p>Código de retorno</p> | <p>Descrição</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>A operação foi concluída com sucesso.</p> | 
| <p>JET_errDatabaseInUse</p> | <p>O acesso exclusivo foi solicitado, mas não pôde ser concedido.</p> | 
| <p>JET_errDatabaseInvalidPath</p> | <p>Um caminho inválido foi fornecido em <em>szFilename</em>. <em>szFilename</em> deve ser não nulo e referir-se a um arquivo válido.</p> | 
| <p>JET_errDatabaseLocked</p> | <p>Outra sessão já abriu o banco de dados exclusivamente (usando JET_bitDbExclusive).</p> | 
| <p>JET_errDatabaseNotFound</p> | <p>O banco de dados não foi anexado anteriormente (consulte <a href="gg294074(v=exchg.10).md">JetAttachDatabase</a>).</p> | 
| <p>JET_errInvalidDatabase</p> | <p>Foi feita uma tentativa de abrir um arquivo que não é um arquivo de banco de dados válido.</p> | 
| <p>JET_errOneDatabasePerSession</p> | <p>Foi feita uma tentativa de abrir mais de um banco de dados e <a href="gg269337(v=exchg.10).md">JET_paramOneDatabasePerSession</a> foi definido. Para obter mais informações, consulte <a href="gg294139(v=exchg.10).md">parâmetros do sistema</a>.</p> | 
| <p>JET_wrnFileOpenReadOnly</p> | <p>O arquivo foi anexado como somente leitura, mas <strong>JetOpenDatabase</strong> não passou JET_bitDbReadOnly. O banco de dados ainda está aberto com acesso somente leitura.</p> | 



#### <a name="requirements"></a>Requisitos


| Requisito | Valor |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>requer o Windows Vista, Windows XP ou Windows 2000 Professional.</p> | 
| <p><strong>Servidor</strong></p> | <p>requer o Windows server 2008, Windows server 2003 ou Windows servidor 2000.</p> | 
| <p><strong>Cabeçalho</strong></p> | <p>Declarado em ESENT. h.</p> | 
| <p><strong>Biblioteca</strong></p> | <p>Use ESENT. lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Implementado como <strong>JetOpenDatabaseW</strong> (Unicode) e <strong>JetOpenDatabaseA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Consulte Também

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetAttachDatabase](./jetattachdatabase-function.md)  
[JetAttachDatabase2](./jetattachdatabase2-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[Parâmetros do sistema](./extensible-storage-engine-system-parameters.md)
