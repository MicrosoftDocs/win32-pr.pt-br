---
description: Especifica se o leitor de origem habilita a DXVA (aceleração de vídeo do DirectX) no decodificador de vídeo.
ms.assetid: ec539038-3fd3-41b7-a0e6-e75e3f2828a7
title: Atributo MF_SOURCE_READER_DISABLE_DXVA (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9362f067d1d6ceae426e9ee6530e08b95837595f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297396"
---
# <a name="mf_source_reader_disable_dxva-attribute"></a>\_Leitor de origem MF \_ \_ desabilitar \_ atributo DXVA

Especifica se o [leitor de origem](source-reader.md) HABILITA a DXVA (aceleração de vídeo do DirectX) no decodificador de vídeo.

## <a name="data-type"></a>Tipo de dados

**UINT32**

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para definir esse atributo, chame [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Comentários

Esse atributo se aplicará se as seguintes condições forem verdadeiras:

-   O leitor de origem decodifica um fluxo de vídeo.
-   O decodificador de vídeo dá suporte à decodificação de DXVA.
-   O aplicativo usa o atributo de Gerenciador de [ \_ leitura de leitor de origem \_ \_ \_ MF](mf-source-reader-d3d-manager.md) para definir o [Direct3D gerenciador de dispositivos](direct3d-device-manager.md) no leitor de origem.

Esse atributo permite que o aplicativo desabilite o DXVA enquanto estiver decodificando as superfícies do Direct3D.

Por padrão, o leitor de origem usa o [Gerenciador de dispositivos Direct3D](direct3d-device-manager.md) para duas finalidades:

-   Para habilitar a decodificação de DXVA no decodificador de vídeo.
-   Para alocar superfícies do Direct3D para os exemplos de vídeo.

Se o valor do leitor de \_ origem \_ MF \_ desabilitar o \_ atributo DXVA for **true**, o leitor de origem desabilita a decodificação de dxva, embora ainda use o [Gerenciador de dispositivos Direct3D](direct3d-device-manager.md) para alocar superfícies Direct3D.

Se o [atributo \_ \_ \_ \_ Gerenciador D3D do leitor de origem MF](mf-source-reader-d3d-manager.md) não estiver definido, o \_ atributo DXVA desabilitar o leitor de origem MF \_ \_ \_ será ignorado.

O valor padrão desse atributo é **false**, o que significa que a decodificação de DXVA está habilitada quando disponível.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Aplicativos de \[ aplicativos da área de trabalho do Windows 7 \| UWP\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2008 R2 \|\]<br/>                           |
| parâmetro<br/>                   | <dl> <dt>Mfreadwrite. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Leitor de origem](source-reader.md)
</dt> <dt>

[Atributos do leitor de origem](source-reader-attributes.md)
</dt> </dl>

 

 




