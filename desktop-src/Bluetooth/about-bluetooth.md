---
title: Sobre o Bluetooth
description: O Bluetooth é um protocolo padrão do setor que permite a conectividade sem fio para uma infinidade de dispositivos, incluindo computadores, impressoras, celulares e dispositivos portáteis.
ms.assetid: 424168a1-e55c-4947-9a80-8594b4d83bbd
keywords:
- Bluetooth com Bluetooth, descrito
- Bluetooth Bluetooth, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b704bb3245adcd75948f7f9fbb411697c7c45f0
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/20/2020
ms.locfileid: "104007159"
---
# <a name="about-bluetooth"></a>Sobre o Bluetooth

O Bluetooth é um protocolo padrão do setor que permite a conectividade sem fio para uma infinidade de dispositivos, incluindo computadores, impressoras, celulares e dispositivos portáteis.

Os principais recursos do Bluetooth incluem:

-   Um protocolo sem fio de consumo de baixo custo e baixa energia com suporte padrão do setor e aceitação mundial.
-   Uma interface de programação definida e familiar que os desenvolvedores podem usar para desenvolver ou portar aplicativos rapidamente.
-   Um site oficial e uma organização cooperativa em todo o setor que explica, promove e padroniza a tecnologia Bluetooth. Para obter mais informações, consulte [www.Bluetooth.com](https://www.bluetooth.com/).

O Bluetooth no Windows fornece serviços principais que são semelhantes àqueles expostos pelo protocolo de controle de transmissão (a parte TCP do TCP/IP). Como muitos protocolos e serviços de rede, a conectividade Bluetooth e a transferência de dados são programadas por meio de chamadas de função do Windows Sockets, usando técnicas comuns de programação do Windows Sockets e extensões Bluetooth específicas. No entanto, como existem diferenças significativas entre uma rede fixa e com fio e uma rede ad hoc sem fio, o Bluetooth fornece extensões como descoberta de serviço/dispositivo e notificação que permitem que os aplicativos operem corretamente no ambiente sem fio. Essas extensões também abrem a maneira de portar simples para tecnologias semelhantes, como IrDA ou transportes de sem fio futuros.

A Microsoft oferece suporte para Bluetooth no Windows XP com Service Pack 1 (SP1) e posterior, no Windows XP Embedded com Service Pack 2 e no Windows CE. Os aplicativos Bluetooth executados no Windows XP devem ser capazes de serem executados em uma imagem de tempo de execução baseada no Windows XP Embedded que inclui as dependências necessárias. Para obter mais informações sobre o Windows XP Embedded, consulte a documentação da ajuda do Windows XP Embedded no MSDN. Para obter mais informações sobre a programação de Windows CE, consulte o SDK do Windows CE.

A Microsoft fornece duas abordagens para a programação de Bluetooth no Windows:

-   Usando a interface do Windows Sockets
-   Gerenciando dispositivos diretamente usando interfaces Bluetooth de não soquete

Esta seção fornece informações de visão geral sobre essas duas abordagens nos tópicos a seguir. Para obter mais informações sobre como usar elementos da API do Windows Sockets para programar Bluetooth, consulte [programação Bluetooth com Windows Sockets](bluetooth-programming-with-windows-sockets.md).



| Seção                                                                                | Conteúdo                                                           |
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [Suporte do Windows Sockets para Bluetooth](windows-sockets-support-for-bluetooth.md)     | Descreve a relação entre o Bluetooth e o Windows Sockets. |
| [Gerenciando dispositivos e serviços Bluetooth](managing-bluetooth-devices-and-services.md) | Descreve como gerenciar dispositivos e serviços Bluetooth.           |



 

 

 




