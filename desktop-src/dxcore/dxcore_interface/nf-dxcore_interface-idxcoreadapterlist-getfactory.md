---
title: IDXCoreAdapterList::GetFactory
description: Recupera um ponteiro de interface [IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md) para o objeto de fábrica do adaptador DXCore. | IDXCoreAdapterList::GetFactory
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 97ae5ef0ba321dafaabf1813d943b738f5af4c586050b91712bf9ad93005cb35
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120094576"
---
# <a name="idxcoreadapterlistgetfactory-method"></a>Método IDXCoreAdapterList::GetFactory

Recupera um ponteiro de interface [IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md) para o objeto de fábrica do adaptador DXCore. Para obter diretrizes de programação e exemplos de código, consulte [Usando DXCore para enumerar adaptadores](../dxcore-enum-adapters.md).

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

Uma referência ao GUID (identificador global exclusivo) da interface que você deseja retornar em *ppvFactory.* Espera-se que esse seja o IID (identificador de interface) [de IDXCoreAdapterFactory.](./nn-dxcore_interface-idxcoreadapterfactory.md)

### <a name="ppvfactory-out"></a>ppvFactory [out]

Tipo: **\* \* void**

O endereço de um ponteiro para uma interface com a IID especificada no *parâmetro riid.* Após o retorno bem-sucedido, *\* ppvFactory* (o endereço desreferenciado) contém um ponteiro para o objeto de fábrica do adaptador DXCore existente. Antes de retornar, a função incrementa a contagem de referência na interface [IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md) do objeto de fábrica.

## <a name="returns"></a>Retornos

Tipo: **[HRESULT](../../com/structure-of-com-error-codes.md)**

Se a função for bem-sucedida, ela **retornará S_OK**. Caso contrário, retornará um [**código de erro HRESULT**](../../com/structure-of-com-error-codes.md) [.](../../com/com-error-codes-10.md)

|Valor retornado|Descrição|
|-|-|
|E_NOINTERFACE|Um valor inválido foi fornecido para *riid.*|
|E_POINTER|`nullptr`foi fornecido para *ppvFactory.*|

## <a name="remarks"></a>Comentários

Durante o tempo que uma referência existir em uma interface [IDXCoreAdapterFactory,](./nn-dxcore_interface-idxcoreadapterfactory.md) em uma interface [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md) ou em uma interface [IDXCoreAdapter,](./nn-dxcore_interface-idxcoreadapter.md) chamadas adicionais para [DXCoreCreateAdapterFactory](../dxcore/nf-dxcore-dxcorecreateadapterfactory.md), [IDXCoreAdapterList::GetFactory]()ou [IDXCoreAdapter::GetFactory](./nf-dxcore_interface-idxcoreadapter-getfactory.md) retornarão ponteiros para o mesmo objeto, aumentando a contagem de referência da interface **IDXCoreAdapterFactory.**

## <a name="see-also"></a>Confira também

[IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), [Referência de DXCore](../dxcore-reference.md), [usando DXCore para enumerar adaptadores](../dxcore-enum-adapters.md)
