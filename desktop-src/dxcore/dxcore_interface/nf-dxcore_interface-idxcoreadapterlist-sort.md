---
title: IDXCoreAdapterList::Sort
description: Classifica um objeto de lista de adaptadores DXCore com base em uma matriz de entrada fornecida de critérios de classificação.
ms.localizationpriority: low
ms.topic: reference
ms.date: 09/03/2019
ms.openlocfilehash: 59580fb8b76c80a264796f829d2b0a1d2e8eabb4375896fbd27fb34a7697cf90
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118278867"
---
# <a name="idxcoreadapterlistsort-method"></a>Método IDXCoreAdapterList::Sort

## <a name="description"></a>Descrição

Classifica um objeto de lista de adaptadores DXCore com base em uma matriz de entrada fornecida de critérios de classificação, em que os itens de matriz anteriormente na matriz de critérios têm um peso mais alto. **Classificar** ajuda você a encontrar mais facilmente seu adaptador ideal em uma lista de adaptadores.

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

O número de elementos que estão na matriz apontada pelo *parâmetro preferences.*

### <a name="preferences-in"></a>preferências [in]

Tipo: **const [DXCoreAdapterPreference](./ne-dxcore_interface-dxcoreadapterpreference.md) \***

Um ponteiro para uma matriz constante de [valores DXCoreAdapterPreference, representando](./ne-dxcore_interface-dxcoreadapterpreference.md) critérios de classificação.

## <a name="returns"></a>Retornos

Tipo: **[HRESULT](../../com/structure-of-com-error-codes.md)**

Se a função for bem-sucedida, ela **retornará S_OK**. Caso contrário, retornará um [**código de erro HRESULT**](../../com/structure-of-com-error-codes.md) [.](../../com/com-error-codes-10.md)

|Valor retornado|Descrição|
|-|-|
|E_INVALIDARG|O *argumento numPreferences* é zero ou o *argumento preferences* é `nullptr` .|

## <a name="remarks"></a>Comentários

Nos casos em que um [valor DXCoreAdapterPreference](./ne-dxcore_interface-dxcoreadapterpreference.md) fornecido não é reconhecido pelo sistema operacional ,ele é ignorado e não causará falha na API. Os **valores DXCoreAdapterPreference conhecidos** ainda serão considerados nesse caso. Para determinar se um tipo de classificação é compreendido pela API, chame [IDXCoreAdapterList::IsAdapterPreferenceSupported.](./nf-dxcore_interface-idxcoreadapterlist-isadapterpreferencesupported.md)

**Os valores DXCoreAdapterPreference** que ocorrem anteriormente na matriz *de preferências* fornecidas são tratados com prioridade mais alta. 

Consulte a **documentação de enumeração DXCoreAdapterPreference** para obter detalhes sobre qual lógica é aplicada para cada tipo. A lógica interna para um tipo pode ser desenvolvida conforme o sistema operacional é desenvolvido.

Quando **a** classificação for retornada, os itens na lista de adaptadores DXCore terão sido classificação dos mais preferíveis para os menos preferíveis. Portanto, chamar [IDXCoreAdapterList::GetAdapter](./nf-dxcore_interface-idxcoreadapterlist-getadapter.md) com o índice 0 recupera o adaptador que melhor corresponde aos tipos de preferência de classificação solicitados; O índice 1 é a próxima melhor combinação e assim por diante.

## <a name="see-also"></a>Confira também

[IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), [Referência de DXCore](../dxcore-reference.md), [usando DXCore para enumerar adaptadores](../dxcore-enum-adapters.md)