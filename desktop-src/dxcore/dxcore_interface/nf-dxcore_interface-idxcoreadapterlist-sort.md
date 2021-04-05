---
title: IDXCoreAdapterList::Sort
description: Classifica um objeto da lista de adaptadores DXCore com base em uma matriz de entrada fornecida de critérios de classificação.
ms.localizationpriority: low
ms.topic: reference
ms.date: 09/03/2019
ms.openlocfilehash: 6260e700053a99b531a66a5c19e15d4a32f07e46
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084821"
---
# <a name="idxcoreadapterlistsort-method"></a>Método IDXCoreAdapterList:: Sort

## <a name="description"></a>Descrição

Classifica um objeto da lista de adaptadores DXCore com base em uma matriz de entrada fornecida de critérios de classificação, em que os itens de matriz na matriz de critérios são fornecidos com um peso mais alto. A **classificação** ajuda a localizar mais facilmente o adaptador ideal em uma lista de adaptadores.

## <a name="syntax"></a>Sintaxe

```cpp
HRESULT Sort(
  uint32_t numPreferences,
  _In_reads_(numPreferences) const DXCoreAdapterPreference* preferences
);
```

## <a name="parameters"></a>Parâmetros

### <a name="numpreferences"></a>numPreferences

Tipo: **uint32_t**

O número de elementos que estão na matriz apontada pelo parâmetro de *preferências* .

### <a name="preferences-in"></a>Preferências [em]

Tipo: **const [DXCoreAdapterPreference](./ne-dxcore_interface-dxcoreadapterpreference.md) \***

Um ponteiro para uma matriz constante de valores [DXCoreAdapterPreference](./ne-dxcore_interface-dxcoreadapterpreference.md) , representando critérios de classificação.

## <a name="returns"></a>Retornos

Tipo: **[HRESULT](../../com/structure-of-com-error-codes.md)**

Se a função for realizada com sucesso, ela retornará **S_OK**. Caso contrário, ele retorna um [código de erro](../../com/com-error-codes-10.md) [**HRESULT**](../../com/structure-of-com-error-codes.md) .

|Valor retornado|Descrição|
|-|-|
|E_INVALIDARG|O argumento *numPreferences* é zero ou o argumento *Preferences* é `nullptr` .|

## <a name="remarks"></a>Comentários

Nos casos em que um valor de [DXCoreAdapterPreference](./ne-dxcore_interface-dxcoreadapterpreference.md) fornecido não é reconhecido pelo sistema operacional (SO), ele é ignorado e não fará com que a API falhe. Os valores **DXCoreAdapterPreference** conhecidos ainda serão considerados nesse caso. Para determinar se um tipo de classificação é compreendido pela API, chame [IDXCoreAdapterList:: IsAdapterPreferenceSupported](./nf-dxcore_interface-idxcoreadapterlist-isadapterpreferencesupported.md).

Os valores de **DXCoreAdapterPreference** que ocorrem anteriormente na matriz de *preferências* fornecida são tratados com prioridade mais alta. 

Consulte a documentação de enumeração **DXCoreAdapterPreference** para obter detalhes sobre qual lógica é aplicada para cada tipo. A lógica interna de um tipo pode ser desenvolvida conforme o sistema operacional é desenvolvido.

Quando a **classificação** retorna, os itens na lista de adaptadores DXCore terão sido classificados do mais preferível ao menos preferível. Portanto, chamar [IDXCoreAdapterList:: getadapter](./nf-dxcore_interface-idxcoreadapterlist-getadapter.md) com o índice 0 recupera o adaptador que melhor corresponde aos tipos de preferência de classificação solicitados; o índice 1 é a próxima melhor correspondência e assim por diante.

## <a name="see-also"></a>Confira também

[IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), [referência de DXCore](../dxcore-reference.md), [usando DXCore para enumerar adaptadores](../dxcore-enum-adapters.md)