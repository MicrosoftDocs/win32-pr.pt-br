---
description: DMO Requisitos mínimos
ms.assetid: cd342f0f-a3dc-4623-a18f-c45071795ef4
title: DMO Requisitos mínimos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7acc4f664d32112512120f2f20687051a0bff193e00adb7ad595e6975c522fce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119749136"
---
# <a name="dmo-minimum-requirements"></a>DMO Requisitos mínimos

cada DMO deve atender aos seguintes requisitos mínimos:

-   Ele deve dar suporte à agregação.
-   Ele deve expor a interface [**IMediaObject**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject) .
-   O modelo de Threading deve ser ' both '. DMOs deve funcionar corretamente em um ambiente de thread livre.

O efeito de áudio DMOs deve dar suporte à interface [**IMediaObjectInPlace**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobjectinplace) , para uso no DirectMusic e no DirectSound.

As interfaces a seguir estão documentadas em outro lugar, mas são úteis para muitas DMOs. No entanto, eles não são necessários.

-   **ISpecifyPropertyPages**, **IPropertyPage**: essas interfaces permitem que um DMO forneça uma página de propriedades para que o usuário defina propriedades.
-   **IPersistStream**: essa interface permite que o DMO salve seu estado no armazenamento persistente.
-   [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig), [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression): essas interfaces permitem que um cliente configure o formato de saída do codificador e as configurações de compactação. (essas duas interfaces fazem parte da API do DirectShow, mas também são recomendadas para DMOs.)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Escrevendo um DMO](writing-a-dmo.md)
</dt> </dl>

 

 



