---
description: O Windows GDI+ é o subsistema do sistema operacional Windows XP ou do Windows Server 2003 que é responsável por exibir informações sobre telas e impressoras. GDI+ é uma API que é exposta por meio de um conjunto de classes C++.
ms.assetid: 8797e7c4-44d8-49f7-aec8-37ee48c24747
title: Visão geral do GDI+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb6eb3885d33ad332ac61454525367788d7aed56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988860"
---
# <a name="overview-of-gdi"></a>Visão geral do GDI+

O Windows GDI+ é o subsistema do sistema operacional Windows XP ou do Windows Server 2003 que é responsável por exibir informações sobre telas e impressoras. GDI+ é uma API que é exposta por meio de um conjunto de classes C++.

Como seu nome sugere, o GDI+ é o sucessor do Windows Graphics Device Interface (GDI), a interface gráfica do dispositivo incluída nas versões anteriores do Windows. O Windows XP ou o Windows Server 2003 dá suporte a GDI para compatibilidade com aplicativos existentes, mas os programadores de novos aplicativos devem usar o GDI+ para todas as suas necessidades gráficas, pois a GDI+ otimiza muitos dos recursos do GDI e também fornece recursos adicionais.

Uma interface de dispositivo de gráficos, como GDI+, permite que os programadores de aplicativos exibam informações em uma tela ou impressora sem precisar se preocupar com os detalhes de um determinado dispositivo de vídeo. O programador de aplicativos faz chamadas para métodos fornecidos por classes GDI+ e esses métodos, por sua vez, fazem as chamadas apropriadas para drivers de dispositivo específicos. A GDI+ isola o aplicativo do hardware de gráficos e é esse isolamento que permite aos desenvolvedores criar aplicativos independentes de dispositivo.

 

 



