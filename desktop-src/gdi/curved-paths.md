---
description: Caminhos curvos
ms.assetid: 1ee9e6c6-5f8d-4727-b5f9-4b179c5371f1
title: Caminhos curvos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b58018b7ef95b30c5ae2751ed963caefee7b9313ca86a8c6a2a4fee246908f8b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119849176"
---
# <a name="curved-paths"></a>Caminhos curvos

Um aplicativo pode mesclar as curvas em um caminho chamando a função [**FlattenPath**](/windows/desktop/api/Wingdi/nf-wingdi-flattenpath) . Essa função é especialmente útil para aplicativos que se ajustam ao texto na delimitação de um caminho que contém curvas. Para ajustar o texto, o aplicativo deve executar as seguintes etapas:

1.  Crie o caminho onde o texto é exibido.
2.  Chame a função [**FlattenPath**](/windows/desktop/api/Wingdi/nf-wingdi-flattenpath) para converter as curvas em um caminho em segmentos de linha.
3.  Chame a função [**GetPath**](/windows/desktop/api/Wingdi/nf-wingdi-getpath) para recuperar esses segmentos de linha.
4.  Calcule o comprimento de cada linha e a largura de cada caractere na cadeia de caracteres.
5.  Use dados de largura de linha e largura de caractere para posicionar cada caractere ao longo da curva.

 

 



