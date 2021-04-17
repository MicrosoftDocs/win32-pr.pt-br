---
description: Por padrão, o sistema do Direct3D tem permissão para gravar no buffer de profundidade. A maioria dos aplicativos deixa de gravar no buffer de profundidade habilitado, mas você pode obter alguns efeitos especiais não permitindo que o sistema Direct3D grave no buffer de profundidade.
ms.assetid: d426ebff-bfce-4e5b-a97b-7b2539b4a9de
title: Alteração do acesso de gravação do buffer de profundidade (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 504a261c4d30c9d0bd9edfbf07f765b2037e8195
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105780324"
---
# <a name="changing-depth-buffer-write-access-direct3d-9"></a>Alteração do acesso de gravação do buffer de profundidade (Direct3D 9)

Por padrão, o sistema do Direct3D tem permissão para gravar no buffer de profundidade. A maioria dos aplicativos deixa de gravar no buffer de profundidade habilitado, mas você pode obter alguns efeitos especiais não permitindo que o sistema Direct3D grave no buffer de profundidade.

Você pode desabilitar as gravações de buffer de profundidade em C++ chamando o método [**IDirect3DDevice9:: Setrenderingstate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) com o parâmetro de estado definido como D3DRS \_ ZWRITEENABLE e o parâmetro de valor definido como 0.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Buffers de profundidade](depth-buffers.md)
</dt> </dl>

 

 
