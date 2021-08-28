---
description: 'Saiba mais sobre: função JetGetSystemParameter'
title: Função JetGetSystemParameter
TOCTitle: JetGetSystemParameter Function
ms:assetid: 6e6ddb49-702c-4c45-ac9f-35ae817696dd
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269291(v=EXCHG.10)
ms:contentKeyID: 32765583
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetSystemParameter
- JetGetSystemParameterA
- JetGetSystemParameterW
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 608a9c464ca645668483934a28a3f79945cd443d
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122984739"
---
# <a name="jetgetsystemparameter-function"></a>Função JetGetSystemParameter


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetgetsystemparameter-function"></a>Função JetGetSystemParameter

A função **JetGetSystemParameter** lê as várias definições de configuração do mecanismo de banco de dados.

```cpp
    JET_ERR JET_API JetGetSystemParameter(
      __in          JET_INSTANCE instance,
      __in          JET_SESID sesid,
      __in          unsigned long paramid,
      __in_out_opt  JET_API_PTR* plParam,
      __out_opt     JET_PSTR szParam,
      __in          unsigned long cbMax
    );
```

### <a name="parameters"></a>Parâmetros

*cópia*

A instância a ser usada para esta chamada.

para Windows 2000, esse parâmetro é ignorado e sempre deve ser **nulo**.

para o Windows XP e versões posteriores, esse parâmetro é um pouco sobrecarregado. se o mecanismo estiver operando no modo herdado (Windows modo de compatibilidade 2000) em que apenas uma instância tem suporte, esse parâmetro poderá ser **nulo** ou poderá conter a instância real retornada por [JetInit](./jetinit-function.md). Em qualquer um dos casos, todas as configurações de parâmetro do sistema são lidas a partir dessa instância. Se o mecanismo estiver operando no modo de várias instâncias, esse parâmetro poderá ser **nulo** ou um ponteiro para uma instância criada usando [JetInit](./jetinit-function.md) ou [JetCreateInstance](./jetcreateinstance-function.md). Quando esse parâmetro for **nulo** , a configuração do parâmetro do sistema global (ou padrão) será lida. Quando esse parâmetro for uma instância, a configuração de parâmetro do sistema para essa instância será lida.

*sesid*

A sessão a ser usada para esta chamada.

Quando especificado, a instância especificada é ignorada e a instância associada à sessão será usada.

*paramid*

A ID do parâmetro do sistema que será lido.

Consulte [parâmetros do sistema](./extensible-storage-engine-system-parameters.md) para obter uma lista completa de parâmetros do sistema e suas propriedades.

*plParam*

O buffer de saída que recebe o valor do parâmetro do sistema selecionado se esse parâmetro do sistema for de um tipo inteiro.

*szParam*

O buffer de saída que recebe o valor do parâmetro do sistema selecionado se o parâmetro do sistema for de um tipo de cadeia de caracteres.

*cbMax*

O tamanho máximo em bytes do buffer de saída da cadeia de caracteres.

### <a name="return-value"></a>Valor Retornado

Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir. para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de Armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).


| <p>Código de retorno</p> | <p>Descrição</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>A operação foi concluída com sucesso.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Não é possível concluir a operação porque toda a atividade na instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errInitInProgress</p> | <p>Não é possível concluir a operação porque a instância associada à sessão está sendo inicializada.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados. esse erro só será retornado pelo Windows XP e versões posteriores.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Um dos parâmetros fornecidos continha um valor inesperado ou continha um valor que não fazia sentido quando combinado com o valor de outro parâmetro.</p><p>Isso pode ocorrer para <strong>JetGetSystemParameter</strong> quando:</p><ul><li><p>A ID do parâmetro do sistema especificada é inválida ou não tem suporte.</p></li><li><p>O parâmetro do sistema especificado requer que o buffer de saída inteiro seja fornecido e o ponteiro do buffer de saída era <strong>nulo</strong>.</p></li><li><p>O parâmetro do sistema especificado requer que um buffer de saída de cadeia de caracteres seja fornecido e o ponteiro do buffer de saída era <strong>nulo</strong>.</p><p><strong>Windows Vista:</strong> isso só pode ocorrer no Windows Vista e versões posteriores.</p></li><li><p>O parâmetro do sistema especificado requer que um buffer de saída de cadeia de caracteres seja fornecido e o tamanho desse buffer de saída seja muito pequeno para aceitar uma cadeia de caracteres terminada em NULL.</p><p><strong>Windows Vista:</strong> isso só pode ocorrer no Windows Vista e versões posteriores.</p></li><li><p>O parâmetro do sistema especificado não pode ser lido porque é somente gravação.</p></li><li><p>O parâmetro do sistema especificado é global somente e foi feita uma tentativa de ler um valor específico de instância para esse parâmetro de sistema. isso só pode ocorrer no Windows XP e versões posteriores.</p></li><li><p>O parâmetro do sistema especificado é somente por instância e foi feita uma tentativa de ler o valor global para esse parâmetro do sistema. isso só pode ocorrer no Windows XP e versões posteriores.</p></li></ul> | 
| <p>JET_errNotInitialized</p> | <p>Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</p> | 
| <p>JET_errTermInProgress</p> | <p>Não é possível concluir a operação porque a instância associada à sessão está sendo desligada.</p> | 
| <p>JET_errInvalidSesid</p> | <p>O identificador de sessão é inválido ou se refere a uma sessão fechada. Esse erro não é retornado em todas as circunstâncias. Os identificadores são validados apenas com base no melhor esforço.</p> | 
| <p>JET_errInvalidInstance</p> | <p>O identificador de instância é inválido ou se refere a uma instância que foi desligada. Esse erro não é retornado em todas as circunstâncias. Os identificadores são validados apenas com base no melhor esforço.</p><p><strong>Windows Vista:</strong> esse erro só será retornado pelo Windows Vista e versões posteriores.</p> | 
| <p>JET_wrnBufferTruncated</p> | <p>A operação foi concluída com êxito, mas o buffer de saída era muito pequeno para receber a configuração de parâmetro do sistema inteira.</p><p>O buffer de saída foi preenchido com a maior parte da configuração de parâmetro do sistema que se ajustaria. Se o buffer de saída tiver pelo menos um caractere de comprimento, a cadeia de caracteres nesse buffer de saída será terminada em nulo.</p><p><strong>Observação  </strong> Esse erro não é retornado por todas as versões. Consulte a seção comentários para obter mais informações.</p> | 
| <p>JET_errBufferTooSmall</p> | <p>A operação falhou porque o buffer de saída era muito pequeno para receber a configuração do parâmetro do sistema inteiro.</p><p><strong>Observação  </strong> Esse erro não é retornado em alguns casos para preservar a compatibilidade de aplicativos. Consulte a seção comentários para obter mais informações.</p><p><strong>Windows Vista:</strong> esse erro só será retornado pelo Windows Vista e versões posteriores.</p> | 



Em caso de sucesso, o buffer de saída apropriado para o parâmetro do sistema solicitado será definido como o valor desse parâmetro do sistema.

Em caso de falha, o estado dos buffers de saída será indefinido.

#### <a name="remarks"></a>Comentários

Há um problema importante nessa API que está presente em todas as versões. Se um parâmetro do sistema com um valor de cadeia de caracteres for solicitado e o buffer de saída for muito pequeno para receber a configuração inteira de parâmetro do sistema, JET_wrnBufferTruncated não será retornado. JET_errSuccess é retornado em vez disso. Se o comprimento da cadeia de caracteres retornada for igual ao tamanho do buffer de saída menos o terminador **NULL** , o chamador deverá reagir como se JET_wrnBufferTruncated fossem retornadas. Se um buffer de saída de cadeia de caracteres de tamanho zero for especificado, o chamador deverá reagir como se JET_errInvalidParameter fosse retornado.

#### <a name="requirements"></a>Requisitos


| Requisito | Valor |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>requer o Windows Vista, Windows XP ou Windows 2000 Professional.</p> | 
| <p><strong>Servidor</strong></p> | <p>requer o Windows server 2008, Windows server 2003 ou Windows servidor 2000.</p> | 
| <p><strong>Cabeçalho</strong></p> | <p>Declarado em ESENT. h.</p> | 
| <p><strong>Biblioteca</strong></p> | <p>Use ESENT. lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Implementado como <strong>JetGetSystemParameterW</strong> (Unicode) e <strong>JetGetSystemParameterA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Consulte Também

[JET_API_PTR](./jet-api-ptr.md)  
[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JET_SESID](./jet-sesid.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[JetStopService](./jetstopservice-function.md)  
[Parâmetros do sistema](./extensible-storage-engine-system-parameters.md)
