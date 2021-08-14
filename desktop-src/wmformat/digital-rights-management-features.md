---
title: Recursos Rights Management dados digitais
description: Recursos Rights Management dados digitais
ms.assetid: c3c1e59f-8ff9-496c-8e63-0c1cf4ce7092
keywords:
- Windows SDK de Formato de Mídia, recursos de DRM
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
# <a name="digital-rights-management-features"></a>Recursos Rights Management dados digitais

\[O Windows drm de mídia de mídia foi preterido e não deve ser usado. Use [Microsoft PlayReady](/windows/uwp/audio-video-camera/playready-client-sdk) em vez disso.\]

O DRM (gerenciamento de direitos digitais) é uma tecnologia que os proprietários de conteúdo podem usar para proteger arquivos de mídia digital criptografando-os com uma chave (um trecho de dados que bloqueia e desbloqueia o conteúdo). Para reproduzir um arquivo ASF protegido, um consumidor deve obter uma licença separada que contenha a chave. Cada licença também contém direitos, determinados pelo proprietário do conteúdo ou pelo emissor da licença, que especificam como o consumidor pode usar o arquivo. Usando a tecnologia DRM, os proprietários de conteúdo podem fornecer músicas, vídeos e outros arquivos de mídia digital pela Internet em um formato de arquivo protegido e controlar o uso de seu conteúdo digital. A tecnologia DRM da Microsoft também é suportada pelo Windows Media Rights Manager, pelo codificador de mídia Windows e Windows Media Player. Para obter mais informações sobre a tecnologia drm da Microsoft, consulte o [site microsoft Windows Media](https://support.microsoft.com/help/17946/windows-media).

> [!Note]  
> O DRM não é suportado pela versão baseada em x64 deste SDK.

 

As seções a seguir discutem os principais recursos relacionados ao DRM do SDK Windows Formato de Mídia.



| Seção                                                                                            | Descrição                                                                                                                          |
|----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [Noções básicas sobre DRM](drm-basics.md)                                                                       | Fornece uma breve visão geral da funcionalidade drm fornecida pelo SDK Windows Formato de Mídia.                                         |
| [Versões do DRM](drm-versions.md)                                                                   | Descreve as principais diferenças entre as versões da proteção drm disponível para aplicativos.                                     |
| [DRM ao vivo](live-drm.md)                                                                           | Descreve os cenários possibilitados pela proteção de DRM "em tempo real".                                                                |
| [Individualização de DRM](drm-individualization.md)                                                 | Descreve a atualização de segurança do aplicativo que os proprietários de conteúdo drm ou os emissores de licença podem exigir.                                   |
| [Fazer o back-up e a restauração de licenças DRM](backing-up-and-restoring-of-drm-licenses.md)           | Descreve os prós e contras de permitir que os usuários fazer backup e restaurar suas licenças de conteúdo.                                       |
| [Exibindo atributos DRM no Editor de Metadados](viewing-drm-attributes-in-the-metadata-editor.md) | Descreve os recursos desse objeto auxiliar drm e os cenários para os que ele foi projetado para dar suporte.                                   |
| [Níveis de proteção de saída](output-protection-levels.md)                                           | Descreve como os Níveis de Proteção de Saída torna as licenças drm versão 10 mais flexíveis.                                                   |
| [Revogação de licença](license-revocation.md)                                                       | Descreve a revogação de licença.                                                                                                        |
| [Windows DRM de mídia 10 para dispositivos de rede](windows-media-drm-10-for-network-devices.md)           | Apresenta Windows DRM de Mídia 10 para Dispositivos de Rede e sua implementação neste SDK.                                              |
| [Caminho de áudio seguro da Microsoft](microsoft-secure-audio-path--deprecated.md)                         | Descreve a arquitetura do Caminho de Áudio Seguro da Microsoft, que fornece o mais alto grau de proteção para conteúdo de áudio protegido. |
| [Gravação de playlist](playlist-burning.md)                                                           | Descreve o recurso de gravação de playlist do DRM e como ele tem suporte no SDK Windows Formato de Mídia.                               |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Habilitando o suporte a DRM**](enabling-drm-support.md)
</dt> <dt>

[**Recursos**](features.md)
</dt> </dl>

 

 