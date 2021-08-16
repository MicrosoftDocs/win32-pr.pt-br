---
description: Especifica a matriz de canais, que é usada para converter os canais de origem nos canais de destino (por exemplo, para converter 5.1 em estéreo).
ms.assetid: 2f2a82bd-f051-4b05-a9c8-37aa4403fab4
title: MFPKEY_WMRESAMP_CHANNELMTX propriedade (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a326cfe27632204f2975ac8b7c3a605c666464f8f62846a5c622a469f2f6e104
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117689250"
---
# <a name="mfpkey_wmresamp_channelmtx-property"></a>Propriedade MFPKEY \_ WMRESAMP \_ CHANNELMTX

Especifica a matriz de canais, que é usada para converter os canais de origem nos canais de destino (por exemplo, para converter 5.1 em estéreo).

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Disponível somente usando [**IPropertyStore.**](/windows/win32/api/propsys/nn-propsys-ipropertystore)

## <a name="data-type"></a>Tipo de Dados

MATRIZ VT \_ I4 \| VT \_

## <a name="applies-to"></a>Aplica-se A

-   [Audio Resampler DSP](audioresampler.md)

## <a name="remarks"></a>Comentários

O valor da propriedade é uma matriz de coeficientes Ns x Nd, em que Ns é o número de canais de origem e Nd é o número de canais de destino. Coeficientes são especificados em decibéis usando a seguinte fórmula:

(int) (65536 \* 20 \* log10(dB))

A matriz é armazenada como uma matriz na ordem principal da linha, em que o número da linha é o canal de origem e o número da coluna é o canal de destino.

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
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>                                             |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                    |
| Cabeçalho<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Media Foundation propriedades](media-foundation-properties.md)
</dt> </dl>

 

 
