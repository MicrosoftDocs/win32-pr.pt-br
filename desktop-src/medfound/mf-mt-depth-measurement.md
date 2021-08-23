---
description: Um valor que define o sistema de medição para um valor de profundidade em um quadro de vídeo.
ms.assetid: 7BFA846B-E614-4117-A196-298E065CB7F8
title: MF_MT_DEPTH_MEASUREMENT atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a292e5a96cec7490917ef0bb897a9a7a67dd303d29692bf6db5ff58e1d4388c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119605787"
---
# <a name="mf_mt_depth_measurement-attribute"></a>Atributo \_ MF MT \_ DEPTH \_ MEASUREMENT

\[Algumas informações estão relacionadas ao produto pré-lançado, que pode ser substancialmente modificado antes de ser lançado comercialmente. A Microsoft não oferece garantias, expressas ou implícitas, das informações aqui fornecidas.\]

Um valor que define o sistema de medição para um valor de profundidade em um quadro de vídeo.

## <a name="data-type"></a>Tipo de dados

**UINT32**

## <a name="remarks"></a>Comentários

Esse valor é um membro da [**\_ enumeração MFDepthMeasurement**](/windows/win32/api/mfapi/ne-mfapi-mfdepthmeasurement)

Se esse atributo não estiver presente, supõe-se que seja **DistanceToFocalPlane.** A distância para o plano focal normalmente é mais fácil de consumir em um sistema de coordenadas euclidiano 3D.

![ilustração de distancetofocalplane](images/distance-to-focal-plane.png)

A distância até o formato focal center normalmente são dados brutos do sensor, como a hora das câmeras de voo.

![ilustração de distancetoopticalcenter](images/distance-to-optical-center.png)

Câmeras de profundidade não conseguem perceber a profundidade de todos os pixels. Quando a confiança de um pixel é baixa, devido a material, oclusão ou fora do intervalo, etc., o valor de profundidade nesse pixel pode ser inválido.

Quando um valor de pixel de profundidade é 0, o pixel é inválido.

Algumas câmeras de profundidade anexam metadados de bitmask para cada pixel além do valor de profundidade para representar o motivo pelo qual a profundidade do pixel é inválida, devido a material, oclusão ou fora do intervalo etc. Recomendamos que você evite anexar metadados como bits em valor de profundidade, pois isso normalmente levará a dificuldades ao usar esses valores no sombreador de pixel. Ao invés. recomendamos que você use um buffer de imagem de 8bits separado com a mesma resolução e anexe-o como atributo do [**IMFSample.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) Esses metadados variam para cada fornecedor de câmera e não são padronizados pela plataforma. É recomendável usar 16 bits completos para o valor de profundidade para facilitar o processamento downstream e o uso de um valor fixo como 0 para invalidação.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10, versão 1709 somente para \[ aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows Servidor, versão 1709 somente \[ aplicativos da área de trabalho\]<br/>                      |
| Cabeçalho<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



 

 




