---
title: IDXCoreAdapterList::GetAdapter
description: Recupera um adaptador específico por índice de um objeto de lista do adaptador DXCore.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 5ba03c9e6f2711adc5264354a6abd70ee489965f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007975"
---
# <a name="idxcoreadapterlistgetadapter-method"></a>Método IDXCoreAdapterList:: getadapter

Recupera um adaptador específico por índice de um objeto de lista do adaptador DXCore. Para obter diretrizes de programação e exemplos de código, consulte [usando DXCore para enumerar adaptadores](../dxcore-enum-adapters.md).

## <a name="syntax"></a>Sintaxe

```cpp
virtual HRESULT STDMETHODCALLTYPE GetAdapter(
  uint32_t index,
  REFIID riid,
  _COM_Outptr_ void **ppvAdapter) = 0;

template<class T>
HRESULT STDMETHODCALLTYPE GetAdapter( 
  uint32_t index,
  _COM_Outptr_ T **ppvAdapter);
```

## <a name="parameters"></a>Parâmetros

### <a name="index"></a>índice

Tipo: **uint32_t**

Um índice de base zero, identificando uma instância de adaptador dentro da lista de adaptadores DXCore.

### <a name="riid"></a>riid

Tipo: **REFIID**

Uma referência ao GUID (identificador global exclusivo) da interface que você deseja retornar em *ppvAdapter*. Espera-se que seja o identificador de interface (IID) de [IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md).

### <a name="ppvadapter-out"></a>ppvAdapter [saída]

Tipo: **void \* \***

O endereço de um ponteiro para uma interface com o IID especificado no parâmetro *riid* . Após o retorno bem-sucedido, *\* ppvAdapter* (o endereço desreferenciado) contém um ponteiro para o adaptador DXCore criado.

## <a name="returns"></a>Retornos

Tipo: **[HRESULT](../../com/structure-of-com-error-codes.md)**

Se a função for realizada com sucesso, ela retornará **S_OK**. Caso contrário, ele retorna um [código de erro](../../com/com-error-codes-10.md) [**HRESULT**](../../com/structure-of-com-error-codes.md) .

|Valor retornado|Descrição|
|-|-|
|DXGI_ERROR_DEVICE_REMOVED|O *índice* é válido, mas o adaptador não está mais em um estado válido.|
|E_INVALIDARG|O *índice* fornecido não é válido.|
|E_NOINTERFACE|Um valor inválido foi fornecido para *riid*.|
|E_POINTER|`nullptr` foi fornecido para *ppvAdapter*.|

## <a name="remarks"></a>Comentários

Várias chamadas passando um índice que representa o mesmo adaptador retornam ponteiros de interface idênticos, mesmo entre diferentes listas de adaptadores. Como resultado, é seguro comparar os ponteiros de interface para determinar se vários ponteiros se referem ao mesmo objeto de adaptador.

## <a name="see-also"></a>Confira também

[IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), [referência de DXCore](../dxcore-reference.md), [usando DXCore para enumerar adaptadores](../dxcore-enum-adapters.md)