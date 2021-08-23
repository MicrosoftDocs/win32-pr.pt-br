---
title: Criando arquivos protegidos
description: Criando arquivos protegidos
ms.assetid: 5237e797-72ec-402e-81ec-ab379747e464
keywords:
- Windows SDK do formato de mídia, criando arquivos protegidos
- Windows SDK do formato de mídia, arquivos protegidos
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
ms.openlocfilehash: a5be729f04f67e1a2e4319bcc8d267c798942293c2df2ee97dcc6a559af612aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119809466"
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

 

 




