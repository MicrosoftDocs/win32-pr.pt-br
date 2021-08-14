---
description: Contém um ponteiro para a interface IMFSourceOpenMonitor de aplicativos.
ms.assetid: 5b94ae87-91fc-49d6-9355-83327cfdb3f3
title: Propriedade MFPKEY_SourceOpenMonitor (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45594e1929e66982d3e518c4ba098d2ca4b22e854e033dc69025aaf3ec5d5cc6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117872974"
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
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                               |
| Cabeçalho<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




