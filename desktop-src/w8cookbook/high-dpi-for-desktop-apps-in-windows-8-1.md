---
title: Alto DPI para aplicativos da área de trabalho no Windows 8.1
description: Alto DPI para aplicativos da área de trabalho no Windows 8.1
ms.assetid: 1E92D3C8-C117-463A-AF31-12D3CAA31E2A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c6c223e9dc39cda9a109280926a5eb47a8fffcc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105786159"
---
# <a name="high-dpi-for-desktop-apps-in-windows-81"></a>Alto DPI para aplicativos da área de trabalho no Windows 8.1

## <a name="platforms"></a>Plataformas

<dl> Clientes-Windows 8.1  
Servidores-Windows Server 2012 R2  
</dl>

## <a name="description"></a>Descrição

Em Windows 8.1 aplicativos de área de trabalho devem ser executados em monitores com dimensionamento de 200% além do dimensionamento de 100%, 125% e 150% com suporte no Windows 8. Além disso, os aplicativos de área de trabalho são dimensionados de acordo com cada monitor, em vez de um único fator de escala aplicado a todos os monitores. Os desenvolvedores também podem chamar novas APIs no Windows 8.1 para obter fatores de escala por monitor.

## <a name="manifestations"></a>Manifestações

Os usuários podem usar novos monitores de alta densidade com Windows 8.1 para uma experiência visual excelente que aproveita os dados de pixels mais altos. Se os aplicativos não tratarem do DPI alto, o Windows os dimensionará para o usuário. Além disso, os usuários podem usar uma mistura de exibições de alta densidade altas no mesmo computador, e o Windows dimensionará o conteúdo adequadamente para cada exibição. Esse é um aprimoramento do Windows 8, onde o conteúdo pode ser muito grande em alguns monitores.

## <a name="mitigation"></a>Atenuação

Como o Windows dimensionará os aplicativos que não se expandem, os desenvolvedores geralmente não precisam realizar trabalho adicional, mas os desenvolvedores que investem em escrever aplicativos que dão suporte a DPI alto terão uma vantagem competitiva, pois esses aplicativos terão uma aparência melhor em novos laptops de alto DPI e monitores de desktop.

## <a name="solution"></a>Solução

Criar um aplicativo que possa aproveitar o alto DPI é uma tarefa complexa de design e implementação. Consulte os links abaixo para obter informações sobre o tutorial, criar conteúdo de apresentação e suporte semelhante.

## <a name="tests"></a>Testes

Mesmo que os desenvolvedores não escolham fazer com que seus aplicativos tirem proveito do DPI alto, eles devem testar seu aplicativo em 100%, 125%, 150% e escala de 200% para garantir que a experiência do usuário final seja satisfatória e competitiva.

## <a name="resources"></a>Recursos

-   [White Paper e tutorial sobre DPI alto no Windows 8.1](../hidpi/high-dpi-desktop-application-development-on-windows.md)
-   [Programas de exemplo da área de trabalho do Windows](https://www.microsoft.com/?ref=go)
-   [COMPILAR sessão de saída 2013 em DPI alto no Windows 8.1](https://channel9.msdn.com/Events/Build/2013/4-184)

 

 