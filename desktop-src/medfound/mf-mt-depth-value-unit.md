---
description: Um valor que define as unidades para um valor de profundidade em um quadro de vídeo.
ms.assetid: 0D7238F3-C224-48BD-8654-B3182DFB244C
title: Atributo MF_MT_DEPTH_VALUE_UNIT (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f6086a34f62c26b3fe1fa611318792c9056a50c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105780370"
---
# <a name="mf_mt_depth_value_unit-attribute"></a>\_Atributo de \_ unidade de valor de profundidade \_ \_ do MF MT

\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente. A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]

Um valor que define as unidades para um valor de profundidade em um quadro de vídeo.

## <a name="data-type"></a>Tipo de dados

**UINT64**

## <a name="remarks"></a>Comentários

O valor de unidade é um valor de UINT64 em comedidores, no intervalo de 1e a 9 metros. Se esse valor não estiver presente, o valor padrão da unidade será 1e-3, o que indica que cada nível de pixel é medido em 1 milímetro no espaço físico.

As câmeras de profundidade não podem detectar a profundidade de todos os pixels. Quando a confiança de um pixel é baixa, devido ao material, oclusão ou fora do intervalo, etc, o valor de profundidade nesse pixel pode ser inválido.

Quando um valor de pixel de profundidade é 0, o pixel é inválido.

Algumas câmeras de profundidade anexam metadados de bitmask para cada pixel, além do valor de profundidade para representar o motivo pelo qual a profundidade de pixel é inválida, devido ao material, oclusão ou fora do intervalo, etc. Recomendamos que você evite anexar esses metadados como bits em valor de profundidade, porque normalmente isso levará a dificuldade ao usar esses valores no sombreador de pixel. Stead. Recomendamos que você use um buffer de imagem 8 bits separado com a mesma resolução e anexe-o como atributo de [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample). Esses metadados variam de acordo com cada fornecedor da câmera e não são padronizados pela plataforma. É recomendável usar 16 bits completos para o valor de profundidade para facilitar o processamento downstream e usar um valor fixo como 0 para invalidação.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10, versão 1709\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows Server, \[ somente aplicativos da área de trabalho da versão 1709\]<br/>                      |
| parâmetro<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



 

 




