---
title: Proteção de DRM e distribuição de licença de conteúdo
description: Proteção de DRM e distribuição de licença de conteúdo
ms.assetid: 147fef8c-7298-450d-a1a9-345c03c49bec
keywords:
- SDK do Windows Media Format, proteção de conteúdo do DRM
- SDK do Windows Media Format, licenças DRM
- ASF (Advanced Systems Format), proteção de conteúdo de DRM
- ASF (formato de sistemas avançados), proteção de conteúdo de DRM
- ASF (Advanced Systems Format), distribuição de licença do DRM
- ASF (formato de sistemas avançados), distribuição de licença do DRM
- DRM (gerenciamento de direitos digitais), proteção de conteúdo
- DRM (gerenciamento de direitos digitais), proteção de conteúdo
- DRM (gerenciamento de direitos digitais), distribuição de licenças
- DRM (gerenciamento de direitos digitais), distribuição de licenças
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25af13947828885d70f3e0fd9fe8bf035eb8c5e5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292830"
---
# <a name="drm-protection-and-content-license-distribution"></a>Proteção de DRM e distribuição de licença de conteúdo

No lado da criação, a tecnologia de gerenciamento de direitos digitais envolve dois processos principais: (1) proteger o conteúdo e (2) fornecer licenças para o conteúdo. A proteção de um arquivo envolve basicamente a criptografia do conteúdo e a inclusão de uma URL no cabeçalho do arquivo que especifica onde uma licença para o conteúdo pode ser obtida. Se você quiser proteger arquivos com o e, em seguida, distribuir os arquivos para outros computadores ou dispositivos, poderá usar o SDK do Windows Media Format ou o SDK do Windows Media Rights Manager para proteger o arquivo. Para cenários de DRM ao vivo, você deve usar o Windows Media Format SDK para proteger o conteúdo conforme ele está sendo codificado.

Para criar e emitir licenças para conteúdo protegido, você pode criar sua própria solução personalizada usando os objetos do SDK do Windows Media Rights Manager ou pode usar um serviço executado por terceiros.

Seja qual for o método usado, os arquivos protegidos que você criar conterão, no objeto de cabeçalho DRM, uma URL que informa aos aplicativos cliente onde obter uma licença para o conteúdo.

> [!Note]  
> O Windows Media Format SDK não oferece suporte para a criação ou a emissão de licenças.

 

No lado da reprodução, um aplicativo habilitado para DRM deve ser capaz de obter licenças para conteúdo protegido, descriptografar o conteúdo usando a chave contida na licença e impor as restrições de licença, como o número de vezes que um arquivo pode ser reproduzido ou se o arquivo pode ser copiado para outro dispositivo. O SDK do Windows Media Format fornece todo o suporte necessário para criar um aplicativo de reprodução de DRM totalmente habilitado.

> [!Note]  
> O DRM não é compatível com a versão baseada em x64 deste SDK.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Recursos de Rights Management digital**](digital-rights-management-features.md)
</dt> <dt>

[**Habilitando o suporte a DRM**](enabling-drm-support.md)
</dt> </dl>

 

 




