---
title: Sobre o IWMPPluginEnable
description: Sobre o IWMPPluginEnable
ms.assetid: 7611a197-f404-4cfb-88b0-05348a41ac42
keywords:
- Plug-ins do Windows Media Player, interfaces
- plug-ins, interfaces
- plug-ins de processamento de sinal digital, interfaces
- Plug-ins do DSP, interfaces
- interfaces, plug-ins do DSP
- Plug-ins do Windows Media Player, interface IWMPPluginEnable
- plug-ins, interface IWMPPluginEnable
- plug-ins de processamento de sinal digital, interface IWMPPluginEnable
- Plug-ins do DSP, interface IWMPPluginEnable
- Interface IWMPPluginEnable
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce7bf0f58be1d2623539cc5ac1329838246c8697
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103915997"
---
# <a name="about-iwmppluginenable"></a>Sobre o IWMPPluginEnable

A interface **IWMPPluginEnable** é necessária para plug-ins do DSP do Windows Media Player. **IWMPPluginEnable** contém dois métodos que armazenam se o Windows Media Player habilitou o plug-in DSP. O Windows Media Player chama **IWMPPluginEnable:: SetEnable** quando cria uma instância do plug-in do DSP, passando um valor **true** se tiver habilitado o plug-in ou **false** caso contrário.

Plug-ins do DSP podem permanecer carregados mesmo quando o usuário optar por desabilitá-los. Quando desabilitado, um plug-in deve copiar dados do buffer de entrada para o buffer de saída, executando somente o processamento de conversão de formato, se aplicável.

O Windows Media Player também chama esse método antes de liberar uma instância do plug-in do DSP. Isso é útil para permitir que clientes do plug-in verifiquem se o plug-in está habilitado no momento. Por exemplo, um plug-in de interface do usuário pode alterar a aparência de seus controles para alertar o usuário de que o plug-in do DSP não está conectado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Interfaces necessárias**](required-interfaces.md)
</dt> </dl>

 

 




