---
description: A \_ estrutura Stride de transporte do MPEG2 \_ descreve o formato dos pacotes TS-2 Transport Stream.
ms.assetid: 269d5fba-2dea-4786-93d6-e52b56c8bb53
title: Estrutura de MPEG2_TRANSPORT_STRIDE (Bdatypes. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MPEG2_TRANSPORT_STRIDE
api_type:
- HeaderDef
api_location:
- bdatypes.h
ms.openlocfilehash: 4a0cdc21bdd8c320728da0c0af8c0af023de68eb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105779325"
---
# <a name="mpeg2_transport_stride-structure"></a>\_Estrutura Stride de transporte MPEG2 \_

A `MPEG2_TRANSPORT_STRIDE` estrutura descreve o formato dos pacotes de transmissão de transporte MPEG-2 (TS). Essa estrutura permite Transportações para fluxos nos quais os pacotes de transporte de 188 bytes não são contíguos. Para a finalidade desta documentação, esses pacotes são chamados de *pacotes Stride*.

Os pacotes Stride são identificados pelo seguinte tipo de mídia:



|             |                                        |
|-------------|----------------------------------------|
| Tipo principal  | Fluxo de MEDIATYPE \_                      |
| Subtype     | \_Stride de \_ transporte MEDIASUBTYPE MPEG2 \_ |
| Tipo de formato | Formatar \_ nenhum                           |



 

O bloco de formato (**pbFormat**) é opcional. Se o bloco de formato for incluído, ele deverá começar com uma estrutura **\_ \_ Stride de transporte MPEG2** . Essa estrutura define o layout do pacote de transporte dentro do pacote Stride. Se o bloco de formato for **nulo**, os pacotes serão considerados para usar um conjunto de valores padrão; consulte a seção comentários para obter detalhes.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _MPEG2_TRANSPORT_STRIDE {
  DWORD dwOffset;
  DWORD dwPacketLength;
  DWORD dwStride;
} MPEG2_TRANSPORT_STRIDE, *PMPEG2_TRANSPORT_STRIDE;
```



## <a name="members"></a>Membros

<dl> <dt>

**dwOffset**
</dt> <dd>

Especifica o deslocamento, em bytes, desde o início do pacote até o primeiro byte do pacote de transporte inserido. O valor deve variar de zero a `(dwStride - dwPacketLength)` , inclusive.

</dd> <dt>

**dwPacketLength**
</dt> <dd>

Especifica o comprimento do pacote de transporte inserido, em bytes. Para pacotes de transporte MPEG-2 padrão, o valor deve ser 188 bytes.

</dd> <dt>

**dwStride**
</dt> <dd>

Especifica o comprimento de todo o pacote Stride, em bytes. O valor deve ser pelo menos `(dwOffset + dwPacketLength)` .

</dd> </dl>

## <a name="remarks"></a>Comentários

O diagrama a seguir ilustra as relações entre os membros da estrutura.

![pacote de Stride MPEG-2](images/mpeg2-stride-packet.png)

Os buffers de entrada que contêm pacotes Stride multiplexados têm algumas restrições:

-   Os pacotes Stride devem ser empacotados de forma contígua no buffer.
-   Nenhum byte pode preceder o primeiro pacote Stride ou seguir o último pacote Stride.
-   Um número integral de pacotes Stride deve caber no buffer; ou seja, o comprimento do buffer% dwStride é igual a zero.

Não há nenhuma restrição quanto ao número de pacotes Stride por buffer.

Se o tipo de mídia não contiver um bloco de formato (**pbFormat** é **nulo**), os seguintes valores padrão serão usados:

-   **dwOffset**: 0
-   **dwPacketLength**: 188
-   **dwStride**: 188

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Bdatypes. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas do DirectShow](directshow-structures.md)
</dt> <dt>

[Tipos de mídia MPEG-2](mpeg-2-media-types.md)
</dt> </dl>

 

 




