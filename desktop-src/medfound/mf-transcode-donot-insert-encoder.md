---
description: Especifica se um codificador deve ser incluído na topologia de transcodificação.
ms.assetid: 73f23aed-d1b9-4821-b1ca-0a07f02b6913
title: Atributo MF_TRANSCODE_DONOT_INSERT_ENCODER (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92d3f8fc5dabfd3e4c55c6242ba9b8f52b6f5c2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105764084"
---
# <a name="mf_transcode_donot_insert_encoder-attribute"></a>\_Atributo de \_ \_ \_ CODIFICAdor INSERT não cercamento MF

Especifica se um codificador deve ser incluído na topologia de transcodificação.

A função [**MFCreateTranscodeTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodetopology) verifica esse atributo durante a compilação da topologia. Se esse atributo não for definido, um codificador será inserido na topologia de transcodificação.

## <a name="data-type"></a>Tipo de dados

**UINT32**



| Valor                                                                        | Significado                                                                                                           |
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Um codificador é inserido na topologia de transcodificação.<br/>                                                      |
| <dl> <dt>1</dt> </dl> | Um codificador não está incluído na topologia de transcodificação. O nó de origem está conectado ao nó de saída.<br/> |



 

## <a name="remarks"></a>Comentários

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

[Atributos de Media Foundation](media-foundation-attributes.md)
</dt> </dl>

 

 




