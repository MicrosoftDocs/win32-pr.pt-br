---
title: Versões de DRM
description: Versões de DRM
ms.assetid: ac802547-a3cc-4b30-a8e6-62b679326486
keywords:
- SDK do Windows Media Format, versões do DRM
- DRM (gerenciamento de direitos digitais), versões
- DRM (gerenciamento de direitos digitais), versões
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be792554e553ccc35dbec71d40ff304af76fafd0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916129"
---
# <a name="drm-versions"></a>Versões de DRM

Há várias versões do DRM (gerenciamento de direitos digitais) do Windows Media. A versão 1 do DRM é muitas vezes separada das outras versões nesta documentação, pois ela é implementada usando técnicas que são diferentes das versões posteriores. A segunda geração do Windows Media DRM é chamada de DRM versão 7 porque foi introduzida como parte do SDK do Windows Media Format 7. Às vezes, ele é chamado de DRM versão 2. As versões posteriores do Windows Media DRM, DRM versão 9 e o novo Windows Media DRM 10, são extensões do DRM versão 7 e usam os mesmos procedimentos para implementação. Todas as versões do Windows Media DRM usam as mesmas rotinas de criptografia; as diferenças entre as versões têm a ver com os recursos de licença.

Ao criar arquivos protegidos usando os objetos do Windows Media Format SDK, você deve dar suporte tanto à versão 1 quanto à versão mais recente. Os arquivos protegidos pela versão 1 do DRM diferem dos arquivos protegidos por versões posteriores apenas no conteúdo do cabeçalho. Os arquivos mais recentes que contêm as informações adicionais de cabeçalho ainda podem ser usados em clientes que processam apenas conteúdo da versão 1. Embora as versões posteriores do DRM ofereçam um nível mais alto de segurança e recursos adicionais, ainda há muitos players que usam apenas a versão 1.

Para obter mais informações sobre versões de DRM, consulte a documentação do SDK do Windows Media Rights Manager.

> [!Note]  
> O DRM não é compatível com a versão baseada em x64 deste SDK.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Recursos de Rights Management digital**](digital-rights-management-features.md)
</dt> <dt>

[**Habilitando o suporte a DRM**](enabling-drm-support.md)
</dt> </dl>

 

 




