---
title: Ações e direitos
description: Ações e direitos
ms.assetid: 711c6a04-6c40-4ea5-8c4f-91d000286b7b
keywords:
- Windows SDK do formato de mídia, DRM (gerenciamento de direitos digitais)
- Windows SDK do formato de mídia, licenças DRM
- Windows SDK do formato de mídia, licenças para DRM
- DRM (gerenciamento de direitos digitais), ações
- DRM (gerenciamento de direitos digitais), ações
- DRM (gerenciamento de direitos digitais), direitos
- DRM (gerenciamento de direitos digitais), direitos
- DRM (gerenciamento de direitos digitais), licenças
- DRM (gerenciamento de direitos digitais), licenças
- licenças, DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b822c0350af12c5e266570a031ca0d3eda7c99b4b8451b751786a60a4a0908d6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089766"
---
# <a name="actions-and-rights"></a>Ações e direitos

quando um arquivo é protegido usando Windows Media DRM, seu uso é completamente restrito. As licenças podem ser emitidas para permitir que um usuário use o conteúdo de maneiras específicas. Cada modo no qual um usuário pode usar o conteúdo é descrito por uma ação. Por exemplo, reproduzir um arquivo em um computador é uma ação.

Uma licença que habilita uma determinada ação é considerada para conceder um direito. Por exemplo, uma licença pode conceder o direito de reproduzir conteúdo em um computador.

Ações e direitos referem-se às mesmas maneiras de usar o conteúdo. A diferença é que a ação refere-se ao uso enquanto a direita se refere à permissão. apesar dessa distinção, a ação de palavras e a direita costumam ser usadas de forma intercambiável nesta documentação e em outros documentos que descrevem Windows DRM de mídia.

as ações governadas por Windows direitos de DRM de mídia estão listadas na seção [constantes de direitos](rights-constants.md) desta documentação.

determinados métodos das APIs estendidas do cliente drm de mídia Windows usam constantes diferentes para se referir aos direitos de DRM básicos. Por exemplo, o método [**IWMDRMLicenseQuery:: QueryLicenseState**](iwmdrmlicensequery-querylicensestate.md) usa um conjunto de cadeias de caracteres específicas para Estados de licença. Mesmo que essas constantes estejam definindo cadeias de caracteres diferentes das constantes de direitos básicas, elas se referem aos mesmos direitos na licença.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Conceitos**](drmconcepts.md)
</dt> </dl>

 

 




