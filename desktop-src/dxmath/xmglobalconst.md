---
description: Declara um objeto para ser uma constante de seleção, para evitar recargas redundantes desse objeto se ele for usado (e declarado) em vários locais na biblioteca DirectXMath.
ms.assetid: FDE5C004-9E8E-4890-8FDC-987C1569D8E5
title: Macro XMGLOBALCONST
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6675b17138fca66e293321a9d848262a8bffc94e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105782567"
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

 

 
