---
description: Especifica o número de threads que o codificador usará.
ms.assetid: 2f463cba-2512-455d-9ce1-8797682d4d67
title: MFPKEY_NUMTHREADS propriedade (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ac8b6ec040ba07a2e38b1e9d8e2df6cf0fcbfcdbba14481e9b50379ecc10df5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119953906"
---
# <a name="mfpkey_numthreads-property"></a>Propriedade \_ NUMTHREADS MFPKEY

Especifica o número de threads que o codificador usará.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCNumThreads

## <a name="data-type"></a>Tipo de Dados

VT \_ I4

## <a name="default-value"></a>Valor padrão

1

## <a name="remarks"></a>Comentários

Esse valor destina-se a dividir a codificação em vários threads para aproveitar computadores com vários processadores. Dividir tarefas de codificação em vários threads pode causar uma pequena diminuição na qualidade em comparação com um único thread.

Para o codificador de vídeo (wmvencod.dll) lançado com Windows XP e Windows Vista, essa propriedade deve ser definida como 1, 2 ou 4. Outros valores serão arredondados para baixo.

Para o codificador de vídeo (wmvencod.dll) lançado com Windows 7, essa propriedade deve ser definida como 1, 2, 4 ou 8. Outros valores serão arredondados para baixo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>                                             |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                    |
| Cabeçalho<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Media Foundation propriedades](media-foundation-properties.md)
</dt> </dl>

 

 




