---
title: Exibindo atributos de arquivos protegidos
description: Exibindo atributos de arquivos protegidos
ms.assetid: fbfa1a1b-afd0-4f61-86ae-488716e16355
keywords:
- Windows SDK do formato de mídia, exibindo atributos de arquivos protegidos
- Windows SDK do formato de mídia, atributos de arquivos protegidos
- Windows SDK do formato de mídia, arquivos protegidos
- ASF (Advanced Systems Format), exibindo atributos de arquivos protegidos
- ASF (formato de sistemas avançados), exibindo atributos de arquivos protegidos
- ASF (Advanced Systems Format), atributos de arquivos protegidos
- ASF (formato de sistemas avançados), atributos de arquivos protegidos
- ASF (Advanced Systems Format), arquivos protegidos
- ASF (formato de sistemas avançados), arquivos protegidos
- DRM (gerenciamento de direitos digitais), exibindo atributos de arquivos protegidos
- DRM (gerenciamento de direitos digitais), exibindo atributos de arquivos protegidos
- DRM (gerenciamento de direitos digitais), atributos de arquivos protegidos
- DRM (gerenciamento de direitos digitais), atributos de arquivos protegidos
- DRM (gerenciamento de direitos digitais), arquivos protegidos
- DRM (gerenciamento de direitos digitais), arquivos protegidos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37cd09e61dbd5515d643cbffe8cce809d0f828e8d153858c78ee52db7e714344
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117844909"
---
# <a name="viewing-attributes-of-protected-files"></a>Exibindo atributos de arquivos protegidos

Em alguns cenários, talvez seja necessário recuperar determinados atributos DRM em um arquivo sem realmente acessar o conteúdo do arquivo. Esse recurso é útil, por exemplo, em aplicativos que processam lotes de arquivos de maneiras diferentes com base nas informações no cabeçalho do arquivo. nas versões anteriores do SDK do formato de mídia Windows, os aplicativos eram solicitados a vincular à biblioteca estática do DRM para abrir qualquer arquivo protegido. Os aplicativos que não têm a biblioteca DRM podem usar a interface [**IWMDRMEditor:: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmeditor-getdrmproperty) no objeto editor de metadados para examinar determinados atributos DRM.

> [!Note]  
> O DRM não é compatível com a versão baseada em x64 deste SDK.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Lista de atributos DRM**](drm-attribute-list.md)
</dt> <dt>

[**Habilitando o suporte a DRM**](enabling-drm-support.md)
</dt> <dt>

[**Interface IWMDRMEditor**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmeditor)
</dt> </dl>

 

 




