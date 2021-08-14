---
title: AccessibleObjectFromPointReturnedNot_S_OK
description: AccessibleObjectFromPointReturnedNot \_ S \_ OK
ms.assetid: F5DA071A-EBB8-454C-9BC0-BC798835B7D0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba0ceabd15e5a401bb67ac14af5a7fb83b96543b4b8046ceee2349d8d57b8de5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118327682"
---
# <a name="accessibleobjectfrompointreturnednot_s_ok"></a>AccessibleObjectFromPointReturnedNot \_ S \_ OK

## <a name="text"></a>Texto

AccessibleObjectFromPoint( {0} , ) retornado e S OK {1} {2} \_ esperado

## <a name="type"></a>Tipo

Aviso

## <a name="description"></a>Descrição

[**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint) não retornou S \_ OK conforme o esperado para as coordenadas determinadas.

## <a name="possible-causes"></a>Possíveis causas

-   A interação do usuário durante a verificação, como mover o foco para um HWND não de destino, interfere no processo de verificação.
-   Uma implementação de MSAA incorreta ou inválida.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Navegação por meio de testes de acerto e localização da tela](navigation-through-hit-testing-and-screen-location.md)
</dt> <dt>

[**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)
</dt> </dl>

 

 




