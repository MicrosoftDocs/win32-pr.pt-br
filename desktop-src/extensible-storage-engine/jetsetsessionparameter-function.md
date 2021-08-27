---
description: 'Saiba mais sobre: função JetSetSessionParameter'
title: Função JetSetSessionParameter
TOCTitle: JetSetSessionParameter Function
ms:assetid: 11aecf42-22ef-4bea-a3d7-961a7bdc85aa
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835038(v=EXCHG.10)
ms:contentKeyID: 49894660
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetSetSessionParameter
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9ce9c50908621f005ec69aa75da4afdfa722b8aa
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122988399"
---
# <a name="jetsetsessionparameter-function"></a>Função JetSetSessionParameter


_**Aplica-se a:** Windows | Windows Servidor_

A função **JetSetSessionParameter** configura o mecanismo de banco de dados.

``` c++
JET_ERR JET_API JetSetSessionParameter (
  __in_opt      JET_SESID sesid,
  __in          unsigned long sesparamid,
  __in_read_bytes_opt_(cbParam)  void* pvParam,
  __in          unsigned long cbParam
);
```

### <a name="parameters"></a>Parâmetros

*sesid*

Especifica a sessão a ser usada para esta chamada.

Quando especificado, a instância especificada é ignorada e a instância associada à sessão será usada.

*sesparamid*

A ID do parâmetro de sessão a ser definido.

*pvParam*

Os dados a serem definidos neste parâmetro de sessão.

*cbParam*

O tamanho dos dados fornecidos.

### <a name="return-value"></a>Valor retornado

Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno listados na tabela a seguir. para obter mais informações sobre os possíveis erros do ESE (extensible Armazenamento engine), consulte [erros do mecanismo de Armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).


| <p>Código de retorno</p> | <p>Descrição</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>A operação foi concluída com sucesso.</p> | 
| <p>JET_errAlreadyInitialized</p> | <p>A instância foi inicializada usando uma chamada para a função <a href="gg294068(v=exchg.10).md">JetInit</a> e essa operação não pode ser executada como resultado. Isso pode acontecer quando é feita uma tentativa de configurar um parâmetro do sistema depois que uma alteração no valor do parâmetro não pode mais afetar o estado do mecanismo de banco de dados.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Não é possível concluir a operação porque toda a atividade na instância associada à sessão foi interrompida como resultado de uma chamada para a função <a href="gg269240(v=exchg.10).md">JetStopService</a> .</p> | 
| <p>JET_errIndexTuplesInvalidLimits</p> | <p>Os parâmetros de índice de tupla especificados eram ilegais. Esse erro é retornado somente quando o parâmetro <em>JET_paramIndexTuplesLengthMin</em>, <em>JET_paramIndexTuplesLengthMax</em>ou <em>JET_paramIndexTuplesToIndexMax</em> é definido como um valor ilegal. Para obter informações sobre esses parâmetros, consulte <a href="gg294119(v=exchg.10).md">parâmetros de índice</a>.</p> | 
| <p>JET_errInitInProgress</p> | <p>Não é possível concluir a operação porque a instância associada à sessão está sendo inicializada.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Um dos parâmetros fornecidos continha um valor inesperado ou continha um valor que não fazia sentido quando combinado com o valor de outro parâmetro. Isso pode acontecer quando ocorre o seguinte:</p><ul><li><p>A ID do parâmetro do sistema especificada é inválida ou não tem suporte.</p></li><li><p>Foi feita uma tentativa de definir um parâmetro de sistema com valor de cadeia de caracteres com uma cadeia de caracteres cujo comprimento estava fora do intervalo legal para o parâmetro.</p></li><li><p>Foi feita uma tentativa de definir um parâmetro de sistema com valor de cadeia de caracteres com um caminho de arquivo em que o comprimento de sua representação de caminho absoluto estava fora do intervalo legal para esse parâmetro.</p></li><li><p>Foi feita uma tentativa de definir um parâmetro de sistema com valor inteiro com um inteiro que estava fora do intervalo legal para o parâmetro.</p></li><li><p>Foi feita uma tentativa de definir JET_paramUnicodeIndexDefault com um ponteiro de <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> nulo, um LCID inválido ou um conjunto sem suporte de sinalizadores <strong>LCMapString</strong> .</p></li><li><p>O parâmetro de sistema especificado não pode ser definido porque é somente leitura.</p></li><li><p>Foi feita uma tentativa de definir um parâmetro do sistema após a chamada da função <a href="gg294068(v=exchg.10).md">JetInit</a> , o mecanismo de banco de dados está no modo de instância única e não foi especificada uma sessão.</p></li><li><p>O parâmetro do sistema especificado é global somente e foi feita uma tentativa de definir um valor específico da instância para esse parâmetro do sistema.</p></li><li><p>O parâmetro do sistema especificado é somente por instância e foi feita uma tentativa de definir o valor global para esse parâmetro do sistema.</p></li></ul> | 
| <p>JET_errInvalidPath</p> | <p>O caminho do sistema de arquivos especificado era inválido. Esse erro pode ser retornado por <strong>JetSetSessionParameter</strong> somente ao definir parâmetros do sistema que representam caminhos do sistema de arquivos. Por exemplo, o parâmetro <em>JET_paramSystemPath</em> pode retornar esse erro. Para obter informações sobre esse parâmetro, consulte <a href="gg269235(v=exchg.10).md">parâmetros do log de transações</a>.</p> | 
| <p>JET_errNotInitialized</p> | <p>Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</p> | 
| <p>JET_errTermInProgress</p> | <p>Não é possível concluir a operação porque a instância associada à sessão está sendo desligada.</p> | 
| <p>JET_errInvalidSesid</p> | <p>O identificador de sessão é inválido ou se refere a uma sessão fechada.</p><p>Esse erro não é retornado em todas as circunstâncias. Os identificadores são validados apenas com base no melhor esforço.</p> | 
| <p>JET_errInvalidInstance</p> | <p>O identificador de instância é inválido ou se refere a uma instância que foi desligada.</p><p>Esse erro não é retornado em todas as circunstâncias. Os identificadores são validados apenas com base no melhor esforço.</p> | 



Em caso de sucesso, o parâmetro do sistema será definido para o valor fornecido.

Se houver falha, o valor do parâmetro do sistema permanecerá inalterado.

#### <a name="requirements"></a>Requisitos


| Requisito | Valor |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>Requer Windows 8.</p> | 
| <p><strong>Servidor</strong></p> | <p>Requer Windows Server 2012.</p> | 
| <p><strong>Cabeçalho</strong></p> | <p>Declarado em ESENT. h.</p> | 
| <p><strong>Biblioteca</strong></p> | <p>Use ESENT. lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte também

[JET_API_PTR](./jet-api-ptr.md)  
[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JET_SESID](./jet-sesid.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetGetSystemParameter](./jetgetsystemparameter-function.md)  
[JetInit](./jetinit-function.md)  
[Parâmetros do sistema](./extensible-storage-engine-system-parameters.md)
