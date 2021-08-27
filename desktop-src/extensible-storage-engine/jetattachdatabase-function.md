---
description: 'Saiba mais sobre: função JetAttachDatabase'
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
ms.openlocfilehash: 2b07312cbfce36b450fe39a39810813adc2d0fd4
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122987699"
---
# <a name="jetattachdatabase-function"></a>Função JetAttachDatabase


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetattachdatabase-function"></a>Função JetAttachDatabase

A função **JetAttachDatabase** anexa um arquivo de banco de dados para uso com uma instância de banco de dados. Para usar o banco de dados, será necessário abri-lo posteriormente com [JetOpenDatabase](./jetopendatabase-function.md).

```cpp
    JET_ERR JET_API JetAttachDatabase(
      __in          JET_SESID sesid,
      __in          const tchar* szFilename,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parâmetros

*sesid*

O contexto da sessão de banco de dados a ser usado para a chamada à API.

*szFilename*

O nome do banco de dados a ser anexado.

*grbit*

Um grupo de bits que especifica zero ou mais das opções a seguir.


| <p>Valor</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_bitDbDeleteCorruptIndexes</p> | <p>Se <a href="gg269337(v=exchg.10).md">JET_paramEnableIndexChecking</a> tiver sido definido, todos os índices sobre dados Unicode serão excluídos. Para obter mais detalhes, consulte a seção Comentários.</p> | 
| <p>JET_bitDbDeleteUnicodeIndexes</p> | <p>Todos os índices sobre dados Unicode serão excluídos, independentemente da configuração de <a href="gg269337(v=exchg.10).md">JET_paramEnableIndexChecking</a>. Para obter mais detalhes, consulte a seção Comentários.</p> | 
| <p>JET_bitDbUpgrade</p> | <p>Obsoleto. Não use.</p> | 
| <p>JET_bitDbReadOnly</p> | <p>Impede modificações no banco de dados.</p> | 



### <a name="return-value"></a>Valor Retornado

Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir. para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de Armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).


| <p>Código de retorno</p> | <p>Descrição</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>A operação foi concluída com sucesso.</p> | 
| <p>JET_errBackupInProgress</p> | <p>Não é permitido anexar um banco de dados durante um backup.</p> | 
| <p>JET_errDatabaseFileReadOnly</p> | <p>O arquivo de banco de dados especificado por <em>szFilename</em> deve ser gravável. O atributo Read-Only não deve ser definido e o processo em execução deve ter privilégios suficientes para gravar no arquivo.</p> | 
| <p>JET_errDatabaseInUse</p> | <p>O arquivo de banco de dados já está aberto por outro processo.</p> | 
| <p>JET_errDatabaseInvalidPath</p> | <p>Um caminho inválido foi fornecido em <em>szFilename</em>. <em>szFilename</em> deve ser não nulo e referir-se a um caminho válido.</p> | 
| <p>JET_errDatabaseSharingViolation</p> | <p>O arquivo de banco de dados já foi anexado por uma sessão diferente.</p> | 
| <p>JET_errFileAccessDenied</p> | <p>O mecanismo de banco de dados não pode abrir o arquivo de banco de dados. O arquivo pode estar em uso por outro processo ou o chamador pode não ter privilégios suficientes para abrir o arquivo.</p> | 
| <p>JET_errFileNotFound</p> | <p>O arquivo fornecido em <em>szFilename</em> não existe.</p> | 
| <p>JET_errPrimaryIndexCorrupted</p> | <p>Há um erro com o índice primário. Isso pode ser de corrupção física (como corrupção de disco ou memória). Ele também pode ser retornado ao anexar um banco de dados que foi modificado pela última vez em um sistema operacional mais antigo e o índice primário está sobre uma coluna com dado Unicode. Consulte os comentários para obter mais informações sobre índices sobre dados Unicode.</p> | 
| <p>JET_errSecondaryIndexCorrupted</p> | <p>Há um erro com um índice secundário. Isso pode ser de corrupção física (como corrupção de disco ou memória). Ele também pode ser retornado ao anexar um banco de dados modificado pela última vez em um sistema operacional mais antigo, e um índice secundário está sobre uma coluna com dado Unicode. Consulte os comentários para obter mais informações sobre índices sobre dados Unicode. Os índices secundários são completamente recriados quando um banco de dados é desfragmentado com um utilitário offline usando o seguinte comando: <strong>esentutl-d</strong>.</p> | 
| <p>JET_errTooManyAttachedDatabases</p> | <p>Somente um número finito de bancos de dados pode ser anexado por instância. Atualmente, o limite é de sete bancos de dados por instância.</p> | 
| <p>JET_wrnDatabaseAttached</p> | <p>Um aviso não fatal que indica que o arquivo de banco de dados já foi anexado por esta sessão.</p> | 



#### <a name="remarks"></a>Comentários

Chamar **JetAttachDatabase** é equivalente a chamar [JetAttachDatabase2](./jetattachdatabase2-function.md) e passar um valor de zero, o que significa que não há nenhum limite para o parâmetro *cpgDatabaseSizeMax* .

Anexar um banco de dados gravável (ou seja, se JET_bitDbReadOnly não foi especificado no parâmetro *grbit* ) abrirá o arquivo exclusivamente no nível do sistema operacional. Nenhum outro processo será capaz de abrir o arquivo. É possível que vários processos anexem um banco de dados individual abrindo-os no modo somente leitura.

O arquivo de banco de dados é desanexado usando [JetDetachDatabase](./jetdetachdatabase-function.md) ou [JetDetachDatabase2](./jetdetachdatabase2-function.md).

Parâmetros de verificação de índice

versões diferentes do Windows normalizam o texto Unicode de maneiras diferentes. isso significa que os índices criados em uma versão do Windows podem não funcionar em outras versões.

antes do Windows Server 2003, quando a versão do sistema operacional foi alterada (incluindo a instalação de um service Pack), cada índice sobre dados Unicode estava em um estado potencialmente corrompido.

os índices criados no Windows Server 2003 e versões posteriores são sinalizados com a versão da normalização Unicode com a qual foram criados. Índices mais antigos não contêm informações de versão. A maioria das alterações de normalização Unicode consiste na adição de novos caracteres, pontos de código que anteriormente não foram definidos agora são definidos e normalizados de forma diferente. Portanto, se os dados binários forem armazenados em uma coluna Unicode, eles serão normalizados de forma diferente conforme novos pontos de código são definidos.

a partir do Windows Server 2003, o mecanismo de banco de dados ESE rastreia entradas de índice Unicode que contêm pontos de código indefinidos. Eles podem ser usados para corrigir um índice quando o conjunto de caracteres Unicode definido for alterado.

Esses parâmetros controlam o que acontece quando o mecanismo de banco de dados ESE é anexado a um banco de dados que foi usado pela última vez em uma compilação diferente do sistema operacional. A versão do sistema operacional é carimbada no cabeçalho do banco de dados.

Se [JET_paramEnableIndexChecking](./database-parameters.md) for definido como **true** e o banco de dados contiver índices potencialmente corrompidos:

  - **JetAttachDatabase** excluirá os índices potencialmente corrompidos se *grbit* contiver JET_bitDbDeleteCorruptIndexes

  - **JetAttachDatabase** retornará um erro se *grbit* não contiver JET_bitDbDeleteCorruptIndexes e houver índices que precisam de exclusão.

Se [JET_paramEnableIndexChecking](./database-parameters.md) for definido como **false**:

  - **JetAttachDatabase** ignorará índices potencialmente corrompidos e retornará JET_errSuccess (supondo que não haja nenhum outro erro).

Windows Servidor 2003 e posterior: se [JET_paramEnableIndexChecking](./database-parameters.md) não tiver sido redefinida, a tabela de correção interna será usada para corrigir entradas de índice. Isso pode não corrigir todas as corrupções de índice, mas será transparente para o aplicativo.

Se o banco de dados foi anexado como somente leitura, o índice não pode ser corrigido ou excluído. Nesse caso, a API retornará, em vez disso, um erro, como JET_errSecondaryIndexCorrupted ou JET_errPrimaryIndexCorrupted.

#### <a name="requirements"></a>Requisitos


| Requisito | Valor |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>requer o Windows Vista, Windows XP ou Windows 2000 Professional.</p> | 
| <p><strong>Servidor</strong></p> | <p>requer o Windows server 2008, Windows server 2003 ou Windows servidor 2000.</p> | 
| <p><strong>Cabeçalho</strong></p> | <p>Declarado em ESENT. h.</p> | 
| <p><strong>Biblioteca</strong></p> | <p>Use ESENT. lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Implementado como <strong>JetAddColumnW</strong> (Unicode) e <strong>JetAddColumnA</strong> (ANSI).</p> | 



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
