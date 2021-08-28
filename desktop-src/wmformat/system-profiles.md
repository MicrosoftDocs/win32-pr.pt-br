---
title: Perfis do sistema
description: Perfis do sistema
ms.assetid: 5f687aae-cf9b-4b2d-a3aa-d130b443fbf3
keywords:
- Windows SDK de Formato de Mídia, perfis do sistema
- FORMATO DE SISTEMAS Avançados (ASF), perfis do sistema
- ASF (Formato de Sistemas Avançados), perfis do sistema
- Windows SDK de Formato de Mídia, IDs de perfil
- ASF (Advanced Systems Format), IDs de perfil
- ASF (Formato de Sistemas Avançados), IDs de perfil
- perfis do sistema, lista de
- IDs de perfil
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6389f82e93a0b27c079bd75ded9eb7d35d78a380ab72d244c5443c07f4c9ed5e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807736"
---
# <a name="system-profiles"></a>Perfis do sistema

A tabela a seguir contém a lista completa de perfis de sistema com suporte. Cada perfil listado tem um nome e uma ID de perfil. A ID do perfil é uma constante definida como o valor guid atribuído ao perfil do sistema. Para usar as IDs de perfil do sistema em seu código, você deve incluir wmsysprf.h em seu aplicativo. Para exemplos que mostram como carregar um perfil do sistema, consulte [Para carregar um perfil do sistema.](to-load-a-system-profile.md)

> [!IMPORTANT]
> Os perfis listados abaixo usam a versão 8 Windows áudio de mídia e Windows codecs de vídeo de mídia. Não há perfis de sistema predefinidos que usam os codecs Windows Media 9 Series. Você pode criar seu próprio perfil Windows Media 9 Series usando um perfil da versão 8 como ponto de partida. Para obter mais informações, consulte [Reutiling Stream Configurations](reusing-stream-configurations.md).

 



| Nome do perfil                                                                      | ID do perfil                     | Descrição                                                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows Vídeo de mídia 8 para PCs de carteira de cores (225 Kbps)                             | WMProfile \_ V80 \_ 255VideoPDA    | Use esse perfil ao criar arquivos de vídeo para reprodução em PCs de pocket de cores mais rápidas.                                                                                 |
| Windows Vídeo de mídia 8 para PCs de carteira de cores (150 Kbps)                             | WMProfile \_ V80 \_ 150VideoPDA    | Use esse perfil ao criar arquivos de vídeo para reprodução na maioria dos PCs do Pocket.                                                                                         |
| Windows Vídeo de mídia 8 para modems discados ou ISDN de canal único (28,8 a 56 Kbps) | WMProfile \_ V80 \_ 28856VideoMBR  | Use esse perfil de taxa de vários bits para públicos-alvo com modems discados ou conexões ISDN de canal único (a largura de banda está entre 28,8 Kbps e 56 Kbps).        |
| Windows Vídeo de mídia 8 para LAN, Modem de Cabo ou xDSL (100 a 768 Kbps)             | WMProfile \_ V80 \_ 100768VideoMBR | Use esse perfil de taxa de bits múltipla para públicos-alvo com conexões ISDN, LAN, modem de cabo ou xDSL de canal duplo (a largura de banda está entre 100 Kbps e 500 Kbps). |
| Windows Vídeo de mídia 8 para modems discado ou LAN (28,8 a 100 Kbps)                | WMProfile \_ V80 \_ 288100VideoMBR | Use esse perfil de taxa de bits múltipla para públicos-alvo com conexões ISDN de modem discado, LAN ou canal duplo (a largura de banda está entre 28,8 e 100 Kbps).         |
| Windows Vídeo de mídia 8 para modems discado (28,8 Kbps)                              | WMProfile \_ V80 \_ 288Video       | Use esse perfil para entrega de áudio/vídeo de baixa taxa de bits em conexões discadas de 28,8 Kbps.                                                                          |
| Windows Vídeo de mídia 8 para modems discado (56 Kbps)                                | WMProfile \_ V80 \_ 56Video        | Use esse perfil para distribuição de áudio/vídeo de baixa taxa de bits em mais de 56 Kbps de conexões discadas.                                                                            |
| Windows Vídeo de mídia 8 para rede local (100 Kbps)                           | WMProfile \_ V80 \_ 100Video       | Use esse perfil para entrega de taxa de bits média em conexões ISDN, LAN ou modem de cabo de canal duplo.                                                              |
| Windows Vídeo de mídia 8 para rede de área local (256 Kbps)                           | WMProfile \_ V80 \_ 256Video       | Use esse perfil para conteúdo de áudio/vídeo de alta qualidade destinado à reprodução local ou para download e reprodução.                                                     |
| Windows Vídeo de mídia 8 para rede de área local (384 Kbps)                           | WMProfile \_ V80 \_ 384Video       | Use esse perfil para conteúdo de áudio/vídeo de alta qualidade destinado à reprodução local ou para download e reprodução.                                                     |
| Windows Vídeo de mídia 8 para rede de área local (768 Kbps)                           | WMProfile \_ V80 \_ 768Video       | Use esse perfil para conteúdo de áudio/vídeo de alta qualidade destinado à reprodução local ou para download e reprodução.                                                     |
| Windows Vídeo de mídia 8 para banda larga (NTSC, 700 Kbps)                              | WMProfile \_ V80 \_ 700NTSCVideo   | Use esse perfil para conteúdo de áudio/vídeo de alta qualidade destinado à reprodução local, download e reprodução.                                                         |
| Windows Vídeo de mídia 8 para banda larga (NTSC, 1400 Kbps)                             | WMProfile \_ V80 \_ 1400NTSCVideo  | Use esse perfil para conteúdo de áudio/vídeo de alta qualidade destinado à reprodução local ou para download e reprodução.                                                     |
| Windows Vídeo de mídia 8 para banda larga (PAL, 384 Kbps)                               | WMProfile \_ V80 \_ 384PALVideo    | Use esse perfil para conteúdo de áudio/vídeo de alta qualidade destinado à reprodução local ou para download e reprodução.                                                     |
| Windows Vídeo de mídia 8 para banda larga (PAL, 700 Kbps)                               | WMProfile \_ V80 \_ 700PALVideo    | Use esse perfil para conteúdo de áudio/vídeo de alta qualidade destinado à reprodução local ou para download e reprodução.                                                     |
| Windows Áudio de mídia 8 para modem discado (Mono, 28,8 Kbps)                         | WMProfile \_ V80 \_ 288MonoAudio   | Use esse perfil para conteúdo de rádio e música (somente áudio).                                                                                                          |
| Windows Áudio de mídia 8 para modem discado (Fm Radio Estéreo, 28,8 Kbps)              | WMProfile \_ V80 \_ 288StereoAudio | Use esse perfil para conteúdo de rádio e música (somente áudio).                                                                                                          |
| Windows Áudio de mídia 8 para modem discado (32 Kbps)                                 | WMProfile \_ V80 \_ 32StereoAudio  | Use esse perfil para conteúdo de rádio e música (somente áudio).                                                                                                          |
| Windows Áudio de mídia 8 para modem discado (qualidade próxima da CD, 48 Kbps)                | WMProfile \_ V80 \_ 48StereoAudio  | Use para rádio, música e conteúdo de áudio de uso geral.                                                                                                            |
| Windows Áudio de mídia 8 para modem discado (qualidade de CD, 64 Kbps)                     | WMProfile \_ V80 \_ 64StereoAudio  | Use esse perfil para públicos-alvo com conexões de Internet ou LAN de alta velocidade.                                                                                  |
| Windows Áudio de mídia 8 para ISDN (melhor que a qualidade de CD, 96 Kbps)                  | WMProfile \_ V80 \_ 96StereoAudio  | Use esse perfil para públicos-alvo com conexões de Internet ou LAN de alta velocidade.                                                                                  |
| Windows Áudio de mídia 8 para ISDN (melhor que a qualidade de CD, 128 Kbps)                 | WMProfile \_ V80 \_ 128StereoAudio | Use esse perfil para públicos-alvo com conexões de Internet ou LAN de alta velocidade.                                                                                  |
| Windows Vídeo de mídia 8 para modem discado (sem áudio, 28,8 Kbps)                     | WMProfile \_ V80 \_ 288VideoOnly   | Use esse perfil ao criar conteúdo somente vídeo para públicos-alvo com modems discado.                                                                         |
| Windows Vídeo de mídia 8 para modem discado (sem áudio, 56 Kbps)                       | WMProfile \_ V80 \_ 56VideoOnly    | Use esse perfil ao criar conteúdo somente vídeo para públicos-alvo com modems discado.                                                                         |
| Windows VBR baseado em Qualidade Justa da Mídia 8 para banda larga                              | WMProfile \_ V80 \_ FAIRVBRVideo   | Perfil baseado em qualidade justa para conteúdo VBR restrito à qualidade.                                                                                     |
| Windows Mídia 8 VBR baseada em Alta Qualidade para Banda Larga.                             | WMProfile \_ V80 \_ HIGHVBRVideo   | Perfil baseado em alta qualidade para conteúdo VBR com restrição de qualidade.                                                                                     |
| Windows Mídia 8 VBR baseada em melhor qualidade para banda larga.                             | WMProfile \_ V80 \_ BESTVBRVideo   | Perfil baseado em melhor qualidade para conteúdo VBR com restrição de qualidade.                                                                                             |



 

Os perfis do sistema estão disponíveis localizados para idiomas diferentes do inglês. Para obter mais informações, consulte [Perfis de sistema localizados.](localized-system-profiles.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IWMProfileManager::LoadProfileByID**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-loadprofilebyid)
</dt> <dt>

[**IWMProfileManager2 Interface**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager2)
</dt> <dt>

[**Trabalhando com perfis**](working-with-profiles.md)
</dt> </dl>

 

 




