---
title: Gerenciador de animação do Windows
description: O Gerenciador de animação do Windows (animação do Windows) permite uma rica animação de elementos da interface do usuário.
ms.assetid: 1d840263-d9da-4cab-9bc3-0c143c9c8741
keywords:
- Animação das janelas de animação do Windows, portal
- Animação do Windows do Gerenciador de animação do Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d274b9f2d5e386fbe01c2caeb9e1e65ddbdc73f3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917426"
---
# <a name="windows-animation-manager"></a>Gerenciador de animação do Windows

## <a name="purpose"></a>Finalidade

O Gerenciador de animação do Windows (animação do Windows) permite uma rica animação de elementos da interface do usuário. Ele foi projetado para simplificar o processo de adição de animação à interface do usuário de um aplicativo e para permitir que os desenvolvedores implementem animações que são suaves, naturais e interativas.

A estrutura de animação gerencia o agendamento e a execução de animações. Ele fornece uma biblioteca de funções matemáticas úteis para especificar o comportamento de um elemento de interface do usuário ao longo do tempo e também permite que os desenvolvedores implementem funções personalizadas que fornecem comportamentos adicionais.

A animação do Windows não executa a renderização; Ele pode ser usado com qualquer plataforma gráfica, incluindo Direct2D, Direct3D ou GDI+.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                   | Descrição                                                                                                                                       |
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [Guia de desenvolvimento de animação do Windows](windows-animation-developer-guide.md)<br/> | O guia do desenvolvedor fornece uma visão geral da animação do Windows e fornece um código de exemplo que aborda as tarefas básicas de animação.<br/>          |
| [Referência de animação do Windows](windows-animation-reference.md)<br/>               | Os tópicos contidos nesta seção fornecem as especificações de referência para o Gerenciador de animação do Windows.<br/>                           |
| [Exemplos de animação do Windows](windows-animation-samples.md)<br/>                   | Os tópicos contidos nesta seção fornecem detalhes sobre os exemplos de código que dão suporte à documentação do Gerenciador de animação do Windows. <br/> |
| [Glossário de animação do Windows](-ui-animation-glossary.md)<br/>                     | Este glossário contém termos e acrônimos de interesse para os desenvolvedores que usam o Gerenciador de animação do Windows.<br/>                               |



 

## <a name="developer-audience"></a>Público de desenvolvedores

A animação do Windows foi projetada para ser usada por desenvolvedores experientes de C/C++ que estão familiarizados com o COM, conceitos de programação de interface do usuário e conceitos gerais de animação.

## <a name="run-time-requirements"></a>Requisitos de tempo de execução

O Gerenciador de animação do Windows foi introduzido no Windows 7.

Os aplicativos que exigem suporte para o Windows Animation Manager no Windows Vista podem utilizar a atualização de plataforma para o Windows Vista. Os aplicativos que exigem a atualização da plataforma para o Windows Vista podem ter Windows Update verificar se estão instalados ou baixá-los e instalá-los em segundo plano caso contrário. Para obter mais informações, consulte [sobre a atualização de plataforma para Windows Vista](../win7ip/platform-update-for-windows-vista-overview.md).

## <a name="additional-resources"></a>Recursos adicionais

-   [Visão geral da animação de cenários do Windows](https://channel9.msdn.com/blogs/yochay/windows-scenic-animation-overview) (vídeo)
-   [Dentro do Windows 7: aprofundamento e tutorial do Gerenciador de animação](https://channel9.msdn.com/blogs/yochay/inside-windows-7-animation-manager-deep-dive) (vídeo)
-   [Animação do Windows-tópicos avançados](https://channel9.msdn.com/posts/yochay/Windows-Animation-Advance-Topics/) (vídeo)
-   [Código de exemplo do Gerenciador de animação do Windows](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DirectCompositionWindowsAnimationManager)

## <a name="related-topics"></a>Tópicos relacionados

[Visão geral da animação (.NET Framework)](/dotnet/framework/wpf/graphics-multimedia/animation-overview)