---
description: 'Saiba mais sobre: função JetGetSessionParameter'
title: Função JetGetSessionParameter
TOCTitle: JetGetSessionParameter Function
ms:assetid: 36fbcc06-a72d-4bfb-976b-1b705487732a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835039(v=EXCHG.10)
ms:contentKeyID: 49894661
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetGetSessionParameter
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7953c2359d651d1bb6c9d5a006c02d9b19de6662
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122477912"
---
# <a name="jetgetsessionparameter-function"></a>Função JetGetSessionParameter


_**Aplica-se a:** Windows | Windows Servidor_

A função **JetGetSessionParameter** lê o parâmetro de sessão para a sessão especificada.

a função **JetGetSessionParameter** foi introduzida no sistema operacional Windows 8.

``` c++
JET_ERR JET_API JetGetSessionParameter (
  __in_opt      JET_SESID sesid,
  __in          unsigned long sesparamid,
  __out_cap_post_count_(cbParamMax, *pcbParamActual)  void* pvParam,
  __in          unsigned long cbParamMax,
  __out_opt_    unsigned long pcbParamActual
);
```

### <a name="parameters"></a>Parâmetros

*sesid*

A sessão a ser usada para esta chamada.

Quando especificado, a instância especificada é ignorada e a instância associada à sessão será usada.

*sesparamid*

A ID do parâmetro de sessão a ser definido.

*pvParam*

Dados neste parâmetro de sessão.

*cbParamMax*

O tamanho máximo do conjunto de dados neste parâmetro de sessão.

*pcbParamActual*

O tamanho real do conjunto de dados neste parâmetro de sessão.

### <a name="return-value"></a>Valor retornado

Em caso de sucesso, o buffer de saída apropriado para o parâmetro de sessão solicitado será definido como o valor desse parâmetro de sessão.

Em caso de falha, o estado dos buffers de saída será indefinido.

#### <a name="remarks"></a>Comentários

O parâmetro Session é usado para o tempo de vida da sessão ou até que o valor seja redefinido.

#### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requer Windows 8.</p> | | <p><strong>Servidor</strong></p> | <p>Requer Windows Server 2012.</p> | | <p><strong>Cabeçalho</strong></p> | <p>Declarado em ESENT. h.</p> | | <p><strong>Biblioteca</strong></p> | <p>Use ESENT. lib.</p> | | <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | 



#### <a name="see-also"></a>Confira também

[JET_API_PTR](./jet-api-ptr.md)  
[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JET_SESID](./jet-sesid.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[JetStopService](./jetstopservice-function.md)  
[Parâmetros do sistema](./extensible-storage-engine-system-parameters.md)
