---
title: Revisitando regras de agregação com com extensões ADSI
description: Veja a seguir uma breve revisão das regras de agregação COM e de extensão de ADSI.
ms.assetid: 3efcdfcf-4965-4436-90b2-dc0f627c71b4
ms.tgt_platform: multiple
keywords:
- Extensões ADSI, regras de agregação COM
- ADSI de agregação COM
- Revisitando regras de agregação com com extensões ADSI ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e9b3e3614c4adc225883f120f8fbf362df3e646
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103641839"
---
# <a name="revisiting-com-aggregation-rules-with-adsi-extensions"></a>Revisitando regras de agregação com com extensões ADSI

Veja a seguir uma breve revisão das regras de agregação COM e de extensão de ADSI.

-   O método **CreateInstance** retorna um ponteiro para uma interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) , como a seguir, que não Delega nenhuma chamada de função para o agregador.

    O método [**IUnknown:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) retorna ponteiros para as interfaces às quais ele dá suporte e erros de interfaces para as quais não dá suporte.

    O método [**IUnknown:: AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) incrementa a contagem de referência no próprio objeto de extensão agregado.

    O método [**IUnkown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) decrementa a contagem de referência no próprio objeto de extensão agregado e se destrói quando a contagem de referência é 0.

-   O objeto de extensão deve armazenar o ponteiro [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) do agregador, como m \_ pOuterUnknown, durante a implementação do método **CreateInstance** .
-   Todas as interfaces às quais o objeto de extensão dá suporte, incluindo [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension), devem herdar de [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), o que delega todas as chamadas de função de volta para o agregador.
    -   [**IUnknown:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) chama "m \_ POuterUnknown->QueryInterface"
    -   [**IUnknown:: AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) chama "m \_ POuterUnknown->AddRef"
    -   [**IUnkown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) chama "m \_ pOuterUnknown-versão de >"

Os gravadores de extensão podem escolher qualquer implementação interna que prefiram, desde que obedeçam às regras padrão de agregação COM. Lembre-se de que um objeto de extensão não precisa funcionar como um objeto autônomo. As extensões são projetadas para funcionar como agregações. No entanto, uma extensão pode ser gravada para funcionar como um objeto autônomo e como uma agregação.

Além do suporte à agregação Standard COM, um objeto de extensão pode dar suporte a [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension) para recursos mais avançados. Se a associação tardia tiver suporte, a extensão deverá:

-   Delega funções para [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) de volta para o agregador.
-   Implemente a interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) em [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension).

 

 