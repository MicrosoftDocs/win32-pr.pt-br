---
description: 'Saiba mais sobre: função JetEnableMultiInstance'
title: Função JetEnableMultiInstance
TOCTitle: JetEnableMultiInstance Function
ms:assetid: d88a7b2a-c0d1-47de-9239-3631150d92da
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294107(v=EXCHG.10)
ms:contentKeyID: 32765722
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetEnableMultiInstanceW
- JetEnableMultiInstanceA
- JetEnableMultiInstance
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 61fb058b14d9a8abeb282d4227b110ba50304a7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105783676"
---
# <a name="jetenablemultiinstance-function"></a>Função JetEnableMultiInstance


_**Aplica-se a:** Windows | Windows Server_

## <a name="jetenablemultiinstance-function"></a>Função JetEnableMultiInstance

A função **JetEnableMultiInstance** configura o mecanismo de banco de dados para uso com várias instâncias no mesmo processo. Uma matriz opcional de parâmetros globais do sistema está disponível para o primeiro chamador que permite a alteração no modo de várias instâncias.

**Windows XP: o JetEnableMultiInstance** é introduzido no Windows XP.

```cpp
    JET_ERR JET_API JetEnableMultiInstance(
      __in_opt      JET_SETSYSPARAM* psetsysparam,
      __in_opt      unsigned long csetsysparam,
      __out_opt     unsigned long* pcsetsucceed
    );
```

### <a name="parameters"></a>Parâmetros

*psetsysparam*

Uma matriz de parâmetros de sistema global para definir se e somente se o mecanismo entrar no modo de várias instâncias como resultado dessa chamada. Se *csetsysparam* for zero, *psetsysparam* será ignorado.

*csetsysparam*

A contagem de elementos para a matriz de parâmetros globais a definir se e somente se o mecanismo entrar no modo de várias instâncias como resultado dessa chamada. Se *csetsysparam* for zero, *psetsysparam* será ignorado.

*pcsetsucceed*

Um ponteiro para a contagem de parâmetros globais do sistema que foram configurados com êxito como resultado dessa chamada.

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
<td><p>JET_errIndexTuplesInvalidLimits</p></td>
<td><p>Os parâmetros de índice de tupla especificados não foram permitidos. Esse erro pode ser retornado por <strong>JetEnableMultiInstance</strong> somente ao definir <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesLengthMin</a>, <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesLengthMax</a>ou <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesToIndexMax</a> como um valor ilegal.</p>
<p><strong>Windows XP:</strong>  Esse valor de retorno é introduzido no Windows XP.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidPath</p></td>
<td><p>O caminho do sistema de arquivos especificado era inválido. Esse erro pode ser retornado por <strong>JetEnableMultiInstance</strong> somente ao definir parâmetros do sistema que representam caminhos do sistema de arquivos. Por exemplo, <a href="gg269235(v=exchg.10).md">JET_paramSystemPath</a> pode retornar esse erro.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRunningInOneInstanceMode</p></td>
<td><p>A operação falhou porque ela é inválida quando o mecanismo de banco de dados está operando em modo de instância única (modo de compatibilidade do Windows 2000).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSystemParamsAlreadySet</p></td>
<td><p><strong>JetEnableMultiInstance</strong> falhou porque o mecanismo já está no modo de várias instâncias.</p>
<p><strong>Observação  </strong> Isso ocorrerá mesmo que nenhum parâmetro do sistema seja especificado.</p></td>
</tr>
</tbody>
</table>


Se essa função for realizada com sucesso, o mecanismo de banco de dados será configurado para ser executado no modo de várias instâncias. O mecanismo também foi configurado com êxito com a lista opcional de parâmetros globais do sistema.

Se essa função falhar, o mecanismo de banco de dados permanecerá no modo atual. Se *pcsetsucceed* for diferente de zero, esse número de parâmetros do sistema permanecerá definido.

#### <a name="remarks"></a>Comentários

Essa função só deve ser usada se o aplicativo precisar configurar um determinado conjunto de parâmetros do sistema atomicamente ao configurar o mecanismo de banco de dados para uso em um cenário de vários usuários no mesmo processo. Se outro método de sincronização estiver disponível, é preferível chamar [JetCreateInstance](./jetcreateinstance-function.md) e [JetSetSystemParameter](./jetsetsystemparameter-function.md) separadamente.

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
<td><p>Implementado como <strong>JetEnableMultiInstanceW</strong> (Unicode) e <strong>JetEnableMultiInstanceA</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Consulte Também

[JET_ERR](./jet-err.md)  
[JET_SETSYSPARAM](./jet-setsysparam-structure.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)
