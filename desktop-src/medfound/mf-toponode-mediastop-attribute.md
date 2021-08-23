---
description: Especifica a hora de parada da apresentação.
ms.assetid: c1022538-ea9f-41e9-9075-c106e8b16b7b
title: Atributo MF_TOPONODE_MEDIASTOP (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea2abc172151afe404f3acc6cf8c75d03bd0ac495564cb0f322283998677f83b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119663866"
---
# <a name="mf_toponode_mediastop-attribute"></a>\_Atributo MF TOPONODE \_ MEDIASTOP

Especifica a hora de parada da apresentação.

## <a name="data-type"></a>Tipo de dados

**UINT64**

Tratar como um valor de **LONGLONG** .

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [**IMFAttributes:: getuint64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).

Para definir esse atributo, chame [**IMFAttributes:: setuint64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64).

## <a name="applies-to"></a>Aplica-se a

[**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)

## <a name="remarks"></a>Comentários

Esse atributo especifica a posição na origem em que a reprodução é interrompida, em unidades de 100 nanossegundos, em relação ao início da origem. Se o atributo não estiver definido, a reprodução será interrompida no final da origem. Por exemplo, para parar a reprodução na marca de 5 segundos, defina esse atributo como 50 milhões. Defina o atributo nos nós de origem na topologia (nós com tipo igual a **SOURCESTREAM de \_ topologia \_ \_ MF**). Defina o atributo antes de chamar [**IMFMediaSession:: settopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology).

> [!Note]  
> Se você inserir manualmente um decodificador na topologia, também deverá definir os atributos de [TOPONODE do MF \_ \_ \_ aqui](mf-toponode-markin-here-attribute.md) e do [MF \_ TOPONODE \_ \_ markout](mf-toponode-markout-here-attribute.md) no nó do decodificador.

 

Depois que a topologia for definida, a definição desse atributo não terá nenhum efeito.

Esse atributo é um valor assinado, embora seja armazenado como um **UINT64**. No entanto, os valores negativos não são significativos.

A constante de GUID para esse atributo é exportada de mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                               |
| Cabeçalho<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Tempos de apresentação da sequência](sequence-presentation-times.md)
</dt> <dt>

[Atributos de nó de topologia](topology-node-attributes.md)
</dt> <dt>

[**\_TOPONODE MF \_ MEDIASTART**](mf-toponode-mediastart-attribute.md)
</dt> </dl>

 

 




