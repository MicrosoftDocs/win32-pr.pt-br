---
description: Especifica a matriz de canal, que é usada para converter os canais de origem nos canais de destino (por exemplo, para converter 5,1 para estéreo).
ms.assetid: 2f2a82bd-f051-4b05-a9c8-37aa4403fab4
title: Propriedade MFPKEY_WMRESAMP_CHANNELMTX (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e39f9a9344dd080362859592fcf1f71657ee8f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105763543"
---
# <a name="mfpkey_wmresamp_channelmtx-property"></a>\_Propriedade MFPKEY WMRESAMP \_ CHANNELMTX

Especifica a matriz de canal, que é usada para converter os canais de origem nos canais de destino (por exemplo, para converter 5,1 para estéreo).

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Disponível apenas usando [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo de Dados

\_Matriz VT i4 \| VT \_

## <a name="applies-to"></a>Aplica-se A

-   [DSP de reamostragem de áudio](audioresampler.md)

## <a name="remarks"></a>Comentários

O valor da propriedade é uma matriz de coeficientes do NS x nd, em que ns é o número de canais de origem e nd é o número de canais de destino. Os coeficientes são especificados em decibéis usando a seguinte fórmula:

inteiro (65536 \* 20 \* log10 (DB))

A matriz é armazenada como uma matriz na ordem de linha principal, em que o número da linha é o canal de origem e o número da coluna é o canal de destino.

Portanto, se a matriz for a seguinte:

``` syntax
00       01       ...      0(Ns-1)
10       11       ...      1(Ns-1)
...      ...      ...      ...
(Nd-1)0 (Nd-1)1 ... (Nd-1)(Ns-1)
```

em seguida, você especificaria a matriz como:

``` syntax
[ 00, 01, ..., 0(Ns-1), 10, 11, ..., 1(Ns-1), ..., (Nd-1)0, (Nd-1)1, ..., (Nd-1)(Ns-1) ]
```

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

 

 
