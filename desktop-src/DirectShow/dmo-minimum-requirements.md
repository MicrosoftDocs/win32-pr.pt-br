---
description: Requisitos mínimos do DMO
ms.assetid: cd342f0f-a3dc-4623-a18f-c45071795ef4
title: Requisitos mínimos do DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1c26267f50619062fb8396f93b7578db4d3d8c4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103919976"
---
# <a name="dmo-minimum-requirements"></a>Requisitos mínimos do DMO

Cada DMO deve atender aos seguintes requisitos mínimos:

-   Ele deve dar suporte à agregação.
-   Ele deve expor a interface [**IMediaObject**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject) .
-   O modelo de Threading deve ser ' both '. DMOs deve funcionar corretamente em um ambiente de thread livre.

O efeito de áudio DMOs deve dar suporte à interface [**IMediaObjectInPlace**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobjectinplace) , para uso no DirectMusic e no DirectSound.

As interfaces a seguir estão documentadas em outro lugar, mas são úteis para muitas DMOs. No entanto, eles não são necessários.

-   **ISpecifyPropertyPages**, **IPropertyPage**: essas interfaces permitem que um DMO forneça uma página de propriedades para que o usuário defina propriedades.
-   **IPersistStream**: essa interface permite que o DMO salve seu estado no armazenamento persistente.
-   [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig), [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression): essas interfaces permitem que um cliente configure o formato de saída do codificador e as configurações de compactação. (Essas duas interfaces fazem parte da API do DirectShow, mas também são recomendadas para DMOs.)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Escrevendo um DMO](writing-a-dmo.md)
</dt> </dl>

 

 



