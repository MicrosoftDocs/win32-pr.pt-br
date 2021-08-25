---
title: Habilitando o suporte a DRM
description: Habilitando o suporte a DRM
ms.assetid: 90e92373-7fc2-4478-a179-22f22dbc3a3d
keywords:
- Windows SDK de Formato de Mídia, habilitando o suporte a DRM
- ASF (Advanced Systems Format), habilitando o suporte a DRM
- ASF (Formato de Sistemas Avançados), habilitando o suporte a DRM
- DRM (gerenciamento de direitos digitais), habilitando o suporte
- DRM (gerenciamento de direitos digitais), habilitando o suporte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dca900089e93b9f2c149f1e349bdf5b91f88a7c3d549b5f54147839a8ed9296
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089746"
---
# <a name="enabling-drm-support"></a>Habilitando o suporte a DRM

Você pode usar o SDK (Microsoft Windows Media Format Software Development Kit) para criar aplicativos que podem aplicar a proteção drm (gerenciamento de direitos digitais) e reproduzir fluxos drm dinâmicos ou arquivos protegidos por DRM. O suporte também é fornecido para fazer o suporte e restaurar as licenças de DRM de um jogador e [*para individualizar os*](wmformat-glossary.md) jogadores.

Esta documentação presume que você tenha uma familiaridade básica com a tecnologia de gerenciamento de direitos digitais da Microsoft. Uma visão geral básica Windows DRM de Mídia digital é fornecida na seção [Recursos de Rights Management Digital](digital-rights-management-features.md) desta documentação. Para obter mais informações sobre DRM, consulte a página Rights Management digital no [site da Microsoft.](https://windows.microsoft.com/windows/products/windows-media)

> [!Note]  
> O DRM não é suportado pela versão baseada em x64 deste SDK.

 

As seções a seguir descrevem como habilitar o suporte a DRM.



| Seção                                                                                                                        | Descrição                                                                                                                                                                                     |
|--------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Obtendo a biblioteca DRM necessária](obtaining-the-required-drm-library.md)                                                   | Descreve as etapas envolvidas na obtenção da biblioteca estática necessária para criar aplicativos habilitados para DRM.                                                                               |
| [Proteção drm e distribuição de licença de conteúdo](drm-protection-and-content-license-distribution.md)                         | Compara as funcionalidades de DRM do SDK Windows Media Format com o SDK Windows Media Rights Manager.                                                                                        |
| [Operações de rede DRM](drm-network-operations.md)                                                                           | Descreve como seu aplicativo deve lidar com as operações de DRM que se comunicam pela Internet ou por outras redes.                                                                          |
| [Criando arquivos protegidos](creating-protected-files.md)                                                                       | Descreve como criar arquivos protegidos por DRM.                                                                                                                                                    |
| [Lendo arquivos protegidos](reading-protected-files.md)                                                                         | Descreve maneiras de adquirir licenças para conteúdo e os benefícios de implementar a aquisição silenciosa de licenças.                                                                                     |
| [Exibindo atributos de arquivos protegidos](viewing-attributes-of-protected-files.md)                                             | Descreve como usar a interface [**IWMDRMEditor**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmeditor) no objeto do editor de metadados para exibir atributos de arquivos protegidos sem ter a biblioteca estática necessária para DRM. |
| [Trabalhando com listas de revogação](working-with-revocation-lists.md)                                                             | Descreve as listas de revogação e como elas são implementadas.                                                                                                                                        |
| [Fazer o back-up e restaurar licenças](backing-up-and-restoring-licenses.md)                                                     | Descreve como os usuários podem gerenciar suas licenças de conteúdo ao fazer o back-up e restaurá-las no computador atual ou em outros computadores.                                                         |
| [Individualizando aplicativos DRM](individualizing-drm-applications.md)                                                       | Descreve como o recurso [*de individualização*](wmformat-glossary.md) aumenta a segurança em um sistema DRM.                                                           |
| [Trabalhando com níveis de proteção de saída](working-with-output-protection-levels.md)                                             | Descreve como dar suporte a Níveis de Proteção de Saída, que são usados para registrar ações permitidas em licenças drm versão 10.                                                                         |
| [Usando o Windows DRM de Mídia 10 para o Protocolo de Dispositivos de Rede](using-the-windows-media-drm-10-for-network-devices-protocol.md) | Descreve como dar suporte ao streaming de dispositivo seguro usando o protocolo WINDOWS Media DRM 10 para Dispositivos de Rede.                                                                                |
| [Implementando a revogação de licença](implementing-license-revocation.md)                                                         | Descreve o processo de revogação de licença e as ações que seu aplicativo deve executar para implementá-la.                                                                                        |
| [Gravar playlists que contêm arquivos seguros](burning-playlists-that-contain-secure-files.md)                                 | Descreve como implementar a gravação de playlist em seu aplicativo.                                                                                                                                |



 

O SDK inclui vários aplicativos de exemplo que demonstram como ler arquivos protegidos; o exemplo mais completo é DRMShow. Para obter mais informações, consulte [Aplicativos de exemplo](sample-applications.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Recursos**](features.md)
</dt> </dl>

 

 




