---
title: IDXCoreAdapterFactory::GetAdapterByLuid
description: Recupera o objeto de adaptador DXCore ([IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md)) para um LUID especificado, se disponível.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 30835948978e5c7f3f11f903322e4fa41f71d210
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366439"
---
# <a name="idxcoreadapterfactorygetadapterbyluid-method"></a>Método IDXCoreAdapterFactory:: GetAdapterByLuid

Recupera o objeto de adaptador DXCore ([IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md)) para um LUID especificado, se disponível. Para obter diretrizes de programação e exemplos de código, consulte [usando DXCore para enumerar adaptadores](../dxcore-enum-adapters.md).

## <a name="syntax"></a>Sintaxe

```cpp
virtual HRESULT STDMETHODCALLTYPE GetAdapterByLuid( 
  const LUID &adapterLUID,
   REFIID riid,
  _COM_Outptr_ void **ppvAdapter) = 0;

template<class T>
HRESULT STDMETHODCALLTYPE GetAdapterByLuid( 
  const LUID &adapterLUID,
  _COM_Outptr_ T **ppvAdapter);
```

## <a name="parameters"></a>Parâmetros

### <a name="adapterluid"></a>adapterLUID

Tipo: **[LUID](/windows/win32/api/winnt/ns-winnt-luid) const\&**

O valor local exclusivo que identifica a instância do adaptador.

### <a name="riid-in"></a>riid [in]

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
|DXGI_ERROR_DEVICE_REMOVED|O LUID de adaptador passado em *adapterLUID* é reconhecido, mas o adaptador não está mais em um estado válido.|
|E_INVALIDARG|Não há tal LUID de adaptador, pois o valor passado em *adapterLUID* está disponível por meio de DXCore.|
|E_NOINTERFACE|Um valor inválido foi fornecido para *riid*.|
|E_POINTER|`nullptr` foi fornecido para *ppvAdapter*.|

## <a name="remarks"></a>Comentários

Várias chamadas passando o mesmo [LUID](/windows/win32/api/winnt/ns-winnt-luid) retornam ponteiros de interface idênticos. Como resultado, é seguro comparar os ponteiros de interface para determinar se vários ponteiros se referem ao mesmo objeto de adaptador.

## <a name="see-also"></a>Confira também

[IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md), [referência de DXCore](../dxcore-reference.md), [usando DXCore para enumerar adaptadores](../dxcore-enum-adapters.md)