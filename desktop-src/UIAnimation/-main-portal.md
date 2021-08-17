---
title: Windows Gerenciador de animação
description: o gerenciador de animação de Windows (Windows animação) permite uma rica animação de elementos da interface do usuário.
ms.assetid: 1d840263-d9da-4cab-9bc3-0c143c9c8741
keywords:
- Windows animação de Windows de animação, portal
- Windows animação de Windows do gerenciador de animação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2e6a8f81fbef55525eff04df52a31f8ee942707c354697658ee0ba01647d082
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117755610"
---
# <a name="windows-animation-manager"></a>Windows Gerenciador de animação

## <a name="purpose"></a>Finalidade

o gerenciador de animação de Windows (Windows animação) permite uma rica animação de elementos da interface do usuário. Ele foi projetado para simplificar o processo de adição de animação à interface do usuário de um aplicativo e para permitir que os desenvolvedores implementem animações que são suaves, naturais e interativas.

A estrutura de animação gerencia o agendamento e a execução de animações. Ele fornece uma biblioteca de funções matemáticas úteis para especificar o comportamento de um elemento de interface do usuário ao longo do tempo e também permite que os desenvolvedores implementem funções personalizadas que fornecem comportamentos adicionais.

Windows A animação não realiza a renderização; ele pode ser usado com qualquer plataforma gráfica, incluindo Direct2D, Direct3D ou GDI+.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                   | Descrição                                                                                                                                       |
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [Windows Guia de desenvolvimento de animação](windows-animation-developer-guide.md)<br/> | o guia do desenvolvedor fornece uma visão geral da animação de Windows e fornece um código de exemplo que aborda as tarefas básicas de animação.<br/>          |
| [Windows Referência de animação](windows-animation-reference.md)<br/>               | os tópicos contidos nesta seção fornecem as especificações de referência para o gerenciador de animação Windows.<br/>                           |
| [Windows Exemplos de animação](windows-animation-samples.md)<br/>                   | os tópicos contidos nesta seção fornecem detalhes sobre os exemplos de código que dão suporte à documentação do Windows Animation Manager. <br/> |
| [Windows Glossário de animação](-ui-animation-glossary.md)<br/>                     | este glossário contém termos e acrônimos de interesse para os desenvolvedores que usam o gerenciador de animação Windows.<br/>                               |



 

## <a name="developer-audience"></a>Público de desenvolvedores

Windows A animação foi projetada para ser usada por desenvolvedores experientes de C/C++ que estão familiarizados com o COM, conceitos de programação de interface do usuário e conceitos gerais de animação.

## <a name="run-time-requirements"></a>Requisitos de tempo de execução

o gerenciador de animação Windows foi introduzido no Windows 7.

os aplicativos que exigem suporte para Windows o gerenciador de animação no Windows vista podem utilizar a atualização de plataforma para Windows Vista. os aplicativos que exigem atualização de plataforma para o Windows Vista podem ter Windows Update verificar se ele está instalado ou baixá-lo e instalá-lo em segundo plano caso contrário. para obter mais informações, consulte [sobre a atualização de plataforma para Windows Vista](../win7ip/platform-update-for-windows-vista-overview.md).

## <a name="additional-resources"></a>Recursos adicionais

-   [visão geral da animação de Cenários do Windows](https://channel9.msdn.com/blogs/yochay/windows-scenic-animation-overview) (vídeo)
-   [dentro do Windows 7: aprofundamento e Tutorial do gerenciador de animação](https://channel9.msdn.com/blogs/yochay/inside-windows-7-animation-manager-deep-dive) (vídeo)
-   [animação de Windows-tópicos avançados](https://channel9.msdn.com/posts/yochay/Windows-Animation-Advance-Topics/) (vídeo)
-   [Windows Código de exemplo do Gerenciador de animação](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DirectCompositionWindowsAnimationManager)

## <a name="related-topics"></a>Tópicos relacionados

[Visão geral da animação (.NET Framework)](/dotnet/framework/wpf/graphics-multimedia/animation-overview)