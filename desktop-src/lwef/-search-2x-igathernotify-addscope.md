---
title: Método IGatherNotify addscope (preterido)
description: Este tópico da interface do Windows Desktop Search foi preterido e é substituído pela API ISearchPersistentItemsChangedSink do Windows Search no SDK do Windows. | Método IGatherNotify addscope (preterido)
ms.assetid: 3b250818-1876-40b2-9a85-91f2bf6f52ec
keywords:
- Método addscope (preterido) recursos de ambiente herdado do Windows
- Método addscope (preterido) recursos de ambiente herdados do Windows, interface IGatherNotify
- Recursos do ambiente Windows herdado da interface IGatherNotify, método addscope (preterido)
topic_type:
- apiref
api_name:
- IGatherNotify.AddScope (Deprecated)
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 967dc4f30acee2f8d8adbcfec04f0508e53bba15
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104298251"
---
# <a name="igathernotifyaddscope-deprecated-method"></a>Método IGatherNotify:: addscope (preterido)

\[**Addscope** pode ser alterado ou indisponível nas versões subsequentes do sistema operacional ou produto.\]

Este tópico da interface do Windows Desktop Search foi preterido e é substituído pela API [**ISearchPersistentItemsChangedSink**](/windows/desktop/api/searchapi/nn-searchapi-isearchpersistentitemschangedsink) do Windows Search no SDK do Windows.

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

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Chamar esse método inicia um rastreamento incremental quando conectado à loja. Depois disso, supõe-se que todas as alterações de URL sejam feitas por notificação após a atualização inicial.

 

 
