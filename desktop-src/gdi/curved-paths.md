---
description: Caminhos curvos
ms.assetid: 1ee9e6c6-5f8d-4727-b5f9-4b179c5371f1
title: Caminhos curvos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fe27e20d7c5c3f59ea4bd38b46049088ae9d409
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827667"
---
# <a name="curved-paths"></a>Caminhos curvos

Um aplicativo pode mesclar as curvas em um caminho chamando a função [**FlattenPath**](/windows/desktop/api/Wingdi/nf-wingdi-flattenpath) . Essa função é especialmente útil para aplicativos que se ajustam ao texto na delimitação de um caminho que contém curvas. Para ajustar o texto, o aplicativo deve executar as seguintes etapas:

1.  Crie o caminho onde o texto é exibido.
2.  Chame a função [**FlattenPath**](/windows/desktop/api/Wingdi/nf-wingdi-flattenpath) para converter as curvas em um caminho em segmentos de linha.
3.  Chame a função [**GetPath**](/windows/desktop/api/Wingdi/nf-wingdi-getpath) para recuperar esses segmentos de linha.
4.  Calcule o comprimento de cada linha e a largura de cada caractere na cadeia de caracteres.
5.  Use dados de largura de linha e largura de caractere para posicionar cada caractere ao longo da curva.

 

 



