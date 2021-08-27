---
description: 'Saiba mais sobre: função JetTerm2'
title: Função JetTerm2
TOCTitle: JetTerm2 Function
ms:assetid: 36464e24-1cc0-4cda-9d7a-f64555c622bf
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269223(v=EXCHG.10)
ms:contentKeyID: 32765525
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetTerm2
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b9f8e5f278a0ef3eb44efd64314745d2fed6d89b
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122466613"
---
# <a name="jetterm2-function"></a>Função JetTerm2


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetterm2-function"></a>Função JetTerm2

A função **JetTerm2** inicia o desligamento de uma instância que foi inicializada pelo [JetInit](./jetinit-function.md).

**JetTerm2** também pode destruir uma instância não inicializada que foi criada pelo [JetCreateInstance](./jetcreateinstance-function.md).

```cpp
    JET_ERR JET_API JetTerm2(
      __in          JET_INSTANCE instance,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parâmetros

*cópia*

A instância a ser usada para esta chamada.

**Windows 2000:**  Esse parâmetro é ignorado e sempre deve ser **nulo**.

**Windows XP e versões posteriores:**  Este parâmetro está sobrecarregado. se o mecanismo estiver operando no modo herdado (Windows modo de compatibilidade 2000) em que apenas uma instância tem suporte, esse parâmetro poderá ser **nulo** ou poderá conter a instância real retornada por [JetInit](./jetinit-function.md). Se o mecanismo estiver operando no modo de várias instâncias, esse parâmetro deverá ser um ponteiro para uma instância que foi criada usando [JetCreateInstance](./jetcreateinstance-function.md).

*grbit*

Um grupo de bits que contém as opções a serem usadas para esta chamada, que incluem zero ou mais dos valores a seguir.


| <p>Valor</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_bitTermComplete</p> | <p>Solicita que a instância seja desligada corretamente. Qualquer trabalho de limpeza opcional que normalmente seria feito em segundo plano em tempo de execução é concluído imediatamente.</p> | 
| <p>JET_bitTermAbrupt</p> | <p>Solicita que a instância seja desligada o mais rápido possível. Qualquer trabalho opcional que normalmente seria feito em segundo plano em tempo de execução é abandonado.</p><p><strong>Observação</strong>  Essa opção pode causar perda de espaço temporária ou permanente no banco de dados. Esse espaço perdido sempre pode ser recuperado por meio de uma desfragmentação offline do banco de dados.</p> | 
| <p>JET_bitTermStopBackup</p> | <p>Solicita que a instância seja desligada mesmo que atualmente haja um backup em andamento. Normalmente, um backup pendente faria com que o <a href="gg269298(v=exchg.10).md">JetTerm</a> falhasse com JET_errBackupInProgress. Quando esse parâmetro não estiver presente, seu valor será presumido como JET_bitTermAbrupt.</p> | 
| <p>JET_bitTermDirty</p> | <p>Solicita que a instância seja desligada com todos os bancos de dados anexados deixados em um estado sujo.</p><p>Windows 7: JET_bitTermDirty é introduzido no Windows 7.</p> | 



### <a name="return-value"></a>Valor Retornado

Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir. para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de Armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).


| <p>Código de retorno</p> | <p>Descrição</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>A operação foi concluída com sucesso.</p> | 
| <p>JET_errBackupInProgress</p> | <p>A operação não pode ser concluída porque uma operação de backup está em andamento na instância.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Um dos parâmetros fornecidos continha um valor inesperado ou a combinação de vários parâmetros gerou um resultado inesperado. Esse erro será retornado por <a href="gg269298(v=exchg.10).md">JetTerm</a> quando o mecanismo estiver no modo de várias instâncias e quando <em>pinstance</em> se referir a uma instância inválida.</p><p><strong>Windows XP:</strong>  esse valor de retorno é introduzido no Windows XP.</p> | 
| <p>JET_errNotInitialized</p> | <p>A operação não pode ser concluída porque a instância ainda não foi inicializada.</p> | 
| <p>JET_errTermInProgress</p> | <p>A operação não pode ser concluída porque a instância está sendo desligada.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Não é possível concluir a operação porque uma operação de restauração está em andamento na instância.</p> | 
| <p>JET_errTooManyActiveUsers</p> | <p>A instância não pode ser desligada porque existem sessões com transações ativas para a instância especificada. Esse erro ocorrerá somente se o JET_bitTermComplete for usado.</p> | 



Se essa função for realizada com sucesso, a instância especificada será desligada. O identificador de instância também será fechado e ficará indisponível para qualquer API que usa um identificador de instância. Todos os outros objetos associados à instância, como sessões, também serão fechados. O estado do arquivo de ponto de verificação, os arquivos de log de transações e os arquivos de banco de dados anexados à instância serão modificados durante o processo de desligamento.

Se essa função falhar como resultado de um erro de uso, a instância permanecerá em um estado inicializado e nada será alterado. Caso contrário, a instância ainda será desligada conforme indicado para o caso de êxito. A diferença é que a instância precisará passar pela recuperação de pane quando for inicializada na próxima vez. O mecanismo tentará liberar o máximo de dados possível para minimizar a quantidade de recuperação necessária. Conceitualmente, essa falha de [JetTerm](./jetterm-function.md) não é diferente de uma falha de processo.

#### <a name="remarks"></a>Comentários

Consulte [JetTerm](./jetterm-function.md).

#### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>requer o Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>requer o Windows server 2008, Windows server 2003 ou Windows servidor 2000.</p> | | <p><strong>Cabeçalho</strong></p> | <p>Declarado em ESENT. h.</p> | | <p><strong>Biblioteca</strong></p> | <p>Use ESENT. lib.</p> | | <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte Também

[arquivos do mecanismo de Armazenamento extensível](./extensible-storage-engine-files.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JetInit](./jetinit-function.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetTerm](./jetterm-function.md)
