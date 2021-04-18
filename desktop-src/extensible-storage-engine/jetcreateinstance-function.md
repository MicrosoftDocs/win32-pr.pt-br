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
ms.openlocfilehash: aa64c9aadd9402ee8356a8f4db81f878022b838b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105793685"
---
# <a name="jetcreateinstance-function"></a>Função JetCreateInstance


_**Aplica-se a:** Windows | Windows Server_

## <a name="jetcreateinstance-function"></a>Função JetCreateInstance

A função **JetCreateInstance** aloca uma nova instância do mecanismo de banco de dados para uso em um único processo.

**Windows XP: o JetCreateInstance** é introduzido no Windows XP.

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

Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir. Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Código de retorno</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_errSuccess</p></td>
<td><p>A operação foi concluída com sucesso.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceNameInUse</p></td>
<td><p>O nome de instância especificado já está em uso para este processo.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Um dos parâmetros fornecidos continha um valor inesperado ou continha um valor que não fazia sentido quando combinado com o valor de outro parâmetro. Isso pode ocorrer para <strong>JetCreateInstance</strong> quando <em>pinstance</em> é <strong>nulo</strong>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRunningInOneInstanceMode</p></td>
<td><p>A operação falhou porque não pode ser usada quando o mecanismo de banco de dados está operando em modo de instância única (modo de compatibilidade do Windows 2000).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTooManyInstances</p></td>
<td><p>Não foi possível criar uma nova instância porque o número máximo de instâncias foi atingido. O número máximo de instâncias com suporte é configurado usando o <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> usando <em>JET_paramMaxInstances</em>.</p></td>
</tr>
</tbody>
</table>


Em caso de êxito, uma nova instância será alocada e o identificador para ela será retornado. Neste ponto, todos os parâmetros do sistema para a instância terão os valores dos parâmetros do sistema padrão global. Depois que uma instância for alocada, ela precisará ser terminada e/ou liberada mais tarde.

Em caso de falha, um erro que representa a causa da falha será retornado e nenhuma instância será alocada.

#### <a name="remarks"></a>Comentários

Uma instância deve ser inicializada com uma chamada para [JetInit](./jetinit-function.md) antes que possa ser usada por algo diferente de [JetSetSystemParameter](./jetsetsystemparameter-function.md).

Uma instância é destruída por uma chamada para a função [JetTerm](./jetterm-function.md) , mesmo que essa instância nunca tenha sido inicializada usando [JetInit](./jetinit-function.md). O número máximo de instâncias que podem ser criadas a qualquer momento é controlado por [JET_paramMaxInstances](./resource-parameters.md), que pode ser configurado por uma chamada para [JetSetSystemParameter](./jetsetsystemparameter-function.md). Uma instância é a unidade de capacidade de recuperação para o mecanismo de banco de dados. Ele controla o ciclo de vida de todos os arquivos usados para proteger a integridade dos dados em um conjunto de arquivos de banco de dado. Esses arquivos incluem o arquivo de ponto de verificação e os arquivos de log de transações.

Se a função for bem sucedido, o mecanismo de banco de dados será automaticamente alterado para o modo de várias instâncias como um efeito colateral dessa chamada. Se o aplicativo desejar permitir apenas uma instância no processo, [JetInit](./jetinit-function.md) deverá ser usado para iniciar o mecanismo de banco de dados no modo de compatibilidade do Windows 2000.

Se houver, o *szDisplayName* será usado para identificar a instância em locais como o log de eventos ou para outros chamadores, como aplicativos de backup (por meio de funções como [JetGetInstanceInfo](./jetgetinstanceinfo-function.md) ou [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)). Se o nome de exibição não for fornecido, o *szInstanceName* exclusivo será usado, em vez disso, se estiver presente, caso contrário, uma cadeia de caracteres vazia será retornada. Se o mecanismo não tiver o modo de execução definido, após essa chamada, ele será definido como modo de várias instâncias.

A sequência de inicialização típica para um processo que potencialmente executa várias instâncias do Jet seria:

  - Uma chamada para [JetCreateInstance2](./jetcreateinstance2-function.md) que irá alocar e nomear a instância.

  - Várias chamadas para [JetSetSystemParameter](./jetsetsystemparameter-function.md) para essa instância a fim de definir diferentes parâmetros do sistema. Observe que alguns parâmetros do sistema precisam ser exclusivos por instância (como [JET_paramSystemPath](./transaction-log-parameters.md) ou [JET_paramLogFilePath](./transaction-log-parameters.md)), portanto, provavelmente, será necessário definir cada um deles.

  - Inicie a instância usando [JetInit](./jetinit-function.md) ou [JetInit2](./jetinit2-function.md). Para encerrar e/ou liberar uma instância, [JetTerm](./jetterm-function.md), [JetTerm2](./jetterm2-function.md) precisa ser usado.

Se esta for a primeira instância a ser iniciada, haverá várias etapas adicionais que serão executadas durante essa chamada para fazer a inicialização e a configuração básica do sistema. Várias etapas podem resultar em erros específicos, começando com JET_errOutOfMemory, mas outros também (consulte os erros acima).

#### <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Cliente</strong></p></td>
<td><p>Requer o Windows Vista ou o Windows XP.</p></td>
</tr>
<tr class="even">
<td><p><strong>Servidor</strong></p></td>
<td><p>Requer o Windows Server 2008 ou o Windows Server 2003.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Cabeçalho</strong></p></td>
<td><p>Declarado em ESENT. h.</p></td>
</tr>
<tr class="even">
<td><p><strong>Biblioteca</strong></p></td>
<td><p>Use ESENT. lib.</p></td>
</tr>
<tr class="odd">
<td><p><strong>DLL</strong></p></td>
<td><p>Requer ESENT.dll.</p></td>
</tr>
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Implementado como <strong>JetCreateInstanceW</strong> (Unicode) e <strong>JetCreateInstanceA</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Consulte Também

[Arquivos do mecanismo de armazenamento extensível](./extensible-storage-engine-files.md)  
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
