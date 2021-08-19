---
title: Listas de comandos e impressão
description: o controle de impressão Direct2D \ 32; é um novo componente do módulo Direct2D no Windows 8.
ms.assetid: C51ACCDE-B205-4F79-A2FD-D112BAAD1616
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de0026071ce8e78fc2ea946e0fffff2993e32ab48a2a20d4de6cdb12ca9b1eaa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119075040"
---
# <a name="printing-and-command-lists"></a>Listas de comandos e impressão

o [](./direct2d-portal.md) [**controle de impressão**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1printcontrol) Direct2D é um novo componente do módulo Direct2D no Windows 8. esse componente permite que os aplicativos Direct2D reutilizem suas chamadas de desenho Direct2D (em termos de alterações de estado e primitivos renderização) para fornecer resultados de impressão semelhantes ao que você vê na tela.

a interface [**ID2D1PrintControl**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1printcontrol) representa um trabalho de impressão virtual: você pode criar um [Direct2D](./direct2d-portal.md) controle de impressão para iniciar um novo trabalho de impressão, passar Direct2D conteúdo para cada página que você deseja imprimir e, em seguida, fechar o controle de impressão para concluir um trabalho de impressão.

> [!Note]  
> Um controle de impressão é mapeado para um e exatamente um trabalho de impressão, e você não pode reutilizá-lo.

o controle de impressão [Direct2D](./direct2d-portal.md) converte e otimiza o conteúdo de Direct2D passado para o subsistema de impressão, que funciona com as impressoras reais para fornecer a impressão real. todos os detalhes específicos de impressão ficam ocultos em Direct2D aplicativos, o que significa que Direct2D aplicativos podem ser impressos sem saber em quais dispositivos eles estão desenhando ou como os desenhos são convertidos para impressão.

para imprimir com [Direct2D](./direct2d-portal.md), você precisa preparar uma lista de comandos de Direct2D para cada página que deseja imprimir e, em seguida, passar essa lista de comandos para o controle de impressão de Direct2D. para preparar essa Direct2D lista de comandos, basta criar e definir uma lista de comandos como o destino de desenho do contexto do dispositivo atual e, em seguida, desenhar para esse contexto de dispositivo, exatamente como se você estiver desenhando em um destino de bitmap para exibição. Confira [dispositivos e contextos de dispositivo](devices-and-device-contexts.md) para obter mais informações sobre dispositivos e destinos.

O diagrama aqui ilustra a interação entre o aplicativo, o contexto do dispositivo, o destino de bitmap, o destino da lista de comandos e o controle de impressão.

> [!Note]  
> o Windows Sub-System de impressão e os componentes da impressora estão em cinza porque estão completamente ocultos dos aplicativos [Direct2D](./direct2d-portal.md) .

![um diagrama que mostra como os comandos e a impressão interagem com um aplicativo e Direct2D.](images/d2dprintcontroldiagram.png)

## <a name="example"></a>Exemplo

o processo completo de impressão de conteúdo de Direct2D inclui as etapas a seguir.

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

[melhorando o desempenho de aplicativos Direct2D e impressão](improving-direct2d-performance.md)