---
description: Dados específicos de tipo para um fluxo binário em um arquivo ASF (Advanced Systems Format).
ms.assetid: 45608dde-894b-4204-80dc-505f068fb158
title: MF_MT_ARBITRARY_HEADER atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55d824aad4f76947786f991807d2f7b301703e3e356d2d1cfb416aa634d49f93
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119826516"
---
# <a name="mf_mt_arbitrary_header-attribute"></a>Atributo DE \_ \_ \_ HEADER ARBITRÁRIO MF MT

Dados específicos de tipo para um fluxo binário em um arquivo ASF (Advanced Systems Format).

## <a name="data-type"></a>Tipo de dados

**[**MT \_ HEADER \_ ARBITRÁRIO**](/windows/desktop/api/mfapi/ns-mfapi-mt_arbitrary_header)** armazenado como **BYTE \[ \]**

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [**IMFAttributes::GetBlob.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)

Para definir esse atributo, chame [**IMFAttributes::SetBlob.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)

## <a name="remarks"></a>Comentários

Arquivos ASF podem conter fluxos com dados binários. O atributo MF MT ARBITRARY HEADER no tipo de mídia contém uma estrutura \_ \_ DE \_ [**\_ \_ HEADER ARBITRÁRIO MT**](/windows/desktop/api/mfapi/ns-mfapi-mt_arbitrary_header) que descreve o fluxo.

Além do atributo \_ MF MT ARBITRARY HEADER, o tipo de mídia para um \_ \_ fluxo binário ASF contém os seguintes atributos:



| Atributo                                                 | Descrição                                            |
|-----------------------------------------------------------|--------------------------------------------------------|
| [**MF \_ MT \_ MAJOR \_ TYPE**](mf-mt-major-type-attribute.md) | O valor do atributo é **Binário MFMediaType. \_** |
| [FORMATO \_ \_ ARBITRÁRIO MF MT \_](mf-mt-arbitrary-format.md)   | Contém dados de formato adicionais.                       |



 

> [!Note]  
> No SDK Windows Formato de Mídia, os fluxos binários são chamados de *fluxos* arbitrários ou fluxos de *dados arbitrários.*

 

A constante GUID para esse atributo é exportada de mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>                                         |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do Server 2008 R2 \[\]<br/>                            |
| Cabeçalho<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de tipo de mídia](media-type-attributes.md)
</dt> </dl>

 

 




