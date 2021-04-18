---
description: Especifica o tipo de carga de um fluxo AAC (codificação de áudio avançado).
ms.assetid: a032fcf4-2584-4047-adbd-d94d4fc4e841
title: Atributo MF_MT_AAC_PAYLOAD_TYPE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd3edba98bdac54b12fb6e3e44fb67373f7fce6a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105772687"
---
# <a name="mf_mt_aac_payload_type-attribute"></a>\_Atributo de \_ \_ tipo de conteúdo MF MT AAC \_

Especifica o tipo de carga de um fluxo AAC (codificação de áudio avançado).

## <a name="data-type"></a>Tipo de dados

**UINT32**

Os valores a seguir são possíveis.



| Valor                                                                        | Significado                                                                                                                           |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | O fluxo contém \_ apenas elementos de bloco de dados brutos \_ .<br/>                                                                    |
| <dl> <dt>1</dt> </dl> | Fluxo de transporte de dados de áudio (ADTS). O fluxo contém uma \_ sequência ADTS, conforme definido por MPEG-2.<br/>                       |
| <dl> <dt>2</dt> </dl> | Formato de intercâmbio de dados de áudio (ADIF). O fluxo contém uma \_ sequência ADIF, conforme definido por MPEG-2.<br/>                     |
| <dl> <dt>3</dt> </dl> | O fluxo contém um fluxo de transporte de áudio MPEG-4 com uma camada de sincronização (LOAS) e uma camada de Multiplex (LATM).<br/> |



 

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para definir esse atributo, chame [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Aplica-se A

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a>Comentários

O \_ tipo de conteúdo MF MT \_ AAC \_ \_ é opcional. Se esse atributo não for especificado, o valor padrão 0 será usado, o que especificará que o fluxo contém \_ apenas elementos de bloco de dados brutos \_ .

Aplica-se somente ao **MFAudioFormat \_ AAC**.

A constante de GUID para esse atributo é exportada de mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de tipo de mídia](media-type-attributes.md)
</dt> </dl>

 

 




