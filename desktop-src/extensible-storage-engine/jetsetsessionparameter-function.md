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
ms.openlocfilehash: 926ae0db2e47ce571f441ab5836c4ddbe6f8bcc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920774"
---
# <a name="jetsetsessionparameter-function"></a>Função JetSetSessionParameter


_**Aplica-se a:** Windows | Windows Server_

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

### <a name="return-value"></a>Retornar valor

Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno listados na tabela a seguir. Para obter mais informações sobre os possíveis erros do ESE (mecanismo de armazenamento extensível), consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).

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
<td><p>JET_errAlreadyInitialized</p></td>
<td><p>A instância foi inicializada usando uma chamada para a função <a href="gg294068(v=exchg.10).md">JetInit</a> e essa operação não pode ser executada como resultado. Isso pode acontecer quando é feita uma tentativa de configurar um parâmetro do sistema depois que uma alteração no valor do parâmetro não pode mais afetar o estado do mecanismo de banco de dados.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Não é possível concluir a operação porque toda a atividade na instância associada à sessão foi interrompida como resultado de uma chamada para a função <a href="gg269240(v=exchg.10).md">JetStopService</a> .</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexTuplesInvalidLimits</p></td>
<td><p>Os parâmetros de índice de tupla especificados eram ilegais. Esse erro é retornado somente quando o parâmetro <em>JET_paramIndexTuplesLengthMin</em>, <em>JET_paramIndexTuplesLengthMax</em>ou <em>JET_paramIndexTuplesToIndexMax</em> é definido como um valor ilegal. Para obter informações sobre esses parâmetros, consulte <a href="gg294119(v=exchg.10).md">parâmetros de índice</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInitInProgress</p></td>
<td><p>Não é possível concluir a operação porque a instância associada à sessão está sendo inicializada.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Não é possível concluir a operação porque a instância associada à sessão encontrou um erro fatal que exige que o acesso a todos os dados seja revogado para proteger a integridade desses dados.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Um dos parâmetros fornecidos continha um valor inesperado ou continha um valor que não fazia sentido quando combinado com o valor de outro parâmetro. Isso pode acontecer quando ocorre o seguinte:</p>
<ul>
<li><p>A ID do parâmetro do sistema especificada é inválida ou não tem suporte.</p></li>
<li><p>Foi feita uma tentativa de definir um parâmetro de sistema com valor de cadeia de caracteres com uma cadeia de caracteres cujo comprimento estava fora do intervalo legal para o parâmetro.</p></li>
<li><p>Foi feita uma tentativa de definir um parâmetro de sistema com valor de cadeia de caracteres com um caminho de arquivo em que o comprimento de sua representação de caminho absoluto estava fora do intervalo legal para esse parâmetro.</p></li>
<li><p>Foi feita uma tentativa de definir um parâmetro de sistema com valor inteiro com um inteiro que estava fora do intervalo legal para o parâmetro.</p></li>
<li><p>Foi feita uma tentativa de definir JET_paramUnicodeIndexDefault com um ponteiro de <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> nulo, um LCID inválido ou um conjunto sem suporte de sinalizadores <strong>LCMapString</strong> .</p></li>
<li><p>O parâmetro de sistema especificado não pode ser definido porque é somente leitura.</p></li>
<li><p>Foi feita uma tentativa de definir um parâmetro do sistema após a chamada da função <a href="gg294068(v=exchg.10).md">JetInit</a> , o mecanismo de banco de dados está no modo de instância única e não foi especificada uma sessão.</p></li>
<li><p>O parâmetro do sistema especificado é global somente e foi feita uma tentativa de definir um valor específico da instância para esse parâmetro do sistema.</p></li>
<li><p>O parâmetro do sistema especificado é somente por instância e foi feita uma tentativa de definir o valor global para esse parâmetro do sistema.</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidPath</p></td>
<td><p>O caminho do sistema de arquivos especificado era inválido. Esse erro pode ser retornado por <strong>JetSetSessionParameter</strong> somente ao definir parâmetros do sistema que representam caminhos do sistema de arquivos. Por exemplo, o parâmetro <em>JET_paramSystemPath</em> pode retornar esse erro. Para obter informações sobre esse parâmetro, consulte <a href="gg269235(v=exchg.10).md">parâmetros do log de transações</a>.</p></td>
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
<p>Esse erro não é retornado em todas as circunstâncias. Os identificadores são validados apenas com base no melhor esforço.</p></td>
</tr>
</tbody>
</table>


Em caso de sucesso, o parâmetro do sistema será definido para o valor fornecido.

Se houver falha, o valor do parâmetro do sistema permanecerá inalterado.

#### <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Cliente</strong></p></td>
<td><p>Requer o Windows 8.</p></td>
</tr>
<tr class="even">
<td><p><strong>Servidor</strong></p></td>
<td><p>Requer o Windows Server 2012.</p></td>
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
</tbody>
</table>


#### <a name="see-also"></a>Confira também

[JET_API_PTR](./jet-api-ptr.md)  
[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JET_SESID](./jet-sesid.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetGetSystemParameter](./jetgetsystemparameter-function.md)  
[JetInit](./jetinit-function.md)  
[Parâmetros do sistema](./extensible-storage-engine-system-parameters.md)
