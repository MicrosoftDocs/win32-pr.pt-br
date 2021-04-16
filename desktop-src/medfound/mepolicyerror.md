---
description: Gerado por uma saída confiável se ocorrer um erro ao impor a política de saída.
ms.assetid: 0cc62915-1ed6-4d1d-9600-0dac0b9034e3
title: Evento MEPolicyError (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b75083974ee0e76d7d8e21f0a2c83c2feee8d59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105768252"
---
# <a name="mepolicyerror-event"></a>Evento MEPolicyError

Gerado por uma saída confiável se ocorrer um erro ao impor a política de saída.

Se a sessão de mídia receber esse evento, ele interromperá a reprodução e encaminhará o evento para o aplicativo.

## <a name="event-values"></a>Valores de evento

Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.



| VARTYPE              | Descrição                           |
|----------------------|---------------------------------------|
| VT \_ vazio<br/> | Nenhum dado do evento.<br/> <br/> |



## <a name="remarks"></a>Comentários

Os valores possíveis recuperados de [**IMFMediaEvent:: GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus) incluem o seguinte.



| Valor                      | Descrição                                                    |
|----------------------------|----------------------------------------------------------------|
| \_política MF \_ E \_ sem suporte | A saída confiável não oferece suporte à política de saída atual. |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>Mfobjects. h (incluir Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Eventos de Media Foundation](media-foundation-events.md)
</dt> </dl>

 

 




