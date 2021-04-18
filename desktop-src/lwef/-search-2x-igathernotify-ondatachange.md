---
title: Método IGatherNotify OnDataChange (preterido)
description: Este tópico da interface do Windows Desktop Search foi preterido e é substituído pela API ISearchPersistentItemsChangedSink do Windows Search no SDK do Windows. | Método IGatherNotify OnDataChange (preterido)
ms.assetid: 0cbfa6b7-44f0-41f0-93a3-d5941b5822de
keywords:
- Método OnDataChange (preterido) recursos de ambiente herdado do Windows
- Método OnDataChange (preterido) recursos de ambiente herdado do Windows, interface IGatherNotify
- Recursos do ambiente Windows herdado da interface IGatherNotify, método OnDataChange (preterido)
topic_type:
- apiref
api_name:
- IGatherNotify.OnDataChange (Deprecated)
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d41edeaa591a7f3cbc9494064906af1815597737
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105788969"
---
# <a name="igathernotifyondatachange-deprecated-method"></a>Método IGatherNotify:: OnDataChange (preterido)

\[**OnDataChange** pode ser alterado ou não estar disponível nas versões subsequentes do sistema operacional ou produto.\]

Este tópico da interface do Windows Desktop Search foi preterido e é substituído pela API [**ISearchPersistentItemsChangedSink**](/windows/desktop/api/searchapi/nn-searchapi-isearchpersistentitemschangedsink) do Windows Search no SDK do Windows.

Esse método notifica o indexador de dados que foram alterados. Quando ele envia a notificação para o indexador, ele inclui o tipo de alteração, endereço físico e endereço lógico.

## <a name="syntax"></a>Sintaxe


```C++
void OnDataChange (Deprecated)(
  [in] long eChangeAdvise,
  [in] BSTR bstrPhysicalAddress,
  [in] BSTR bstrLogicalAddress
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*eChangeAdvise* \[ no\]
</dt> <dd>

Tipo: **longo**

Um valor enumerado que especifica o tipo de alteração.

</dd> <dt>

*bstrPhysicalAddress* \[ no\]
</dt> <dd>

Tipo: **BSTR**

O endereço físico do item que foi alterado.

</dd> <dt>

*bstrLogicalAddress* \[ no\]
</dt> <dd>

Tipo: **BSTR**

O endereço lógico do item que foi alterado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

 

 
