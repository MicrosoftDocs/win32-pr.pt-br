---
title: Método IGatherNotify addscope (preterido)
description: este tópico Windows interface de pesquisa da área de trabalho foi preterido e é substituído pela API do ISearchPersistentItemsChangedSink search Windows no SDK do Windows. | Método IGatherNotify addscope (preterido)
ms.assetid: 3b250818-1876-40b2-9a85-91f2bf6f52ec
keywords:
- método addscope (preterido) herdado Windows recursos de ambiente
- método addscope (preterido) herdado Windows recursos de ambiente, interface IGatherNotify
- IGatherNotify interface herdada Windows recursos de ambiente, método addscope (preterido)
topic_type:
- apiref
api_name:
- IGatherNotify.AddScope (Deprecated)
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a49c0cf652b0cfde59167fa98498a978d3c2c41d3a886ee092b8f4a28d35f61b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118755587"
---
# <a name="igathernotifyaddscope-deprecated-method"></a>Método IGatherNotify:: addscope (preterido)

\[**Addscope** pode ser alterado ou indisponível nas versões subsequentes do sistema operacional ou produto.\]

este tópico Windows interface de pesquisa da área de trabalho foi preterido e é substituído pela API do [**ISearchPersistentItemsChangedSink**](/windows/desktop/api/searchapi/nn-searchapi-isearchpersistentitemschangedsink) search Windows no SDK do Windows.

Adiciona a página inicial ou a URL que você está monitorando. Isso inicia um rastreamento incremental quando você se conecta e, em seguida, pressupõe que todas as alterações de URL adicionais sejam feitas por notificação.

## <a name="syntax"></a>Sintaxe


```C++
void AddScope (Deprecated)(
  [in] BSTR bstrScope
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*bstrScope* \[ no\]
</dt> <dd>

Tipo: **BSTR**

Uma cadeia de caracteres que especifica a página inicial ou URL que você está monitorando.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Chamar esse método inicia um rastreamento incremental quando conectado à loja. Depois disso, supõe-se que todas as alterações de URL sejam feitas por notificação após a atualização inicial.

 

 
