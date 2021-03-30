---
title: Recursos de Rights Management digital
description: Recursos de Rights Management digital
ms.assetid: c3c1e59f-8ff9-496c-8e63-0c1cf4ce7092
keywords:
- SDK do Windows Media Format, recursos do DRM
- DRM (gerenciamento de direitos digitais), recursos
- DRM (gerenciamento de direitos digitais), recursos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bd9c30b350fdf430d5b20bbe112c5309ac9da4f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641277"
---
# <a name="digital-rights-management-features"></a>Recursos de Rights Management digital

\[O recurso DRM do Windows Media foi preterido e não deve ser usado. Em vez disso, use [o Microsoft PlayReady](/windows/uwp/audio-video-camera/playready-client-sdk) .\]

O DRM (gerenciamento de direitos digitais) é uma tecnologia que os proprietários de conteúdo podem usar para proteger arquivos de mídia digital criptografando-os com uma chave (um dado que bloqueia e desbloqueia o conteúdo). Para reproduzir um arquivo ASF protegido, um consumidor deve obter uma licença separada que contém a chave. Cada licença também contém direitos, determinados pelo proprietário do conteúdo ou pelo emissor da licença, que especificam como o consumidor pode usar o arquivo. Usando a tecnologia DRM, os proprietários de conteúdo podem entregar músicas, vídeos e outros arquivos de mídia digital pela Internet em um formato de arquivo protegido e controlar o uso de seu conteúdo digital. A tecnologia Microsoft DRM também tem suporte do Windows Media Rights Manager, do Windows Media Encoder e do Windows Media Player. Para obter mais informações básicas sobre a tecnologia DRM da Microsoft, consulte o [site do Microsoft Windows Media](https://support.microsoft.com/help/17946/windows-media).

> [!Note]  
> O DRM não é compatível com a versão baseada em x64 deste SDK.

 

As seções a seguir discutem os principais recursos relacionados ao DRM do SDK do Windows Media Format.



| Seção                                                                                            | Descrição                                                                                                                          |
|----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [Noções básicas de DRM](drm-basics.md)                                                                       | Fornece uma breve visão geral da funcionalidade DRM fornecida pelo Windows Media Format SDK.                                         |
| [Versões de DRM](drm-versions.md)                                                                   | Descreve as principais diferenças entre as versões de proteção de DRM disponíveis para aplicativos.                                     |
| [DRM ao vivo](live-drm.md)                                                                           | Descreve os cenários possibilitados pela proteção de DRM "em tempo real".                                                                |
| [Individualização de DRM](drm-individualization.md)                                                 | Descreve a atualização de segurança do aplicativo que os proprietários de conteúdo do DRM ou os emissores de licença podem exigir.                                   |
| [Fazendo backup e restaurando licenças DRM](backing-up-and-restoring-of-drm-licenses.md)           | Descreve os prós e contras de permitir que os usuários façam backup e restaure suas licenças de conteúdo.                                       |
| [Exibindo atributos DRM no editor de metadados](viewing-drm-attributes-in-the-metadata-editor.md) | Descreve os recursos desse objeto auxiliar DRM e os cenários para os quais ele foi projetado para dar suporte.                                   |
| [Níveis de proteção de saída](output-protection-levels.md)                                           | Descreve como os níveis de proteção de saída tornam as licenças do DRM versão 10 mais flexíveis.                                                   |
| [Revogação de licença](license-revocation.md)                                                       | Descreve a revogação de licenças.                                                                                                        |
| [Windows Media DRM 10 para dispositivos de rede](windows-media-drm-10-for-network-devices.md)           | Apresenta o Windows Media DRM 10 para dispositivos de rede e sua implementação neste SDK.                                              |
| [Caminho de áudio seguro da Microsoft](microsoft-secure-audio-path--deprecated.md)                         | Descreve a arquitetura de caminho de áudio seguro da Microsoft, que fornece o nível mais alto de proteção para conteúdo de áudio protegido. |
| [Gravação de playlist](playlist-burning.md)                                                           | Descreve o recurso de gravação de playlist do DRM e como ele tem suporte no Windows Media Format SDK.                               |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Habilitando o suporte a DRM**](enabling-drm-support.md)
</dt> <dt>

[**Recursos**](features.md)
</dt> </dl>

 

 