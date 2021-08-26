---
description: Especifica se uma transformação Media Foundation (MFT) dá suporte a alterações de formato dinâmico.
ms.assetid: 64d32c78-8bee-4d3c-a770-5a097cb71b13
title: MFT_SUPPORT_DYNAMIC_FORMAT_CHANGE atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3286d9bfd2185006975cf128cc60f2b774eba6ba74229b3e290c743c4cde3930
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012606"
---
# <a name="mft_support_dynamic_format_change-attribute"></a>Atributo MFT \_ SUPPORT \_ DYNAMIC FORMAT \_ \_ CHANGE

Especifica se uma transformação Media Foundation (MFT) dá suporte a alterações de formato dinâmico.

## <a name="data-type"></a>Tipo de dados

**UINT32**

Trate como um valor booliana.

## <a name="remarks"></a>Comentários

Esse atributo pode ter os valores a seguir.



| Valor     | Descrição                                                            |
|-----------|------------------------------------------------------------------------|
| **TRUE**  | O cliente pode alterar o formato de entrada durante o streaming.               |
| **FALSE** | O MFT deve ser esvaziado antes que o cliente possa alterar o formato de entrada. |



 

Para obter esse atributo, primeiro chame [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) para obter o armazenamento de atributo global para o MFT. Em [**seguida, chame IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) para obter o valor do atributo.

Se [**GetAttributes falhar**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) ou o atributo não estiver presente, o valor padrão será **FALSE.**

[Os MFTs assíncronos](asynchronous-mfts.md) devem retornar o valor **TRUE.**

Para obter mais informações, consulte [Tratamento de alterações de fluxo.](handling-stream-changes.md)

A constante GUID para esse atributo é exportada de mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Aplicativos \| UWP de aplicativos da área de trabalho do Vista\]<br/>                              |
| Servidor mínimo com suporte<br/> | Windows Aplicativos \[ UWP do Server 2008 Desktop \|\]<br/>                        |
| Cabeçalho<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[MFTs assíncronos](asynchronous-mfts.md)
</dt> <dt>

[Transformar atributos](transform-attributes.md)
</dt> <dt>

[**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
</dt> </dl>

 

 




