---
description: 'Saiba mais sobre: função JetAttachDatabase2'
title: Função JetAttachDatabase2
TOCTitle: JetAttachDatabase2 Function
ms:assetid: 8667f3fc-d178-49f1-9474-f09352614f92
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269322(v=EXCHG.10)
ms:contentKeyID: 32765612
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetAttachDatabase2A
- JetAttachDatabase2
- JetAttachDatabase2W
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 069339aefbac335bf1c7bb4b35efe4466b526225
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122475932"
---
# <a name="jetattachdatabase2-function"></a>Função JetAttachDatabase2


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetattachdatabase2-function"></a>Função JetAttachDatabase2

A função **JetAttachDatabase2** anexa um arquivo de banco de dados para uso com uma instância de banco de dados e especifica um tamanho máximo para esse banco de dados. Para usar o banco de dados, será necessário abri-lo posteriormente com [JetOpenDatabase](./jetopendatabase-function.md).

```cpp
    JET_ERR JET_API JetAttachDatabase2(
      __in          JET_SESID sesid,
      __in          const tchar* szFilename,
      __in          const unsigned long cpgDatabaseSizeMax,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parâmetros

*sesid*

O contexto de sessão de banco de dados que será usado para a chamada à API.

*szFilename*

O nome do banco de dados a ser anexado.

*cpgDatabaseSizeMax*

O tamanho máximo, em páginas de banco de dados, para o banco de dados. O tamanho da página do banco de dados padrão é 4 quilobytes, que pode ser alterado usando a função [JetSetSystemParameter](./jetsetsystemparameter-function.md) antes de criar um banco de dados.

Passar zero significa que não há nenhum máximo imposto pelo mecanismo de banco de dados.

*grbit*

Um grupo de bits que contém as opções a serem usadas para esta chamada, que incluem zero ou mais dos seguintes:


| <p>Valor</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_bitDbDeleteCorruptIndexes</p> | <p>Se <a href="gg269337(v=exchg.10).md">JET_paramEnableIndexChecking</a> tiver sido definido, todos os índices sobre dados Unicode serão excluídos. Para obter mais detalhes, consulte a seção Comentários.</p> | 
| <p>JET_bitDbDeleteUnicodeIndexes</p> | <p>Todos os índices sobre dados Unicode serão excluídos, independentemente da configuração de <a href="gg269337(v=exchg.10).md">JET_paramEnableIndexChecking</a>. Para obter mais detalhes, consulte a seção Comentários.</p> | 
| <p>JET_bitDbReadOnly</p> | <p>Impede modificações no banco de dados.</p> | 
| <p>JET_bitDbUpgrade</p> | <p>Reservado para uso futuro.</p> | 



### <a name="return-value"></a>Valor Retornado

A função retorna um dos [JET_ERR](./jet-err.md) códigos de erro. Veja a seguir as mais comumente retornadas. (para obter uma lista completa de erros para essa API, consulte [códigos de erro do mecanismo de Armazenamento extensível](./extensible-storage-engine-error-codes.md).)


| <p>Código de retorno</p> | <p>Descrição</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>A operação foi concluída com sucesso.</p> | 
| <p>JET_errBackupInProgress</p> | <p>Não é permitido anexar um banco de dados durante um backup.</p> | 
| <p>JET_errDatabaseFileReadOnly</p> | <p>O arquivo de banco de dados especificado por <em>szFilename</em> deve ser gravável. O atributo Read-Only não deve ser definido e o processo em execução deve ter privilégios suficientes para gravar no arquivo.</p> | 
| <p>JET_errDatabaseInUse</p> | <p>O arquivo de banco de dados já está aberto por outro processo.</p> | 
| <p>JET_errDatabaseInvalidPath</p> | <p>Um caminho inválido foi fornecido em <em>szFilename</em>. <em>szFilename</em> deve ser não nulo e referir-se a um caminho válido.</p> | 
| <p>JET_errDatabaseSharingViolation</p> | <p>O arquivo de banco de dados já foi anexado por uma sessão diferente.</p> | 
| <p>JET_errFileNotFound</p> | <p>O arquivo fornecido em <em>szFilename</em> não existe.</p> | 
| <p>JET_errPrimaryIndexCorrupted</p> | <p>Há um erro com o índice primário. Isso pode ser de corrupção física (como corrupção de disco ou memória). Ele também pode ser retornado ao anexar um banco de dados que foi modificado pela última vez em um sistema operacional mais antigo e o índice primário está sobre uma coluna com dado Unicode. Consulte os comentários para obter mais informações sobre índices sobre dados Unicode.</p> | 
| <p>JET_errSecondaryIndexCorrupted</p> | <p>Há um erro com um índice secundário. Isso pode ser de corrupção física (como corrupção de disco ou memória). Ele também pode ser retornado ao anexar um banco de dados modificado pela última vez em um sistema operacional mais antigo, e um índice secundário está sobre uma coluna com dado Unicode. Consulte os comentários para obter mais informações sobre índices sobre dados Unicode. Os índices secundários são completamente recriados quando um banco de dados é desfragmentado com um utilitário offline usando o seguinte comando: <strong>esentutl-d</strong>.</p> | 
| <p>JET_errTooManyAttachedDatabases</p> | <p>Somente um número finito de bancos de dados pode ser anexado por instância. Atualmente, o limite é de sete bancos de dados por instância.</p> | 
| <p>JET_wrnDatabaseAttached</p> | <p>Um aviso não fatal que indica que o arquivo de banco de dados já foi anexado por esta sessão.</p> | 



#### <a name="remarks"></a>Comentários

O arquivo de banco de dados é desanexado usando [JetDetachDatabase](./jetdetachdatabase-function.md) ou [JetDetachDatabase2](./jetdetachdatabase2-function.md).

Consulte [JetAttachDatabase](./jetattachdatabase-function.md) para ver comentários.

#### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>requer o Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>requer o Windows server 2008, Windows server 2003 ou Windows servidor 2000.</p> | | <p><strong>Cabeçalho</strong></p> | <p>Declarado em ESENT. h.</p> | | <p><strong>Biblioteca</strong></p> | <p>Use ESENT. lib.</p> | | <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | | <p><strong>Unicode</strong></p> | <p>Implementado como <strong>JetAttachDatabase2W</strong> (Unicode) e <strong>JetAttachDatabase2A</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Consulte Também

[arquivos do mecanismo de Armazenamento extensível](./extensible-storage-engine-files.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetAttachDatabase](./jetattachdatabase-function.md)  
[JetCreateDatabase](./jetcreatedatabase-function.md)  
[JetOpenDatabase](./jetopendatabase-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)
