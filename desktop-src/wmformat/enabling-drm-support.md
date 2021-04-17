---
title: Habilitando o suporte a DRM
description: Habilitando o suporte a DRM
ms.assetid: 90e92373-7fc2-4478-a179-22f22dbc3a3d
keywords:
- SDK do Windows Media Format, habilitando o suporte a DRM
- ASF (Advanced Systems Format), habilitando o suporte a DRM
- ASF (formato de sistemas avançados), habilitando o suporte a DRM
- DRM (gerenciamento de direitos digitais), habilitando o suporte
- DRM (gerenciamento de direitos digitais), habilitando o suporte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 936210eb9d560bffe12acf5cc33fb9f864f8404c
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/09/2020
ms.locfileid: "105811423"
---
# <a name="enabling-drm-support"></a>Habilitando o suporte a DRM

Você pode usar o SDK (Software Development Kit) do Microsoft Windows Media Format para criar aplicativos que podem aplicar a proteção DRM (gerenciamento de direitos digitais) e reproduzir fluxos DRM ao vivo ou arquivos protegidos por DRM. O suporte também é fornecido para fazer backup e restaurar as licenças DRM de um player e para [*individualizar*](wmformat-glossary.md) os jogadores.

Esta documentação pressupõe que você tenha uma familiaridade básica com a tecnologia de gerenciamento de direitos digitais da Microsoft. Uma visão geral básica do DRM do Windows Media é fornecida na seção [recursos de Rights Management digital](digital-rights-management-features.md) desta documentação. Para obter mais informações sobre DRM, consulte a página de Rights Management digital no [site da Microsoft](https://windows.microsoft.com/windows/products/windows-media).

> [!Note]  
> O DRM não é compatível com a versão baseada em x64 deste SDK.

 

As seções a seguir descrevem como habilitar o suporte a DRM.



| Seção                                                                                                                        | Descrição                                                                                                                                                                                     |
|--------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Obtendo a biblioteca de DRM necessária](obtaining-the-required-drm-library.md)                                                   | Descreve as etapas envolvidas na obtenção da biblioteca estática que é necessária para criar aplicativos habilitados para DRM.                                                                               |
| [Proteção de DRM e distribuição de licença de conteúdo](drm-protection-and-content-license-distribution.md)                         | Compara os recursos de DRM do SDK do Windows Media Format com o SDK do Windows Media Rights Manager.                                                                                        |
| [Operações de rede DRM](drm-network-operations.md)                                                                           | Descreve como seu aplicativo deve lidar com as operações de DRM que se comunicam pela Internet ou por outras redes.                                                                          |
| [Criando arquivos protegidos](creating-protected-files.md)                                                                       | Descreve como criar arquivos protegidos por DRM.                                                                                                                                                    |
| [Lendo arquivos protegidos](reading-protected-files.md)                                                                         | Descreve maneiras de adquirir licenças para conteúdo e os benefícios de implementar a aquisição de licença silenciosa.                                                                                     |
| [Exibindo atributos de arquivos protegidos](viewing-attributes-of-protected-files.md)                                             | Descreve como usar a interface [**IWMDRMEditor**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmeditor) no objeto editor de metadados para exibir atributos de arquivos protegidos sem ter a biblioteca estática necessária para DRM. |
| [Trabalhando com listas de revogação](working-with-revocation-lists.md)                                                             | Descreve as listas de revogação e como elas são implementadas.                                                                                                                                        |
| [Fazendo backup e restaurando licenças](backing-up-and-restoring-licenses.md)                                                     | Descreve como os usuários podem gerenciar suas licenças de conteúdo fazendo backup e restaurando-as em seu computador atual ou em outros computadores.                                                         |
| [Individualizando aplicativos DRM](individualizing-drm-applications.md)                                                       | Descreve como o recurso de [*individualização*](wmformat-glossary.md) aumenta a segurança em um sistema DRM.                                                           |
| [Trabalhando com níveis de proteção de saída](working-with-output-protection-levels.md)                                             | Descreve como dar suporte a níveis de proteção de saída, que são usados para registrar ações permitidas em licenças do DRM versão 10.                                                                         |
| [Usando o protocolo Windows Media DRM 10 para dispositivos de rede](using-the-windows-media-drm-10-for-network-devices-protocol.md) | Descreve como dar suporte ao streaming de dispositivo seguro usando o protocolo Windows Media DRM 10 para dispositivos de rede.                                                                                |
| [Implementando a revogação de licenças](implementing-license-revocation.md)                                                         | Descreve o processo de revogação de licenças e as ações que seu aplicativo deve executar para implementá-lo.                                                                                        |
| [Gravar playlists que contêm arquivos seguros](burning-playlists-that-contain-secure-files.md)                                 | Descreve como implementar a gravação de playlist em seu aplicativo.                                                                                                                                |



 

O SDK inclui vários aplicativos de exemplo que demonstram como ler arquivos protegidos; o exemplo mais completo é DRMShow. Para obter mais informações, consulte [aplicativos de exemplo](sample-applications.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Recursos**](features.md)
</dt> </dl>

 

 




