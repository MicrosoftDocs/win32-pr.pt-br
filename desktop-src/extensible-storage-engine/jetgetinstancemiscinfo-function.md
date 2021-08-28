---
description: 'Saiba mais sobre: Função JetGetInstanceMiscInfo'
title: Função JetGetInstanceMiscInfo
TOCTitle: JetGetInstanceMiscInfo Function
ms:assetid: 0bfe36fe-4ddd-442b-b934-57a7bfb28e5f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269183(v=EXCHG.10)
ms:contentKeyID: 32765486
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetInstanceMiscInfo
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 07167dc0f2cad5192dc30e9897541b6619086bfc
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481342"
---
# <a name="jetgetinstancemiscinfo-function"></a>Função JetGetInstanceMiscInfo


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetgetinstancemiscinfo-function"></a>Função JetGetInstanceMiscInfo

A **função JetGetInstanceMiscInfo** recupera informações sobre a instância, enquanto a instância está online.

**Windows Vista: JetGetInstanceMiscInfo** é introduzido no Windows Vista.

```cpp
    JET_ERR JET_API JetGetInstanceMiscInfo(
      __in          JET_INSTANCE instance,
      __out         void* pvResult,
      __in          unsigned long cbMax,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a>Parâmetros

*Instância*

Identifica a instância de banco de dados que será usada para a chamada à API.

*pvResult*

Ponteiro para um buffer que receberá as informações. O tipo do buffer depende de *InfoLevel.* O chamador é responsável por alinhar o buffer adequadamente.

*cbMax*

O tamanho, em bytes, do buffer passado em *pvResult.*

*InfoLevel*

Determina que tipo de informações serão recuperadas para a instância especificada pela *instância*. O formato dos dados armazenados em *pvResult* depende *de InfoLevel.*

As opções a seguir estão disponíveis para uso com esse parâmetro.


| <p>Valor</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_InstanceMiscInfoLogSignature</p> | <p><em>pvResult</em> é interpretado como uma <a href="gg269340(v=exchg.10).md">estrutura JET_SIGNATURE</a> da sequência de log de transações associada a essa instância.</p> | 



### <a name="return-value"></a>Valor Retornado

Essa função retorna o [JET_ERR](./jet-err.md) de dados com um dos códigos de retorno a seguir. Para obter mais informações sobre os possíveis erros de ESE, consulte [Extensible Armazenamento Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Código de retorno</p> | <p>Descrição</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>A operação foi concluída com sucesso.</p> | 
| <p>JET_errBufferTooSmall</p> | <p>O buffer era muito pequeno.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Foi especificado um <a href="gg294048(v=exchg.10).md">JET_INSTANCE</a> ou <em>um InfoLevel</em> inválido.</p> | 



#### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requer Windows Vista.</p> | | <p><strong>Servidor</strong></p> | <p>Requer Windows Server 2008.</p> | | <p><strong>Cabeçalho</strong></p> | <p>Declarado em Esent.h.</p> | | <p><strong>Biblioteca</strong></p> | <p>Use ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | 



#### <a name="see-also"></a>Consulte Também

[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JET_SIGNATURE](./jet-signature-structure.md)
