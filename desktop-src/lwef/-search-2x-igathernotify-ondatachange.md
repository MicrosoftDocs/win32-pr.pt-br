---
title: Método IGatherNotify OnDataChange (preterido)
description: este tópico Windows interface de pesquisa da área de trabalho foi preterido e é substituído pela API do ISearchPersistentItemsChangedSink search Windows no SDK do Windows. | Método IGatherNotify OnDataChange (preterido)
ms.assetid: 0cbfa6b7-44f0-41f0-93a3-d5941b5822de
keywords:
- OnDataChange (preterido) método herdado Windows recursos de ambiente
- método OnDataChange (preterido) herdado Windows recursos de ambiente, interface IGatherNotify
- recursos de ambiente herdado Windows da interface IGatherNotify, método OnDataChange (preterido)
topic_type:
- apiref
api_name:
- IGatherNotify.OnDataChange (Deprecated)
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 95533a7937136a0f828a292efe7e398258e3c880974e031d9d7d2797f721f2a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118481590"
---
# <a name="igathernotifyondatachange-deprecated-method"></a>Método IGatherNotify:: OnDataChange (preterido)

\[**OnDataChange** pode ser alterado ou não estar disponível nas versões subsequentes do sistema operacional ou produto.\]

este tópico Windows interface de pesquisa da área de trabalho foi preterido e é substituído pela API do [**ISearchPersistentItemsChangedSink**](/windows/desktop/api/searchapi/nn-searchapi-isearchpersistentitemschangedsink) search Windows no SDK do Windows.

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

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

 

 
