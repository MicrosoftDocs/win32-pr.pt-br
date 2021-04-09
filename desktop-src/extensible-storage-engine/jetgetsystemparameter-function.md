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
ms.openlocfilehash: 80005be47037bade1f22e8125d4633c5dac45f8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171340"
---
# <a name="jetgetsystemparameter-function"></a>Função JetGetSystemParameter


_**Aplica-se a:** Windows | Windows Server_

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

Para o Windows 2000, esse parâmetro é ignorado e sempre deve ser **nulo**.

Para o Windows XP e versões posteriores, esse parâmetro é um pouco sobrecarregado. Se o mecanismo estiver operando no modo herdado (modo de compatibilidade do Windows 2000) em que apenas uma instância tem suporte, esse parâmetro poderá ser **nulo** ou poderá conter a instância real retornada por [JetInit](./jetinit-function.md). Em qualquer um dos casos, todas as configurações de parâmetro do sistema são lidas a partir dessa instância. Se o mecanismo estiver operando no modo de várias instâncias, esse parâmetro poderá ser **nulo** ou um ponteiro para uma instância criada usando [JetInit](./jetinit-function.md) ou [JetCreateInstance](./jetcreateinstance-function.md). Quando esse parâmetro for **nulo** , a configuração do parâmetro do sistema global (ou padrão) será lida. Quando esse parâmetro for uma instância, a configuração de parâmetro do sistema para essa instância será lida.

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
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Não é possível concluir a operação porque toda a atividade na instância associada à sessão foi interrompida como resultado de uma chamada para <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInitInProgress</p></td>
<td><p>Não é possível concluir a operação porque a instância associada à sessão está sendo inicializada.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados. Esse erro só será retornado pelo Windows XP e por versões posteriores.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Um dos parâmetros fornecidos continha um valor inesperado ou continha um valor que não fazia sentido quando combinado com o valor de outro parâmetro.</p>
<p>Isso pode ocorrer para <strong>JetGetSystemParameter</strong> quando:</p>
<ul>
<li><p>A ID do parâmetro do sistema especificada é inválida ou não tem suporte.</p></li>
<li><p>O parâmetro do sistema especificado requer que o buffer de saída inteiro seja fornecido e o ponteiro do buffer de saída era <strong>nulo</strong>.</p></li>
<li><p>O parâmetro do sistema especificado requer que um buffer de saída de cadeia de caracteres seja fornecido e o ponteiro do buffer de saída era <strong>nulo</strong>.</p>
<p><strong>Windows Vista:  </strong> Isso só pode acontecer no Windows Vista e versões posteriores.</p></li>
<li><p>O parâmetro do sistema especificado requer que um buffer de saída de cadeia de caracteres seja fornecido e o tamanho desse buffer de saída seja muito pequeno para aceitar uma cadeia de caracteres terminada em NULL.</p>
<p><strong>Windows Vista:  </strong> Isso só pode acontecer no Windows Vista e versões posteriores.</p></li>
<li><p>O parâmetro do sistema especificado não pode ser lido porque é somente gravação.</p></li>
<li><p>O parâmetro do sistema especificado é global somente e foi feita uma tentativa de ler um valor específico de instância para esse parâmetro de sistema. Isso só pode acontecer no Windows XP e versões posteriores.</p></li>
<li><p>O parâmetro do sistema especificado é somente por instância e foi feita uma tentativa de ler o valor global para esse parâmetro do sistema. Isso só pode acontecer no Windows XP e versões posteriores.</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_errNotInitialized</p></td>
<td><p>Não é possível concluir a operação porque a instância associada à sessão ainda não foi inicializada.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Não é possível concluir a operação porque uma operação de restauração está em andamento na instância associada à sessão.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTermInProgress</p></td>
<td><p>Não é possível concluir a operação porque a instância associada à sessão está sendo desligada.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidSesid</p></td>
<td><p>O identificador de sessão é inválido ou se refere a uma sessão fechada. Esse erro não é retornado em todas as circunstâncias. Os identificadores são validados apenas com base no melhor esforço.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidInstance</p></td>
<td><p>O identificador de instância é inválido ou se refere a uma instância que foi desligada. Esse erro não é retornado em todas as circunstâncias. Os identificadores são validados apenas com base no melhor esforço.</p>
<p><strong>Windows Vista:  </strong> Esse erro só será retornado pelo Windows Vista e por versões posteriores.</p></td>
</tr>
<tr class="odd">
<td><p>JET_wrnBufferTruncated</p></td>
<td><p>A operação foi concluída com êxito, mas o buffer de saída era muito pequeno para receber a configuração de parâmetro do sistema inteira.</p>
<p>O buffer de saída foi preenchido com a maior parte da configuração de parâmetro do sistema que se ajustaria. Se o buffer de saída tiver pelo menos um caractere de comprimento, a cadeia de caracteres nesse buffer de saída será terminada em nulo.</p>
<p><strong>Observação  </strong> Esse erro não é retornado por todas as versões. Consulte a seção comentários para obter mais informações.</p></td>
</tr>
<tr class="even">
<td><p>JET_errBufferTooSmall</p></td>
<td><p>A operação falhou porque o buffer de saída era muito pequeno para receber a configuração do parâmetro do sistema inteiro.</p>
<p><strong>Observação  </strong> Esse erro não é retornado em alguns casos para preservar a compatibilidade de aplicativos. Consulte a seção comentários para obter mais informações.</p>
<p><strong>Windows Vista:  </strong> Esse erro só será retornado pelo Windows Vista e por versões posteriores.</p></td>
</tr>
</tbody>
</table>


Em caso de sucesso, o buffer de saída apropriado para o parâmetro do sistema solicitado será definido como o valor desse parâmetro do sistema.

Em caso de falha, o estado dos buffers de saída será indefinido.

#### <a name="remarks"></a>Comentários

Há um problema importante nessa API que está presente em todas as versões. Se um parâmetro do sistema com um valor de cadeia de caracteres for solicitado e o buffer de saída for muito pequeno para receber a configuração inteira de parâmetro do sistema, JET_wrnBufferTruncated não será retornado. JET_errSuccess é retornado em vez disso. Se o comprimento da cadeia de caracteres retornada for igual ao tamanho do buffer de saída menos o terminador **NULL** , o chamador deverá reagir como se JET_wrnBufferTruncated fossem retornadas. Se um buffer de saída de cadeia de caracteres de tamanho zero for especificado, o chamador deverá reagir como se JET_errInvalidParameter fosse retornado.

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
<td><p>Implementado como <strong>JetGetSystemParameterW</strong> (Unicode) e <strong>JetGetSystemParameterA</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


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
