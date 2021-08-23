---
description: Como implementar IUnknown
ms.assetid: 4e363ccb-9725-4be6-bb31-283bf1d658f5
title: Como implementar IUnknown
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1f905ac7e31be955a7b24f8504fc6b52ca8031e4a7deef86ef8bccd537b5ca6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119748696"
---
# <a name="how-to-implement-iunknown"></a>Como implementar IUnknown

o Microsoft DirectShow é baseado no Component Object Model (com). Se você escrever seu próprio filtro, deverá implementá-lo como um objeto COM. as classes base DirectShow fornecem uma estrutura da qual fazer isso. Não é necessário usar as classes base, mas isso pode simplificar o processo de desenvolvimento. este artigo descreve alguns dos detalhes internos de objetos COM e sua implementação nas classes base DirectShow.

Este artigo pressupõe que você saiba como programar aplicativos cliente COM, em outras palavras, que você entende os métodos em **IUnknown**, mas não assume nenhuma experiência anterior ao desenvolver objetos com. DirectShow lida com muitos dos detalhes do desenvolvimento de um objeto COM. Se tiver experiência em desenvolver objetos COM, você deverá ler a seção [usando CUnknown](using-cunknown.md), que descreve a classe base [**CUnknown**](cunknown.md) .

COM é uma especificação, não uma implementação. Ele define as regras que um componente deve seguir; colocar essas regras em vigor é deixado para o desenvolvedor. no DirectShow, todos os objetos derivam de um conjunto de classes base C++. Os construtores e métodos de classe base fazem a maior parte do trabalho de "escrituração" COM, como manter uma contagem de referência consistente. Ao derivar o filtro de uma classe base, você herda a funcionalidade da classe. Para usar classes base COM eficiência, você precisa de uma compreensão geral de como elas implementam a especificação COM.

Este artigo contém os tópicos a seguir.

-   [Como o IUnknown funciona](how-iunknown-works.md)
-   [Usando CUnknown](using-cunknown.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[DirectShow e COM](directshow-and-com.md)
</dt> </dl>

 

 



