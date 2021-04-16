---
description: Habilita ou desabilita o Read-Ahead em uma fonte de mídia.
ms.assetid: b2b8711f-ba63-4fba-bb88-8d254135eb21
title: Propriedade MFPKEY_MediaSource_DisableReadAhead (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d06fe354431a24e15152268ba0ea6352e535c5e7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750147"
---
# <a name="mfpkey_mediasource_disablereadahead-property"></a>\_Propriedade MFPKEY Mediate \_ DisableReadAhead

Habilita ou desabilita o Read-Ahead em uma fonte de mídia.



Tipo de dados

Tipo PROPVARIANT (VT)

Membro PROPVARIANT

**BOOL de variante \_**

BOOL do VT \_

**boolVal**



## <a name="remarks"></a>Comentários

Os aplicativos podem usar essa propriedade para configurar algumas fontes de mídia. Para definir a propriedade, passe um ponteiro **IPropertyStore** para o resolvedor de origem. Para obter mais informações, consulte [Configurando uma origem de mídia](configuring-a-media-source.md).

Se o valor for **Variant \_ true**, a origem da mídia não será lida com antecedência no fluxo de bytes. Essa configuração pode otimizar o desempenho se você planeja ler uma quantidade limitada de dados da fonte de mídia, por exemplo, para obter uma imagem em miniatura de um arquivo de vídeo.

Para reprodução de áudio/vídeo típica, essa propriedade deve ser definida como **Variant \_ false**. O valor padrão é **Variant \_ false**.

Nem toda fonte de mídia dá suporte a essa propriedade.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|------------------------------------------------------------------------------------|
| Cliente<br/> | Windows 7<br/>                                                               |
| parâmetro<br/> | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




