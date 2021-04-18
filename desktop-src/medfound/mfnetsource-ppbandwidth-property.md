---
description: Especifica a largura de banda do par de pacotes e a largura de banda de tempo de execução detectada pela origem da rede.
ms.assetid: 430de7fc-fe62-4b89-b3fc-7cd956e40892
title: Propriedade MFNETSOURCE_PPBANDWIDTH (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae0f23f289f68e46bba726a4391023ce9001e2ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105772663"
---
# <a name="mfnetsource_ppbandwidth-property"></a>\_Propriedade MFNETSOURCE PPBANDWIDTH

Especifica a largura de banda do par de pacotes e a largura de banda de tempo de execução detectada pela origem da rede. O valor da propriedade é uma matriz de dois valores:

-   Largura de banda do par de pacotes, em bits por segundo.
-   A largura de banda em tempo de execução, em bits por segundo.



Tipo de dados

Tipo PROPVARIANT (VT)

Membro PROPVARIANT

Matriz de valores **ULONG** (**Caul**)

\_UI4 de vetor \| VT \_ VT

**caul**



## <a name="remarks"></a>Comentários

A constante **MFNETSOURCE \_ PPBANDWIDTH** define o GUID para essa chave de propriedade. O identificador de propriedade (PID) é zero.

Esta propriedade é somente para leitura. Para recuperar essa propriedade, consulte a origem da rede para a interface **IPropertyStore** e chame **IPropertyStore:: GetValue**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                               |
| parâmetro<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades de Media Foundation](media-foundation-properties.md)
</dt> <dt>

[Recursos de origem da rede](network-source-features.md)
</dt> <dt>

[Rede em Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




