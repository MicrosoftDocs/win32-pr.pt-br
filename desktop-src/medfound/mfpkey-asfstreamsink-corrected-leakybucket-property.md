---
description: Especifica o &\# 0034; Bucket de vazamento&\# 0034; parâmetros para um fluxo em um coletor de mídia ASF.
ms.assetid: b01e59b6-0a7f-4125-867c-532385a27c15
title: Propriedade MFPKEY_ASFSTREAMSINK_CORRECTED_LEAKYBUCKET (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05a4ebc2dc41a1f43906aff5d2fe8caea8d53057
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827307"
---
# <a name="mfpkey_asfstreamsink_corrected_leakybucket-property"></a>\_ \_ Propriedade LEAKYBUCKET MFPKEY ASFSTREAMSINK corrigida \_

Especifica os parâmetros de "Bucket de vazamentos" (consulte comentários) para um fluxo em um coletor de mídia ASF.



Tipo de dados

Tipo PROPVARIANT (VT)

Membro PROPVARIANT

Matriz de valores **DWORD** (**Caul**)

\_UI4 de vetor \| VT \_ VT

**caul**



## <a name="remarks"></a>Comentários

Um aplicativo pode definir essa propriedade em um fluxo do coletor de mídia ASF depois que o tipo de mídia para o fluxo é negociado. Use essa propriedade para especificar a janela de buffer real que o Windows Media Codec usará. Você pode obter essas informações do codec usando a interface **IWMCodecLeakyBucket** , que está documentada no Windows Media Format SDK.

O valor dessa propriedade é uma matriz de três valores **DWORD** na seguinte ordem:

-   Taxa de bits, em bits por segundo.
-   Tamanho do buffer, em bytes.
-   Total do buffer inicial, em bytes.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                               |
| parâmetro<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink)
</dt> <dt>

[Propriedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




