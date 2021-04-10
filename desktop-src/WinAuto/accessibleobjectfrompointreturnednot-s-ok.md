---
title: AccessibleObjectFromPointReturnedNot_S_OK
description: AccessibleObjectFromPointReturnedNot \_ S \_ OK
ms.assetid: F5DA071A-EBB8-454C-9BC0-BC798835B7D0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85756504520f7d665c1cd1ba7db7c76c1ec5b12a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292232"
---
# <a name="accessibleobjectfrompointreturnednot_s_ok"></a>AccessibleObjectFromPointReturnedNot \_ S \_ OK

## <a name="text"></a>Texto

AccessibleObjectFromPoint ( {0} , {1} ) retornou {2} e esperado S \_ OK

## <a name="type"></a>Tipo

Aviso

## <a name="description"></a>Descrição

[**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint) não retornou S \_ OK conforme esperado para as coordenadas fornecidas.

## <a name="possible-causes"></a>Possíveis causas

-   A interação do usuário durante a verificação, como a movimentação do foco para um HWND não-alvo, interfere no processo de verificação.
-   Uma implementação de MSAA incorreta ou inválida.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Navegação por meio de teste de clique e local da tela](navigation-through-hit-testing-and-screen-location.md)
</dt> <dt>

[**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)
</dt> </dl>

 

 




