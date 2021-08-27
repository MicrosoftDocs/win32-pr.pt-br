---
description: 'Saiba mais sobre: função JetGrowDatabase'
title: Função JetGrowDatabase
TOCTitle: JetGrowDatabase Function
ms:assetid: d9719991-6c80-4dcb-a1d6-f0c7de61f459
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294109(v=EXCHG.10)
ms:contentKeyID: 32765724
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGrowDatabase
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 710e41b29c55ec435db6eb1b9e1536740819478e
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479062"
---
# <a name="jetgrowdatabase-function"></a>Função JetGrowDatabase


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetgrowdatabase-function"></a>Função JetGrowDatabase

A função **JetGrowDatabase** estende o tamanho de um banco de dados que está aberto no momento.

```cpp
    JET_ERR JET_API JetGrowDatabase(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          unsigned long cpg,
      __in          unsigned long* pcpgReal
    );
```

### <a name="parameters"></a>Parâmetros

*sesid*

O contexto da sessão de banco de dados a ser usado para a chamada à API.

*DBID*

O banco de dados que será estendido.

*CPG*

O tamanho desejado do banco de dados, em páginas.

*pcpgReal*

Ponteiro para um número que recebe o tamanho do banco de dados, em páginas, após a chamada à API. Se a chamada à API falhar, o conteúdo de *pcpgReal* será indefinido.

### <a name="return-value"></a>Valor Retornado

Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir. para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de Armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).


| <p>Código de retorno</p> | <p>Descrição</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>A operação foi concluída com sucesso.</p> | 
| <p>JET_errDiskFull</p> | <p>Não há espaço livre suficiente no volume para executar a operação de crescimento.</p> | 
| <p>JET_errDiskIO</p> | <p>Um erro relacionado a arquivo foi retornado por <a href="gg269242(v=exchg.10).md">JetSetDatabaseSize</a>. Para obter mais informações sobre outros erros relacionados a arquivos que podem ser retornados, consulte <a href="gg269242(v=exchg.10).md">JetSetDatabaseSize</a>.</p> | 



#### <a name="remarks"></a>Comentários

Se **JetGrowDatabase** for chamado antes da inserção de grandes quantidades de dados, o arquivo de banco de dado será aumentado em uma única operação. Isso reduzirá a probabilidade de o arquivo de banco de dados ficar fragmentado no nível do sistema de arquivos e também reduzir o número de vezes que o arquivo de banco de dados precisa ser aumentado. Aumentar o arquivo de banco de dados uma vez pode ser mais rápido do que expandi-lo várias vezes.

No momento, há suporte para o aumento do arquivo. Para reduzir um arquivo, use o recurso de desfragmentação do programa utilitário de **esentutl.exe** .

Para definir o tamanho de um banco de dados que não está aberto, consulte [JetSetDatabaseSize](./jetsetdatabasesize-function.md).

O tamanho do arquivo pode não corresponder ao número de páginas retornadas em *pcpgReal*. Há duas páginas reservadas adicionais que podem não ser contadas em *pcpgReal*.

#### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>requer o Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>requer o Windows server 2008, Windows server 2003 ou Windows servidor 2000.</p> | | <p><strong>Cabeçalho</strong></p> | <p>Declarado em ESENT. h.</p> | | <p><strong>Biblioteca</strong></p> | <p>Use ESENT. lib.</p> | | <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte Também

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_OBJECTINFO](./jet-objectinfo-structure.md)  
[JET_OBJECTLIST](./jet-objectlist-structure.md)  
[JetSetDatabaseSize](./jetsetdatabasesize-function.md)
