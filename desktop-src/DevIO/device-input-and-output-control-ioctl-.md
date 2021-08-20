---
description: A função DeviceIoControl fornece uma interface de controle de entrada e saída de dispositivo (IOCTL) por meio da qual um aplicativo pode se comunicar diretamente com um driver de dispositivo.
ms.assetid: 2dffd86a-162c-4e09-bfa1-73b87522741a
title: Controle de entrada e saída do dispositivo (IOCTL)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f5885ad3eb327e9c2df07977c7a1e16cbc962a9466b019ce8e14cbb3a3a82b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118004614"
---
# <a name="device-input-and-output-control-ioctl"></a>Controle de entrada e saída do dispositivo (IOCTL)

A função [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) fornece uma interface de controle de entrada e saída de dispositivo (IOCTL) por meio da qual um aplicativo pode se comunicar diretamente com um driver de dispositivo. A função **DeviceIoControl** é uma interface de finalidade geral que pode enviar códigos de controle para uma variedade de dispositivos. Cada código de controle representa uma operação para o driver executar. Por exemplo, um código de controle pode solicitar que um driver de dispositivo retorne informações sobre o dispositivo correspondente ou direcione o driver para executar uma ação no dispositivo, como a formatação de um disco.

Vários códigos de controle padrão são definidos nos arquivos de cabeçalho do SDK. Além disso, os drivers de dispositivo podem definir seus próprios códigos de controle específicos do dispositivo. Para obter uma lista de códigos de controle padrão incluídos na documentação do SDK, consulte a seção comentários de [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol).

Os tipos de códigos de controle que você pode especificar dependem do dispositivo que está sendo acessado e da plataforma na qual seu aplicativo está sendo executado. Os aplicativos podem usar os códigos de controle padrão ou códigos de controle específicos do dispositivo para executar operações de entrada e saída diretas em uma unidade de disquete, unidade de disco rígido, unidade de fita ou unidade de CD-ROM.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Chamando DeviceIoControl](calling-deviceiocontrol.md)
</dt> </dl>

 

 
