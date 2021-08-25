---
description: 'Saiba mais sobre: Função JetPrereadKeys'
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
ms.openlocfilehash: 067fe72e2e00fc01b433dbda819d5e89336fc68c
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467183"
---
# <a name="jetprereadkeys-function"></a>Função JetPrereadKeys


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetprereadkeys-function"></a>Função JetPrereadKeys

A **função JetPrereadKeys** lê os valores de chave para melhorar o desempenho da limpeza do armazenamento de versão.

**Windows 7: a função PrereadKeys** é introduzida no Windows 7.

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

O contexto de sessão do banco de dados a ser usado para a chamada à API.

*Tableid*

O cursor a ser usado para essa chamada.

*rgpvKeys*

Uma matriz de ponteiros para chaves. As chaves podem ser feitas com [JetMakeKey](./jetmakekey-function.md) ou recuperadas com [JetGetBookmark.](./jetgetbookmark-function.md) As chaves devem ser ordenadas em ordem crescente ou decrescente, dependendo do grbit passado. As chaves podem ser classificação com memcmp.

*rgcbKeys*

Uma matriz de comprimentos de chave. rgpvKeys \[ n deve apontar para uma chave de comprimento \] rgcbKeys \[ n\]

*ckeys*

O número de chaves. rgpvKeys e rgcbKeys devem apontar para uma matriz com pelo menos elementos ckeys.

*pckeysPreread*

Retorna o número de chaves para as que as pré-leituras foram realmente emitidas. Este parâmetro pode ser NULL.

*grbit*

Isso deve ser JET_bitPrereadForward ou JET_bitPrereadBackward. Se grbit for JET_bitPrereadForward, as chaves deverão ser classificação em ordem crescente. Se grbit for JET_bitPrereadBackward, as chaves deverão ser classificação em ordem decrescente.

### <a name="return-value"></a>Valor Retornado

Essa função retorna o [JET_ERR](./jet-err.md) de dados com um dos códigos de retorno a seguir. Para obter mais informações sobre os possíveis erros de ESE, consulte [Extensible Armazenamento Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).

Vários erros de E/S podem ser retornados juntamente com estes erros de uso de API:


| <p>Código de retorno</p> | <p>Descrição</p> | 
|--------------------|--------------------|
| <p>JET_errInvalidGrbit</p> | <p>Grbit não foi JET_bitPrereadForward nem JET_bitPrereadBackward.</p> | 
| <p>JET_errInvalidBufferSize</p> | <p>Um tamanho de chave incorreto foi passado. As chaves não podem ser 0 nem maiores que o comprimento máximo da chave para a tabela.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Um parâmetro inválido foi passado. Isso pode ser causado por um valor nulo para um parâmetro necessário ou pode indicar que a matriz de chaves não está corretamente classificação.</p> | 



**JetPrereadKeys** percorre as páginas internas da árvore b para determinar quais páginas folha contêm as chaves especificadas por rgpvKeys/rgcbKeys. A lista de páginas folha é classificação e, em seguida, os pré-leituras são emitidos para os intervalos de páginas. O número de páginas que podem ser pré-lidas é limitado, portanto, é possível que nem todas as chaves possam ser pré-lidas. Nesse caso, o número de chaves realmente pré-lidas é retornado em pckeysPreread.

#### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requer Windows 7.</p> | | <p><strong>Servidor</strong></p> | <p>Requer Windows Server 2008 R2.</p> | | <p><strong>Cabeçalho</strong></p> | <p>Declarado em Esent.h.</p> | | <p><strong>Biblioteca</strong></p> | <p>Use ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | 

