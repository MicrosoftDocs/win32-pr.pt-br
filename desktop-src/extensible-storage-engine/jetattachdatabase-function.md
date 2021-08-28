---
description: 'Saiba mais sobre: Função JetAttachDatabase'
title: Função JetAttachDatabase
TOCTitle: JetAttachDatabase Function
ms:assetid: bc4c9a76-203c-424a-ac17-f096e3a6e04e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294074(v=EXCHG.10)
ms:contentKeyID: 32765689
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetAttachDatabase
- JetAttachDatabaseW
- JetAttachDatabaseA
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: eb68677ad55c137ebb40ffaef1ad0fd686bb4eb7
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122466753"
---
# <a name="jetattachdatabase-function"></a>Função JetAttachDatabase


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetattachdatabase-function"></a>Função JetAttachDatabase

A **função JetAttachDatabase** anexa um arquivo de banco de dados para uso com uma instância de banco de dados. Para usar o banco de dados, ele precisará ser aberto posteriormente com [JetOpenDatabase.](./jetopendatabase-function.md)

```cpp
    JET_ERR JET_API JetAttachDatabase(
      __in          JET_SESID sesid,
      __in          const tchar* szFilename,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parâmetros

*sesid*

O contexto de sessão do banco de dados a ser usado para a chamada à API.

*szFilename*

O nome do banco de dados a ser anexado.

*grbit*

Um grupo de bits que especificam zero ou mais das opções a seguir.


| <p>Valor</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_bitDbDeleteCorruptIndexes</p> | <p>Se <a href="gg269337(v=exchg.10).md">JET_paramEnableIndexChecking</a> tiver sido definido, todos os índices sobre dados Unicode serão excluídos. Para obter mais detalhes, consulte a seção Comentários.</p> | 
| <p>JET_bitDbDeleteUnicodeIndexes</p> | <p>Todos os índices sobre dados Unicode serão excluídos, independentemente da configuração <a href="gg269337(v=exchg.10).md">de JET_paramEnableIndexChecking</a>. Para obter mais detalhes, consulte a seção Comentários.</p> | 
| <p>JET_bitDbUpgrade</p> | <p>Obsoleto. Não use.</p> | 
| <p>JET_bitDbReadOnly</p> | <p>Impede modificações no banco de dados.</p> | 



### <a name="return-value"></a>Valor Retornado

Essa função retorna o [JET_ERR](./jet-err.md) de dados com um dos códigos de retorno a seguir. Para obter mais informações sobre os possíveis erros de ESE, consulte [Extensible Armazenamento Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Código de retorno</p> | <p>Descrição</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>A operação foi concluída com sucesso.</p> | 
| <p>JET_errBackupInProgress</p> | <p>A anexação de um banco de dados não é permitida durante um backup.</p> | 
| <p>JET_errDatabaseFileReadOnly</p> | <p>O arquivo de banco de dados especificado <em>por szFilename</em> deve ser escrito. O Read-Only atributo não deve ser definido e o processo em execução deve ter privilégios suficientes para gravar no arquivo.</p> | 
| <p>JET_errDatabaseInUse</p> | <p>O arquivo de banco de dados já está aberto por outro processo.</p> | 
| <p>JET_errDatabaseInvalidPath</p> | <p>Um caminho inválido foi dado em <em>szFilename.</em> <em>szFilename</em> deve ser não NULL e se referir a um caminho válido.</p> | 
| <p>JET_errDatabaseSharingViolation</p> | <p>O arquivo de banco de dados já foi anexado por uma sessão diferente.</p> | 
| <p>Jet_errfileaccessdenied</p> | <p>O mecanismo de banco de dados não pode abrir o arquivo de banco de dados. O arquivo pode estar em uso por outro processo ou o chamador pode não ter privilégios suficientes para abrir o arquivo.</p> | 
| <p>JET_errFileNotFound</p> | <p>O arquivo dado <em>em szFilename</em> não existe.</p> | 
| <p>JET_errPrimaryIndexCorrupted</p> | <p>Há um erro com o índice primário. Isso pode ser de corrupção física (como corrupção de disco ou memória). Ele também pode ser retornado ao anexar um banco de dados modificado pela última vez em um sistema operacional mais antigo e o índice primário está sobre uma coluna com dados Unicode. Consulte os comentários para obter mais informações sobre índices sobre dados Unicode.</p> | 
| <p>JET_errSecondaryIndexCorrupted</p> | <p>Há um erro com um índice secundário. Isso pode ser de corrupção física (como corrupção de disco ou memória). Ele também pode ser retornado ao anexar um banco de dados modificado pela última vez em um sistema operacional mais antigo e um índice secundário está sobre uma coluna com dados Unicode. Consulte os comentários para obter mais informações sobre índices sobre dados Unicode. Os índices secundários são completamente reconstruídos quando um banco de dados é desfragmentado com um utilitário offline usando o seguinte comando: <strong>esentutl -d</strong>.</p> | 
| <p>JET_errTooManyAttachedDatabases</p> | <p>Somente um número finito de bancos de dados pode ser anexado por instância. Atualmente, o limite é de sete bancos de dados por instância.</p> | 
| <p>JET_wrnDatabaseAttached</p> | <p>Um aviso nãofatal que indica que o arquivo de banco de dados já foi anexado por esta sessão.</p> | 



#### <a name="remarks"></a>Comentários

Chamar **JetAttachDatabase** é equivalente a chamar [JetAttachDatabase2](./jetattachdatabase2-function.md) e passar um valor igual a zero, o que significa que não há nenhum limite para o *parâmetro cpgDatabaseSizeMax.*

Anexar um banco de dados que pode ser escrito (ou seja, se JET_bitDbReadOnly não tiver sido especificado no parâmetro *grbit)* abrirá o arquivo exclusivamente no nível do sistema operacional. Nenhum outro processo poderá abrir o arquivo. É possível que vários processos anexem um banco de dados individual abrindo-os no modo somente leitura.

O arquivo de banco de dados é desvinculado [usando JetDetachDatabase](./jetdetachdatabase-function.md) ou [JetDetachDatabase2](./jetdetachdatabase2-function.md).

Parâmetros de verificação de índice

Versões diferentes Windows normalizar o texto Unicode de maneiras diferentes. Isso significa que os índices construídos em uma versão Windows podem não funcionar em outras versões.

Antes do Windows Server 2003, quando a versão do sistema operacional era alterada (incluindo a instalação de um Service Pack), cada índice sobre dados Unicode estava em um estado potencialmente corrompido.

Índices criados no Windows Server 2003 e posterior são sinalizados com a versão da normalização Unicode com a qual foram criados. Índices mais antigos não contêm informações de versão. A maioria das alterações de normalização Unicode consiste na adição de novos caracteres, pontos de código que anteriormente eram indefinido agora estão definidos e normalizam de maneira diferente. Portanto, se os dados binários são armazenados em uma coluna Unicode, eles serão normalizado de maneira diferente à medida que novos pontos de código são definidos.

A partir Windows Server 2003, o mecanismo de banco de dados ESE rastreia entradas de índice Unicode que contêm pontos de código indefinido. Eles podem ser usados para corrigir um índice quando o conjunto de caracteres Unicode definidos muda.

Esses parâmetros controlam o que acontece quando o mecanismo de banco de dados ESE é anexado a um banco de dados que foi usado pela última vez em um build diferente do sistema operacional. A versão do sistema operacional é carimbada no header do banco de dados.

Se [JET_paramEnableIndexChecking](./database-parameters.md) estiver definido como **TRUE** e o banco de dados contiver índices potencialmente corrompidos:

  - **JetAttachDatabase** excluirá os índices potencialmente corrompidos se *o grbit* contiver JET_bitDbDeleteCorruptIndexes

  - **JetAttachDatabase** retornará um erro se *grbit* não contiver JET_bitDbDeleteCorruptIndexes e houver índices que precisam de exclusão.

Se [JET_paramEnableIndexChecking](./database-parameters.md) estiver definido como **FALSE:**

  - **JetAttachDatabase** ignorará índices potencialmente corrompidos e retornará JET_errSuccess (supondo que não haja outros erros).

Windows Servidor 2003 e posterior: [se JET_paramEnableIndexChecking](./database-parameters.md) não tiver sido redefinido, a tabela de correção interna será usada para corrigir entradas de índice. Isso pode não corrigir todos os danos de índice, mas será transparente para o aplicativo.

Se o banco de dados tiver sido anexado como somente leitura, o índice não poderá ser fixo ou excluído. Nesse caso, a API retornará um erro, como JET_errSecondaryIndexCorrupted ou JET_errPrimaryIndexCorrupted.

#### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requer Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>Requer Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</p> | | <p><strong>Cabeçalho</strong></p> | <p>Declarado em ESENT. h.</p> | | <p><strong>Biblioteca</strong></p> | <p>Use ESENT. lib.</p> | | <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | | <p><strong>Unicode</strong></p> | <p>Implementado como <strong>JetAddColumnW</strong> (Unicode) e <strong>JetAddColumnA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Consulte Também

[arquivos do mecanismo de Armazenamento extensível](./extensible-storage-engine-files.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetAttachDatabase2](./jetattachdatabase2-function.md)  
[JetCreateDatabase](./jetcreatedatabase-function.md)  
[JetDetachDatabase](./jetdetachdatabase-function.md)  
[JetDetachDatabase2](./jetdetachdatabase2-function.md)  
[JetOpenDatabase](./jetopendatabase-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)
