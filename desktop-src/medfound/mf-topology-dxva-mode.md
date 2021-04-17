---
description: Especifica se o carregador de topologia permite o DXVA (Microsoft DirectX Video Acceleration) na topologia.
ms.assetid: 03783ef3-f957-41e3-9734-94cb34ecc088
title: Atributo MF_TOPOLOGY_DXVA_MODE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ad75b37a2ca2e971077b05d1bbeb92748530614
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105762440"
---
# <a name="mf_topology_dxva_mode-attribute"></a>\_Atributo do \_ modo DXVA da topologia MF \_

Especifica se o carregador de topologia permite o DXVA (Microsoft DirectX Video Acceleration) na topologia.

## <a name="data-type"></a>Tipo de dados

**[**MFTOPOLOGY \_ \_Modo DXVA**](/windows/desktop/api/mfidl/ne-mfidl-mftopology_dxva_mode)** armazenado como **UINT32**

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para definir esse atributo, chame [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Aplica-se a

[**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a>Comentários

O valor desse atributo é uma constante de enumeração do [**\_ \_ modo MFTOPOLOGY DXVA**](/windows/desktop/api/mfidl/ne-mfidl-mftopology_dxva_mode) . O valor padrão é **MFTOPOLOGY \_ DXVA \_ Default**.

Esse atributo controla qual MFTs recebe um ponteiro para o Gerenciador de dispositivos do Direct3D. Para habilitar a aceleração de vídeo completa, defina o valor como **MFTOPOLOGY \_ DXVA \_ Full**. O valor **\_ \_ padrão de DXVA MFTOPOLOGY** é definido para compatibilidade com versões anteriores; ele corresponde ao comportamento de todas as versões mais antigas do Microsoft Media Foundation.

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

[Gerenciador de Dispositivos Direct3D](direct3d-device-manager.md)
</dt> <dt>

[Atributos de topologia](topology-attributes.md)
</dt> </dl>

 

 




