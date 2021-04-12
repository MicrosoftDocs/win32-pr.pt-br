---
title: Método IGatherNotify OnDataMove (preterido)
description: Este tópico da interface do Windows Desktop Search foi preterido e é substituído pela API ISearchPersistentItemsChangedSink do Windows Search no SDK do Windows. | Método IGatherNotify OnDataMove (preterido)
ms.assetid: cc223d0f-6508-4e38-b365-c60660db5324
keywords:
- Método OnDataMove (preterido) recursos de ambiente herdado do Windows
- Método OnDataMove (preterido) recursos de ambiente herdado do Windows, interface IGatherNotify
- Recursos do ambiente Windows herdado da interface IGatherNotify, método OnDataMove (preterido)
topic_type:
- apiref
api_name:
- IGatherNotify.OnDataMove (Deprecated)
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9fe38cd11e9072981334e5b724445ea3393d4361
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104298250"
---
# <a name="igathernotifyondatamove-deprecated-method"></a>Método IGatherNotify:: OnDataMove (preterido)

\[**OnDataMove** pode ser alterado ou não estar disponível nas versões subsequentes do sistema operacional ou produto.\]

Este tópico da interface do Windows Desktop Search foi preterido e é substituído pela API [**ISearchPersistentItemsChangedSink**](/windows/desktop/api/searchapi/nn-searchapi-isearchpersistentitemschangedsink) do Windows Search no SDK do Windows.

Esse método notifica o indexador de dados que foram movidos. Quando ele envia a notificação para o indexador, ele inclui o endereço antigo, o novo endereço e o endereço lógico.

## <a name="syntax"></a>Sintaxe


```C++
void OnDataMove (Deprecated)(
  [in] long eChangeAdviseSemantics,
  [in] BSTR bstrOldAddress,
  [in] BSTR bstrNewAddress,
  [in] BSTR bstrLogicalAddress
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*eChangeAdviseSemantics* \[ no\]
</dt> <dd>

Tipo: **longo**

Um parâmetro enumerado que descreve o tipo de movimentação que ocorreu.

</dd> <dt>

*bstrOldAddress* \[ no\]
</dt> <dd>

Tipo: **BSTR**

O endereço antigo do item que foi movido. Para arquivos normais,*eChangeAdviseSematics* é **nulo**. Para uma pasta ou diretório, defina *eChangeAdviseSematics* para o \_ diretório de semântica da AC \_ \_ do GTHR.

</dd> <dt>

*bstrNewAddress* \[ no\]
</dt> <dd>

Tipo: **BSTR**

O novo endereço do item que foi movido.

</dd> <dt>

*bstrLogicalAddress* \[ no\]
</dt> <dd>

Tipo: **BSTR**

O endereço lógico do item que foi movido.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

 

 
