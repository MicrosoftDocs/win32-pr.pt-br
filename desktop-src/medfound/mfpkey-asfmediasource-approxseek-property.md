---
description: Especifica se a origem de mídia ASF usa busca aproximada.
ms.assetid: 4877b67c-524c-4717-a90f-6de21918d3d8
title: Propriedade MFPKEY_ASFMediaSource_ApproxSeek (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f68dedbf2b008870021e620029a039c21465d4bb45a23428225d7c88fae6583
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117874330"
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
    > requer Windows 7.

     

O valor padrão dessa propriedade é **Variant \_ false**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                               |
| Cabeçalho<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




