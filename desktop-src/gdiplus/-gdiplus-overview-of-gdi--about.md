---
description: Windows GDI+ é o subsistema do sistema operacional Windows XP ou Windows Server 2003 que é responsável por exibir informações em telas e impressoras. GDI+ é uma API exposta por meio de um conjunto de classes C++.
ms.assetid: 8797e7c4-44d8-49f7-aec8-37ee48c24747
title: Visão geral do GDI+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15ca4eadf9eaf27cbe35103753a49c4bc25d2974ee1051481b0b52787a6602e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119830756"
---
# <a name="overview-of-gdi"></a>Visão geral do GDI+

Windows GDI+ é o subsistema do sistema operacional Windows XP ou Windows Server 2003 que é responsável por exibir informações em telas e impressoras. GDI+ é uma API exposta por meio de um conjunto de classes C++.

Como seu nome sugere, GDI+ é o sucesso do Windows Graphics Device Interface (GDI), a interface do dispositivo gráfico incluída em versões anteriores do Windows. Windows O XP ou o Windows Server 2003 dá suporte à GDI para compatibilidade com aplicativos existentes, mas os programadores de novos aplicativos devem usar o GDI+ para todas as suas necessidades gráficas porque o GDI+ otimiza muitos dos recursos da GDI e também fornece recursos adicionais.

Uma interface de dispositivo gráfico, como GDI+, permite que os programadores de aplicativos exibem informações em uma tela ou impressora sem precisar se preocupar com os detalhes de um dispositivo de exibição específico. O programador de aplicativos faz chamadas para métodos fornecidos por classes GDI+ e esses métodos, por sua vez, fazem as chamadas apropriadas para drivers de dispositivo específicos. GDI+ isola o aplicativo do hardware gráfico e é esse problema que permite aos desenvolvedores criar aplicativos independentes de dispositivo.

 

 



