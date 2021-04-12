---
title: Sobre a API de acesso do dispositivo
description: A API de acesso ao dispositivo é para desenvolvedores de C++ que estão criando um aplicativo da Windows Store para interagir com dispositivos especializados no Windows 8.
ms.assetid: DDF115A2-A811-450A-80F7-AAFB0EEA4037
ms.topic: article
ms.date: 02/11/2020
ms.openlocfilehash: 213c7ecc618e4b183ee879d23db3b2c0eca35397
ms.sourcegitcommit: 3d718d8f69d3f86eaecf94c5705d761c5a9ef4a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/20/2020
ms.locfileid: "104294591"
---
# <a name="about-the-device-access-api"></a>Sobre a API de acesso do dispositivo

A API de acesso ao dispositivo é para desenvolvedores de C++ que estão criando um aplicativo da Windows Store para interagir com dispositivos especializados no Windows 8. Este tópico descreve os cenários aos quais a API de acesso ao dispositivo se aplica. Ele também explica como a API de acesso ao dispositivo aplica regras de segurança para aplicativos da Windows Store no Windows 8.

- [Habilitando a funcionalidade de dispositivo personalizada em aplicativos de dispositivo da Windows Store](#enabling-custom-device-functionality-in-windows-store-device-apps)

## <a name="enabling-custom-device-functionality-in-windows-store-device-apps"></a>Habilitando a funcionalidade de dispositivo personalizada em aplicativos de dispositivo da Windows Store

Os desenvolvedores de IHVs (fornecedores independentes de hardware) e OEMs podem criar um aplicativo da Windows Store emparelhado com seu dispositivo e adquirido automaticamente quando o dispositivo é instalado. Esse aplicativo, conhecido como um aplicativo de dispositivo da Windows Store, pode fornecer funcionalidade de dispositivo exclusiva.

Dispositivos que não têm drivers de classe interna ou APIs de Windows Runtime para se comunicar com o dispositivo no Windows 8 são conhecidos como *dispositivos especializados*. Esses dispositivos podem exigir um driver personalizado. Para obter mais informações sobre os tipos de dispositivos que exigem drivers personalizados, consulte o guia de design de aplicativo do dispositivo Windows Store para dispositivos especializados.

O aplicativo de dispositivo da Windows Store para um dispositivo especializado que deve se comunicar com o driver personalizado de um dispositivo não pode usar as APIs do Microsoft Win32 como [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) e [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) para enviar os IOCTLs para o dispositivo. O ambiente de segurança restrito em que os aplicativos de dispositivo da Windows Store são executados requer que você use a API de acesso do dispositivo para se comunicar com o driver personalizado de um aplicativo da Windows Store.

O desenvolvedor de um dispositivo personalizado restringe o acesso a aplicativos aprovados e com privilégios. Por exemplo, o fabricante de um dispositivo de player de mídia pode querer que os usuários reproduzam música somente por meio do aplicativo de música fornecido por IHV e restrinjam o aplicativo de qualquer concorrente de sincronizar mídia do dispositivo. Ao criar o driver de dispositivo, você define uma propriedade no arquivo de informações (INF) para especificar que somente aplicativos privilegiados podem acessar o dispositivo. Os metadados no próprio dispositivo especificam as IDs do pacote para o conjunto de aplicativos aprovados. Consulte [aplicativos de dispositivo UWP para dispositivos internos](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices) para obter mais detalhes sobre o processo de configuração desses metadados em seu dispositivo.

## <a name="related-topics"></a>Tópicos relacionados

[Exemplo de acesso de driver personalizado](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Custom%20driver%20access%20sample), [aplicativos de dispositivo UWP para dispositivos internos](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices), [centro de desenvolvimento de hardware](/windows-hardware/drivers/)