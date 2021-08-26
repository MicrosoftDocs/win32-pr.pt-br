---
description: O D3DX é uma biblioteca de ferramentas projetadas para fornecer funcionalidades gráficas adicionais sobre o Direct3D. O D3DX é fornecido como uma DLL (biblioteca de vínculo dinâmico).
ms.assetid: d7b8c6ba-5c4f-494c-a24f-3b81a176725f
title: D3DX (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 556d1f7dfe7f8d841220af4f5dbe650bd74e4c8dff86812650545a07129af644
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119986906"
---
# <a name="d3dx-direct3d-9"></a>D3DX (Direct3D 9)

> [!NOTE]
> A biblioteca D3DX foi preterida. Se atualizar para uma versão mais recente do Direct3D e o código do utilitário associado não for uma opção, você poderá usar o pacote de NuGet [Microsoft.DXSDK.D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) em vez de depender do SDK do DirectX herdado ou do DirectSetup.

O D3DX é uma biblioteca de ferramentas projetadas para fornecer funcionalidades gráficas adicionais sobre o Direct3D. O D3DX é fornecido como uma DLL (biblioteca de vínculo dinâmico).

Apenas uma versão do D3DX é fornecida nesta versão do SDK do DirectX. A DLL D3DX de varejo está incluída no redistribuível fornecido no SDK e é instalada automaticamente como parte da instalação do **DirectX com DirectSetup.** A biblioteca D3DX incluída nesta versão depende dos runtimes do Direct3D fornecidos com esse SDK. Os aplicativos que se vinculam à versão do D3DX nesta versão também devem redistribuir o runtime desse SDK.

Várias versões do D3DX podem residir de forma independente em um único sistema simultaneamente. Vinculando estaticamente um aplicativo a D3dx9.lib, o aplicativo vincula dinamicamente à DLL DLL D3DX de varejo correspondente em tempo de run-time. Essa DLL corresponde aos headers D3DX em que o aplicativo é compilado (nomeado com a constante VERSION do SDK do D3DX \_ \_ em D3dx9core.h). À medida que novas versões do D3DX são enviadas em versões futuras do SDK do DirectX, os aplicativos que se vinculam a bibliotecas D3DX anteriores permanecerão inalterados.

A biblioteca D3DX aborda essas áreas gerais de funcionalidade:

-   [Suporte a desenho de linha no D3DX (Direct3D 9)](line-drawing-support-in-d3dx.md)
-   [Suporte à malha no D3DX (Direct3D 9)](mesh-support-in-d3dx.md)
-   [Suporte à função matemática no D3DX (Direct3D 9)](math-function-support-in-d3dx.md)
-   [Suporte à textura no D3DX (Direct3D 9)](texture-support-in-d3dx.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Introdução](getting-started.md)
</dt> </dl>

 

 



