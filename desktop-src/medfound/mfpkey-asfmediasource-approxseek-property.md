---
description: Especifica se a origem de mídia ASF usa busca aproximada.
ms.assetid: 4877b67c-524c-4717-a90f-6de21918d3d8
title: Propriedade MFPKEY_ASFMediaSource_ApproxSeek (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 253a18ebbdf78e3aa0ef0e79f41c4bf180a04b48
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105797594"
---
# <a name="mfpkey_asfmediasource_approxseek-property"></a>\_Propriedade MFPKEY ASFMediaSource \_ ApproxSeek

Especifica se a origem de mídia ASF usa busca aproximada.



Tipo de dados

Tipo PROPVARIANT (VT)

Membro PROPVARIANT

**BOOL de variante \_**

BOOL do VT \_

**boolVal**



## <a name="remarks"></a>Comentários

Os aplicativos podem usar essa propriedade para configurar a origem da mídia ASF. Para definir a propriedade, passe um ponteiro **IPropertyStore** para o resolvedor de origem. Para obter mais informações, consulte [Configurando uma origem de mídia](configuring-a-media-source.md).

A fonte de mídia do ASF trata da seguinte maneira:

-   Se o valor dessa propriedade for **Variant \_ true**, a origem da mídia usará a busca aproximada, que é menos precisa, mas mais rápida do que a procura exata.
-   Se o valor for **Variant \_ false** e o arquivo ASF tiver um índice, a origem da mídia usará a busca exata.
-   Se o arquivo ASF não contiver um índice, a origem da mídia usará approxmate procurando, a menos que a propriedade [MFPKEY \_ ASFMediaSource \_ IterativeSeekIfNoIndex](mfpkey-asfmediasource-iterativeseekifnoindex.md) esteja definida como **Variant \_ true**.
-   Se o arquivo ASF não contiver um índice e a propriedade [MFPKEY \_ ASFMediaSource \_ IterativeSeekIfNoIndex](mfpkey-asfmediasource-iterativeseekifnoindex.md) for **Variant \_ true**, a origem de mídia usará a busca iterativa. A busca iterativa é mais precisa, mas mais lenta que a busca aproximada (mas geralmente menos precisa do que a procura exata).
    > [!Note]  
    > Requer o Windows 7.

     

O valor padrão dessa propriedade é **Variant \_ false**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                               |
| parâmetro<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




