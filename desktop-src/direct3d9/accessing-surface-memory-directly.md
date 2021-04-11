---
description: 'Você pode acessar diretamente a memória da superfície usando o método IDirect3DSurface9:: LockRect.'
ms.assetid: ad669c22-6163-4fbb-bad0-160ced5bc558
title: Acessando a memória da superfície diretamente (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7ed9a65265671e6509172eccd9a1b66ea91507f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296093"
---
# <a name="accessing-surface-memory-directly-direct3d-9"></a>Acessando a memória da superfície diretamente (Direct3D 9)

Você pode acessar diretamente a memória da superfície usando o método [**IDirect3DSurface9:: LockRect**](/windows/desktop/api) . Quando você chama esse método, o parâmetro pRect é um ponteiro para uma estrutura [**Rect**](/previous-versions//dd162897(v=vs.85)) que descreve o retângulo na superfície para acessar diretamente. Para solicitar que toda a superfície seja bloqueada, defina pRect como **NULL**. Além disso, você pode especificar um **Rect** que cubra apenas uma parte da superfície. Ao fornecer que não há dois retângulos sobrepostos, dois threads ou processos podem bloquear simultaneamente vários retângulos em uma superfície. Observe que um buffer de fundo de uma amostra não pode ser bloqueado.

O método [**IDirect3DSurface9:: LockRect**](/windows/desktop/api) preenche uma estrutura de [**D3DLOCKED \_ Rect**](d3dlocked-rect.md) com todas as informações para acessar corretamente a memória da superfície. A estrutura inclui informações sobre a densidade e tem um ponteiro para os bits bloqueados. Quando você terminar de acessar a memória da superfície, chame o método [**IDirect3DSurface9:: UnlockRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-unlockrect) para desbloqueá-la.

Embora você tenha uma superfície bloqueada, você pode manipular diretamente o conteúdo. A lista a seguir descreve algumas dicas para evitar problemas comuns com a renderização direta da memória da superfície.

-   Nunca assuma uma densidade de exibição constante. Sempre examine as informações de timbre retornadas pelo método [**IDirect3DSurface9:: LockRect**](/windows/desktop/api) . Essa densidade pode variar por vários motivos, incluindo o local da memória da superfície, o tipo de cartão de vídeo ou até a versão do driver do Direct3D. Para obter mais informações, consulte [largura vs. pitch (Direct3D 9)](width-vs--pitch.md).
-   Certifique-se de que você copia para superfícies desbloqueadas. Os métodos de cópia do Direct3D falharão se forem chamados em uma superfície bloqueada.
-   Limite a atividade do aplicativo enquanto uma superfície está bloqueada.
-   Sempre copie os dados alinhados para exibir a memória. O Windows 98 usa um manipulador de falhas de página, Vflatd. 386, para implementar um buffer de quadro simples virtual para cartões de vídeo com memória comutada pelo banco. O manipulador permite que esses dispositivos de exibição apresentem um buffer de quadro linear para o Direct3D. Copiar dados não alinhados para exibir a memória pode fazer com que o sistema suspenda operações se a cópia abranger bancos de memória.
-   Uma superfície não poderá ser bloqueada se pertencer a um recurso atribuído ao \_ pool de memória padrão D3DPOOL, a menos que seja uma textura dinâmica ou uma superfície criada usando [**IDirect3DDevice9:: CreateOffscreenPlainSurface**](/windows/desktop/api). As superfícies de buffer de fundo, que podem ser acessadas usando os métodos [**IDirect3DDevice9:: GetBackBuffer**](/windows/desktop/api) e [**IDirect3DSwapChain9:: GetBackBuffer**](/windows/desktop/api) , só poderão ser bloqueadas se a cadeia de permuta tiver sido criada com o membro flags de [**D3DPRESENT \_ Parameters**](d3dpresent-parameters.md) D3DPRESENTFLAG \_ \_ BackBuffer.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Superfícies de Direct3D](direct3d-surfaces.md)
</dt> </dl>

 

 
