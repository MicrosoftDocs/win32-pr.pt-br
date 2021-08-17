---
title: Proteção drm e distribuição de licença de conteúdo
description: Proteção drm e distribuição de licença de conteúdo
ms.assetid: 147fef8c-7298-450d-a1a9-345c03c49bec
keywords:
- Windows SDK de Formato de Mídia, proteção de conteúdo drm
- Windows SDK de Formato de Mídia, licenças DRM
- ASF (Advanced Systems Format), proteção de conteúdo DRM
- ASF (Formato de Sistemas Avançados), proteção de conteúdo drm
- ASF (Advanced Systems Format), distribuição de licenças DRM
- ASF (Formato de Sistemas Avançados), distribuição de licença drm
- DRM (gerenciamento de direitos digitais), proteção de conteúdo
- DRM (gerenciamento de direitos digitais), proteção de conteúdo
- DRM (gerenciamento de direitos digitais), distribuição de licenças
- DRM (gerenciamento de direitos digitais), distribuição de licenças
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc2b0c666136d3713a0b725bfa9d8ff7dd25e84f3cc9d82fd3a97b66137e47d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118704310"
---
# <a name="drm-protection-and-content-license-distribution"></a>Proteção drm e distribuição de licença de conteúdo

No lado da criação, a tecnologia de gerenciamento de direitos digitais envolve dois processos principais: (1) proteger o conteúdo e (2) fornecer licenças para o conteúdo. A proteção de um arquivo basicamente envolve criptografar o conteúdo e incluir uma URL no título do arquivo que especifica onde uma licença para o conteúdo pode ser obtida. Se você quiser proteger arquivos com e distribuir os arquivos para outros computadores ou dispositivos, poderá usar o SDK de Formato de Mídia do Windows ou o SDK do Windows Media Rights Manager para proteger o arquivo. Para cenários de DRM dinâmico, você deve usar o SDK Windows Formato de Mídia para proteger o conteúdo conforme ele está sendo codificado.

Para criar e emitir licenças para conteúdo protegido, você pode criar sua própria solução personalizada usando os objetos do SDK do Windows Media Rights Manager ou pode usar um serviço executado por terceiros.

Independentemente do método usado, os arquivos protegidos que você criar conterão, no objeto de título DRM, uma URL que informa aos aplicativos cliente onde obter uma licença para o conteúdo.

> [!Note]  
> O Windows SDK de Formato de Mídia não dá suporte à criação ou à emissão de licenças.

 

No lado da reprodução, um aplicativo habilitado para DRM deve ser capaz de obter licenças para conteúdo protegido, descriptografar esse conteúdo usando a chave contida na licença e impor as restrições de licença, como o número de vezes que um arquivo pode ser reproduzido ou se o arquivo pode ser copiado para outro dispositivo. O Windows SDK de Formato de Mídia fornece todo o suporte necessário para criar um aplicativo de reprodução drm totalmente habilitado.

> [!Note]  
> O DRM não é suportado pela versão baseada em x64 deste SDK.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Recursos Rights Management dados digitais**](digital-rights-management-features.md)
</dt> <dt>

[**Habilitando o suporte a DRM**](enabling-drm-support.md)
</dt> </dl>

 

 




