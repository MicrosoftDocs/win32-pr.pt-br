---
title: Alto DPI para aplicativos da área de trabalho no Windows 8.1
description: Alto DPI para aplicativos da área de trabalho no Windows 8.1
ms.assetid: 1E92D3C8-C117-463A-AF31-12D3CAA31E2A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbef80ce11de41ca50b7cf5ce4076b294b9331b62be417686f7ba0a3a63b98dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117852422"
---
# <a name="high-dpi-for-desktop-apps-in-windows-81"></a>Alto DPI para aplicativos da área de trabalho no Windows 8.1

## <a name="platforms"></a>Plataformas

<dl> Clientes-Windows 8.1  
servidores-Windows Server 2012 R2  
</dl>

## <a name="description"></a>Descrição

em Windows 8.1 aplicativos de área de trabalho devem ser executados em monitores com escala de 200% além do dimensionamento de 100%, 125% e 150% com suporte no Windows 8. Além disso, os aplicativos de área de trabalho são dimensionados de acordo com cada monitor, em vez de um único fator de escala aplicado a todos os monitores. os desenvolvedores também podem chamar novas APIs no Windows 8.1 para obter fatores de escala por monitor.

## <a name="manifestations"></a>Manifestações

os usuários podem usar novos monitores de alta densidade com Windows 8.1 para uma experiência visual excelente que aproveita os dados de pixels mais altos. se os aplicativos não tratarem o DPI alto, Windows irá dimensioná-los para o usuário. além disso, os usuários podem usar uma combinação de exibições de alta densidade altas no mesmo computador e Windows dimensionará o conteúdo de forma adequada para cada exibição. essa é uma melhoria em relação a Windows 8, em que o conteúdo pode ser muito grande em alguns monitores.

## <a name="mitigation"></a>Atenuação

como Windows dimensionará os aplicativos que não se expandem, os desenvolvedores geralmente não precisam realizar trabalho adicional, mas os desenvolvedores que investem em escrever aplicativos que dão suporte a DPI alto terão uma vantagem competitiva, pois esses aplicativos terão uma aparência melhor em novos laptops de dpi alta e monitores de desktop.

## <a name="solution"></a>Solução

Criar um aplicativo que possa aproveitar o alto DPI é uma tarefa complexa de design e implementação. Consulte os links abaixo para obter informações sobre o tutorial, criar conteúdo de apresentação e suporte semelhante.

## <a name="tests"></a>Testes

Mesmo que os desenvolvedores não escolham fazer com que seus aplicativos tirem proveito do DPI alto, eles devem testar seu aplicativo em 100%, 125%, 150% e escala de 200% para garantir que a experiência do usuário final seja satisfatória e competitiva.

## <a name="resources"></a>Recursos

-   [White Paper e tutorial sobre DPI alto no Windows 8.1](../hidpi/high-dpi-desktop-application-development-on-windows.md)
-   [programas de exemplo Windows desktop](https://www.microsoft.com/?ref=go)
-   [COMPILAR sessão de saída 2013 em DPI alto no Windows 8.1](https://channel9.msdn.com/Events/Build/2013/4-184)

 

 