---
title: Usando as funções de configuração do monitor de High-Level
description: Usando as funções de configuração do monitor de High-Level
ms.assetid: 23e5d45d-a924-4119-b21d-b24764b53a94
keywords:
- monitorar, funções
- monitorar, funções de configuração de alto nível
- monitor, enumerando monitores físicos
- monitorar, configurações contínuas
- configurações do monitor, funções de configuração de alto nível
- configuração do monitor, funções
- monitorar a configuração, enumerando monitores físicos
- configuração do monitor, configurações contínuas
- Enumerando monitores físicos
- funções de configuração de alto nível
- configurações de monitor contínuo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 827d19ef0006dc89208061c18ef34c28c8f993c3e0d6ebd0d1c1005daf2cd640
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066596"
---
# <a name="using-the-high-level-monitor-configuration-functions"></a>Usando as funções de configuração do monitor de High-Level

## <a name="enumerating-physical-monitors"></a>Enumerando monitores físicos

Há várias funções que enumeram dispositivos de exibição, incluindo [**EnumDisplayMonitors**](/windows/desktop/api/winuser/nf-winuser-enumdisplaymonitors) e [**MonitorFromWindow**](/windows/desktop/api/winuser/nf-winuser-monitorfromwindow). essas funções são documentadas na documentação do Windows GDI, no tópico [vários monitores de exibição](/windows/desktop/gdi/multiple-display-monitors). Essas funções retornam identificadores **HMONITOR** . Apesar do nome, no entanto, um identificador **HMONITOR** pode ser associado a mais de um monitor físico. Para definir as configurações em um monitor, o aplicativo deve obter um identificador exclusivo para o monitor físico chamando [**GetPhysicalMonitorsFromHMONITOR**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromhmonitor).

Se seu aplicativo usar o Direct3D, você poderá obter um identificador de monitor de um dispositivo Direct3D chamando [**GetPhysicalMonitorsFromIDirect3DDevice9**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromidirect3ddevice9).

## <a name="supported-functions"></a>Funções com suporte

Um monitor pode não dar suporte a todas as funções de configuração do monitor. Para descobrir a quais funções um monitor dá suporte, chame [**GetMonitorCapabilities**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-getmonitorcapabilities).

## <a name="continuous-monitor-settings"></a>Configurações de Monitor contínuo

Uma configuração de monitor *contínua* é aquela que pode variar entre alguns valores mínimo e máximo. A maioria das funções de configuração do monitor de alto nível controla as configurações de monitor contínuas. Por exemplo, brilho e contraste são configurações contínuas.

As configurações de monitor contínuo não têm unidades reais definidas. As unidades são arbitrárias e podem variar de um fabricante para outro. Se dois monitores tiverem o mesmo valor de brilho, por exemplo, um monitor poderá parecer muito mais brilhante do que o outro. Normalmente, um aplicativo apresentará controles deslizantes ou controles de cima para baixo para o usuário. Em seguida, o usuário pode ajustar as configurações para fornecer a melhor qualidade subjetiva.

## <a name="changes-in-monitor-state"></a>Alterações no estado do monitor

Um monitor pode alterar Estados por vários motivos, incluindo:

-   O usuário altera as configurações com os controles de painel frontal do monitor.
-   O usuário altera a resolução de tela, a taxa de atualização ou a profundidade de bits do monitor.
-   O aplicativo usa as funções de monitor de baixo nível para alterar uma configuração que não pode ser acessada das funções de alto nível.
-   O aplicativo chama [**RestoreMonitorFactoryColorDefaults**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-restoremonitorfactorycolordefaults) ou [**RestoreMonitorFactoryDefaults**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-restoremonitorfactorydefaults).

Todos esses eventos podem alterar as configurações do monitor. Eles também podem alterar o valor mínimo e máximo de uma configuração.

## <a name="dependencies-among-monitor-settings"></a>dependências entre Configurações do Monitor

Alterar a temperatura de cor pode alterar a unidade atual e obter as configurações, e o inverso também é verdadeiro. Essas são as únicas dependências entre as funções de configuração de monitor de alto nível. Outras configurações podem ser acessíveis somente por meio das funções de monitor de baixo nível. Pode haver dependências entre essas configurações e as configurações de alto nível. Essas dependências são específicas do fornecedor. Um aplicativo pode lidar com esse problema de várias maneiras:

-   Use apenas funções de alto nível.
-   Depois de chamar uma função de nível baixo, obtenha o valor atual de cada configuração de monitor. Infelizmente, essa abordagem pode ser lenta, pois obter cada configuração leva cerca de 40 milissegundos.
-   Use funções de nível baixo somente com modelos de monitor específicos cujo comportamento você entende.

## <a name="disabled-monitor-settings"></a>Monitor desabilitado Configurações

Um aplicativo não pode desabilitar nenhuma configuração de monitor chamando as funções de monitor de alto nível. No entanto, um aplicativo pode desabilitar acidentalmente uma configuração se usar as funções de nível baixo para alterar uma configuração de monitor que não é suportada pelas funções de alto nível. Além disso, um usuário pode desabilitar uma configuração usando o controle de painel frontal. Esses comportamentos são específicos do fornecedor.

Se uma configuração de monitor for desabilitada, qualquer função que definir ou recuperar essa configuração falhará e definirá a configuração de monitor do último código de erro para erro \_ desabilitado \_ \_ . Quando isso ocorre, o aplicativo pode executar um dos seguintes procedimentos:

-   Exiba uma mensagem de erro e sugira ao usuário que ele tente ajustar a configuração usando o controle de painel frontal.
-   Chame a função [**RestoreMonitorFactoryDefaults**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-restoremonitorfactorydefaults) . Se um monitor tiver os padrões do MC \_ Restore \_ Factory \_ habilita o sinalizador de \_ \_ \_ recursos de configurações do monitor, essa função habilitará todas as configurações do monitor com suporte nas funções de monitor de alto nível. Infelizmente, a função também redefine as configurações do monitor para o padrão de fábrica.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando a configuração do monitor](using-monitor-configuration.md)
</dt> </dl>

 

 