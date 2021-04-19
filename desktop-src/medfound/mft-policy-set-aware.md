---
description: Especifica se o IMFTransform deseja receber notificações de conclusão de MEPolicySet.
title: MFT_POLICY_SET_AWARE (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2effa9eab2b0b126c2849d39ce7ffe3f62d81e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105814608"
---
# <a name="mft_policy_set_aware-attribute"></a>\_Atributo de \_ reconhecimento de conjunto de políticas de MFT \_

Se for diferente de zero, indica que o **IMFTransform** deseja receber notificações de conclusão de [MEPolicySet](./mepolicyset.md) .

## <a name="data-type"></a>Tipo de dados

**UINT32** (Tratado como **bool**)

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [**IMFAttributes:: GetUINT32**](/windows/win32/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para definir esse atributo, chame [**IMFAttributes:: setuint32**](/windows/win32/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Aplica-se a

[**IMFInputTrustAuthority**](/windows/win32/api/mfidl/nn-mfidl-imfinputtrustauthority)

## <a name="remarks"></a>Comentários

Este atributot pode ser usado por um **IMFInputTrustAuthority** Decrypter. Uma implementação de um módulo de descriptografia de conteúdo (CDM) pode incluir uma implementação de **IMFInputTrustAuthority**. O objeto **IMFInputTrustAuthority** é acessado por meio de [IMFContentDecryptionModule:: CreateTrustedInput](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmodule-createtrustedinput).


A constante de GUID para esse atributo é exportada de mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Atualização de abril de 2020 do Windows 10   <br/>                                        |
| parâmetro<br/>                   | <dl> <dt>Mftransform. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt>  <dt>

[Atributos de transformação](transform-attributes.md)
</dt> </dl>

 

 
