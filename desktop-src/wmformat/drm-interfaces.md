---
title: Interfaces de cliente DRM do Microsoft Windows Media
description: Interfaces de cliente DRM do Microsoft Windows Media
ms.assetid: 27bbc33f-8102-4db2-bbc6-1a1da92bac80
keywords:
- SDK do Windows Media Format, interfaces
- DRM (gerenciamento de direitos digitais), interfaces
- DRM (gerenciamento de direitos digitais), interfaces
- APIs estendidas do cliente DRM, interfaces
- APIs estendidas do cliente, interfaces
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b4e259ef5b8ef410db072a7f942d139f682bc90
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104369077"
---
# <a name="microsoft-windows-media-drm-client-interfaces"></a>Interfaces de cliente DRM do Microsoft Windows Media

A tabela a seguir descreve as interfaces compatíveis com as APIs de cliente DRM do Windows Media.



| Interface                                                                    | Descrição                                                                                                     |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [**IDRMStatusCallback**](idrmstatuscallback.md)                             | Fornece a definição para um retorno de chamada de status que você pode implementar para lidar com operações DRM assíncronas.     |
| [**IWMDRMDecrypt**](iwmdrmdecrypt.md)                                       | Fornece um método para descriptografar o conteúdo.                                                                       |
| [**IWMDRMEncrypt**](iwmdrmencrypt.md)                                       | Fornece um método para criptografar dados no local.                                                                 |
| [**IWMDRMEncryptScatter**](iwmdrmencryptscatter.md)                         | Criptografa dados de blocos não contíguos.                                                                       |
| [**IWMDRMEventGenerator**](iwmdrmeventgenerator.md)                         | Extensão da interface **IMFMediaEventGenerator** que fornece um método para cancelar operações assíncronas. |
| [**IWMDRMIndividualizationStatus**](iwmdrmindividualizationstatus.md)       | Permite a recuperação de informações de status avançadas sobre o progresso da individualização.                       |
| [**IWMDRMLicense**](iwmdrmlicense.md)                                       | Representa uma ou mais licenças no repositório de licenças local.                                                     |
| [**IWMDRMLicenseBackupRestoreStatus**](iwmdrmlicensebackuprestorestatus.md) | Permite a recuperação de informações de status detalhadas sobre uma operação de backup ou restauração de licença.                   |
| [**IWMDRMLicenseManagement**](iwmdrmlicensemanagement.md)                   | Habilita operações de gerenciamento para o armazenamento de licença local.                                                      |
| [**IWMDRMLicenseManagement**](iwmdrmlicensemanagement.md)                   | Fornece opções de gerenciamento adicionais para o armazenamento de licença local.                                             |
| [**IWMDRMLicenseQuery**](iwmdrmlicensequery.md)                             | Permite que os aplicativos consultem os direitos e o estado da licença de um arquivo protegido.                                |
| [**IWMDRMNetReceiver**](iwmdrmnetreceiver.md)                               | Fornece métodos necessários para criar um aplicativo de receptor de Microsoft Windows Media DRM para dispositivos de rede.          |
| [**IWMDRMNetTransmitter**](iwmdrmnettransmitter.md)                         | Fornece métodos necessários para criar um aplicativo Microsoft Windows Media DRM para dispositivos de rede transmissor.       |
| [**IWMDRMNonSilentLicenseAquisition**](iwmdrmnonsilentlicenseaquisition.md) | Fornece métodos que habilitam a aquisição de licenças com a intervenção do usuário.                                        |
| [**IWMDRMProvider**](iwmdrmprovider.md)                                     | Cria os outros objetos das APIs estendidas do Microsoft Windows Media DRM Client.                              |
| [**IWMDRMSecurity**](iwmdrmsecurity.md)                                     | Gerencia vários processos relacionados à segurança para o computador cliente e o subsistema DRM.                           |
| [**IWMDRMSecurity**](iwmdrmsecurity.md)                                     | Gerencia a revogação e a renovação de componentes.                                                                       |
| [**IWMSecureBuffer**](iwmsecurebuffer.md)                                   | Habilita criptografia e descriptografia de buffers.                                                                   |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Referência de programação**](drm-programming-reference.md)
</dt> </dl>

 

 




