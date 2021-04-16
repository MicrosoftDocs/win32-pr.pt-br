---
description: Especifica se uma Media Foundation de transformação (MFT) dá suporte a alterações de formato dinâmico.
ms.assetid: 64d32c78-8bee-4d3c-a770-5a097cb71b13
title: Atributo MFT_SUPPORT_DYNAMIC_FORMAT_CHANGE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8224e9b7f0f05f430afac464e61900c7ce879fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105773019"
---
# <a name="mft_support_dynamic_format_change-attribute"></a>MFT \_ dá suporte ao \_ \_ atributo de alteração de formato dinâmico \_

Especifica se uma Media Foundation de transformação (MFT) dá suporte a alterações de formato dinâmico.

## <a name="data-type"></a>Tipo de dados

**UINT32**

Tratar como um valor booliano.

## <a name="remarks"></a>Comentários

Esse atributo pode ter os valores a seguir.



| Valor     | Descrição                                                            |
|-----------|------------------------------------------------------------------------|
| **TRUE**  | O cliente pode alterar o formato de entrada durante o streaming.               |
| **FALSE** | A MFT deve ser descarregada antes que o cliente possa alterar o formato de entrada. |



 

Para obter esse atributo, primeiro chame [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) para obter o repositório de atributo global para o MFT. Em seguida, chame [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) para obter o valor do atributo.

Se [**GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) falhar ou o atributo não estiver presente, o valor padrão se for **false**.

O [MFTs assíncrono](asynchronous-mfts.md) deve retornar o valor **true**.

Para obter mais informações, consulte [lidando com alterações de fluxo](handling-stream-changes.md).

A constante de GUID para esse atributo é exportada de mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Aplicativos de \[ aplicativos \| UWP do Windows Vista desktop\]<br/>                              |
| Servidor mínimo com suporte<br/> | Aplicativos do Windows Server 2008 \[ Desktop aplicativos \| UWP\]<br/>                        |
| parâmetro<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[MFTs assíncrona](asynchronous-mfts.md)
</dt> <dt>

[Atributos de transformação](transform-attributes.md)
</dt> <dt>

[**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
</dt> </dl>

 

 




