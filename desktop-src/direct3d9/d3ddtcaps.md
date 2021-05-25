---
description: Constantes que descrevem os tipos de dados de vértice com suporte de um dispositivo.
ms.assetid: 751d7b92-b187-40e5-882c-6fdb80e1ff5f
title: D3DDTCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97ded570b8f451ea7e99050467f70f945d202bd4
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343222"
---
# <a name="d3ddtcaps"></a>D3DDTCAPS

Constantes que descrevem os tipos de dados de vértice com suporte de um dispositivo.



| \#definir              | Valor       | Descrição                                                                                                                   |
|-----------------------|-------------|-------------------------------------------------------------------------------------------------------------------------------|
| D3DDTCAPS \_ UBYTE4     | 0x00000001L | byte de 4D não assinado.                                                                                                             |
| D3DDTCAPS \_ UBYTE4N    | 0x00000002L | Byte normalizado, 4D não assinado. Cada um dos quatro bytes é normalizado dividindo para 255,0.                                      |
| D3DDTCAPS \_ SHORT2N    | 0x00000004L | Normalizado, 2D assinado por curto, expandido para (primeiro byte/32767.0, segundo byte/32767.0, 0, 1).                                     |
| D3DDTCAPS \_ SHORT4N    | 0x00000008L | Normalizado, 4D assinado curto, expandido para (primeiro byte/32767.0, segundo byte/32767.0, terceiro byte/32767.0, quarto byte/32767.0).  |
| D3DDTCAPS \_ USHORT2N   | 0x00000010L | Normalizado, 2D não assinado curto, expandido para (primeiro byte/65535.0, segundo byte/65535.0, 0, 1).                                   |
| D3DDTCAPS \_ USHORT4N   | 0x00000020L | 4D normalizado não assinado curto, expandido para (primeiro byte/65535.0, segundo byte/65535.0, terceiro byte/65535.0, quarto byte/65535.0). |
| D3DDTCAPS \_ UDEC3      | 0x00000040L | Formato 3D sem assinatura 10 10 10 expandido para (valor, valor, valor, 1).                                                             |
| D3DDTCAPS \_ DEC3N      | 0x00000080L | Formato 3D assinado 10 10 10 normalizado e expandido para (v \[ 0 \] /511.0, v \[ 1 \] /511.0, v \[ 2 \] /511.0, 1).                           |
| D3DDTCAPS \_ FLOAT16 \_ 2 | 0x00000100L | Números de ponto flutuante de 16 bits 2D.                                                                                             |
| D3DDTCAPS \_ FLOAT16 \_ 4 | 0x00000200L | Números de ponto flutuante de 16 bits 4D.                                                                                             |



 

Essas constantes são usadas pelo membro DeclTypes de [**D3DCAPS9.**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)

## <a name="constant-information"></a>Informações constantes



|  Requisito                        | Valor           |
|--------------------------|------------|
| parâmetro                   | d3d9caps.h |
| Sistema operacional mínimo | Windows 98 |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Constantes Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 



