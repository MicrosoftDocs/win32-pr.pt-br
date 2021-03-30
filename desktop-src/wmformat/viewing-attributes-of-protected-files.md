---
title: Exibindo atributos de arquivos protegidos
description: Exibindo atributos de arquivos protegidos
ms.assetid: fbfa1a1b-afd0-4f61-86ae-488716e16355
keywords:
- SDK do Windows Media Format, exibindo atributos de arquivos protegidos
- SDK do Windows Media Format, atributos de arquivos protegidos
- SDK do Windows Media Format, arquivos protegidos
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
ms.openlocfilehash: 642e9f580c3dffa1d3785985d548a5f971cfc218
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103640120"
---
# <a name="viewing-attributes-of-protected-files"></a>Exibindo atributos de arquivos protegidos

Em alguns cenários, talvez seja necessário recuperar determinados atributos DRM em um arquivo sem realmente acessar o conteúdo do arquivo. Esse recurso é útil, por exemplo, em aplicativos que processam lotes de arquivos de maneiras diferentes com base nas informações no cabeçalho do arquivo. Nas versões anteriores do Windows Media Format SDK, eram necessários aplicativos para vincular à biblioteca estática do DRM a fim de abrir qualquer arquivo protegido. Os aplicativos que não têm a biblioteca DRM podem usar a interface [**IWMDRMEditor:: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmeditor-getdrmproperty) no objeto editor de metadados para examinar determinados atributos DRM.

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

 

 




