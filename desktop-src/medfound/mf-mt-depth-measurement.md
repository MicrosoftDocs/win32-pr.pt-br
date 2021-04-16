---
description: Um valor que define o sistema de medidas para um valor de profundidade em um quadro de vídeo.
ms.assetid: 7BFA846B-E614-4117-A196-298E065CB7F8
title: Atributo MF_MT_DEPTH_MEASUREMENT (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8be6c06ea09f4017ae65935081eaa81d1ad00cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104558015"
---
# <a name="mf_mt_depth_measurement-attribute"></a>\_Atributo de \_ medida de profundidade do MF MT \_

\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente. A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]

Um valor que define o sistema de medidas para um valor de profundidade em um quadro de vídeo.

## <a name="data-type"></a>Tipo de dados

**UINT32**

## <a name="remarks"></a>Comentários

Esse valor é um membro da enumeração [**\_ MFDepthMeasurement**](/windows/win32/api/mfapi/ne-mfapi-mfdepthmeasurement)

Se esse atributo não estiver presente, supõe-se que seja **DistanceToFocalPlane**. Normalmente, a distância para o plano focal é mais fácil de consumir em um sistema de coordenadas euclidiana 3D.

![ilustração de distancetofocalplane](images/distance-to-focal-plane.png)

A distância para o formato do centro focal é normalmente dados brutos do sensor, como o tempo de câmeras de voo.

![ilustração de distancetoopticalcenter](images/distance-to-optical-center.png)

As câmeras de profundidade não podem detectar a profundidade de todos os pixels. Quando a confiança de um pixel é baixa, devido ao material, oclusão ou fora do intervalo, etc, o valor de profundidade nesse pixel pode ser inválido.

Quando um valor de pixel de profundidade é 0, o pixel é inválido.

Algumas câmeras de profundidade anexam metadados de bitmask para cada pixel, além do valor de profundidade para representar o motivo pelo qual a profundidade de pixel é inválida, devido ao material, oclusão ou fora do intervalo, etc. Recomendamos que você evite anexar esses metadados como bits em valor de profundidade, porque normalmente isso levará a dificuldade ao usar esses valores no sombreador de pixel. Stead. Recomendamos que você use um buffer de imagem 8 bits separado com a mesma resolução e anexe-o como atributo de [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample). Esses metadados variam de acordo com cada fornecedor da câmera e não são padronizados pela plataforma. É recomendável usar 16 bits completos para o valor de profundidade para facilitar o processamento downstream e usar um valor fixo como 0 para invalidação.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10, versão 1709\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows Server, \[ somente aplicativos da área de trabalho da versão 1709\]<br/>                      |
| parâmetro<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



 

 




