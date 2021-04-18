---
description: Especifica o número de threads que o codificador usará.
ms.assetid: 2f463cba-2512-455d-9ce1-8797682d4d67
title: Propriedade MFPKEY_NUMTHREADS (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c93f6d38e3bb79bbb692f9bec1b1dc0edb232d0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104505731"
---
# <a name="mfpkey_numthreads-property"></a>\_Propriedade MFPKEY NUMTHREADS

Especifica o número de threads que o codificador usará.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCNumThreads

## <a name="data-type"></a>Tipo de Dados

\_I4 VT

## <a name="default-value"></a>Valor padrão

1

## <a name="remarks"></a>Comentários

Esse valor destina-se a dividir a codificação em vários threads para aproveitar os computadores com vários processadores. A divisão de tarefas de codificação em vários threads pode causar uma pequena queda na qualidade em comparação com um único thread.

Para o codificador de vídeo (wmvencod.dll) lançado com o Windows XP e o Windows Vista, essa propriedade deve ser definida como 1, 2 ou 4. Outros valores serão arredondados para baixo.

Para o codificador de vídeo (wmvencod.dll) lançado com o Windows 7, essa propriedade deve ser definida como 1, 2, 4 ou 8. Outros valores serão arredondados para baixo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                             |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                    |
| parâmetro<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




