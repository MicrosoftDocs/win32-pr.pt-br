---
description: 'Saiba mais sobre: Função JetSetSystemParameter'
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
ms.openlocfilehash: c1d72fa8b5cda24435cec0f4ec5f0751862bc14c
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122986539"
---
# <a name="jetsetsystemparameter-function"></a>Função JetSetSystemParameter


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetsetsystemparameter-function"></a>Função JetSetSystemParameter

A **função JetSetSystemParameter** é usada para definir as várias definições de configuração do mecanismo de banco de dados.

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

Especifica a instância a ser usada para essa chamada.

**Windows 2000:**  Por Windows 2000, esse parâmetro é ignorado e sempre deve ser **NULL.**

**Windows XP:**  Para Windows XP e versões posteriores, esse parâmetro é um pouco sobrecarregado. Se o mecanismo estiver operando no modo herdado (Windows modo de compatibilidade 2000), em que há suporte para apenas uma instância, esse parâmetro poderá ser **NULL** ou poderá conter a instância real retornada pelo [JetInit](./jetinit-function.md). Em ambos os casos, todas as configurações de parâmetro do sistema são lidas dessa instância. Se o mecanismo estiver operando no modo de várias instâncias, esse parâmetro poderá ser **NULL** ou um ponteiro para uma instância criada usando [JetInit](./jetinit-function.md) ou [JetCreateIndex.](./jetcreateindex-function.md) Quando esse parâmetro for **NULL,** a configuração de parâmetro do sistema global (ou padrão) será lida. Quando esse parâmetro é uma instância, a configuração de parâmetro do sistema para essa instância é lida.

Embora esse seja tecnicamente um parâmetro out, essa API nunca modifica o conteúdo do buffer fornecido.

*sesid*

Especifica a sessão a ser usada para essa chamada.

Quando especificado, a instância especificada é ignorada e a instância associada à sessão será usada.

*paramid*

A ID do parâmetro do sistema que será definido. Confira [Parâmetros do Sistema](./extensible-storage-engine-system-parameters.md) para ver uma lista completa dos parâmetros do sistema e suas propriedades.

*lParam*

Fornece o valor a ser definido para o parâmetro do sistema selecionado se esse parâmetro do sistema for de um tipo inteiro.

*szParam*

Fornece o valor para o parâmetro do sistema selecionado se esse parâmetro do sistema for de um tipo de cadeia de caracteres.

### <a name="return-value"></a>Valor Retornado

Essa função retorna o [JET_ERR](./jet-err.md) de dados com um dos códigos de retorno a seguir. Para obter mais informações sobre os possíveis erros de ESE, consulte [Extensible Armazenamento Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Código de retorno</p> | <p>Descrição</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>A operação foi concluída com sucesso.</p><p><strong>Windows Vista:</strong>  No Windows Vista e versões posteriores, o sucesso pode ser retornado sem uma alteração no valor do parâmetro do sistema. Consulte o JET_paramEnableAdvanced do sistema no tópico <a href="gg269346(v=exchg.10).md">Meta Parameters</a> para obter mais informações.</p> | 
| <p>JET_errAlreadyInitialized</p> | <p>A instância foi inicializada usando uma chamada para <a href="gg294068(v=exchg.10).md">JetInit</a> e essa operação não pode ser executada como resultado. Isso pode acontecer para <strong>JetSetSystemParameter</strong> quando é feita uma tentativa de configurar um parâmetro do sistema após uma alteração em seu valor não pode afetar o estado do mecanismo de banco de dados.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Não é possível concluir a operação porque todas as atividades na instância associada à sessão foram encerradas como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errIndexTuplesInvalidLimits</p> | <p>Os parâmetros de índice de tupla especificados eram ilícitos. Esse erro pode ser retornado por <strong>JetSetSystemParameter</strong> somente ao definir JET_paramIndexTuplesLengthMin <a href="gg294119(v=exchg.10).md">,</a> <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesLengthMax</a>ou JET_paramIndexTuplesToIndexMax <a href="gg294119(v=exchg.10).md">como</a> um valor ilegal.</p><p><strong>Windows XP e Windows Server 2003:</strong>  Isso só pode acontecer no Windows XP e Windows Server 2003.</p> | 
| <p>JET_errInitInProgress</p> | <p>Não é possível concluir a operação porque a instância associada à sessão está sendo inicializada.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</p><p><strong>Windows XP:</strong>  Esse erro só será retornado por Windows XP e versões posteriores.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Um dos parâmetros fornecidos continha um valor inesperado ou continha um valor que não fazia sentido quando combinado com o valor de outro parâmetro. Isso pode acontecer para <strong>JetSetSystemParameter</strong> quando:</p><ul><li><p>A ID do parâmetro do sistema especificada é inválida ou não é compatível.</p></li><li><p>Foi feita uma tentativa de definir um parâmetro de sistema com valor de cadeia de caracteres com uma cadeia de caracteres cujo comprimento estava fora do intervalo legal para o parâmetro.</p></li><li><p>Foi feita uma tentativa de definir um parâmetro de sistema com valor de cadeia de caracteres com um caminho de arquivo em que o comprimento de sua representação de caminho absoluto estava fora do intervalo legal para esse parâmetro.</p><p><strong>Windows Vista:</strong>  Isso só pode acontecer no Windows Vista e versões posteriores.</p></li><li><p>Foi feita uma tentativa de definir um parâmetro de sistema com valor inteiro com um inteiro que estava fora do intervalo legal para o parâmetro.</p></li><li><p>Foi feita uma tentativa de definir <strong></strong>JET_paramUnicodeIndexDefault com um ponteiro<a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> NULL, um LCID inválido ou um conjunto sem suporte de sinalizadores LCMapString.</p><p><strong>Windows Vista:</strong>  Isso só pode acontecer no Windows Vista e versões posteriores.</p></li><li><p>O parâmetro do sistema especificado não pode ser definido porque é somente leitura.</p></li><li><p>Foi feita uma tentativa de definir um parâmetro do sistema depois que <a href="gg294068(v=exchg.10).md">JetInit</a> foi chamado, o mecanismo de banco de dados está no modo de instância única e uma sessão não foi especificada.</p><p><strong>Windows XP e Windows Server 2003:</strong>  Isso só pode acontecer no Windows XP e Windows Server 2003.</p></li><li><p>O parâmetro do sistema especificado é global apenas e foi feita uma tentativa de definir um valor específico da instância para esse parâmetro do sistema.</p><p><strong>Windows XP e Windows Server 2003:</strong>  Isso só pode acontecer no Windows XP e Windows Server 2003.</p></li><li><p>O parâmetro de sistema especificado é somente por instância e foi feita uma tentativa de definir o valor global para esse parâmetro do sistema.</p><p><strong>Windows XP e Windows Server 2003:</strong>  Isso só pode acontecer no Windows XP e Windows Server 2003.</p></li></ul> | 
| <p>JET_errInvalidPath</p> | <p>O caminho do sistema de arquivos especificado era inválido. Esse erro pode ser retornado pelo <strong>JetSetSystemParameter</strong> somente ao definir parâmetros do sistema que representam caminhos do sistema de arquivos. Por exemplo, <a href="gg269235(v=exchg.10).md">JET_paramSystemPath</a> pode retornar esse erro.</p> | 
| <p>JET_errNotInitialized</p> | <p>Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</p> | 
| <p>JET_errTermInProgress</p> | <p>Não é possível concluir a operação porque a instância associada à sessão está sendo desligado.</p> | 
| <p>JET_errInvalidSesid</p> | <p>O alça de sessão é inválido ou refere-se a uma sessão fechada.</p><p>Esse erro não é retornado em todas as circunstâncias. Os alças são validados apenas com base no melhor esforço.</p> | 
| <p>JET_errInvalidInstance</p> | <p>O handle de instância é inválido ou refere-se a uma instância que foi desligado.</p><p>Esse erro não é retornado em todas as circunstâncias. Os alças são validados apenas com base no melhor esforço.</p><p><strong>Windows Vista:</strong>  Esse erro só será retornado pelo Windows Vista e versões posteriores.</p> | 



Em caso de êxito, a configuração para o parâmetro do sistema será definida como o valor fornecido.

Em caso de falha, a configuração do parâmetro do sistema permanecerá inalterada.

#### <a name="remarks"></a>Comentários

**JetSetSystemParameter** faz um trabalho ruim de validar a configuração escolhida para cada parâmetro do sistema. É necessário ter cuidado para não depender dessa validação para impor boas configurações. Preste muita atenção à descrição de cada parâmetro do sistema e siga essas diretrizes para uma boa configuração de parâmetro do sistema.

Há um conjunto de parâmetros do sistema que sempre devem ser definidos para garantir que o mecanismo de banco de dados funcione conforme o esperado. Especificamente, todos os parâmetros do sistema que afetam o layout físico dos arquivos usados pelo mecanismo de banco de dados sempre devem ser definidos. Para obter mais informações, consulte [Parâmetros do sistema.](./extensible-storage-engine-system-parameters.md)

Cada parâmetro do sistema tem um valor padrão. Esses valores padrão foram evoluindo ao longo do tempo e são bastante arbitrários. É altamente recomendável que um aplicativo avalie todos os valores padrão para garantir que eles sejam apropriados. Se eles não são apropriados, eles devem ser configurados pelo aplicativo. Isso é importante, pois muitos desses parâmetros podem afetar muito a confiabilidade, o desempenho e a utilização de recursos do mecanismo de banco de dados.

#### <a name="requirements"></a>Requisitos


| Requisito | Valor |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requer Windows Vista, Windows XP ou Windows 2000 Professional.</p> | 
| <p><strong>Servidor</strong></p> | <p>Requer Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</p> | 
| <p><strong>Cabeçalho</strong></p> | <p>Declarado em Esent.h.</p> | 
| <p><strong>Biblioteca</strong></p> | <p>Use ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Implementado como <strong>JetSetSystemParameterW</strong> (Unicode) e <strong>JetSetSystemParameterA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Consulte Também

[JET_API_PTR](./jet-api-ptr.md)  
[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JET_SESID](./jet-sesid.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetGetSystemParameter](./jetgetsystemparameter-function.md)  
[JetInit](./jetinit-function.md)  
[Parâmetros do sistema](./extensible-storage-engine-system-parameters.md)
