---
description: 'Saiba mais sobre: função JetCreateInstance2'
title: Função JetCreateInstance2
TOCTitle: JetCreateInstance2 Function
ms:assetid: 1f894b19-fa15-4d89-a3d1-ee13b346f545
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269202(v=EXCHG.10)
ms:contentKeyID: 32765505
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCreateInstance2
- JetCreateInstance2W
- JetCreateInstance2A
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cc09639d48fe4cea93b115c9243587653ad70f44
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122465043"
---
# <a name="jetcreateinstance2-function"></a>Função JetCreateInstance2


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetcreateinstance2-function"></a>Função JetCreateInstance2

A função **JetCreateInstance2** é usada para alocar uma nova instância do mecanismo de banco de dados para uso em um único processo, com um nome de exibição especificado.

**Windows xp:** o **JetCreateInstance2** é introduzido no Windows XP.  

```cpp
    JET_ERR JET_API JetCreateInstance2(
      __out         JET_INSTANCE* pinstance,
      __in_opt      const tchar* szInstanceName,
      __in_opt      const tchar* szDisplayName,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parâmetros

*pinstance*

O buffer de saída que receberá a instância recém-criada.

*szInstanceName*

Especifica um identificador de cadeia de caracteres exclusivo para a instância a ser criada. Essa cadeia de caracteres deve ser exclusiva em um determinado processo que hospeda o mecanismo de banco de dados.

**Observação** Um valor nulo é tratado como um identificador de cadeia de caracteres válido para uma instância. Somente uma instância pode ter um identificador de cadeia de caracteres nulo.

*szDisplayName*

Um nome de exibição para a instância a ser criada. Quando esse parâmetro não estiver presente, seu valor será presumido como nulo.

*grbit*

Reservado para uso futuro. Quando esse parâmetro não estiver presente, seu valor será presumido como zero.

### <a name="return-value"></a>Valor Retornado

Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir. para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de Armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).


| <p>Código de retorno</p> | <p>Descrição</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>A operação foi concluída com sucesso.</p> | 
| <p>JET_errInstanceNameInUse</p> | <p>O nome de instância especificado já está em uso para este processo.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Um dos parâmetros fornecidos continha um valor inesperado ou continha um valor que não fazia sentido quando combinado com o valor de outro parâmetro. Isso pode ocorrer para <a href="gg269354(v=exchg.10).md">JetCreateInstance</a> quando <em>pinstance</em> é nulo.</p> | 
| <p>JET_errRunningInOneInstanceMode</p> | <p>a operação falhou porque não pode ser usada quando o mecanismo de banco de dados está operando no modo de instância única (Windows modo de compatibilidade 2000).</p> | 
| <p>JET_errTooManyInstances</p> | <p>Não foi possível criar uma nova instância porque o número máximo de instâncias foi atingido. O número máximo de instâncias com suporte é configurado usando o <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> usando <em>JET_paramMaxInstances</em>.</p> | 



Em caso de êxito, uma nova instância será alocada e o identificador para ela será retornado. Neste ponto, todos os parâmetros do sistema para a instância terão os valores dos parâmetros do sistema padrão global. Depois que uma instância for alocada, ela precisará ser terminada e/ou liberada mais tarde.

Em caso de falha, um erro que representa a causa da falha será retornado e nenhuma instância será alocada.

#### <a name="remarks"></a>Comentários

Uma instância deve ser inicializada com uma chamada para [JetInit](./jetinit-function.md) antes que possa ser usada por algo diferente de [JetSetSystemParameter](./jetsetsystemparameter-function.md).

Uma instância é destruída por uma chamada para a função [JetTerm](./jetterm-function.md) , mesmo que essa instância nunca tenha sido inicializada usando [JetInit](./jetinit-function.md). O número máximo de instâncias que podem ser criadas a qualquer momento é controlado por *JET_paramMaxInstances*, que pode ser configurado por uma chamada para [JetSetSystemParameter](./jetsetsystemparameter-function.md). Uma instância é a unidade de capacidade de recuperação para o mecanismo de banco de dados. Ele controla o ciclo de vida de todos os arquivos usados para proteger a integridade dos dados em um conjunto de arquivos de banco de dado. Esses arquivos incluem o arquivo de ponto de verificação e os arquivos de log de transações.

Se a função for bem sucedido, o mecanismo de banco de dados será automaticamente alterado para o modo de várias instâncias como um efeito colateral dessa chamada. se o aplicativo desejar permitir apenas uma instância no processo, [JetInit](./jetinit-function.md) deverá ser usado para iniciar o mecanismo de banco de dados no modo de compatibilidade Windows 2000.

Se estiver presente, o parâmetro *szDisplayName* será usado para identificar a instância em locais como log de eventos ou em relação a outros chamadores, como aplicativos de backup (por meio de funções como [JetGetInstanceInfo](./jetgetinstanceinfo-function.md) ou [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)). Se o nome de exibição não for fornecido, o parâmetro *szInstanceName* exclusivo será usado, se presente, caso contrário, uma cadeia de caracteres vazia será retornada. Se o mecanismo não tiver o modo de execução definido, após essa chamada, ele será definido como modo de várias instâncias.

A sequência de inicialização típica para um processo que potencialmente executa várias instâncias do Jet seria:

  - Uma chamada para **JetCreateInstance2** que irá alocar e nomear a instância.

  - Várias chamadas para [JetSetSystemParameter](./jetsetsystemparameter-function.md) para essa instância a fim de definir diferentes parâmetros do sistema. Observe que alguns parâmetros do sistema precisam ser exclusivos para cada instância (como *JET_paramSystemPath* ou *JET_paramLogFilePath*), portanto, é mais provável que cada um deles precise ser definido.

  - Inicie a instância usando [JetInit](./jetinit-function.md) ou [JetInit2](./jetinit2-function.md). Para encerrar e/ou liberar uma instância, use [JetTerm](./jetterm-function.md) ou [JetTerm2](./jetterm2-function.md).

Se esta for a primeira instância a ser iniciada, haverá várias etapas adicionais que serão executadas durante essa chamada para fazer a inicialização e a configuração básica do sistema. Várias etapas podem resultar em erros específicos, começando com JET_errOutOfMemory, mas outros também (consulte valores de retorno para obter mais informações).

#### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>requer o Windows Vista ou Windows XP.</p> | | <p><strong>Servidor</strong></p> | <p>requer o Windows server 2008 ou Windows server 2003.</p> | | <p><strong>Cabeçalho</strong></p> | <p>Declarado em ESENT. h.</p> | | <p><strong>Biblioteca</strong></p> | <p>Use ESENT. lib.</p> | | <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | | <p><strong>Unicode</strong></p> | <p>Implementado como <strong>JetCreateInstance2W</strong> (Unicode) e <strong>JetCreateInstance2A</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Consulte Também

[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetEnableMultiInstance](./jetenablemultiinstance-function.md)  
[JetGetInstanceInfo](./jetgetinstanceinfo-function.md)  
[JetInit](./jetinit-function.md)  
[JetInit2](./jetinit2-function.md)  
[JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[JetTerm](./jetterm-function.md)  
[JetTerm2](./jetterm2-function.md)
