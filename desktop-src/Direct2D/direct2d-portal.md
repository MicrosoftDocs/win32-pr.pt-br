---
title: Direct2D
description: .
ms.assetid: 03b3b91c-9751-4f8d-af24-85067f06930b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2eae62ba2d6ff44920d6b6d4890a8c48bc3c0f8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007833"
---
# <a name="direct2d"></a>Direct2D

## <a name="purpose"></a>Finalidade

Direct2D é uma API de elementos gráficos 2D com aceleração de hardware e modo imediato que fornece alto desempenho e renderização de alta qualidade para geometria 2D, bitmaps e texto. A API Direct2D foi projetada para interoperar bem com GDI, GDI+ e Direct3D.

## <a name="developer-audience"></a>Público de desenvolvedores

O Direct2D é projetado principalmente para uso pelas seguintes classes de desenvolvedores:

-   Desenvolvedores de aplicativos nativos de grande escala empresarial.
-   Desenvolvedores que criam kits de controle e bibliotecas para consumo por desenvolvedores de downstream.
-   Desenvolvedores que exigem renderização do lado do servidor de gráficos 2D.
-   Os desenvolvedores que usam gráficos do Direct3D e precisam de renderização simples, de alto desempenho em 2 e de texto para menus, elementos de interface do usuário (IU) e HUDs (exibições de cabeçotes).

## <a name="run-time-requirements"></a>Requisitos de tempo de execução

-   Windows 7 ou Windows Vista com Service Pack 2 (SP2) e atualização de plataforma para Windows Vista e posterior.
-   Windows Server 2008 R2 ou Windows Server 2008 com Service Pack 2 (SP2) e atualização de plataforma para Windows Server 2008 e posterior.

> [!Note]
>
> A atualização de plataforma para o Windows Vista e a atualização de plataforma para Windows Server 2008 são um conjunto de bibliotecas de tempo de execução que permite aos desenvolvedores direcionar aplicativos para o Windows 7, Windows Vista, Windows Server 2008 R2 e Windows Server 2008. Essas atualizações estarão disponíveis para todos os clientes do Windows Vista e do Windows Server 2008 por meio do Windows Update. Aplicativos de terceiros que exigem atualização de plataforma para Windows Vista ou atualização de plataforma para Windows Server 2008 podem ter Windows Update detectar se a atualização necessária está instalada; Se não estiver, Windows Update será baixado e instalado em segundo plano. Para obter mais informações sobre as duas atualizações, consulte [atualização de plataforma para Windows Vista](https://support.microsoft.com/kb/971644).

 

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                          | Descrição                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [O que há de novo no Direct2D](what-s-new-in-direct2d-for-windows-8-consumer-preview.md)<br/> | Aqui estão algumas das novas adições ao Direct2D. <br/>                                                                                                                   |
| [Sobre o Direct2D](direct2d-overview.md)<br/>                                             | Apresenta o Direct2D, uma API que fornece aos desenvolvedores do Win32 a capacidade de executar tarefas de renderização de gráficos 2D com desempenho e qualidade visual superiores. <br/> |
| [Guia de início rápido do Direct2D para Windows 8](direct2d-quickstart-with-device-context.md)<br/>    | Resume as etapas necessárias para desenhar com Direct2D e fornece código de exemplo.<br/>                                                                                     |
| [Introdução com Direct2D](getting-started-with-direct2d-nav.md)<br/>              | Descreve como começar a criar aplicativos Direct2D e fornece código de exemplo.<br/>                                                                             |
| [Guia de programação](programming-guide.md)<br/>                                          | Esta seção contém tópicos de programação conceitual que descrevem como usar a API Direct2D. <br/>                                                                    |
| [Referência de Direct2D](reference.md)<br/>                                                      | Descreve a API Direct2D em detalhes.<br/>                                                                                                                              |
| [Ferramentas e utilitários](tools-and-utilities.md)<br/>                                      | Ferramentas e utilitários fornecidos para Direct2D.<br/>                                                                                                                         |
| [Amostras](d2d-samples.md)<br/>                                                          | Aplicativos de exemplo que demonstram a API Direct2D.<br/>                                                                                                             |
| [Glossário do Direct2D](direct2d-glossary.md)<br/>                                          | Descreve os termos comumente usados pela documentação do Direct2D. <br/>                                                                                                      |



 

## <a name="additional-resources"></a>Recursos adicionais

-   [**Elementos gráficos e jogos do DirectX**](/windows/desktop/directx)
-   [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal)

 

