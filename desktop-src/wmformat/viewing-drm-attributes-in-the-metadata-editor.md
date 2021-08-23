---
title: Exibindo atributos DRM no Editor de Metadados
description: Exibindo atributos DRM no Editor de Metadados
ms.assetid: e25fb8c8-8f4d-40fd-aa6f-675921e0ccdd
keywords:
- Windows SDK de Formato de Mídia, exibição de atributo DRM
- DRM (gerenciamento de direitos digitais), exibição de atributo
- DRM (gerenciamento de direitos digitais), exibição de atributo
- Windows SDK de Formato de Mídia, Editor de Metadados
- DRM (gerenciamento de direitos digitais), Editor de Metadados
- DRM (gerenciamento de direitos digitais), Editor de Metadados
- Windows SDK de Formato de Mídia, interface IWMDRMEditor
- DRM (gerenciamento de direitos digitais), interface IWMDRMEditor
- DRM (gerenciamento de direitos digitais), interface IWMDRMEditor
- Editor de Metadados, exibição de atributo DRM
- Editor de Metadados, interface IWMDRMEditor
- IWMDRMEditor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 129f20457f2e359584e6c37eee499b902988f95c0993cf5cd31a85b81d60d162
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119584816"
---
# <a name="viewing-drm-attributes-in-the-metadata-editor"></a>Exibindo atributos DRM no Editor de Metadados

O Editor de Metadados expõe a interface IWMDRMEditor, que permite que os aplicativos de edição examinem determinados atributos de um header DRM em um arquivo ASF protegido e atributos na licença de conteúdo, se um estiver presente, mesmo que o aplicativo não tenha a biblioteca estática específica do DRM (wmstubdrm.lib) necessária para aplicativos de player e de autor drm totalmente habilitados.

> [!Note]  
> O DRM não é suportado pela versão baseada em x64 deste SDK.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Recursos Rights Management digital**](digital-rights-management-features.md)
</dt> <dt>

[**IWMDRMEditor Interface**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmeditor)
</dt> </dl>

 

 




