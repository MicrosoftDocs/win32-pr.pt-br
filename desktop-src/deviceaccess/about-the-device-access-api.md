---
title: Sobre o API de Acesso a Dispositivo
description: O API de Acesso a Dispositivo é para desenvolvedores C++ que estão criando um aplicativo Windows Store para interagir com dispositivos especializados no Windows 8.
ms.assetid: DDF115A2-A811-450A-80F7-AAFB0EEA4037
ms.topic: article
ms.date: 02/11/2020
ms.openlocfilehash: 08d603e74ff33250bbc5a65e440fc47a0103cd6eb996badf94dbdc51b6b2d3e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119755016"
---
# <a name="about-the-device-access-api"></a>Sobre o API de Acesso a Dispositivo

O API de Acesso a Dispositivo é para desenvolvedores C++ que estão criando um aplicativo Windows Store para interagir com dispositivos especializados no Windows 8. Este tópico descreve os cenários aos API de Acesso a Dispositivo se aplica. Ele também explica como o API de Acesso a Dispositivo aplica regras de segurança para aplicativos Windows Store no Windows 8.

- [Habilitando a funcionalidade personalizada do dispositivo Windows aplicativos de dispositivo da Store](#enabling-custom-device-functionality-in-windows-store-device-apps)

## <a name="enabling-custom-device-functionality-in-windows-store-device-apps"></a>Habilitando a funcionalidade personalizada do dispositivo Windows aplicativos de dispositivo da Store

Os desenvolvedores de IHVs (fornecedores independentes de hardware) e OEMs podem criar um aplicativo da Windows Store emparelhado com seu dispositivo e adquirido automaticamente quando o dispositivo é instalado. Esse aplicativo, conhecido como um aplicativo de dispositivo Windows Store, pode fornecer funcionalidade de dispositivo exclusiva.

Dispositivos que não têm drivers de classe ou APIs de runtime Windows para se comunicar com o dispositivo no Windows 8 são conhecidos como *dispositivos especializados.* Esses dispositivos podem exigir um driver personalizado. Para obter mais informações sobre os tipos de dispositivos que exigem drivers personalizados, consulte o guia de design do aplicativo de dispositivo Windows Store para dispositivos especializados.

O aplicativo de dispositivo Windows Store para um dispositivo especializado que deve se comunicar com o driver personalizado de um dispositivo não pode usar APIs do Microsoft Win32 como [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) e [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) para enviar IOCTLs para o dispositivo. O ambiente de segurança restrito em que Windows aplicativos de dispositivo da Store são executados exige que você use o API de Acesso a Dispositivo para se comunicar com o driver personalizado de um aplicativo Windows Store.

O desenvolvedor de um dispositivo personalizado restringe o acesso a aplicativos aprovados e privilegiados. Por exemplo, o fabricante de um dispositivo de player de mídia pode querer que os usuários reproduzam música somente por meio do aplicativo de música fornecido por IHV e restrinjam o aplicativo de qualquer concorrente de sincronizar mídia do dispositivo. Quando estiver criando o driver de dispositivo, você definirá uma propriedade no arquivo INF (informações) para especificar que somente aplicativos privilegiados podem acessar o dispositivo. Os metadados no próprio dispositivo especificam as IDs do pacote para o conjunto de aplicativos aprovados. Consulte [Aplicativos de dispositivo UWP para dispositivos](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices) internos para obter mais detalhes sobre o processo de configuração desses metadados em seu dispositivo.

## <a name="related-topics"></a>Tópicos relacionados

[Exemplo de acesso de driver personalizado,](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Custom%20driver%20access%20sample)aplicativos de dispositivo [UWP para dispositivos internos,](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices) [Centro de Desenvolvimento de Hardware](/windows-hardware/drivers/)