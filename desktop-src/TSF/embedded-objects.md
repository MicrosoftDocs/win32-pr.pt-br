---
title: Objetos inseridos (estrutura de serviços de texto)
description: A estrutura de serviços de texto permite que um serviço de texto incorpore objetos em um fluxo de texto de aplicativo.
ms.assetid: 44cb22b5-707b-4f21-b986-5258ed273543
keywords:
- TSF (estrutura de serviços de texto), objetos inseridos
- TSF (estrutura de serviços de texto), objetos inseridos
- Aplicativos habilitados para TSF, objetos inseridos
- objetos inseridos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39e4f819e6f42cc4e8d2ed81e47c79efe5ff7407
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104560132"
---
# <a name="embedded-objects-text-services-framework"></a>Objetos inseridos (estrutura de serviços de texto)

A estrutura de serviços de texto permite que um serviço de texto incorpore objetos em um fluxo de texto de aplicativo. Os objetos inseridos são inseridos no fluxo de texto usando o valor [TS \_ Char \_ inserido](ts-char--constants.md). Esse valor é resolvido para o caractere de substituição de objeto Unicode U + fffc, usando a notação hexadecimal. Por exemplo, a ilustração a seguir mostra a renderização de um objeto inserido que representa *a ideograma* de CJK, em combinação com a sequência de caracteres Unicode que representa a tradução em inglês de "sol".

![codificação de caracteres de um objeto inserido](images/emb-obj.gif)

A linha superior da figura contém o texto traduzido, que consiste na palavra "sol" seguida pelo caractere japonês para sol, *Olá*. A linha central da figura mostra o caractere Unicode. No caso de U + fffc, esse é o caractere de substituição do objeto. A linha inferior da figura mostra o valor hexadecimal de cada caractere.

## <a name="supporting-embedded-objects-in-an-application"></a>Suporte a objetos incorporados em um aplicativo

O Gerenciador do TSF insere um objeto inserido no fluxo de texto chamando [ITextStoreACP:: InsertEmbedded](/windows/desktop/api/textstor/nf-textstor-itextstoreacp-insertembedded) para um aplicativo baseado em ACP ou [ITextStoreAnchor:: InsertEmbedded](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-insertembedded) para um aplicativo baseado em âncora. Quando um objeto inserido é inserido, o aplicativo deve colocar o valor de **TS \_ Char \_ inserido** na posição do caractere (ou no local da âncora) em que o objeto é inserido e armazenar o IDataObject associado ao objeto incorporado. Quando [ITextStoreACP:: gettext](/windows/desktop/api/textstor/nf-textstor-itextstoreacp-gettext) ou [ITextStoreAnchor:: gettext](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-gettext) é chamado e um objeto incorporado está contido no texto obtido, o valor **\_ \_ inserido de TS Char** indica a presença e o local do objeto inserido. Para obter o objeto incorporado, chame [ITextStoreACP:: getembedded](/windows/desktop/api/textstor/nf-textstor-itextstoreacp-getembedded) com a posição de caractere do objeto inserido ou [ITextStoreAnchor:: getembedded](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getembedded) com o local de âncora do objeto inserido.

O aplicativo normalmente não reconhece o conteúdo do objeto inserido. O aplicativo pode tentar obter informações de exibição do próprio objeto. Se o objeto incorporado puder fornecer dados em um formato reconhecido pelo aplicativo, como CF \_ UNICODETEXT ou \_ o bitmap CF, o aplicativo poderá exibir informações gráficas fornecidas pelo objeto.

## <a name="inserting-embedded-objects"></a>Inserindo objetos inseridos

Um serviço de texto insere um objeto inserido em um contexto chamando [ITfRange:: InsertEmbedded](/windows/desktop/api/msctf/nf-msctf-itfrange-insertembedded) ou [ITfInsertAtSelection:: InsertEmbeddedAtSelection](/windows/desktop/api/msctf/nf-msctf-itfinsertatselection-insertembeddedatselection). O serviço de texto deve fornecer o IDataObject inserido.

 

 
