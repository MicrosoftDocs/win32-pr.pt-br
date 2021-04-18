---
description: Como implementar IUnknown
ms.assetid: 4e363ccb-9725-4be6-bb31-283bf1d658f5
title: Como implementar IUnknown
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e27c12e25d56adab1841a375ac6c1ce0857a73b5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500162"
---
# <a name="how-to-implement-iunknown"></a>Como implementar IUnknown

O Microsoft DirectShow é baseado na Component Object Model (COM). Se você escrever seu próprio filtro, deverá implementá-lo como um objeto COM. As classes base do DirectShow fornecem uma estrutura da qual fazer isso. Não é necessário usar as classes base, mas isso pode simplificar o processo de desenvolvimento. Este artigo descreve alguns dos detalhes internos de objetos COM e sua implementação nas classes base do DirectShow.

Este artigo pressupõe que você saiba como programar aplicativos cliente COM, em outras palavras, que você entende os métodos em **IUnknown**, mas não assume nenhuma experiência anterior ao desenvolver objetos com. O DirectShow lida com muitos dos detalhes do desenvolvimento de um objeto COM. Se tiver experiência em desenvolver objetos COM, você deverá ler a seção [usando CUnknown](using-cunknown.md), que descreve a classe base [**CUnknown**](cunknown.md) .

COM é uma especificação, não uma implementação. Ele define as regras que um componente deve seguir; colocar essas regras em vigor é deixado para o desenvolvedor. No DirectShow, todos os objetos derivam de um conjunto de classes base C++. Os construtores e métodos de classe base fazem a maior parte do trabalho de "escrituração" COM, como manter uma contagem de referência consistente. Ao derivar o filtro de uma classe base, você herda a funcionalidade da classe. Para usar classes base COM eficiência, você precisa de uma compreensão geral de como elas implementam a especificação COM.

Este artigo contém os tópicos a seguir.

-   [Como o IUnknown funciona](how-iunknown-works.md)
-   [Usando CUnknown](using-cunknown.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[DirectShow e COM](directshow-and-com.md)
</dt> </dl>

 

 



