---
description: Define o número de threads de trabalho que são usados por um decodificador de vídeo.
ms.assetid: A1570BB5-62BC-46C0-B9C9-61F99AA13BBE
title: Propriedade CODECAPI_AVDecNumWorkerThreads (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5d7c57d1b4176ad65313a5583a70f9ba4f7427a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105772643"
---
# <a name="codecapi_avdecnumworkerthreads-property"></a>\_Propriedade CODECAPI AVDecNumWorkerThreads

Define o número de threads de trabalho que são usados por um decodificador de vídeo.

## <a name="data-type"></a>Tipo de dados

**Long** (**VT \_ i4**)

## <a name="property-guid"></a>GUID da propriedade

CODECAPI \_ AVDecNumWorkerThreads

## <a name="remarks"></a>Comentários

Se o valor for 1, o decodificador selecionará o número de threads.

Para a interface [**ICodecAPI**](/windows/desktop/api/strmif/nn-strmif-icodecapi) , defina essa propriedade como um valor **longo** (**VT \_ i4**). Para a interface [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) , defina essa propriedade como um **UINT32**, embora o valor seja assinado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Aplicativos de \[ aplicativos da área de trabalho do Windows 8 \| UWP\]<br/>                                     |
| Servidor mínimo com suporte<br/> | Aplicativos do Windows Server 2012 \[ Desktop aplicativos \| UWP\]<br/>                           |
| parâmetro<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades de Media Foundation](media-foundation-properties.md)
</dt> <dt>

[**ICodecAPI**](/windows/desktop/api/strmif/nn-strmif-icodecapi)
</dt> </dl>

 

