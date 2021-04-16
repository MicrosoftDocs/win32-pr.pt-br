---
description: 'Saiba mais sobre: função JetPrereadKeys'
title: Função JetPrereadKeys
TOCTitle: JetPrereadKeys Function
ms:assetid: fc2f46bc-1f81-4af2-aa63-9757e819efc2
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294143(v=EXCHG.10)
ms:contentKeyID: 32765757
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetPrereadKeys
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d35407c171bdcd54eb44e9830f382c08a1e6c6c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104461098"
---
# <a name="jetprereadkeys-function"></a>Função JetPrereadKeys


_**Aplica-se a:** Windows | Windows Server_

## <a name="jetprereadkeys-function"></a>Função JetPrereadKeys

A função **JetPrereadKeys** lê os valores de chave para melhorar o desempenho da limpeza do repositório de versão.

**Windows 7:** a função PrereadKeys é introduzida no Windows 7.

```cpp
    JET_ERR JET_API JetPrereadKeys(
      __in JET_SESID sesid,
      __in JET_TABLEID tableid,
      __in_ecount(ckeys) const void ** rgpvKeys,
      __in_ecount(ckeys) const unsigned long * rgcbKeys,
      __in long ckeys,
      __out_opt long * pckeysPreread,
      __in JET_GRBIT grbit
     );
```

### <a name="parameters"></a>Parâmetros

*sesid*

O contexto da sessão de banco de dados a ser usado para a chamada à API.

*TableID*

O cursor a ser usado para esta chamada.

*rgpvKeys*

Uma matriz de ponteiros para chaves. As chaves podem ser feitas com [JetMakeKey](./jetmakekey-function.md) ou recuperadas com [JetGetBookmark](./jetgetbookmark-function.md). As chaves devem ser classificadas em ordem crescente ou decrescente, dependendo do grbit passado. As chaves podem ser classificadas com memcmp.

*rgcbKeys*

Uma matriz de comprimentos de chave. rgpvKeys \[ n \] deve apontar para uma chave de comprimento rgcbKeys \[ n\]

*ckeys*

O número de chaves. rgpvKeys e rgcbKeys devem cada ponto para uma matriz com pelo menos elementos ckeys.

*pckeysPreread*

Retorna o número de chaves para as quais as subleituras foram realmente emitidas. Este parâmetro pode ser NULL.

*grbit*

Deve ser JET_bitPrereadForward ou JET_bitPrereadBackward. Se grbit for JET_bitPrereadForward, as chaves deverão ser classificadas em ordem crescente. Se grbit for JET_bitPrereadBackward, as chaves deverão ser classificadas em ordem decrescente.

### <a name="return-value"></a>Valor Retornado

Essa função retorna o tipo de dados [JET_ERR](./jet-err.md) com um dos códigos de retorno a seguir. Para obter mais informações sobre os possíveis erros do ESE, consulte [erros do mecanismo de armazenamento extensível](./extensible-storage-engine-errors.md) e [parâmetros de tratamento de erros](./error-handling-parameters.md).

Vários erros de e/s podem ser retornados junto com esses erros de uso de API:

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
<td><p>JET_errInvalidGrbit</p></td>
<td><p>Grbit não foi JET_bitPrereadForward nem JET_bitPrereadBackward.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidBufferSize</p></td>
<td><p>Um tamanho de chave incorreto foi passado. As chaves não podem ser 0 nem maiores que o comprimento máximo da chave para a tabela.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Um parâmetro inválido foi passado. Isso pode ser causado por um valor nulo para um parâmetro necessário ou pode indicar que a matriz de chave não está classificada corretamente.</p></td>
</tr>
</tbody>
</table>


**JetPrereadKeys** percorre as páginas internas da árvore b para determinar quais páginas de folha contêm as chaves especificadas por RgpvKeys/rgcbKeys. A lista de páginas de folha é classificada e, em seguida, as conleituras são emitidas para os intervalos de páginas. O número de páginas que podem ser conlidas é limitado, portanto, é possível que nem todas as chaves possam ser conlidas. Nesse caso, o número de chaves realmente lidas é retornado em pckeysPreread.

#### <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Cliente</strong></p></td>
<td><p>Requer o Windows 7.</p></td>
</tr>
<tr class="even">
<td><p><strong>Servidor</strong></p></td>
<td><p>Requer o Windows Server 2008 R2.</p></td>
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
