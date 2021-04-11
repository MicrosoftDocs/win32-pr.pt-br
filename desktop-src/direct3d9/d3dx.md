---
description: D3DX é uma biblioteca de ferramentas projetadas para fornecer funcionalidade gráfica adicional sobre o Direct3D. D3DX é fornecido como uma DLL (biblioteca de vínculo dinâmico).
ms.assetid: d7b8c6ba-5c4f-494c-a24f-3b81a176725f
title: D3DX (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c54899b47936d309502a591fed6fdd81ea90fe3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296091"
---
# <a name="d3dx-direct3d-9"></a>D3DX (Direct3D 9)

D3DX é uma biblioteca de ferramentas projetadas para fornecer funcionalidade gráfica adicional sobre o Direct3D. D3DX é fornecido como uma DLL (biblioteca de vínculo dinâmico).

Apenas uma versão do D3DX é fornecida nesta versão do SDK do DirectX. A DLL de D3DX de varejo está incluída no redistribuível fornecido no SDK e é instalada automaticamente como parte da [instalação do DirectX com DirectSetup](https://msdn.microsoft.com/library/ee418267(VS.85).aspx). A biblioteca D3DX incluída nesta versão depende dos tempos de execução do Direct3D fornecidos com esse SDK. Os aplicativos que se vinculam à versão do D3DX nesta versão também devem redistribuir o tempo de execução desse SDK.

Várias versões do D3DX podem residir de forma independente em um único sistema simultaneamente. Ao vincular estaticamente um aplicativo a D3dx9. lib, o aplicativo é vinculado dinamicamente à DLL de varejo D3DX correspondente em tempo de execução. Essa DLL corresponde aos cabeçalhos D3DX em que o aplicativo é compilado (nomeado com a constante de versão do SDK do D3DX \_ \_ em D3dx9core. h). À medida que novas versões do D3DX forem enviadas em versões futuras do SDK do DirectX, os aplicativos que se vinculam a bibliotecas anteriores do D3DX permanecerão inalterados.

A biblioteca D3DX aborda essas áreas gerais de funcionalidade:

-   [Suporte de desenho de linha no D3DX (Direct3D 9)](line-drawing-support-in-d3dx.md)
-   [Suporte a malha no D3DX (Direct3D 9)](mesh-support-in-d3dx.md)
-   [Suporte à função matemática no D3DX (Direct3D 9)](math-function-support-in-d3dx.md)
-   [Suporte a textura em D3DX (Direct3D 9)](texture-support-in-d3dx.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Introdução](getting-started.md)
</dt> </dl>

 

 



