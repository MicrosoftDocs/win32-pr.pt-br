---
title: Estruturas de cliente DRM do Microsoft Windows Media
description: Estruturas de cliente DRM do Microsoft Windows Media
ms.assetid: 794de1b7-d60c-435e-9f77-c4df109b5372
keywords:
- SDK do Windows Media Format, estruturas
- DRM (gerenciamento de direitos digitais), estruturas
- DRM (gerenciamento de direitos digitais), estruturas
- APIs estendidas do cliente DRM, estruturas
- APIs estendidas do cliente, estruturas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43264c37ed9830026f87998823017d17c9d75f7e
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104369076"
---
# <a name="microsoft-windows-media-drm-client-structures"></a>Estruturas de cliente DRM do Microsoft Windows Media

As estruturas a seguir têm suporte das APIs estendidas do cliente DRM do Windows Media.



| Estrutura ou enumeração                                                                    | Descrição                                                                                                                                                 |
|---------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_IDs de \_ proteção de saída de áudio DRM \_ \_**](drm-audio-output-protection-ids.md)              | Contém uma lista de identificadores de proteção de saída de áudio.                                                                                                     |
| [**\_IDs de proteção de saída de áudio DRM \_ \_ \_ \_ ex**](drm-audio-output-protection-ids-ex.md)       | Contém uma lista de identificadores de proteção de saída de áudio. Essa estrutura estende **as \_ \_ IDs de \_ proteção \_ de saída de áudio DRM** adicionando um número de versão.          |
| [**\_OPL de cópia DRM \_**](drmdrm-copy-opl.md)                                                   | Contém informações sobre os níveis de proteção de saída especificados em uma licença para ações de cópia.                                                               |
| [**\_dados de \_ estado da licença DRM \_**](drmdrm-license-state-data.md)                              | Contém informações sobre as restrições de licença para um direito de DRM.                                                                                        |
| [**\_níveis mínimos de \_ proteção de saída \_ \_ do DRM**](drmdrm-minimum-output-protection-levels.md) | Mantém os níveis mínimos de proteção de saída (OPLs) para reprodução de vários tipos de conteúdo.                                                                 |
| [**\_IDs de \_ saída \_ OPL DRM**](drmdrm-opl-output-ids.md)                                      | Mantém um número de identificadores de saída OPL.                                                                                                                   |
| [**\_proteção de saída DRM \_**](drm-output-protection.md)                                    | Contém informações sobre uma tecnologia de proteção de saída.                                                                                                    |
| [**\_proteção de saída DRM \_ \_ ex**](drm-output-protection-ex.md)                             | Contém informações sobre uma tecnologia de proteção de saída. Essa estrutura estende **a \_ \_ proteção de saída DRM** adicionando um número de versão.                     |
| [**\_OPL de reprodução DRM \_**](drmdrm-play-opl.md)                                                   | Contém informações sobre o OPLs especificado em uma licença para ações de reprodução.                                                                                   |
| [**execução do DRM \_ \_ OPL \_ ex**](drm-play-opl-ex.md)                                               | Contém informações estendidas sobre o OPLs especificado em uma licença para ações de reprodução.                                                                          |
| [**\_IDs de \_ proteção de saída de vídeo DRM \_ \_**](drmdrm-video-output-protection-ids.md)           | Mantém uma matriz de estruturas de **\_ proteção de \_ saída \_ de vídeo DRM** .                                                                                            |
| [**\_IDs de proteção de saída de vídeo DRM \_ \_ \_ \_ ex**](drm-video-output-protection-ids-ex.md)       | Mantém uma matriz de estruturas de **\_ proteção de \_ saída \_ de vídeo DRM** . Essa estrutura estende **as \_ \_ IDs da \_ proteção \_ de saída de vídeo DRM** adicionando um número de versão. |
| [**\_status de \_ restauração de backup do WM \_**](wm-backup-restore-status.md)                             | Contém informações sobre uma operação de backup ou restauração de licença pendente.                                                                                      |
| [**o \_ status individual do WM \_**](drmwm-individualize-status.md)                             | Contém informações sobre um processo de individualização pendente.                                                                                                |
| [**\_restrições de \_ vídeo \_ analógico WMDRM**](wmdrm-analog-video-restrictions.md)               | Contém informações sobre uma restrição para reproduzir conteúdo como vídeo analógico.                                                                             |
| [**\_restrições de \_ vídeo analógico WMDRM \_ \_ ex**](wmdrm-analog-video-restrictions-ex.md)        | Contém informações estendidas sobre uma restrição para reproduzir conteúdo como vídeo analógico.                                                                    |
| [**\_bloco de \_ dispersão de criptografia WMDRM \_**](wmdrm-encrypt-scatter-block.md)                       | Contém um bloco de dados a serem criptografados.                                                                                                                   |
| [**\_informações de \_ dispersão de criptografia WMDRM \_**](wmdrm-encrypt-scatter-info.md)                         | Contém as informações necessárias para configurar a interface [**IWMDRMEncryptScatter**](iwmdrmencryptscatter.md) para uso.                                        |
| [**\_filtro de licença do WMDRM \_**](wmdrm-license-filter.md)                                      | Contém informações de filtragem para a criação de enumerações de licenças.                                                                                           |
| [**\_níveis de \_ proteção de saída do WMDRM \_**](wmdrm-output-protection-levels.md)                 | Contém os níveis de proteção de saída exigidos por uma licença para executar várias ações.                                                                    |
| [**WMDRMCryptoData**](wmdrmcryptodata.md)                                                  | Contém informações sobre o algoritmo criptográfico usado para criptografar e descriptografar conteúdo.                                                                 |
| [**política de WMDRMNET \_**](wmdrmnet-policy.md)                                                 | Contém a política a ser usada para operações do Windows Media DRM para dispositivos de rede.                                                                        |
| [**\_ \_ requisitos globais da política de WMDRMNET \_**](wmdrmnet-policy-global-requirements.md)       | Mantém requisitos globais para o Windows Media DRM para dispositivos de rede.                                                                                        |
| [**\_ \_ ambiente mínimo da política de WMDRMNET \_**](wmdrmnet-policy-minimum-environment.md)       | Contém os requisitos mínimos de segurança para o Windows Media DRM para dispositivos de rede.                                                                       |
| [**política de WMDRMNET \_ \_ TRANSCRYPTPLAY**](wmdrmnet-policy-transcryptplay.md)                  | Mantém as informações de política para reproduzir conteúdo usando o Windows Media DRM para dispositivos de rede.                                                               |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Referência de programação**](drm-programming-reference.md)
</dt> </dl>

 

 




