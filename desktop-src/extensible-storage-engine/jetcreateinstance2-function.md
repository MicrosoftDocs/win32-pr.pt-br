---
description: 'Saiba mais sobre: Função JetCreateInstance2'
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
ms.openlocfilehash: 7cebf23486505cd0381bd8cd62024ad0bc767633
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122987419"
---
# <a name="jetcreateinstance2-function"></a>Função JetCreateInstance2


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetcreateinstance2-function"></a>Função JetCreateInstance2

A **função JetCreateInstance2** é usada para alocar uma nova instância do mecanismo de banco de dados para uso em um único processo, com um nome de exibição especificado.

**Windows XP:****JetCreateInstance2** é introduzido no Windows XP.  

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

Especifica um identificador de cadeia de caracteres exclusivo para a instância a ser criada. Essa cadeia de caracteres deve ser exclusiva dentro de um determinado processo que hospeda o mecanismo de banco de dados.

**Observação** Um valor NULL é tratado como um identificador de cadeia de caracteres válido para uma instância. Apenas uma instância pode ter um identificador de cadeia de caracteres NULL.

*Szdisplayname*

Um nome de exibição para a instância a ser criada. Quando esse parâmetro não está presente, presume-se que seu valor seja NULL.

*grbit*

Reservado para uso futuro. Quando esse parâmetro não está presente, presume-se que seu valor seja zero.

### <a name="return-value"></a>Valor Retornado

Essa função retorna o [JET_ERR](./jet-err.md) de dados com um dos códigos de retorno a seguir. Para obter mais informações sobre os possíveis erros de ESE, consulte [Extensible Armazenamento Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Código de retorno</p> | <p>Descrição</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>A operação foi concluída com sucesso.</p> | 
| <p>JET_errInstanceNameInUse</p> | <p>O nome da instância especificado já está em uso para esse processo.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Um dos parâmetros fornecidos continha um valor inesperado ou continha um valor que não fazia sentido quando combinado com o valor de outro parâmetro. Isso pode acontecer para <a href="gg269354(v=exchg.10).md">JetCreateInstance</a> quando <em>a pinstance</em> é NULL.</p> | 
| <p>JET_errRunningInOneInstanceMode</p> | <p>A operação falhou porque não pode ser usada quando o mecanismo de banco de dados está operando no modo de instância única (Windows modo de compatibilidade 2000).</p> | 
| <p>JET_errTooManyInstances</p> | <p>Não foi possível criar uma nova instância porque o número máximo de instâncias foi atingido. O número máximo de instâncias com suporte é configurado usando <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> usando <em>JET_paramMaxInstances</em>.</p> | 



Em caso de êxito, uma nova instância será alocada e o identificador para ela será retornado. Neste ponto, todos os parâmetros do sistema para a instância terão os valores dos parâmetros do sistema padrão global. Depois que uma instância for alocada, ela precisará ser encerrada e/ou liberada posteriormente.

Em caso de falha, um erro que representa a causa da falha será retornado e nenhuma instância será alocada.

#### <a name="remarks"></a>Comentários

Uma instância deve ser inicializada com uma chamada para [JetInit](./jetinit-function.md) antes que ela possa ser usada por qualquer coisa diferente de [JetSetSystemParameter](./jetsetsystemparameter-function.md).

Uma instância é destruída por uma chamada para a [função JetTerm,](./jetterm-function.md) mesmo que essa instância nunca seja inicializada usando [JetInit](./jetinit-function.md). O número máximo de instâncias que podem ser criadas a qualquer momento é controlado por *JET_paramMaxInstances*, que pode ser configurado por uma chamada para [JetSetSystemParameter](./jetsetsystemparameter-function.md). Uma instância é a unidade de capacidade de recuperação para o mecanismo de banco de dados. Ele controla o ciclo de vida de todos os arquivos usados para proteger a integridade dos dados em um conjunto de arquivos de banco de dados. Esses arquivos incluem o arquivo de ponto de verificação e os arquivos de log de transações.

Se a função for bem-sucedida, o mecanismo de banco de dados será alterado automaticamente para o modo de várias instâncias como um efeito colateral dessa chamada. Se o aplicativo desejar permitir apenas uma instância no processo, [o JetInit](./jetinit-function.md) deverá ser usado para iniciar o mecanismo de banco de dados no modo de compatibilidade Windows 2000.

Se presente, o parâmetro *szDisplayName* será usado para identificar a instância em locais como o Log de Eventos ou para outros chamadores, como aplicativos de backup (por meio de funções como [JetGetInstanceInfo](./jetgetinstanceinfo-function.md) ou [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)). Se o nome de exibição não for fornecido, o parâmetro *szInstanceName* exclusivo será usado, se presente, caso contrário, uma cadeia de caracteres vazia será retornada. Se o mecanismo não tiver o modo de execução definido, após essa chamada, ele será definido como modo de várias instâncias.

A sequência de início típica para um processo potencialmente executando várias instâncias do Jet seria:

  - Uma chamada para **JetCreateInstance2** que alocará e nomeará a instância.

  - Várias chamadas para [JetSetSystemParameter](./jetsetsystemparameter-function.md) para essa instância para definir parâmetros de sistema diferentes. Observe que alguns parâmetros do sistema precisam ser exclusivos para cada instância (como *JET_paramSystemPath* *ou JET_paramLogFilePath*) portanto, provavelmente, cada um deles precisará ser definido.

  - Inicie a instância usando [JetInit](./jetinit-function.md) ou [JetInit2](./jetinit2-function.md). Para encerrar e/ou liberar uma instância, use [JetTerm](./jetterm-function.md) ou [JetTerm2.](./jetterm2-function.md)

Se esta for a primeira instância a ser iniciada, haverá várias etapas adicionais que serão executadas durante essa chamada para fazer a inicialização e a configuração básicas do sistema. Várias dessas etapas podem resultar em erros específicos, começando com JET_errOutOfMemory, mas outros também (consulte Valores de retorno para obter mais informações).

#### <a name="requirements"></a>Requisitos


| Requisito | Valor |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requer Windows Vista ou Windows XP.</p> | 
| <p><strong>Servidor</strong></p> | <p>Requer Windows Server 2008 ou Windows Server 2003.</p> | 
| <p><strong>Cabeçalho</strong></p> | <p>Declarado em Esent.h.</p> | 
| <p><strong>Biblioteca</strong></p> | <p>Use ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Implementado como <strong>JetCreateInstance2W</strong> (Unicode) e <strong>JetCreateInstance2A</strong> (ANSI).</p> | 



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
