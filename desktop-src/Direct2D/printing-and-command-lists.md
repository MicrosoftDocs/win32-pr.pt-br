---
title: Listas de comandos e impressão
description: O controle de impressão Direct2D \ 32; é um novo componente do módulo Direct2D no Windows 8.
ms.assetid: C51ACCDE-B205-4F79-A2FD-D112BAAD1616
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b6beb16a24c972016686e2dffe915a947128a63
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366137"
---
# <a name="printing-and-command-lists"></a>Listas de comandos e impressão

O [](./direct2d-portal.md) [**controle de impressão**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1printcontrol) Direct2D é um novo componente do módulo Direct2D no Windows 8. Esse componente permite que os aplicativos Direct2D reutilizem suas chamadas de desenho Direct2D (em termos de alterações de estado e primitivos de renderização) para fornecer resultados de impressão semelhantes ao que você vê na tela.

A interface [**ID2D1PrintControl**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1printcontrol) representa um trabalho de impressão virtual: você pode criar um controle de impressão [Direct2D](./direct2d-portal.md) para iniciar um novo trabalho de impressão, passar o conteúdo do Direct2D para cada página que você deseja imprimir e, em seguida, fechar o controle de impressão para concluir um trabalho de impressão.

> [!Note]  
> Um controle de impressão é mapeado para um e exatamente um trabalho de impressão, e você não pode reutilizá-lo.

O controle de impressão [Direct2D](./direct2d-portal.md) converte e otimiza o conteúdo do Direct2D passado para o subsistema de impressão, que funciona com as impressoras reais para fornecer a impressão real. Todos os detalhes específicos de impressão ficam ocultos dos aplicativos Direct2D, o que significa que os aplicativos Direct2D podem imprimir sem saber em quais dispositivos eles estão desenhando ou como os desenhos são convertidos para impressão.

Para imprimir com o [Direct2D](./direct2d-portal.md), você precisa preparar uma lista de comandos do Direct2D para cada página que deseja imprimir e, em seguida, passar essa lista de comandos para o controle de impressão Direct2D. Para preparar essa lista de comandos do Direct2D, basta criar e definir uma lista de comandos como o destino de desenho do contexto do dispositivo atual e, em seguida, desenhar para esse contexto de dispositivo, exatamente como se você estiver desenhando em um destino de bitmap para exibição. Confira [dispositivos e contextos de dispositivo](devices-and-device-contexts.md) para obter mais informações sobre dispositivos e destinos.

O diagrama aqui ilustra a interação entre o aplicativo, o contexto do dispositivo, o destino de bitmap, o destino da lista de comandos e o controle de impressão.

> [!Note]  
> Os componentes de impressora e Sub-System de impressão do Windows estão em cinza porque estão completamente ocultos dos aplicativos [Direct2D](./direct2d-portal.md) .

![um diagrama que mostra como os comandos e a impressão interagem com um aplicativo e Direct2D.](images/d2dprintcontroldiagram.png)

## <a name="example"></a>Exemplo

O processo completo de impressão do conteúdo do Direct2D inclui as etapas a seguir.

1.  Crie um controle de impressão para iniciar um trabalho de impressão.
2.  Adicione uma página ao controle de impressão passando uma lista de comandos.
3.  Repita a etapa 2 para cada página no restante do documento
4.  Feche o controle de impressão para concluir o trabalho de impressão.

Este é um exemplo de código que mostra o processo.

```cpp
ID2D1CommandList* commandList;
// Skip command list creation and drawing for simplicity.

// Set print control properties.
D2D1_PRINT_CONTROL_PROPERTIES printControlProperties;
printControlProperties.rasterDPI = 150.0f; // Use the default rasterization DPI for all unsupported Direct2D commands 
                                                                                                                                                                            //  or options.
printControlProperties.fontSubset = D2D1_PRINT_FONT_SUBSET_MODE_DEFAULT; // Using the default font subset strategy.
printControlProperties.colorSpace = D2D1_COLOR_SPACE_SRGB; // Color space for vector graphics in Direct2D print control.

// Create a Direct2D Print Control to initiate a print job.
ID2D1PrintControl* d2dPrintControl;
d2dDevice->CreatePrintControl(
    wicFactory,
    documentTarget,
    printControlProperties,
    &d2dPrintControl
    );

// Add Direct2D drawing commands encapsulated in a command list.
// You can add in more pages by calling this API multiple times.
d2dPrintControl->AddPage(commandList);

// Close the print control to complete a print job.
d2dPrintControl->Close();
```

## <a name="related-topics"></a>Tópicos relacionados

[**ID2D1CommandList**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1commandlist)

[**ID2D1PrintControl**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1printcontrol)

[Melhorando o desempenho de aplicativos Direct2D e impressão](improving-direct2d-performance.md)