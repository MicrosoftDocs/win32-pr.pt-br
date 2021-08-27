---
description: 'Saiba mais sobre: Função JetTerm'
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
ms.openlocfilehash: 832f98d32f164e91cd9dfc8befac4cbd0e518632
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481152"
---
# <a name="jetterm-function"></a>Função JetTerm


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetterm-function"></a>Função JetTerm

A **função JetTerm** inicia o desligamento de uma instância que foi inicializada pelo [JetInit](./jetinit-function.md).

**JetTerm** também pode ser usado para destruir uma instância não reinicializada que foi criada pelo [JetCreateInstance](./jetcreateinstance-function.md).

```cpp
    JET_ERR JET_API JetTerm(
      __in          JET_INSTANCE instance
    );
```

### <a name="parameters"></a>Parâmetros

*Instância*

Especifica a instância a ser usada para essa chamada.

**Windows 2000:**  Esse parâmetro é ignorado e sempre deve ser **NULL.**

**Windows XP e versões posteriores:**  Esse parâmetro está sobrecarregado. Se o mecanismo estiver operando no modo herdado (modo de compatibilidade Windows 2000), em que há suporte para apenas uma instância, esse parâmetro poderá ser **NULL** ou conter a instância real retornada pelo [JetInit](./jetinit-function.md). Se o mecanismo estiver operando no modo de várias instâncias, esse parâmetro deverá ser um ponteiro para uma instância que foi criada usando [JetCreateInstance](./jetcreateinstance-function.md).

### <a name="return-value"></a>Valor Retornado

Essa função retorna o [JET_ERR](./jet-err.md) de dados com um dos códigos de retorno a seguir. Para obter mais informações sobre os possíveis erros de ESE, consulte [Extensible Armazenamento Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Código de retorno</p> | <p>Descrição</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>A operação foi concluída com sucesso.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Um dos parâmetros fornecidos continha um valor inesperado ou a combinação de vários parâmetros gerou um resultado inesperado. Esse erro será retornado pelo <strong>JetTerm</strong> quando o mecanismo estiver no modo de várias instâncias e quando o <em>pinstance</em> se referir a uma instância inválida.</p><p><strong>Windows XP:</strong>  Esse valor de retorno é introduzido no Windows XP.</p> | 
| <p>JET_errNotInitialized</p> | <p>A operação não pode ser concluída porque a instância ainda não foi inicializada.</p> | 
| <p>JET_errTermInProgress</p> | <p>A operação não pode ser concluída porque a instância está sendo desligado.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Não é possível concluir a operação porque uma operação de restauração está em andamento na instância.</p> | 
| <p>JET_errBackupInProgress</p> | <p>A operação não pode ser concluída porque uma operação de backup está em andamento na instância.</p> | 
| <p>JET_errTooManyActiveUsers</p> | <p>A instância não pode ser fechada porque atualmente há sessões com transações ativas para a instância especificada. Esse erro ocorrerá somente se o JET_bitTermComplete for usado.</p> | 



Se essa função for bem-sucedida, a instância especificada será desligado. O handle de instância também será fechado e ficará indisponível para qualquer API que aceita um handle de instância. Todos os outros objetos associados à instância, como sessões, também serão fechados. O estado do arquivo de ponto de verificação, os arquivos de log de transações e os arquivos de banco de dados anexados à instância serão modificados durante o processo de desligamento.

Se essa função falhar como resultado de um erro de uso, a instância permanecerá em um estado inicializado e nada será alterando. Caso contrário, a instância ainda será fechada de acordo com o caso de êxito. A diferença é que a instância precisará passar pela recuperação de falha quando for inicializada pela próxima vez. O mecanismo tentará liberar o máximo de dados possível para minimizar a quantidade de recuperação necessária. Conceitualmente, essa falha de **JetTerm** não é diferente de uma falha de processo.

#### <a name="remarks"></a>Comentários

Se o processo de host de uma instância for finalado por algum motivo antes que **JetTerm** seja chamado com êxito nessa instância, a instância será considerada em um estado de queda. A recuperação de falha ocorrerá na próxima tentativa de inicializar essa instância.

#### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requer Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p><strong>Servidor</strong></p> | <p>Requer Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</p> | | <p><strong>Cabeçalho</strong></p> | <p>Declarado em Esent.h.</p> | | <p><strong>Biblioteca</strong></p> | <p>Use ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte Também

[Arquivos extensíveis Armazenamento mecanismo](./extensible-storage-engine-files.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JetInit](./jetinit-function.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetTerm2](./jetterm2-function.md)
