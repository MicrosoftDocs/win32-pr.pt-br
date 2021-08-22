---
description: Declara um objeto para ser uma constante de seleção, para evitar recargas redundantes desse objeto se ele for usado (e declarado) em vários locais na biblioteca DirectXMath.
ms.assetid: FDE5C004-9E8E-4890-8FDC-987C1569D8E5
title: Macro XMGLOBALCONST
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be72254865aed46de86955c2a27a4d73351311c5aa63a44a6e218be7a3915d1c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119117996"
---
# <a name="xmglobalconst-macro"></a>Macro XMGLOBALCONST

Declara um objeto para ser uma constante de *seleção* , para evitar recargas redundantes desse objeto se ele for usado (e declarado) em vários locais na biblioteca DirectXMath.

## <a name="syntax"></a>Sintaxe

``` syntax
#define XMGLOBALCONST  extern const __declspec(selectany)
```

## <a name="remarks"></a>Comentários

O uso de XMGLOBALCONST permite a especificação de constantes globais. Isso ajuda a reduzir o tamanho do segmento de dados de um aplicativo, evitar a criação e destruição de objetos redundantes e reduzir as operações de carga e armazenamento.

## <a name="requirements"></a>Requisitos

**Cabeçalho:** Declarado em DirectXMath. h.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Macros da biblioteca DirectXMath](ovw-xnamath-reference-macros.md)
</dt> <dt>

[Constantes globais na biblioteca DirectXMath](pg-xnamath-internals.md)
</dt> <dt>

[selectany](/previous-versions/visualstudio/visual-studio-6.0/aa273550(v=vs.60))
</dt> <dt>

[declspec](/previous-versions/visualstudio/visual-studio-6.0/aa273692(v=vs.60))
</dt> </dl>

 

 
