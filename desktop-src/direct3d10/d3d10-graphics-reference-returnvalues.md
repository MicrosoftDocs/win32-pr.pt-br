---
description: A tabela a seguir contém códigos de retorno de funções de API.
ms.assetid: 7b67d428-d000-4c3e-adc1-b5fc67a15a6a
title: Códigos de retorno do Direct3D 10
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32c7e7bca25d240bf7775a6f4d6476148e3749e283ab4f8fb3511bf8b53bb711
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119282796"
---
# <a name="direct3d-10-return-codes"></a>Códigos de retorno do Direct3D 10

A tabela a seguir contém códigos de retorno de funções de API.



| HRESULT                                         | Descrição                                                                                                                                           |
|-------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_Arquivo de erro d3d10 \_ \_ não \_ encontrado                  | O arquivo não foi encontrado.                                                                                                                               |
| Erro D3D10 em \_ \_ excesso de \_ \_ \_ objetos de estado exclusivos \_ | Há muitas instâncias exclusivas de um tipo específico de [objeto de estado](d3d10-graphics-programming-guide-api-features-state-objects.md).          |
| D3DERR \_ INVALIDCALL                             | A chamada do método é inválida. Por exemplo, o parâmetro de um método não pode ser um ponteiro válido.                                                             |
| D3DERR \_ WASSTILLDRAWING                         | A operação blit anterior que está transferindo informações para ou desta superfície está incompleta.                                                   |
| E \_ falha                                         | Tentativa de criar um dispositivo com a [camada de depuração](d3d10-graphics-programming-guide-api-features-layers.md) habilitada e a camada não está instalada. |
| E \_ INVALIDARG                                   | Um parâmetro inválido foi passado para a função de retorno.                                                                                            |
| E \_ OUTOFMEMORY                                  | O Direct3D não pôde alocar memória suficiente para concluir a chamada.                                                                                   |
| E \_ NOTIMPL                                      | A chamada de método não é implementada com a combinação de parâmetros passada.                                                                              |
| \_falso                                        | Valor de êxito alternativo, indicando uma conclusão bem-sucedida, mas não padrão (o significado preciso depende do contexto).                                 |
| S \_ OK                                           | Não ocorreu nenhum erro.                                                                                                                                    |



 

Para escrever código que manipula [valores HRESULT](../winprog/windows-data-types.md) de robustez, use as macros com êxito (HR) e com falha (HR).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência do Direct3D](d3d10-graphics-reference-d3d10.md)
</dt> <dt>

[Referência para Direct3D 10](d3d10-graphics-reference.md)
</dt> </dl>

 

 
