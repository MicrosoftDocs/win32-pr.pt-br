---
description: 'Saiba mais sobre: função JetCreateInstance'
title: Função JetCreateInstance
TOCTitle: JetCreateInstance Function
ms:assetid: 9d6c8c9f-3d3b-4308-87d3-84b1ef270262
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269354(v=EXCHG.10)
ms:contentKeyID: 32765641
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCreateInstanceW
- JetCreateInstance
- JetCreateInstanceA
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f22c411dd68b29b0cf305888f9dcce16add9a2dc
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122985039"
---
# <a name="jetcreateinstance-function"></a>Função JetCreateInstance


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetcreateinstance-function"></a>Função JetCreateInstance

A função **JetCreateInstance** aloca uma nova instância do mecanismo de banco de dados para uso em um único processo.

**Windows xp: o JetCreateInstance** é introduzido no Windows XP.

```cpp
    JET_ERR JET_API JetCreateInstance(
      __out         JET_INSTANCE* pinstance,
      __in_opt      const tchar* szInstanceName
    );
```

### <a name="parameters"></a>Parâmetros

*pinstance*

O buffer de saída que recebe a instância recém-criada.

*szInstanceName*

Um identificador de cadeia de caracteres exclusivo para a instância a ser criada. Essa cadeia de caracteres deve ser exclusiva em um determinado processo que hospeda o mecanismo de banco de dados.

**Observação** Um valor nulo é tratado como um identificador de cadeia de caracteres válido para uma instância. Somente uma instância pode ter um identificador de cadeia de caracteres nulo.

### <a name="return-value"></a>Valor Retornado

Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir. para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de Armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).


| <p>Código de retorno</p> | <p>Descrição</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>A operação foi concluída com sucesso.</p> | 
| <p>JET_errInstanceNameInUse</p> | <p>O nome de instância especificado já está em uso para este processo.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Um dos parâmetros fornecidos continha um valor inesperado ou continha um valor que não fazia sentido quando combinado com o valor de outro parâmetro. Isso pode ocorrer para <strong>JetCreateInstance</strong> quando <em>pinstance</em> é <strong>nulo</strong>.</p> | 
| <p>JET_errRunningInOneInstanceMode</p> | <p>a operação falhou porque não pode ser usada quando o mecanismo de banco de dados está operando no modo de instância única (Windows modo de compatibilidade 2000).</p> | 
| <p>JET_errTooManyInstances</p> | <p>Não foi possível criar uma nova instância porque o número máximo de instâncias foi atingido. O número máximo de instâncias com suporte é configurado usando o <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> usando <em>JET_paramMaxInstances</em>.</p> | 



Em caso de êxito, uma nova instância será alocada e o identificador para ela será retornado. Neste ponto, todos os parâmetros do sistema para a instância terão os valores dos parâmetros do sistema padrão global. Depois que uma instância for alocada, ela precisará ser terminada e/ou liberada mais tarde.

Em caso de falha, um erro que representa a causa da falha será retornado e nenhuma instância será alocada.

#### <a name="remarks"></a>Comentários

Uma instância deve ser inicializada com uma chamada para [JetInit](./jetinit-function.md) antes que possa ser usada por algo diferente de [JetSetSystemParameter](./jetsetsystemparameter-function.md).

Uma instância é destruída por uma chamada para a função [JetTerm](./jetterm-function.md) , mesmo que essa instância nunca tenha sido inicializada usando [JetInit](./jetinit-function.md). O número máximo de instâncias que podem ser criadas a qualquer momento é controlado por [JET_paramMaxInstances](./resource-parameters.md), que pode ser configurado por uma chamada para [JetSetSystemParameter](./jetsetsystemparameter-function.md). Uma instância é a unidade de capacidade de recuperação para o mecanismo de banco de dados. Ele controla o ciclo de vida de todos os arquivos usados para proteger a integridade dos dados em um conjunto de arquivos de banco de dado. Esses arquivos incluem o arquivo de ponto de verificação e os arquivos de log de transações.

Se a função for bem sucedido, o mecanismo de banco de dados será automaticamente alterado para o modo de várias instâncias como um efeito colateral dessa chamada. se o aplicativo desejar permitir apenas uma instância no processo, [JetInit](./jetinit-function.md) deverá ser usado para iniciar o mecanismo de banco de dados no modo de compatibilidade Windows 2000.

Se houver, o *szDisplayName* será usado para identificar a instância em locais como o log de eventos ou para outros chamadores, como aplicativos de backup (por meio de funções como [JetGetInstanceInfo](./jetgetinstanceinfo-function.md) ou [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)). Se o nome de exibição não for fornecido, o *szInstanceName* exclusivo será usado, em vez disso, se estiver presente, caso contrário, uma cadeia de caracteres vazia será retornada. Se o mecanismo não tiver o modo de execução definido, após essa chamada, ele será definido como modo de várias instâncias.

A sequência de inicialização típica para um processo que potencialmente executa várias instâncias do Jet seria:

  - Uma chamada para [JetCreateInstance2](./jetcreateinstance2-function.md) que irá alocar e nomear a instância.

  - Várias chamadas para [JetSetSystemParameter](./jetsetsystemparameter-function.md) para essa instância a fim de definir diferentes parâmetros do sistema. Observe que alguns parâmetros do sistema precisam ser exclusivos por instância (como [JET_paramSystemPath](./transaction-log-parameters.md) ou [JET_paramLogFilePath](./transaction-log-parameters.md)), portanto, provavelmente, será necessário definir cada um deles.

  - Inicie a instância usando [JetInit](./jetinit-function.md) ou [JetInit2](./jetinit2-function.md). Para encerrar e/ou liberar uma instância, [JetTerm](./jetterm-function.md), [JetTerm2](./jetterm2-function.md) precisa ser usado.

Se esta for a primeira instância a ser iniciada, haverá várias etapas adicionais que serão executadas durante essa chamada para fazer a inicialização e a configuração básica do sistema. Várias etapas podem resultar em erros específicos, começando com JET_errOutOfMemory, mas outros também (consulte os erros acima).

#### <a name="requirements"></a>Requisitos


| Requisito | Valor |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>requer o Windows Vista ou Windows XP.</p> | 
| <p><strong>Servidor</strong></p> | <p>requer o Windows server 2008 ou Windows server 2003.</p> | 
| <p><strong>Cabeçalho</strong></p> | <p>Declarado em ESENT. h.</p> | 
| <p><strong>Biblioteca</strong></p> | <p>Use ESENT. lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Implementado como <strong>JetCreateInstanceW</strong> (Unicode) e <strong>JetCreateInstanceA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Consulte Também

[arquivos do mecanismo de Armazenamento extensível](./extensible-storage-engine-files.md)  
[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetCreateInstance2](./jetcreateinstance2-function.md)  
[JetEnableMultiInstance](./jetenablemultiinstance-function.md)  
[JetGetInstanceInfo](./jetgetinstanceinfo-function.md)  
[JetInit](./jetinit-function.md)  
[JetInit2](./jetinit2-function.md)  
[JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[JetTerm](./jetterm-function.md)  
[JetTerm2](./jetterm2-function.md)
