---
title: Opções de fábrica de classes
description: Opções de fábrica de classes
ms.assetid: e9e33e07-7628-4c5e-965d-e12a9c1d69c2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fab52ea11a0e7e20d10757eb8d6e86577afc35c
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103641882"
---
# <a name="class-factory-options"></a>Opções de fábrica de classes

Um controle ActiveX, em virtude de ser um objeto COM, deve ter um código de servidor associado que dê suporte à criação de controle por meio de [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) como um mínimo.

É opcional, não obrigatório, que esse objeto de classe também ofereça suporte a [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2) para o gerenciamento de licenciamento. Somente os fornecedores que se preocupam com o licenciamento precisam dar suporte ao mecanismo de licenciamento do COM. Em outras palavras, como **IClassFactory2** é a única maneira de alcançar o licenciamento de nível com, essa interface é necessária no objeto de classe para os controles que desejam ser licenciados.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Controles](controls.md)
</dt> </dl>

 

 