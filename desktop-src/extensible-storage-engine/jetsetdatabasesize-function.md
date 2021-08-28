---
description: 'Saiba mais sobre: Função JetSetDatabaseSize'
title: Função JetSetDatabaseSize
TOCTitle: JetSetDatabaseSize Function
ms:assetid: 4a87bf43-c8f7-4966-9f1f-68c16d1cb558
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269242(v=EXCHG.10)
ms:contentKeyID: 32765544
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetDatabaseSizeW
- JetSetDatabaseSize
- JetSetDatabaseSizeA
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 55a7625de4c8e1ef96740650313d3036cbb605f7
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122988859"
---
# <a name="jetsetdatabasesize-function"></a>Função JetSetDatabaseSize


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetsetdatabasesize-function"></a>Função JetSetDatabaseSize

A **função JetSetDatabaseSize** define o tamanho de um arquivo de banco de dados não aberto.

```cpp
    JET_ERR JET_API JetSetDatabaseSize(
      __in          JET_SESID sesid,
      __in          JET_PCSTR szDatabaseName,
      __in          unsigned long cpg,
      __out         unsigned long* pcpgReal
    );
```

### <a name="parameters"></a>Parâmetros

*sesid*

Identifica o contexto de sessão do banco de dados a ser usado para a chamada à API.

*szDatabaseName*

Identifica o nome do arquivo de banco de dados cujo tamanho deve ser alterado.

*Cpg*

Especifica o tamanho desejado do banco de dados, em páginas.

*pcpgReal*

Ponteiro para um número que recebe o tamanho do banco de dados, em páginas, após a chamada à API. Se a chamada à API não for bem-sucedida, o conteúdo *de pcpgReal* será indefinido.

### <a name="return-value"></a>Valor Retornado

Essa função retorna o [JET_ERR](./jet-err.md) de dados com um dos códigos de retorno a seguir. Para obter mais informações sobre os possíveis erros de ESE, consulte [Extensible Armazenamento Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Código de retorno</p> | <p>Descrição</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>A operação foi concluída com sucesso.</p> | 
| <p>JET_errDatabaseInconsistent<br />JET_errDatabaseDirtyShutdown</p> | <p>JET_errDatabaseInconsistent e JET_errDatabaseDirtyShutdown são o mesmo valor numérico. O banco de dados cujo tamanho deve ser ajustado deve estar em um desligamento limpo, conhecido como um estado consistente. Um banco de dados inconsistente não está corrompido, mas requer que os arquivos de log sejam reprodução.</p> | 
| <p>JET_errDatabaseInvalidPath</p> | <p><em>szDatabaseName</em> não deve ser uma cadeia de caracteres vazia e não NULL.</p> | 
| <p>JET_errDiskFull</p> | <p>Não há espaço livre suficiente no volume para executar a operação de crescimento. <strong>JetSetDatabaseSize</strong> também pode retornar muitos erros relacionados ao arquivo, incluindo, mas não se limitando a:</p><ul><li><p>JET_errDiskIO</p></li><li><p>JET_errFileNotFound</p></li><li><p>JET_errInvalidPath</p></li><li><p>Jet_errfileaccessdenied</p></li><li><p>JET_errOutOfFileHandles</p></li></ul> | 
| <p>JET_errInvalidParameter</p> | <p>Um dos motivos pelos quais esse erro pode ser retornado é se <em>cpg atender</em> ao tamanho mínimo do banco de dados. O tamanho mínimo atual do banco de dados é de 256 páginas.</p> | 
| <p>JET_errOutOfMemory</p> | <p>O sistema tem poucos recursos de memória.</p> | 



#### <a name="remarks"></a>Comentários

Se **JetSetDatabaseSize** for chamado antes de inserir grandes quantidades de dados, o arquivo de banco de dados será aumentado em uma operação. Isso reduzirá a probabilidade de o arquivo de banco de dados ficar fragmentado no nível do sistema de arquivos e também reduzirá o número de vezes que o arquivo de banco de dados precisa ser aumentado. Aumentar o arquivo de banco de dados uma vez pode ser mais rápido do que austá-lo várias vezes.

No momento, há suporte apenas para o aumento do arquivo. Para reduzir um arquivo, use o recurso de desfragmentação do programa esentutl.exe utilitário.

Se *cpg* for menor que o tamanho atual do banco de dados, a operação será ignorada. Se *cpg* for menor que o tamanho mínimo do banco de dados (atualmente 256 páginas), ele retornará JET_errInvalidParameter.

Para definir o tamanho de um banco de dados aberto, consulte [JetGrowDatabase](./jetgrowdatabase-function.md).

O tamanho do arquivo pode não corresponder ao número de páginas retornadas em *pcpgReal.* Há duas páginas reservadas adicionais que podem não ser contadas em *pcpgReal.*

#### <a name="requirements"></a>Requisitos


| Requisito | Valor |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requer Windows Vista, Windows XP ou Windows 2000 Professional.</p> | 
| <p><strong>Servidor</strong></p> | <p>Requer Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</p> | 
| <p><strong>Cabeçalho</strong></p> | <p>Declarado em Esent.h.</p> | 
| <p><strong>Biblioteca</strong></p> | <p>Use ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Implementado como <strong>JetSetDatabaseSizeW</strong> (Unicode) e <strong>JetSetDatabaseSizeA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Consulte Também

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_OBJECTINFO](./jet-objectinfo-structure.md)  
[JET_OBJECTLIST](./jet-objectlist-structure.md)  
[JetGrowDatabase](./jetgrowdatabase-function.md)
