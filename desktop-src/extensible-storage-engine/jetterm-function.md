---
description: 'Saiba mais sobre: função JetTerm'
title: Função JetTerm
TOCTitle: JetTerm Function
ms:assetid: 7711c960-98f4-4134-b8ae-8ddf7b26b6b0
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269298(v=EXCHG.10)
ms:contentKeyID: 32765590
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetTerm
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a22e9f21ab1c3d296a770c53bc6ad5847264b703
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122988409"
---
# <a name="jetterm-function"></a>Função JetTerm


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetterm-function"></a>Função JetTerm

A função **JetTerm** inicia o desligamento de uma instância que foi inicializada pelo [JetInit](./jetinit-function.md).

**JetTerm** também pode ser usado para destruir uma instância não inicializada que foi criada pelo [JetCreateInstance](./jetcreateinstance-function.md).

```cpp
    JET_ERR JET_API JetTerm(
      __in          JET_INSTANCE instance
    );
```

### <a name="parameters"></a>Parâmetros

*cópia*

Especifica a instância a ser usada para esta chamada.

**Windows 2000:**  Esse parâmetro é ignorado e sempre deve ser **nulo**.

**Windows XP e versões posteriores:**  Este parâmetro está sobrecarregado. se o mecanismo estiver operando no modo herdado (Windows modo de compatibilidade 2000) em que apenas uma instância tem suporte, esse parâmetro poderá ser **nulo** ou poderá conter a instância real retornada por [JetInit](./jetinit-function.md). Se o mecanismo estiver operando no modo de várias instâncias, esse parâmetro deverá ser um ponteiro para uma instância que foi criada usando [JetCreateInstance](./jetcreateinstance-function.md).

### <a name="return-value"></a>Valor Retornado

Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir. para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de Armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).


| <p>Código de retorno</p> | <p>Descrição</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>A operação foi concluída com sucesso.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Um dos parâmetros fornecidos continha um valor inesperado ou a combinação de vários parâmetros gerou um resultado inesperado. Esse erro será retornado por <strong>JetTerm</strong> quando o mecanismo estiver no modo de várias instâncias e quando <em>pinstance</em> se referir a uma instância inválida.</p><p><strong>Windows XP:</strong>  esse valor de retorno é introduzido no Windows XP.</p> | 
| <p>JET_errNotInitialized</p> | <p>A operação não pode ser concluída porque a instância ainda não foi inicializada.</p> | 
| <p>JET_errTermInProgress</p> | <p>A operação não pode ser concluída porque a instância está sendo desligada.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Não é possível concluir a operação porque uma operação de restauração está em andamento na instância.</p> | 
| <p>JET_errBackupInProgress</p> | <p>A operação não pode ser concluída porque uma operação de backup está em andamento na instância.</p> | 
| <p>JET_errTooManyActiveUsers</p> | <p>A instância não pode ser desligada porque existem sessões com transações ativas para a instância especificada. Esse erro ocorrerá somente se o JET_bitTermComplete for usado.</p> | 



Se essa função for realizada com sucesso, a instância especificada será desligada. O identificador de instância também será fechado e ficará indisponível para qualquer API que usa um identificador de instância. Todos os outros objetos associados à instância, como sessões, também serão fechados. O estado do arquivo de ponto de verificação, os arquivos de log de transações e os arquivos de banco de dados anexados à instância serão modificados durante o processo de desligamento.

Se essa função falhar como resultado de um erro de uso, a instância permanecerá em um estado inicializado e nada será alterado. Caso contrário, a instância ainda será desligada de acordo com o caso de êxito. A diferença é que a instância precisará passar pela recuperação de pane quando for inicializada na próxima vez. O mecanismo tentará liberar o máximo de dados possível para minimizar a quantidade de recuperação necessária. Conceitualmente, essa falha de **JetTerm** não é diferente de uma falha de processo.

#### <a name="remarks"></a>Comentários

Se o processo de host de uma instância for encerrado por qualquer motivo antes que **JetTerm** seja chamado com êxito nessa instância, a instância será considerada em um estado de falha. A recuperação de falha ocorrerá na próxima tentativa de inicializar essa instância.

#### <a name="requirements"></a>Requisitos


| Requisito | Valor |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>requer o Windows Vista, Windows XP ou Windows 2000 Professional.</p> | 
| <p><strong>Servidor</strong></p> | <p>requer o Windows server 2008, Windows server 2003 ou Windows servidor 2000.</p> | 
| <p><strong>Cabeçalho</strong></p> | <p>Declarado em ESENT. h.</p> | 
| <p><strong>Biblioteca</strong></p> | <p>Use ESENT. lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte Também

[arquivos do mecanismo de Armazenamento extensível](./extensible-storage-engine-files.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JetInit](./jetinit-function.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetTerm2](./jetterm2-function.md)
