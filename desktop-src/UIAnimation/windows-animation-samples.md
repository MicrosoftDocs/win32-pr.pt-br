---
title: Exemplos de animação do Windows
description: Os tópicos contidos nesta seção fornecem detalhes sobre os exemplos de código que dão suporte à documentação do Gerenciador de animação do Windows.
ms.assetid: 33b1770a-5acb-4ab5-999c-9663f4c075f0
keywords:
- Animação do Windows animações do Windows, exemplos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c2fe31e7fa12feab010bec3da710d4b2b80dd1d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292600"
---
# <a name="windows-animation-samples"></a>Exemplos de animação do Windows

Os tópicos contidos nesta seção fornecem detalhes sobre os exemplos de código que dão suporte à documentação do Gerenciador de animação do Windows.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                     | Descrição                                                                                                         |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [Exemplo de animação orientada por aplicativo](application-driven-animation-sample.md)<br/> |                                                                                                                     |
| [Exemplo de animação orientada por temporizador](timer-driven-animation-sample.md)<br/>             |                                                                                                                     |
| [Exemplo de interpolador personalizado](custom-interpolator-sample.md)<br/>                   | Mostra como usar a animação do Windows com seu próprio interpolador personalizado, com Direct2D usado para renderização. <br/> |
| [Exemplo de layout de grade](grid-layout-sample.md)<br/>                                   | Mostra como usar a animação do Windows, usando Direct2D para animar uma grade de imagens. <br/>                         |
| [Exemplo de comparação de prioridade](priority-comparison-sample.md)<br/>                   | Mostra como usar a animação do Windows com sua própria comparação de prioridade, usando Direct2D para renderização.<br/>      |



 

## <a name="sample-files"></a>Arquivos de exemplo

Cada exemplo contém muitos dos seguintes arquivos de chave:

<dl> <dt>

<span id="Application.cpp"></span><span id="application.cpp"></span><span id="APPLICATION.CPP"></span>Application. cpp
</dt> <dd>

Define o ponto de entrada do aplicativo.

</dd> <dt>

<span id="MainWindow.h"></span><span id="mainwindow.h"></span><span id="MAINWINDOW.H"></span>MainWindow. h
</dt> <dd>

Declara a classe CMainWindow.

</dd> <dt>

<span id="MainWindow.cpp"></span><span id="mainwindow.cpp"></span><span id="MAINWINDOW.CPP"></span>MainWindow. cpp
</dt> <dd>

Inicializa os componentes de animação e a plataforma de gráficos, carrega imagens e renderiza a área do cliente.

</dd> <dt>

<span id="LayoutManager.h"></span><span id="layoutmanager.h"></span><span id="LAYOUTMANAGER.H"></span>LayoutManager. h
</dt> <dd>

Declara a classe CLayoutManager.

</dd> <dt>

<span id="LayoutManager.cpp"></span><span id="layoutmanager.cpp"></span><span id="LAYOUTMANAGER.CPP"></span>LayoutManager. cpp
</dt> <dd>

Calcula o layout das imagens na janela principal, cria storyboards, adiciona transições ao storyboard e agenda o storyboard.

</dd> <dt>

<span id="Thumbnail.h"></span><span id="thumbnail.h"></span><span id="THUMBNAIL.H"></span>Miniatura. h
</dt> <dd>

Declara a classe CThumbNail.

</dd> <dt>

<span id="Thumbnail.cpp"></span><span id="thumbnail.cpp"></span><span id="THUMBNAIL.CPP"></span>Thumbnail. cpp
</dt> <dd>

Cria variáveis de animação e renderiza miniaturas.

</dd> </dl>

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Guia de desenvolvimento de animação do Windows](windows-animation-developer-guide.md)
</dt> <dt>

[Referência de animação do Windows](windows-animation-reference.md)
</dt> </dl>

 

 





