---
title: IDXCoreAdapterList::GetFactory
description: 'Recupera um ponteiro de interface [IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md) para o objeto de fábrica do adaptador DXCore. | IDXCoreAdapterList:: GetFactory'
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 08dc93f5c7e086e33d15f666a2c5b94fd7dd7e58
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105802156"
---
# <a name="idxcoreadapterlistgetfactory-method"></a>Método IDXCoreAdapterList:: GetFactory

Recupera um ponteiro de interface [IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md) para o objeto de fábrica do adaptador DXCore. Para obter diretrizes de programação e exemplos de código, consulte [usando DXCore para enumerar adaptadores](../dxcore-enum-adapters.md).

## <a name="syntax"></a>Sintaxe

```cpp
virtual HRESULT STDMETHODCALLTYPE GetFactory(
  REFIID riid,
  _COM_Outptr_ void** ppvFactory) = 0;

template <class T>
HRESULT GetFactory(
  _COM_Outptr_ T** ppvFactory);
```

## <a name="parameters"></a>Parâmetros

### <a name="riid"></a>riid

Tipo: **REFIID**

Uma referência ao GUID (identificador global exclusivo) da interface que você deseja retornar em *ppvFactory*. Espera-se que seja o identificador de interface (IID) de [IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md).

### <a name="ppvfactory-out"></a>ppvFactory [saída]

Tipo: **void \* \***

O endereço de um ponteiro para uma interface com o IID especificado no parâmetro *riid* . Após o retorno bem-sucedido, *\* ppvFactory* (o endereço desreferenciado) contém um ponteiro para o objeto de fábrica do adaptador DXCore existente. Antes de retornar, a função incrementa a contagem de referência na interface [IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md) do objeto de fábrica.

## <a name="returns"></a>Retornos

Tipo: **[HRESULT](../../com/structure-of-com-error-codes.md)**

Se a função for realizada com sucesso, ela retornará **S_OK**. Caso contrário, ele retorna um [código de erro](../../com/com-error-codes-10.md) [**HRESULT**](../../com/structure-of-com-error-codes.md) .

|Valor retornado|Descrição|
|-|-|
|E_NOINTERFACE|Um valor inválido foi fornecido para *riid*.|
|E_POINTER|`nullptr` foi fornecido para *ppvFactory*.|

## <a name="remarks"></a>Comentários

Durante o tempo em que uma referência existe em uma interface [IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md) , uma interface [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md) ou uma interface [IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md) , chamadas adicionais para [DXCoreCreateAdapterFactory](../dxcore/nf-dxcore-dxcorecreateadapterfactory.md), [IDXCoreAdapterList:: GetFactory]()ou [IDXCoreAdapter:: GetFactory](./nf-dxcore_interface-idxcoreadapter-getfactory.md) retornarão ponteiros para o mesmo objeto, aumentando a contagem de referência da interface **IDXCoreAdapterFactory** .

## <a name="see-also"></a>Confira também

[IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), [referência de DXCore](../dxcore-reference.md), [usando DXCore para enumerar adaptadores](../dxcore-enum-adapters.md)
