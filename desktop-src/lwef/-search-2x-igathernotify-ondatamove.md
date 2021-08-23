---
title: Método IGatherNotify OnDataMove (preterido)
description: Este tópico Windows interface de Pesquisa de Área de Trabalho foi preterido e substituído pela API ISearchPersistentItemsChangedSink do Windows Windows Search. | Método IGatherNotify OnDataMove (preterido)
ms.assetid: cc223d0f-6508-4e38-b365-c60660db5324
keywords:
- Método OnDataMove (preterido) herdado Windows de ambiente
- Método OnDataMove (preterido) herdado Windows recursos de ambiente, interface IGatherNotify
- Interface IGatherNotify herdada Windows recursos de ambiente, método OnDataMove (preterido)
topic_type:
- apiref
api_name:
- IGatherNotify.OnDataMove (Deprecated)
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2f3d4f7d91bc9e9741f227812997a820ab4180ccf438d52ae8cfea93f67dc0bf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119665866"
---
# <a name="igathernotifyondatamove-deprecated-method"></a>Método IGatherNotify::OnDataMove (preterido)

\[**OnDataMove pode** ser alterado ou não disponível em versões subsequentes do sistema operacional ou produto.\]

Este tópico Windows interface de Pesquisa de Área de Trabalho foi preterido e foi substituído pela API do Windows Search [**ISearchPersistentItemsChangedSink**](/windows/desktop/api/searchapi/nn-searchapi-isearchpersistentitemschangedsink) no SDK do Windows.

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

*eChangeAdviseSemantics* \[ Em\]
</dt> <dd>

Tipo: **longo**

Um parâmetro enumerado que descreve o tipo de movimentação que ocorreu.

</dd> <dt>

*bstrOldAddress* \[ Em\]
</dt> <dd>

Tipo: **BSTR**

O endereço antigo do item que foi movido. Para arquivos normais,*eChangeAdviseSematics* é **NULL.** Para uma pasta ou diretório, de definido *eChangeAdviseSematics* como GTHR \_ CA \_ SEMANTICS \_ DIRECTORY.

</dd> <dt>

*bstrNewAddress* \[ Em\]
</dt> <dd>

Tipo: **BSTR**

O novo endereço do item que foi movido.

</dd> <dt>

*bstrLogicalAddress* \[ Em\]
</dt> <dd>

Tipo: **BSTR**

O endereço lógico do item que foi movido.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

 

 
