---
title: Criando arquivos protegidos
description: Criando arquivos protegidos
ms.assetid: 5237e797-72ec-402e-81ec-ab379747e464
keywords:
- SDK do Windows Media Format, criando arquivos protegidos
- SDK do Windows Media Format, arquivos protegidos
- ASF (Advanced Systems Format), criando arquivos protegidos
- ASF (formato de sistemas avançados), criando arquivos protegidos
- ASF (Advanced Systems Format), arquivos protegidos
- ASF (formato de sistemas avançados), arquivos protegidos
- ASF (Advanced Systems Format), WMStubDRM. lib
- ASF (formato de sistemas avançados), WMStubDRM. lib
- WMStubDRM. lib, criando arquivos protegidos
- WMStubDRM. lib, arquivos protegidos
- DRM (gerenciamento de direitos digitais), WMStubDRM. lib
- DRM (gerenciamento de direitos digitais), WMStubDRM. lib
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 160a14d96da924bdb2a307bc804514a1ec3de083
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104293768"
---
# <a name="creating-protected-files"></a>Criando arquivos protegidos

Para criar arquivos de mídia digital protegidos usando o DRM versão 1 ou o DRM versões 7 e posteriores, vincule ao arquivo WMStubDRM. lib que você obteve da Microsoft e crie o objeto do gravador. Para a proteção da versão 1, use a interface [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) para definir os atributos DRM que você deseja aplicar. Para as versões 7 e posteriores, use os métodos de interface [**IWMDRMWriter**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmwriter) .

Os tópicos a seguir descrevem em detalhes como proteger arquivos.

-   [Protegendo arquivos com DRM versão 1](protecting-files-with-drm-version-1.md)
-   [Protegendo arquivos com DRM versão 7 ou posterior](protecting-files-with-drm-version-7-or-later.md)

> [!Note]  
> O DRM não é compatível com a versão baseada em x64 deste SDK.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Lista de atributos DRM**](drm-attribute-list.md)
</dt> <dt>

[**Propriedades de DRM**](drm-properties.md)
</dt> <dt>

[**Versões de DRM**](drm-versions.md)
</dt> <dt>

[**Habilitando o suporte a DRM**](enabling-drm-support.md)
</dt> <dt>

[**Obtendo a biblioteca de DRM necessária**](obtaining-the-required-drm-library.md)
</dt> <dt>

[**Lendo arquivos protegidos**](reading-protected-files.md)
</dt> </dl>

 

 




