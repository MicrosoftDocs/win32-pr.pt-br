---
description: Especifica se um buffer contém o início de um pacote ASF (Advanced Systems Format).
ms.assetid: eca3f9b7-6051-4654-8016-a9c679519bc7
title: Atributo MFASFSPLITTER_PACKET_BOUNDARY (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0904c6b5a002d6aa18361365946a176521674ea22f7a45cc042b89d844c4210d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119464056"
---
# <a name="mfasfsplitter_packet_boundary-attribute"></a>Atributo de limite de \_ pacote MFASFSPLITTER \_

Especifica se um buffer contém o início de um pacote ASF (Advanced Systems Format).

## <a name="data-type"></a>Tipo de dados

**UINT32**

Tratar como um valor booliano.

## <a name="remarks"></a>Comentários

Se um buffer de mídia expor a interface [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) por meio de **QueryInterface** e o valor desse atributo for diferente de zero, o divisor de ASF tratará o buffer como o início de um novo pacote.

Esse atributo se aplicará se você estiver usando o divisor de ASF para analisar dados ASF. Se os dados do ASF tiverem comprimentos de pacotes variáveis, você deverá definir esse atributo nos buffers de mídia que passar para o método [**IMFASFSplitter::P arsedata**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-parsedata) . Defina o atributo como **true** se o buffer contiver o início de um novo pacote. Se o buffer contiver uma continuação do pacote anterior, defina o atributo como **false**. Os buffers não podem abranger vários pacotes.

Para dados ASF com tamanhos de pacotes fixos, esse atributo não é necessário e um buffer pode abranger vários pacotes.

Observe que as implementações padrão do [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) fornecido pelo Media Foundation não expõem [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes). Para usar esse atributo, você deve fornecer sua própria implementação de **IMFMediaBuffer**; por exemplo, encapsulando os buffers retornados por [**MFCreateMemoryBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatememorybuffer).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                     |
| parâmetro<br/>                   | <dl> <dt>Wmcontainer. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos ASF](asf-attributes.md)
</dt> <dt>

[**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer)
</dt> </dl>

 

 




