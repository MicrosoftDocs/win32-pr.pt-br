---
title: Ações e direitos
description: Ações e direitos
ms.assetid: 711c6a04-6c40-4ea5-8c4f-91d000286b7b
keywords:
- SDK do Windows Media Format, DRM (gerenciamento de direitos digitais)
- SDK do Windows Media Format, licenças DRM
- SDK do Windows Media Format, licenças para DRM
- DRM (gerenciamento de direitos digitais), ações
- DRM (gerenciamento de direitos digitais), ações
- DRM (gerenciamento de direitos digitais), direitos
- DRM (gerenciamento de direitos digitais), direitos
- DRM (gerenciamento de direitos digitais), licenças
- DRM (gerenciamento de direitos digitais), licenças
- licenças, DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1d044850bb5ee73e804065c67840362ec0b7b0d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104004986"
---
# <a name="actions-and-rights"></a>Ações e direitos

Quando um arquivo é protegido usando o Windows Media DRM, seu uso é completamente restrito. As licenças podem ser emitidas para permitir que um usuário use o conteúdo de maneiras específicas. Cada modo no qual um usuário pode usar o conteúdo é descrito por uma ação. Por exemplo, reproduzir um arquivo em um computador é uma ação.

Uma licença que habilita uma determinada ação é considerada para conceder um direito. Por exemplo, uma licença pode conceder o direito de reproduzir conteúdo em um computador.

Ações e direitos referem-se às mesmas maneiras de usar o conteúdo. A diferença é que a ação refere-se ao uso enquanto a direita se refere à permissão. Apesar dessa distinção, a ação de palavras e a direita costumam ser usadas de forma intercambiável nesta documentação e em outros documentos que descrevem o DRM do Windows Media.

As ações governadas pelos direitos de DRM do Windows Media são listadas na seção [constantes de direitos](rights-constants.md) desta documentação.

Determinados métodos das APIs estendidas do cliente DRM do Windows Media usam constantes diferentes para se referir aos direitos de DRM básicos. Por exemplo, o método [**IWMDRMLicenseQuery:: QueryLicenseState**](iwmdrmlicensequery-querylicensestate.md) usa um conjunto de cadeias de caracteres específicas para Estados de licença. Mesmo que essas constantes estejam definindo cadeias de caracteres diferentes das constantes de direitos básicas, elas se referem aos mesmos direitos na licença.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Conceitos**](drmconcepts.md)
</dt> </dl>

 

 




