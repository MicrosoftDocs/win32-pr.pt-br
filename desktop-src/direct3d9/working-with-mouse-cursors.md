---
description: Os métodos de cursor do mouse permitem que o aplicativo especifique um cursor de cor fornecendo uma superfície que contém uma imagem.
ms.assetid: 300a8a6f-abcd-49c9-889b-14b12ff5c821
title: Trabalhando com cursores do mouse (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 999bd324c8c3a1a2c743b5417f5d316a9d0f9493ccb4b749545e53e23e58917f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118518914"
---
# <a name="working-with-mouse-cursors-direct3d-9"></a>Trabalhando com cursores do mouse (Direct3D 9)

Os métodos de cursor do mouse permitem que o aplicativo especifique um cursor de cor fornecendo uma superfície que contém uma imagem. O sistema garantirá que esse cursor será atualizado pela metade da taxa de exibição ou mais se a taxa de quadros do aplicativo for lenta. No entanto, o cursor nunca será atualizado com mais frequência do que a taxa de atualização de exibição.

A posição do cursor do mouse está vinculada ao cursor do sistema, adequadamente dimensionada para a resolução espacial do modo de exibição atual, mas pode ser movida explicitamente pelo aplicativo. Isso é análogo ao comportamento do cursor do mouse do sistema com suporte da API do Win32. Para obter mais informações sobre como usar um cursor do mouse em seu aplicativo do Direct3D, consulte os tópicos de referência a seguir.

-   [**IDirect3DDevice9::ShowCursor**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-showcursor)
-   [**IDirect3DDevice9::SetCursorPosition**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setcursorposition)
-   [**IDirect3DDevice9::SetCursorProperties**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setcursorproperties)

O Direct3D garante que o mouse tenha suporte por implementações de hardware ou pelo tempo de execução do Direct3D que executa operações de transferência acelerada por hardware ao chamar [**IDirect3DDevice9::P reenviado**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Dicas de programação](programming-tips.md)
</dt> </dl>

 

 
