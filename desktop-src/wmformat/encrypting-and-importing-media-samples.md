---
title: Criptografando e importando amostras de mídia
description: Criptografando e importando amostras de mídia
ms.assetid: f9784c9a-c672-432d-a3ad-eb2ed73ac523
keywords:
- SDK do Windows Media Format, importação de DRM
- SDK do Windows Media Format, importar
- SDK do Windows Media Format, criptografando amostras de mídia
- DRM (gerenciamento de direitos digitais), importar
- DRM (gerenciamento de direitos digitais), importar
- DRM (gerenciamento de direitos digitais), criptografia de amostras de mídia
- DRM (gerenciamento de direitos digitais), criptografia de amostras de mídia
- APIs estendidas do cliente DRM, importar
- APIs estendidas do cliente, importar
- APIs estendidas do cliente DRM, criptografando amostras de mídia
- APIs estendidas do cliente, criptografando amostras de mídia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 473db9580990b62818842aaa5eeea3e82f38c5ad
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104365556"
---
# <a name="encrypting-and-importing-media-samples"></a>Criptografando e importando amostras de mídia

Para cada exemplo de mídia criptografada usando o DRM do Windows Media, você deve gerar um valor salt que seja estritamente maior do que o anterior (monotônico aumentando). Use o novo valor de Salt para criar uma chave de criptografia transitória aplicando o algoritmo de criptografia SHA-1 ao vetor de inicialização concatenado com o valor de Salt.

Em seguida, criptografe o exemplo de acordo com o algoritmo RC4 usando a chave transitória gerada. Antes que o exemplo seja passado para o SDK, seu aplicativo deve associar o valor de Salt ao exemplo definindo um atributo de extensão.

Aqui estão as etapas para criptografar amostras de mídia:

1.  Chame o método **QueryInterface** do objeto de exemplo para obter a interface [**INSSBuffer3**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3) .
2.  Incrementar o valor de Salt.
3.  Criptografe o exemplo usando um algoritmo de criptografia RC1. Para a criptografia, você cria uma chave concatenando o vetor de inicialização e o valor de Salt.
4.  Forneça o valor de Salt para o SDK chamando [**INSSBuffer:: SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Importação de DRM**](drm-import.md)
</dt> <dt>

[**Exemplo de criptografia de exemplo de mídia**](media-sample-encryption-example.md)
</dt> </dl>

 

 




