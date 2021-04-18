---
description: Especifica a hora de início para as apresentações que são enfileiradas após a primeira apresentação.
ms.assetid: 087f5d61-b3e6-4fdf-98e6-b018de7b237f
title: Atributo MF_TOPOLOGY_START_TIME_ON_PRESENTATION_SWITCH (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5f4c50271ad2da9682be9d259ad855352e844af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105783726"
---
# <a name="mf_topology_start_time_on_presentation_switch-attribute"></a>\_ \_ \_ Hora de início da topologia MF \_ no \_ atributo do \_ comutador de apresentação

Especifica a hora de início para as apresentações que são enfileiradas após a primeira apresentação.

## <a name="data-type"></a>Tipo de dados

**Int64** armazenado como **UINT64**

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [**IMFAttributes:: getuint64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).

Para definir esse atributo, chame [**IMFAttributes:: setuint64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64).

## <a name="applies-to"></a>Aplica-se A

[**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a>Comentários

Quando o aplicativo enfileira a primeira apresentação na sessão de mídia, o aplicativo especifica a hora de início no parâmetro *pvarStartPosition* do método [**IMFMediaSession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) . No entanto, para todas as apresentações subsequentes, a hora de início é fornecida pela \_ hora de início da topologia MF \_ \_ \_ no \_ \_ atributo switch de apresentação na topologia. A hora de início é especificada em unidades de 100 a nanossegundos, em relação ao início da apresentação. Por exemplo, se o valor for 50 milhões, a reprodução iniciará 5 segundos na apresentação. Se esse atributo não for definido, a hora de início padrão será zero.

A constante de GUID para esse atributo é exportada de mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                         |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]<br/>                            |
| parâmetro<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de topologia](topology-attributes.md)
</dt> </dl>

 

 




