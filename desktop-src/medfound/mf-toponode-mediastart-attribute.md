---
description: Especifica a hora de início da apresentação.
ms.assetid: a2a64cac-0dc1-41b0-b59c-a477c7304ba1
title: Atributo MF_TOPONODE_MEDIASTART (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ab00727cc328bfd6ba780050160fb21eecbb96f
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105815412"
---
# <a name="mf_toponode_mediastart-attribute"></a>\_Atributo MF TOPONODE \_ MEDIASTART

Especifica a hora de início da apresentação.

## <a name="data-type"></a>Tipo de dados

**UINT64**

Tratar como um valor de **LONGLONG** .

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [**IMFAttributes:: getuint64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).

Para definir esse atributo, chame [**IMFAttributes:: setuint64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64).

## <a name="applies-to"></a>Aplica-se a

[**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)

## <a name="remarks"></a>Comentários

Esse atributo especifica a posição na origem em que a reprodução é iniciada, em unidades de 100 nanossegundos, em relação ao início da origem. Se o atributo não estiver definido, a reprodução começará em zero (o início do arquivo). Por exemplo, para iniciar a reprodução na marca de 5 segundos, defina esse atributo como 50 milhões. Defina o atributo nos nós de origem na topologia (nós com tipo igual a **SOURCESTREAM de \_ topologia \_ \_ MF**). Defina o atributo antes de chamar [**IMFMediaSession:: settopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology).

> [!Note]  
> Se você inserir manualmente um decodificador na topologia, também deverá definir os atributos de [TOPONODE do MF \_ \_ \_ aqui](mf-toponode-markin-here-attribute.md) e do [MF \_ TOPONODE \_ \_ markout](mf-toponode-markout-here-attribute.md) no nó do decodificador.

 

Esse atributo é um valor assinado, embora seja armazenado como um **UINT64**. No entanto, os valores negativos não são significativos.

A constante de GUID para esse atributo é exportada de mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                               |
| parâmetro<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Tempos de apresentação da sequência](sequence-presentation-times.md)
</dt> <dt>

[Atributos de nó de topologia](topology-node-attributes.md)
</dt> <dt>

[**\_TOPONODE MF \_ MEDIASTOP**](mf-toponode-mediastop-attribute.md)
</dt> </dl>

 

 




