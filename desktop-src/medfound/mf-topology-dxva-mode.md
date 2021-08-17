---
description: Especifica se o carregador de topologia habilita a DXVA (Aceleração de Vídeo) do Microsoft DirectX na topologia.
ms.assetid: 03783ef3-f957-41e3-9734-94cb34ecc088
title: MF_TOPOLOGY_DXVA_MODE atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5462ccf575f94935d100eb70a6d806e139f09762151c2dad8d4e155ca5d1d17e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117875719"
---
# <a name="mf_topology_dxva_mode-attribute"></a>Atributo MF \_ TOPOLOGY \_ DXVA \_ MODE

Especifica se o carregador de topologia habilita a DXVA (Aceleração de Vídeo) do Microsoft DirectX na topologia.

## <a name="data-type"></a>Tipo de dados

**[**MFTOPOLOGY \_ MODO DXVA \_ armazenado**](/windows/desktop/api/mfidl/ne-mfidl-mftopology_dxva_mode)** como **UINT32**

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para definir esse atributo, chame [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Aplica-se a

[**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a>Comentários

O valor desse atributo é uma constante de enumeração [**MFTOPOLOGY \_ DXVA \_ MODE.**](/windows/desktop/api/mfidl/ne-mfidl-mftopology_dxva_mode) O valor padrão é **MFTOPOLOGY \_ DXVA \_ DEFAULT.**

Esse atributo controla quais MFTs recebem um ponteiro para o gerenciador de dispositivos Direct3D. Para habilitar a aceleração completa de vídeo, de definido o valor como **MFTOPOLOGY \_ DXVA \_ FULL**. O valor **MFTOPOLOGY \_ DXVA \_ DEFAULT** é definido para compatibilidade com versões anteriores; ele corresponde ao comportamento de todas as versões anteriores do Microsoft Media Foundation.

A constante GUID para esse atributo é exportada de mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>                                         |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do Server 2008 R2 \[\]<br/>                            |
| Cabeçalho<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Direct3D Gerenciador de Dispositivos](direct3d-device-manager.md)
</dt> <dt>

[Atributos de topologia](topology-attributes.md)
</dt> </dl>

 

 




