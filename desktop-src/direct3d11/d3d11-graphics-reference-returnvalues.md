---
title: Códigos de retorno do Direct3D 11
description: Os códigos de retorno de funções de API.
ms.assetid: c0856a58-b760-44e5-8acf-145720b403d1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4130ed07faaabfd24bb48454d4e450f307c7a12
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007685"
---
# <a name="direct3d-11-return-codes"></a>Códigos de retorno do Direct3D 11

Códigos de retorno de funções de API.

| HRESULT | Description |
|-|-|
| D3D11_ERROR_FILE_NOT_FOUND (0x887C0002) | O arquivo não foi encontrado. |
| D3D11_ERROR_TOO_MANY_UNIQUE_STATE_OBJECTS (0x887C0001) | Há muitas instâncias exclusivas de um tipo específico de objeto de estado. |
| D3D11_ERROR_TOO_MANY_UNIQUE_VIEW_OBJECTS (0x887C0003) | Há muitas instâncias exclusivas de um determinado tipo de objeto de exibição. |
| D3D11_ERROR_DEFERRED_CONTEXT_MAP_WITHOUT_INITIAL_DISCARD (0x887C0004) | A primeira chamada para [**ID3D11DeviceContext:: map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) após o [**ID3D11Device:: CreateDeferredContext**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdeferredcontext) ou [**ID3D11DeviceContext:: FinishCommandList**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-finishcommandlist) por recurso não foi D3D11_MAP_WRITE_DISCARD. |
| D3DERR_INVALIDCALL (substituído por DXGI_ERROR_INVALID_CALL) (0x887A0001) | A chamada do método é inválida. Por exemplo, o parâmetro de um método não pode ser um ponteiro válido. |
| D3DERR_WASSTILLDRAWING (substituído por DXGI_ERROR_WAS_STILL_DRAWING) (0x887A000A) | A operação blit anterior que está transferindo informações para ou desta superfície está incompleta. |
| E_FAIL (0x80004005) | Tentativa de criar um dispositivo com a camada de depuração habilitada e a camada não está instalada. |
| E_INVALIDARG (0x80070057) | Um parâmetro inválido foi passado para a função de retorno. |
| E_OUTOFMEMORY (0x8007000E) | O Direct3D não pôde alocar memória suficiente para concluir a chamada. |
| E_NOTIMPL (0x80004001) | A chamada de método não é implementada com a combinação de parâmetros passada. |
| S_FALSE ((HRESULT) 1L) | Valor de êxito alternativo, indicando uma conclusão bem-sucedida, mas não padrão (o significado preciso depende do contexto). |
| S_OK ((HRESULT) 0L) | Não ocorreu nenhum erro. |

Para obter mais códigos de retorno, consulte [DXGI_ERROR](/windows/desktop/direct3ddxgi/dxgi-error).

## <a name="related-topics"></a>Tópicos relacionados

* [Referência do Direct3D 11](d3d11-graphics-reference.md)