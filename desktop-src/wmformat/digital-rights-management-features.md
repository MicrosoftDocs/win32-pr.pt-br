---
title: Recursos de Rights Management digital
description: Recursos de Rights Management digital
ms.assetid: c3c1e59f-8ff9-496c-8e63-0c1cf4ce7092
keywords:
- Windows SDK do formato de mídia, recursos do DRM
- DRM (gerenciamento de direitos digitais), recursos
- DRM (gerenciamento de direitos digitais), recursos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e389efdbfd3edef3f3c881cab8482c8ed03b6bb09eb4a7773caa59b4b9b1ad4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118704865"
---
# <a name="digital-rights-management-features"></a>Recursos de Rights Management digital

\[o recurso DRM de mídia Windows foi preterido e não deve ser usado. em vez disso, Use [Microsoft PlayReady](/windows/uwp/audio-video-camera/playready-client-sdk) .\]

O DRM (gerenciamento de direitos digitais) é uma tecnologia que os proprietários de conteúdo podem usar para proteger arquivos de mídia digital criptografando-os com uma chave (um dado que bloqueia e desbloqueia o conteúdo). Para reproduzir um arquivo ASF protegido, um consumidor deve obter uma licença separada que contém a chave. Cada licença também contém direitos, determinados pelo proprietário do conteúdo ou pelo emissor da licença, que especificam como o consumidor pode usar o arquivo. Usando a tecnologia DRM, os proprietários de conteúdo podem entregar músicas, vídeos e outros arquivos de mídia digital pela Internet em um formato de arquivo protegido e controlar o uso de seu conteúdo digital. a tecnologia Microsoft DRM também é compatível com o Windows media rights Manager, o Windows o codificador de mídia e o Windows Media Player. para obter mais informações básicas sobre a tecnologia DRM da microsoft, consulte o [site da microsoft Windows Media](https://support.microsoft.com/help/17946/windows-media).

> [!Note]  
> O DRM não é compatível com a versão baseada em x64 deste SDK.

 

as seções a seguir discutem os principais recursos relacionados ao DRM do SDK do formato de mídia do Windows.



| Seção                                                                                            | Descrição                                                                                                                          |
|----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [Noções básicas de DRM](drm-basics.md)                                                                       | fornece uma breve visão geral da funcionalidade DRM fornecida pelo SDK do formato de mídia Windows.                                         |
| [Versões de DRM](drm-versions.md)                                                                   | Descreve as principais diferenças entre as versões de proteção de DRM disponíveis para aplicativos.                                     |
| [DRM ao vivo](live-drm.md)                                                                           | Descreve os cenários possibilitados pela proteção de DRM "em tempo real".                                                                |
| [Individualização de DRM](drm-individualization.md)                                                 | Descreve a atualização de segurança do aplicativo que os proprietários de conteúdo do DRM ou os emissores de licença podem exigir.                                   |
| [Fazendo backup e restaurando licenças DRM](backing-up-and-restoring-of-drm-licenses.md)           | Descreve os prós e contras de permitir que os usuários façam backup e restaure suas licenças de conteúdo.                                       |
| [Exibindo atributos DRM no editor de metadados](viewing-drm-attributes-in-the-metadata-editor.md) | Descreve os recursos desse objeto auxiliar DRM e os cenários para os quais ele foi projetado para dar suporte.                                   |
| [Níveis de proteção de saída](output-protection-levels.md)                                           | Descreve como os níveis de proteção de saída tornam as licenças do DRM versão 10 mais flexíveis.                                                   |
| [Revogação de licença](license-revocation.md)                                                       | Descreve a revogação de licenças.                                                                                                        |
| [Windows Mídia DRM 10 para dispositivos de rede](windows-media-drm-10-for-network-devices.md)           | apresenta Windows mídia DRM 10 para dispositivos de rede e sua implementação neste SDK.                                              |
| [Caminho de áudio seguro da Microsoft](microsoft-secure-audio-path--deprecated.md)                         | Descreve a arquitetura de caminho de áudio seguro da Microsoft, que fornece o nível mais alto de proteção para conteúdo de áudio protegido. |
| [Gravação de playlist](playlist-burning.md)                                                           | descreve o recurso de gravação de playlist do DRM e como ele tem suporte no SDK do formato de mídia Windows.                               |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Habilitando o suporte a DRM**](enabling-drm-support.md)
</dt> <dt>

[**Recursos**](features.md)
</dt> </dl>

 

 