---
description: 'Saiba mais sobre: JET_PFNREALLOC função de retorno de chamada'
title: JET_PFNREALLOC função de retorno de chamada
TOCTitle: JET_PFNREALLOC Callback Function
ms:assetid: 443d0b7e-1c3b-4584-9bc3-938724527313
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269237(v=EXCHG.10)
ms:contentKeyID: 32765539
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f7427a28752384f6c30e050458e5844dcaedd1a7
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122989139"
---
# <a name="jet_pfnrealloc-callback-function"></a>JET_PFNREALLOC função de retorno de chamada


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jet_pfnrealloc-callback-function"></a>JET_PFNREALLOC função de retorno de chamada

A função JET_PFNREALLOC é um retorno de chamada compatível com [realocação](/cpp/c-runtime-library/reference/realloc?view=vs-2019) usado pelo [JetEnumerateColumns](./jetenumeratecolumns-function.md) para alocar memória para seus buffers de saída.

```cpp
    void * JET_API JET_PFNREALLOC(
      [in]                 void* pvContext,
      [in]                 void* pv,
      [in]                 unsigned long cb
    );
```

### <a name="parameters"></a>Parâmetros

*pvContext*

O ponteiro de contexto fornecido para [JetEnumerateColumns](./jetenumeratecolumns-function.md). Esse ponteiro de contexto pode ser usado para transmitir o estado do chamador de [JetEnumerateColumns](./jetenumeratecolumns-function.md) para a implementação desse retorno de chamada.

*PV*

Se não for NULL, especifica um ponteiro para um bloco de memória alocado anteriormente por este retorno de chamada. Se for NULL, um novo bloco de memória do tamanho solicitado será alocado.

*CB*

O novo tamanho do bloco de memória em bytes. Se esse parâmetro for 0 (zero) e um bloco de memória for especificado, esse bloco de memória será liberado.

### <a name="return-value"></a>Valor Retornado

O sistema pode gerar códigos de êxito ou de falha como resultado de uma chamada para essa função. para obter informações sobre como retornar esses códigos como hresults, consulte [erros do mecanismo de Armazenamento extensível](./extensible-storage-engine-errors.md).


| <p>Código de retorno</p> | <p>Descrição</p> | 
|--------------------|--------------------|
| <p>Êxito</p> | <p>Se um bloco de memória alocado anteriormente tiver sido especificado e um novo tamanho zero for especificado, esse bloco será liberado e nulo será retornado. Se um bloco de memória alocado anteriormente tiver sido especificado e um novo tamanho diferente de zero tiver sido especificado, o bloco de memória realocada será retornado. Se nenhum bloco de memória tiver sido especificado, um bloco de memória recentemente alocado do tamanho especificado será retornado.</p> | 
| <p>Falha</p> | <p>NULL será retornado. Se um bloco de memória alocado anteriormente tiver sido fornecido, esse bloco permanecerá alocado.</p> | 



### <a name="requirements"></a>Requisitos


| Requisito | Valor |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>requer o Windows Vista, Windows XP ou Windows 2000 Professional.</p> | 
| <p><strong>Servidor</strong></p> | <p>requer o Windows server 2008, Windows server 2003 ou Windows servidor 2000.</p> | 
| <p><strong>Cabeçalho</strong></p> | <p>Declarado em ESENT. h.</p> | 



### <a name="see-also"></a>Consulte Também

[JetEnumerateColumns](./jetenumeratecolumns-function.md)
