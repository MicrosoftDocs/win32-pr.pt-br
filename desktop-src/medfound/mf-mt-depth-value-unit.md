---
description: Um valor que define as unidades para um valor de profundidade em um quadro de vídeo.
ms.assetid: 0D7238F3-C224-48BD-8654-B3182DFB244C
title: MF_MT_DEPTH_VALUE_UNIT atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca57fa5cf72be266ac58ee504b1d4b7c4f2506646f33295e468d2ed0781ab8d7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060636"
---
# <a name="mf_mt_depth_value_unit-attribute"></a>Atributo \_ MF MT \_ DEPTH \_ VALUE \_ UNIT

\[Algumas informações estão relacionadas ao produto pré-lançado, que pode ser substancialmente modificado antes de ser lançado comercialmente. A Microsoft não oferece garantias, expressas ou implícitas, das informações aqui fornecidas.\]

Um valor que define as unidades para um valor de profundidade em um quadro de vídeo.

## <a name="data-type"></a>Tipo de dados

**UINT64**

## <a name="remarks"></a>Comentários

O valor da unidade é um valor UINT64 em nanometers, no intervalo de 1e a 9 metros. Se esse valor não estiver presente, o valor padrão da unidade será 1e-3, o que indica que cada nível de pixel é medido em 1 milímetro no espaço físico.

Câmeras de profundidade não conseguem perceber a profundidade de todos os pixels. Quando a confiança de um pixel é baixa, devido a material, oclusão ou fora do intervalo, etc., o valor de profundidade nesse pixel pode ser inválido.

Quando um valor de pixel de profundidade é 0, o pixel é inválido.

Algumas câmeras de profundidade anexam metadados de bitmask para cada pixel além do valor de profundidade para representar o motivo pelo qual a profundidade do pixel é inválida, devido a material, oclusão ou fora do intervalo etc. Recomendamos que você evite anexar metadados como bits em valor de profundidade, pois isso normalmente levará a dificuldades ao usar esses valores no sombreador de pixel. Ao invés. recomendamos que você use um buffer de imagem de 8bits separado com a mesma resolução e anexe-o como atributo do [**IMFSample.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) Esses metadados variam para cada fornecedor de câmera e não são padronizados pela plataforma. É recomendável usar 16 bits completos para o valor de profundidade para facilitar o processamento downstream e usar um valor fixo como 0 para invalidação.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10, versão 1709 somente para \[ aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows Servidor, versão 1709 somente \[ aplicativos da área de trabalho\]<br/>                      |
| Cabeçalho<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



 

 




