---
description: 'Saiba mais sobre: função JetSetSystemParameter'
title: Função JetSetSystemParameter
TOCTitle: JetSetSystemParameter Function
ms:assetid: a244b5c9-6f6e-49d1-a6f7-9248feb9b92d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294044(v=EXCHG.10)
ms:contentKeyID: 32765643
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetSystemParameterA
- JetSetSystemParameterW
- JetSetSystemParameter
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bbb57a1b50f3ad39525b894932f7111b56c3a076
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164631"
---
# <a name="jetsetsystemparameter-function"></a>Função JetSetSystemParameter


_**Aplica-se a:** Windows | Windows Server_

## <a name="jetsetsystemparameter-function"></a>Função JetSetSystemParameter

A função **JetSetSystemParameter** é usada para definir as várias definições de configuração do mecanismo de banco de dados.

```cpp
    JET_ERR JET_API JetSetSystemParameter(
      __in_out_opt  JET_INSTANCE* pinstance,
      __in          JET_SESID sesid,
      __in          unsigned long paramid,
      __in          JET_API_PTR lParam,
      __in_opt      JET_PCSTR szParam
    );
```

### <a name="parameters"></a>Parâmetros

*pinstance*

Especifica a instância a ser usada para esta chamada.

**Windows 2000:**  Para o Windows 2000, esse parâmetro é ignorado e sempre deve ser **nulo**.

**Windows XP:**  Para o Windows XP e versões posteriores, esse parâmetro é um pouco sobrecarregado. Se o mecanismo estiver operando no modo herdado (modo de compatibilidade do Windows 2000) em que apenas uma instância tem suporte, esse parâmetro poderá ser **nulo** ou poderá conter a instância real retornada por [JetInit](./jetinit-function.md). Em qualquer um dos casos, todas as configurações de parâmetro do sistema são lidas a partir dessa instância. Se o mecanismo estiver operando no modo de várias instâncias, esse parâmetro poderá ser **nulo** ou um ponteiro para uma instância criada usando [JetInit](./jetinit-function.md) ou [JetCreateIndex](./jetcreateindex-function.md). Quando esse parâmetro for **nulo** , a configuração do parâmetro do sistema global (ou padrão) será lida. Quando esse parâmetro for uma instância, a configuração de parâmetro do sistema para essa instância será lida.

Embora esse seja tecnicamente um parâmetro out, essa API nunca modifica o conteúdo do buffer fornecido.

*sesid*

Especifica a sessão a ser usada para esta chamada.

Quando especificado, a instância especificada é ignorada e a instância associada à sessão será usada.

*paramid*

A ID do parâmetro do sistema que será definido. Consulte [parâmetros do sistema](./extensible-storage-engine-system-parameters.md) para obter uma lista completa de parâmetros do sistema e suas propriedades.

*lParam*

Fornece o valor a ser definido para o parâmetro do sistema selecionado se esse parâmetro do sistema for de um tipo inteiro.

*szParam*

Fornece o valor para o parâmetro de sistema selecionado se esse parâmetro de sistema for de um tipo de cadeia de caracteres.

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
<td><p>A operação foi concluída com sucesso.</p>
<p><strong>Windows Vista:</strong>  No Windows Vista e versões posteriores, o sucesso pode ser retornado sem uma alteração no valor do parâmetro do sistema. Consulte o parâmetro sistema JET_paramEnableAdvanced no tópico <a href="gg269346(v=exchg.10).md">Metaparâmetros</a> para obter mais informações.</p></td>
</tr>
<tr class="even">
<td><p>JET_errAlreadyInitialized</p></td>
<td><p>A instância foi inicializada usando uma chamada para <a href="gg294068(v=exchg.10).md">JetInit</a> e essa operação não pode ser executada como resultado. Isso pode ocorrer para <strong>JetSetSystemParameter</strong> quando for feita uma tentativa de configurar um parâmetro do sistema depois que uma alteração no seu valor não puder afetar o estado do mecanismo de banco de dados.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Não é possível concluir a operação porque toda a atividade na instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexTuplesInvalidLimits</p></td>
<td><p>Os parâmetros de índice de tupla especificados eram ilegais. Esse erro pode ser retornado por <strong>JetSetSystemParameter</strong> somente ao definir <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesLengthMin</a>, <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesLengthMax</a>ou <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesToIndexMax</a> como um valor ilegal.</p>
<p><strong>Windows XP e Windows Server 2003:</strong>  Isso só pode acontecer no Windows XP e no Windows Server 2003.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInitInProgress</p></td>
<td><p>Não é possível concluir a operação porque a instância associada à sessão está sendo inicializada.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</p>
<p><strong>Windows XP:</strong>  Esse erro só será retornado pelo Windows XP e por versões posteriores.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Um dos parâmetros fornecidos continha um valor inesperado ou continha um valor que não fazia sentido quando combinado com o valor de outro parâmetro. Isso pode ocorrer para <strong>JetSetSystemParameter</strong> quando:</p>
<ul>
<li><p>A ID do parâmetro do sistema especificada é inválida ou não tem suporte.</p></li>
<li><p>Foi feita uma tentativa de definir um parâmetro de sistema com valor de cadeia de caracteres com uma cadeia de caracteres cujo comprimento estava fora do intervalo legal para o parâmetro.</p></li>
<li><p>Foi feita uma tentativa de definir um parâmetro de sistema com valor de cadeia de caracteres com um caminho de arquivo em que o comprimento de sua representação de caminho absoluto estava fora do intervalo legal para esse parâmetro.</p>
<p><strong>Windows Vista:</strong>  Isso só pode acontecer no Windows Vista e versões posteriores.</p></li>
<li><p>Foi feita uma tentativa de definir um parâmetro de sistema com valor inteiro com um inteiro que estava fora do intervalo legal para o parâmetro.</p></li>
<li><p>Foi feita uma tentativa de definir JET_paramUnicodeIndexDefault com um ponteiro de <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> <strong>nulo</strong> , um LCID inválido ou um conjunto sem suporte de sinalizadores LCMapString.</p>
<p><strong>Windows Vista:</strong>  Isso só pode acontecer no Windows Vista e versões posteriores.</p></li>
<li><p>O parâmetro de sistema especificado não pode ser definido porque é somente leitura.</p></li>
<li><p>Foi feita uma tentativa de definir um parâmetro do sistema depois que <a href="gg294068(v=exchg.10).md">JetInit</a> foi chamado, o mecanismo de banco de dados está no modo de instância única e uma sessão não foi especificada.</p>
<p><strong>Windows XP e Windows Server 2003:</strong>  Isso só pode acontecer no Windows XP e no Windows Server 2003.</p></li>
<li><p>O parâmetro do sistema especificado é global somente e foi feita uma tentativa de definir um valor específico de instância para esse parâmetro de sistema.</p>
<p><strong>Windows XP e Windows Server 2003:</strong>  Isso só pode acontecer no Windows XP e no Windows Server 2003.</p></li>
<li><p>O parâmetro do sistema especificado é somente por instância e foi feita uma tentativa de definir o valor global para esse parâmetro do sistema.</p>
<p><strong>Windows XP e Windows Server 2003:</strong>  Isso só pode acontecer no Windows XP e no Windows Server 2003.</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidPath</p></td>
<td><p>O caminho do sistema de arquivos especificado era inválido. Esse erro pode ser retornado por <strong>JetSetSystemParameter</strong> somente ao definir parâmetros do sistema que representam caminhos do sistema de arquivos. Por exemplo, <a href="gg269235(v=exchg.10).md">JET_paramSystemPath</a> pode retornar esse erro.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>Não é possível concluir a operação porque a instância associada à sessão está sendo desligada.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidSesid</p></td>
<td><p>O identificador de sessão é inválido ou se refere a uma sessão fechada.</p>
<p>Esse erro não é retornado em todas as circunstâncias. Os identificadores são validados apenas com base no melhor esforço.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidInstance</p></td>
<td><p>O identificador de instância é inválido ou se refere a uma instância que foi desligada.</p>
<p>Esse erro não é retornado em todas as circunstâncias. Os identificadores são validados apenas com base no melhor esforço.</p>
<p><strong>Windows Vista:</strong>  Esse erro só será retornado pelo Windows Vista e por versões posteriores.</p></td>
</tr>
</tbody>
</table>


Em caso de sucesso, a configuração do parâmetro System será definida como o valor fornecido.

Em caso de falha, a configuração para o parâmetro do sistema permanecerá inalterada.

#### <a name="remarks"></a>Comentários

O **JetSetSystemParameter** faz um trabalho insatisfatório de validar a configuração escolhida para cada parâmetro do sistema. Deve-se ter cuidado para não confiar nessa validação para impor configurações boas. Preste muita atenção à descrição de cada parâmetro do sistema e siga essas diretrizes para obter uma boa configuração de parâmetro do sistema.

Há um conjunto de parâmetros do sistema que devem ser sempre definidos para garantir que o mecanismo de banco de dados funcione conforme o esperado. Especificamente, todos os parâmetros do sistema que afetam o layout físico dos arquivos usados pelo mecanismo de banco de dados sempre devem ser definidos. Para obter mais informações, consulte [parâmetros do sistema](./extensible-storage-engine-system-parameters.md).

Cada parâmetro do sistema tem um valor padrão. Esses valores padrão evoluíram ao longo do tempo e são bastante arbitrários. É altamente recomendável que um aplicativo avalie todos os valores padrão para garantir que eles sejam apropriados. Se eles não forem apropriados, eles deverão ser configurados pelo aplicativo. Isso é importante, pois muitos desses parâmetros podem afetar significativamente a confiabilidade, o desempenho e a utilização de recursos do mecanismo de banco de dados.

#### <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Cliente</strong></p></td>
<td><p>Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p><strong>Servidor</strong></p></td>
<td><p>Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</p></td>
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
<td><p>Implementado como <strong>JetSetSystemParameterW</strong> (Unicode) e <strong>JetSetSystemParameterA</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Consulte Também

[JET_API_PTR](./jet-api-ptr.md)  
[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JET_SESID](./jet-sesid.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetGetSystemParameter](./jetgetsystemparameter-function.md)  
[JetInit](./jetinit-function.md)  
[Parâmetros do sistema](./extensible-storage-engine-system-parameters.md)
