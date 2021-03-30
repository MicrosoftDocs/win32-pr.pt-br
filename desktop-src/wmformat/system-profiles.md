---
title: Perfis de sistema
description: Perfis de sistema
ms.assetid: 5f687aae-cf9b-4b2d-a3aa-d130b443fbf3
keywords:
- SDK do Windows Media Format, perfis do sistema
- ASF (Advanced Systems Format), perfis de sistema
- ASF (formato de sistemas avançados), perfis de sistema
- SDK do Windows Media Format, IDs de perfil
- ASF (Advanced Systems Format), IDs de perfil
- ASF (formato de sistemas avançados), IDs de perfil
- perfis de sistema, lista de
- IDs de perfil
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eeca66023e6de6aba9c07a6bcb84a73756e316a8
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103640167"
---
# <a name="system-profiles"></a>Perfis de sistema

A tabela a seguir contém a lista completa de perfis de sistema com suporte. Cada perfil listado tem um nome e uma ID de perfil. A ID do perfil é uma constante definida para o valor de GUID atribuído ao perfil do sistema. Para usar as IDs de perfil do sistema em seu código, você deve incluir wmsysprf. h em seu aplicativo. Para obter exemplos que mostram como carregar um perfil do sistema, consulte [para carregar um perfil do sistema](to-load-a-system-profile.md).

> [!IMPORTANT]
> Os perfis listados abaixo usam os codecs de vídeo da versão 8 do Windows Media e do Windows Media. Não há nenhum perfil de sistema predefinido que use os codecs da série Windows Media 9. Você pode criar seu próprio perfil do Windows Media 9 Series usando um perfil da versão 8 como um ponto de partida. Para obter mais informações, consulte [reutilizando configurações de fluxo](reusing-stream-configurations.md).

 



| Nome do perfil                                                                      | ID do perfil                     | Descrição                                                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows Media Video 8 para Pocket PCs coloridos (225 kbps)                             | WMProfile \_ V80 \_ 255VideoPDA    | Use esse perfil ao criar arquivos de vídeo para reprodução em Pocket PCs com cores mais rápidas.                                                                                 |
| Windows Media Video 8 para Pocket PCs coloridos (150 kbps)                             | WMProfile \_ V80 \_ 150VideoPDA    | Use esse perfil ao criar arquivos de vídeo para reprodução na maioria dos Pocket PCs.                                                                                         |
| Windows Media Video 8 para modems de conexão discada ou ISDN de canal único (28,8 a 56 Kbps) | WMProfile \_ V80 \_ 28856VideoMBR  | Use este perfil de taxa de bits múltipla para públicos-alvo com modems de conexão discada ou conexões ISDN de canal único (a largura de banda é entre 28,8 kbps e 56 Kbps).        |
| Windows Media Video 8 para LAN, modem para cabo ou xDSL (100 a 768 Kbps)             | WMProfile \_ V80 \_ 100768VideoMBR | Use este perfil de taxa de bits múltipla para públicos-alvo com conexões ISDN, LAN, cabo ou xDSL de canal duplo (a largura de banda é entre 100 kbps e 500 kbps). |
| Windows Media Video 8 para modems dial-up ou LAN (28,8 a 100 kbps)                | WMProfile \_ V80 \_ 288100VideoMBR | Use este perfil de taxa de bits múltipla para públicos-alvo com conexões dial-up, LAN ou ISDN de canal duplo (a largura de banda é entre 28,8 e 100 kbps).         |
| Windows Media Video 8 para modems de conexão discada (28,8 kbps)                              | WMProfile \_ V80 \_ 288Video       | Use este perfil para entrega de áudio/vídeo de taxa baixa em conexões discadas de 28,8 kbps.                                                                          |
| Windows Media Video 8 para modems de conexão discada (56 Kbps)                                | WMProfile \_ V80 \_ 56Video        | Use este perfil para entrega de áudio/vídeo de taxa baixa em conexões discadas de 56 Kbps.                                                                            |
| Windows Media Video 8 para rede local (100 kbps)                           | WMProfile \_ V80 \_ 100Video       | Use este perfil para entrega de taxa de bits média em conexões ISDN de canal duplo, LAN ou modem a cabo.                                                              |
| Windows Media Video 8 para rede local (256 kbps)                           | WMProfile \_ V80 \_ 256Video       | Use este perfil para conteúdo de áudio/vídeo de alta qualidade destinado à reprodução local ou para download e reprodução.                                                     |
| Windows Media Video 8 para rede local (384 kbps)                           | WMProfile \_ V80 \_ 384Video       | Use este perfil para conteúdo de áudio/vídeo de alta qualidade destinado à reprodução local ou para download e reprodução.                                                     |
| Windows Media Video 8 para rede local (768 Kbps)                           | WMProfile \_ V80 \_ 768Video       | Use este perfil para conteúdo de áudio/vídeo de alta qualidade destinado à reprodução local ou para download e reprodução.                                                     |
| Windows Media Video 8 para banda larga (NTSC, 700 Kbps)                              | WMProfile \_ V80 \_ 700NTSCVideo   | Use este perfil para conteúdo de áudio/vídeo de alta qualidade destinado à reprodução local ou download e reprodução.                                                         |
| Windows Media Video 8 para banda larga (NTSC, 1400 kbps)                             | WMProfile \_ V80 \_ 1400NTSCVideo  | Use este perfil para conteúdo de áudio/vídeo de alta qualidade destinado à reprodução local ou para download e reprodução.                                                     |
| Windows Media Video 8 para banda larga (PAL, 384 kbps)                               | WMProfile \_ V80 \_ 384PALVideo    | Use este perfil para conteúdo de áudio/vídeo de alta qualidade destinado à reprodução local ou para download e reprodução.                                                     |
| Windows Media Video 8 para banda larga (PAL, 700 Kbps)                               | WMProfile \_ V80 \_ 700PALVideo    | Use este perfil para conteúdo de áudio/vídeo de alta qualidade destinado à reprodução local ou para download e reprodução.                                                     |
| Windows Media Audio 8 para modem de conexão discada (mono, 28,8 kbps)                         | WMProfile \_ V80 \_ 288MonoAudio   | Use este perfil para conteúdo de rádio e música (somente áudio).                                                                                                          |
| Windows Media Audio 8 para modem dial-up (FM Radio estéreo, 28,8 kbps)              | WMProfile \_ V80 \_ 288StereoAudio | Use este perfil para conteúdo de rádio e música (somente áudio).                                                                                                          |
| Windows Media Audio 8 para modem de conexão discada (32 kbps)                                 | WMProfile \_ V80 \_ 32StereoAudio  | Use este perfil para conteúdo de rádio e música (somente áudio).                                                                                                          |
| Windows Media Audio 8 para modem dial-up (perto da qualidade do CD, 48 kbps)                | WMProfile \_ V80 \_ 48StereoAudio  | Use para o conteúdo de áudio de rádio, música e uso geral.                                                                                                            |
| Windows Media Audio 8 para modem de conexão discada (qualidade de CD, 64 Kbps)                     | WMProfile \_ V80 \_ 64StereoAudio  | Use esse perfil para públicos-alvo com conexões de Internet ou LAN de alta velocidade.                                                                                  |
| Windows Media Audio 8 para ISDN (melhor do que a qualidade do CD, 96 kbps)                  | WMProfile \_ V80 \_ 96StereoAudio  | Use esse perfil para públicos-alvo com conexões de Internet ou LAN de alta velocidade.                                                                                  |
| Windows Media Audio 8 para ISDN (melhor do que a qualidade do CD, 128 kbps)                 | WMProfile \_ V80 \_ 128StereoAudio | Use esse perfil para públicos-alvo com conexões de Internet ou LAN de alta velocidade.                                                                                  |
| Windows Media Video 8 para modem de conexão discada (sem áudio, 28,8 kbps)                     | WMProfile \_ V80 \_ 288VideoOnly   | Use esse perfil ao criar conteúdo somente de vídeo para públicos-alvo com modems de conexão discada.                                                                         |
| Windows Media Video 8 para modem de conexão discada (sem áudio, 56 Kbps)                       | WMProfile \_ V80 \_ 56VideoOnly    | Use esse perfil ao criar conteúdo somente de vídeo para públicos-alvo com modems de conexão discada.                                                                         |
| VBR com base na qualidade justa do Windows Media 8 para banda larga                              | WMProfile \_ V80 \_ FAIRVBRVideo   | Perfil com base em alta qualidade para o conteúdo de VBR, com restrição de qualidade.                                                                                     |
| VBR com base em alta qualidade do Windows Media 8 para banda larga.                             | WMProfile \_ V80 \_ HIGHVBRVideo   | Perfil com base na melhor qualidade para o conteúdo de VBR com limitação de qualidade.                                                                                     |
| Taxa de bits de alta qualidade baseada no Windows Media 8 para banda larga.                             | WMProfile \_ V80 \_ BESTVBRVideo   | Perfil com base na melhor qualidade para o conteúdo de VBR com restrição de qualidade.                                                                                             |



 

Os perfis de sistema estão disponíveis localizados para idiomas diferentes do inglês. Para obter mais informações, consulte [perfis de sistema localizados](localized-system-profiles.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IWMProfileManager::LoadProfileByID**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-loadprofilebyid)
</dt> <dt>

[**Interface IWMProfileManager2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager2)
</dt> <dt>

[**Trabalhando com perfis**](working-with-profiles.md)
</dt> </dl>

 

 




