---
description: O gerenciamento de textura é o processo de determinar quais texturas são necessárias para a renderização em um determinado momento e garantir que essas texturas sejam carregadas na memória de vídeo.
ms.assetid: ea6d64ee-f570-49eb-b5fd-67fcde3f8ddc
title: Gerenciamento automático de textura (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0eb14eede197661bc127a062229ebed31274ae8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826601"
---
# <a name="automatic-texture-management-direct3d-9"></a>Gerenciamento automático de textura (Direct3D 9)

O gerenciamento de textura é o processo de determinar quais texturas são necessárias para a renderização em um determinado momento e garantir que essas texturas sejam carregadas na memória de vídeo. Assim como acontece com qualquer algoritmo, os esquemas de gerenciamento de textura variam em complexidade, mas qualquer abordagem ao gerenciamento de textura envolve as seguintes tarefas principais.

-   Acompanhando a quantidade de memória de textura disponível.
-   Calculando quais texturas são necessárias para a renderização e quais não são.
-   Determinar quais recursos de textura existentes podem ser recarregados com outra imagem de textura e quais superfícies devem ser destruídas e substituídas por novos recursos de textura.

O Direct3D implementa o gerenciamento de textura com suporte do sistema para garantir que as texturas sejam carregadas para um desempenho ideal. Os recursos de textura que o Direct3D gerencia são chamados de texturas gerenciadas.

O Gerenciador de textura rastreia texturas com um carimbo de data/hora que identifica quando a textura foi usada pela última vez. Em seguida, ele usa um algoritmo menos usado recentemente para determinar quais texturas devem ser removidas. As prioridades de textura são usadas como separadores de ligação quando duas texturas são destinadas para remoção da memória. Se duas texturas tiverem o mesmo valor de prioridade, a textura menos usada recentemente será removida. No entanto, se duas texturas tiverem o mesmo carimbo de data/hora, a textura que tem uma prioridade mais baixa será removida primeiro.

Você solicita o gerenciamento automático de textura para superfícies de textura ao criá-las. Para recuperar uma textura gerenciada em um aplicativo C++, crie um recurso de textura chamando [**IDirect3DDevice9:: CreateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture) e ESPECIFICANDO o D3DPOOL \_ gerenciado para o parâmetro de pool. Você não tem permissão para especificar onde deseja que a textura seja criada. Você não pode usar os \_ sinalizadores D3DPOOL padrão ou D3DPOOL \_ SYSTEMMEM ao criar uma textura gerenciada. Depois de criar a textura gerenciada, você pode chamar o método [**IDirect3DDevice9:: SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) para defini-lo como um estágio na cascata de textura do dispositivo de renderização.

Você pode atribuir uma prioridade a texturas gerenciadas chamando o método [**IDirect3DResource9:: prepriorion**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dresource9-setpriority) para a superfície de textura.

O Direct3D baixa automaticamente as texturas na memória de vídeo conforme necessário. O sistema pode armazenar em cache as texturas gerenciadas na memória de vídeo local ou não local, dependendo da disponibilidade da memória de vídeo não local ou de outros fatores. O local do cache de suas texturas gerenciadas não é comunicado ao seu aplicativo, nem essas informações são necessárias para usar o gerenciamento automático de textura. Se seu aplicativo usa mais texturas do que pode caber na memória de vídeo, o Direct3D remove as texturas mais antigas da memória de vídeo para liberar espaço para as novas texturas. Se você usar uma textura removida novamente, o sistema usará a superfície de textura da memória do sistema original para recarregar a textura no cache de memória de vídeo. Embora o recarregamento da textura seja necessário, ele também diminui o desempenho do aplicativo.

Você pode modificar dinamicamente a cópia original da memória do sistema da textura atualizando ou bloqueando o recurso de textura. Quando o sistema detecta uma superfície suja-depois que uma atualização é concluída, ou quando a superfície é desbloqueada, o Gerenciador de textura atualiza automaticamente a cópia da memória de vídeo da textura. O impacto de desempenho incorrido é semelhante ao recarregamento de uma textura removida.

Ao inserir um novo nível em um jogo, seu aplicativo pode precisar liberar todas as texturas gerenciadas da memória de vídeo (chamando [**IDirect3DDevice9:: EvictManagedResources**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-evictmanagedresources)).

Para obter mais informações sobre o gerenciamento de recursos, consulte [Managing Resources (Direct3D 9)](managing-resources.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Texturas do Direct3D](direct3d-textures.md)
</dt> </dl>

 

 
