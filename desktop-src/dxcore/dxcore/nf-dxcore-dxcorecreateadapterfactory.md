---
title: DXCoreCreateAdapterFactory
description: Cria uma fábrica de adaptadores DXCore, que você pode usar para gerar outros objetos DXCore.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 90567d732f6febc5d95b460b2ff88929dd12b2f22275de9db0d6bc5f88ef99ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118985176"
---
# <a name="dxcorecreateadapterfactory-function"></a>Função DXCoreCreateAdapterFactory

## <a name="description"></a>Descrição

Cria uma fábrica de adaptadores DXCore, que você pode usar para gerar outros objetos DXCore. Para obter diretrizes de programação e exemplos de código, consulte [Usando DXCore para enumerar adaptadores](../dxcore-enum-adapters.md).

## <a name="parameters"></a>Parâmetros

### <a name="riid"></a>riid

Tipo: **REFIID**

Uma referência ao GUID (identificador global exclusivo) da interface que você deseja retornar em *ppvFactory.* Espera-se que esse seja o IID (identificador de interface) [de IDXCoreAdapterFactory.](../dxcore_interface/nn-dxcore_interface-idxcoreadapterfactory.md)

### <a name="ppvfactory-out"></a>ppvFactory [out]

Tipo: **\* \* void**

O endereço de um ponteiro para uma interface com a IID especificada no *parâmetro riid.* Após o retorno bem-sucedido, *\* ppvFactory* (o endereço desreferenciado) contém um ponteiro para a fábrica DXCore criada.

## <a name="returns"></a>Retornos

Tipo: **[HRESULT](../../com/structure-of-com-error-codes.md)**

Se a função for bem-sucedida, ela **retornará S_OK**. Caso contrário, retornará um [**código de erro HRESULT**](../../com/structure-of-com-error-codes.md) [.](../../com/com-error-codes-10.md)

|Valor retornado|Descrição|
|-|-|
|E_NOINTERFACE|Um valor inválido foi fornecido para *riid.*|
|E_POINTER|`nullptr`foi fornecido para *ppvFactory.*|

## <a name="remarks"></a>Comentários

Durante o tempo que uma referência existir em uma interface [IDXCoreAdapterFactory,](../dxcore_interface/nn-dxcore_interface-idxcoreadapterfactory.md) em uma interface [IDXCoreAdapterList](../dxcore_interface/nn-dxcore_interface-idxcoreadapterlist.md) ou em uma interface [IDXCoreAdapter,](../dxcore_interface/nn-dxcore_interface-idxcoreadapter.md) chamadas adicionais para **DXCoreCreateAdapterFactory**, [IDXCoreAdapterList::GetFactory](../dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-getfactory.md)ou [IDXCoreAdapter::GetFactory](../dxcore_interface/nf-dxcore_interface-idxcoreadapter-getfactory.md) retornarão ponteiros para o mesmo objeto, aumentando a contagem de referência da interface **IDXCoreAdapterFactory.**

## <a name="see-also"></a>Confira também

[Referência de DXCore](../dxcore-reference.md), [usando DXCore para enumerar adaptadores](../dxcore-enum-adapters.md)