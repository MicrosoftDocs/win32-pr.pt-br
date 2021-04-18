---
title: Códigos de retorno do Direct3D 12
description: Veja a seguir os códigos de retorno das funções de API.
ms.assetid: 5F6CC962-7DB7-489F-82A4-9388313014D3
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cd04c0c7702f00f1338ce884adc745522390c8d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105810777"
---
# <a name="direct3d-12-return-codes"></a>Códigos de retorno do Direct3D 12

Veja a seguir os códigos de retorno das funções de API. Para obter mais códigos de retorno, consulte [ \_ erro dxgi](/windows/desktop/direct3ddxgi/dxgi-error).



| HRESULT                                                                  | Descrição                                                                                                           |
|--------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| \_Adaptador de erro D3D12 \_ \_ não \_ encontrado                                        | O PSO armazenado em cache especificado foi criado em um adaptador diferente e não pode ser reutilizado no adaptador atual.          |
| Incompatibilidade de versão do driver de \_ erro D3D12 \_ \_ \_                                  | O PSO armazenado em cache especificado foi criado em uma versão de driver diferente e não pode ser reutilizado no adaptador atual.  |
| D3DERR \_ INVALIDCALL (substituído pela \_ chamada de erro dxgi \_ inválido \_ )           | A chamada do método é inválida. Por exemplo, o parâmetro de um método não pode ser um ponteiro válido.                             |
| D3DERR \_ WASSTILLDRAWING (substituído pelo \_ erro dxgi \_ \_ ainda estava \_ desenhando) | A operação blit anterior que está transferindo informações para ou desta superfície está incompleta.                   |
| E \_ falha                                                                  | Tentativa de criar um dispositivo com a camada de depuração habilitada e a camada não está instalada.                             |
| E \_ INVALIDARG                                                            | Um parâmetro inválido foi passado para a função de retorno.                                                             |
| E \_ OUTOFMEMORY                                                           | O Direct3D não pôde alocar memória suficiente para concluir a chamada.                                                   |
| E \_ NOTIMPL                                                               | A chamada de método não é implementada com a combinação de parâmetros passada.                                               |
| \_falso                                                                 | Valor de êxito alternativo, indicando uma conclusão bem-sucedida, mas não padrão (o significado preciso depende do contexto). |
| S \_ OK                                                                    | Não ocorreu nenhum erro.                                                                                                    |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência do Direct3D 12](direct3d-12-reference.md)
</dt> </dl>

 

 