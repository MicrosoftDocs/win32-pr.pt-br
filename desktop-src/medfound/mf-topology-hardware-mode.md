---
description: Especifica se é para carregar transformações de Microsoft Media Foundation baseadas em hardware (MFTs) na topologia.
ms.assetid: f7ac3c9b-c163-412f-84c0-27bf551091d8
title: Atributo MF_TOPOLOGY_HARDWARE_MODE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52da08dc1da36072f02627ec632bb8caf189c1748545c1ded5c3e4ebdedc1234
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117875663"
---
# <a name="mf_topology_hardware_mode-attribute"></a>\_Atributo de \_ modo de hardware de topologia MF \_

Especifica se é para carregar transformações de Microsoft Media Foundation baseadas em hardware (MFTs) na topologia.

## <a name="data-type"></a>Tipo de dados

**[**MFTOPOLOGY \_ \_Modo de hardware**](/windows/desktop/api/mfidl/ne-mfidl-mftopology_hardware_mode)** armazenado como **UINT32**

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para definir esse atributo, chame [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Aplica-se a

[**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a>Comentários

Esse atributo é opcional. Defina o atributo antes de resolver a topologia.



| Valor                                  | Descrição                                                                                                                                                                                                                                                                       |
|----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **MFTOPOLOGY \_ HWMODE \_ usar \_ hardware**  | O carregador de topologia carregará MFTs baseadas em hardware, como decodificadores de hardware, quando disponível.<br/> O carregador de topologia voltará automaticamente para a decodificação de software se nenhum decodificador de hardware for encontrado ou se um decodificador de hardware não conseguir se conectar por algum motivo.<br/> |
| **\_somente MFTOPOLOGY HWMODE \_ software \_** | O carregador de topologia carregará apenas MFTs de software, incluindo os decodificadores de software.                                                                                                                                                                                                    |



 

O valor padrão é **MFTOPOLOGY \_ HWMODE \_ software \_ apenas**, para compatibilidade com os aplicativos existentes. O valor recomendado é **MFTOPOLOGY \_ HWMODE \_ use \_ hardware**.

Se o carregador de topologia inserir uma MFT de hardware na topologia, ele definirá o atributo de atributo de URL de hardware de enumeração de MFT no nó de topologia. [ \_ \_ \_ \_ ](mft-enum-hardware-url-attribute.md) Para verificar se um MFT de hardware está presente, enumere os nós na topologia resolvida e verifique se esse atributo está presente.

A constante de GUID para esse atributo é exportada de mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[somente aplicativos de área de trabalho Windows 7\]<br/>                                         |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do Server 2008 R2\]<br/>                            |
| Cabeçalho<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de topologia](topology-attributes.md)
</dt> </dl>

 

 




