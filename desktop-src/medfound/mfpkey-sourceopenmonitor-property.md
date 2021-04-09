---
description: Contém um ponteiro para a interface IMFSourceOpenMonitor de aplicativos.
ms.assetid: 5b94ae87-91fc-49d6-9355-83327cfdb3f3
title: Propriedade MFPKEY_SourceOpenMonitor (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a49826ee16a733993b9052e12d9e6fcd5003410
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091409"
---
# <a name="mfpkey_sourceopenmonitor-property"></a>\_Propriedade MFPKEY SourceOpenMonitor

Contém um ponteiro para a interface [**IMFSourceOpenMonitor**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor) do aplicativo.



Tipo de dados

Tipo PROPVARIANT (VT)

Membro PROPVARIANT

Ponteiro **IUnknown**

VT \_ desconhecido

**punkVal**



## <a name="remarks"></a>Comentários

Os aplicativos podem passar essa propriedade para o resolvedor de origem para obter notificações de eventos da origem da rede.

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

 

 




