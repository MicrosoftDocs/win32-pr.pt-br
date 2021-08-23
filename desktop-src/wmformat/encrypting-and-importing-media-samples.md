---
title: Criptografando e importando amostras de mídia
description: Criptografando e importando amostras de mídia
ms.assetid: f9784c9a-c672-432d-a3ad-eb2ed73ac523
keywords:
- Windows SDK de formato de mídia, importação de DRM
- Windows SDK do formato de mídia, importar
- Windows SDK de formato de mídia, criptografando amostras de mídia
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
ms.openlocfilehash: 5ed604fc114feed6bd308b9a89c6bde6d6c96abeb9e88a7b9ace19d553de1596
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119658836"
---
# <a name="encrypting-and-importing-media-samples"></a>Criptografando e importando amostras de mídia

para cada amostra de mídia que você criptografa usando Windows DRM de mídia, você deve gerar um valor salt que seja estritamente maior do que o anterior (monotônico aumentando). Use o novo valor de Salt para criar uma chave de criptografia transitória aplicando o algoritmo de criptografia SHA-1 ao vetor de inicialização concatenado com o valor de Salt.

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

 

 




