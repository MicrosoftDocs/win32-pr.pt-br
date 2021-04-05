---
title: Interface IEnumTfRenderingMarkup
description: A interface IEnumTfRenderingMarkup é implementada pelo Gerenciador do TSF e usada por aplicativos. Essa interface pode ser recuperada por ITfContextRenderingMarkup GetRenderingMarkup e enumera as informações de marcação de renderização.
ms.assetid: 6062a6f5-f973-4cd5-94d3-05aa418e0198
keywords:
- Estrutura de serviços de texto da interface IEnumTfRenderingMarkup
- Estrutura de serviços de texto da interface IEnumTfRenderingMarkup, descrita
topic_type:
- apiref
api_name:
- IEnumTfRenderingMarkup
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3005c8fe37a26b11f5155b639f8c151cf59c2cf0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007959"
---
# <a name="ienumtfrenderingmarkup-interface"></a>Interface IEnumTfRenderingMarkup

A interface **IEnumTfRenderingMarkup** é implementada pelo Gerenciador do TSF e usada por aplicativos. Essa interface pode ser recuperada por [ITfContextRenderingMarkup:: GetRenderingMarkup](itfcontextrenderingmarkup-getrenderingmarkup.md) e enumera as informações de marcação de renderização.



| Métodos IEnumTfRenderingMarkup            | Descrição                                                                                                                                            |
|-------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [8i](ienumtfrenderingmarkup-clone.md) | O método **IEnumTfRenderingMarkup:: clone** cria uma cópia do objeto enumerador.                                                                  |
| [Próximo](ienumtfrenderingmarkup-next.md)   | O método **IEnumTfRenderingMarkup:: Next** Obtém, da posição atual, o número especificado de elementos na sequência de enumeração.          |
| [Redefinir](ienumtfrenderingmarkup-reset.md) | O método **IEnumTfRenderingMarkup:: Reset** redefine o objeto enumerador movendo a posição atual para o início da sequência de enumeração. |
| [Skip](ienumtfrenderingmarkup-skip.md)   | O método **IEnumTfRenderingMarkup:: Skip** Obtém, da posição atual, o número especificado de elementos na sequência de enumeração.          |



 

## <a name="members"></a>Membros

A interface **IEnumTfRenderingMarkup** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , mas não tem membros adicionais.

## <a name="remarks"></a>Comentários

> [!Note]  
> Essa interface não está atualmente nos arquivos de cabeçalho públicos. Para usar essa API, você deve compilar o [protótipo](prototypes.md)em MIDL.

 

 

 