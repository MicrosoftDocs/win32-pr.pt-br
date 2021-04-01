---
description: Especifica se os metadados são gravados no arquivo transcodificado.
ms.assetid: 0fbfc035-c9d1-4014-a28a-93d7e6adc718
title: Atributo MF_TRANSCODE_SKIP_METADATA_TRANSFER (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54978d76ec1392c3be731e1452a653d1423976a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164756"
---
# <a name="mf_transcode_skip_metadata_transfer-attribute"></a>\_Atributo de \_ \_ transferência de metadados ignorar transcodificação MF \_

Especifica se os metadados são gravados no arquivo transcodificado. Esse atributo de contêiner é armazenado no perfil transcodificar.

## <a name="data-type"></a>Tipo de dados

**UINT32**

Os valores possíveis para o \_ atributo de transferência de metadados MF de ignorar transcodificação \_ \_ \_ são descritos na tabela a seguir.



| Valor                                                                        | Significado                                                                                             |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Transfere automaticamente os metadados em nível de arquivo do arquivo de origem para o arquivo transcodificado.<br/> |
| <dl> <dt>1</dt> </dl> | Os metadados do arquivo de origem não são gravados no arquivo transcodificado.<br/>                          |



 

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para definir esse atributo, chame [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

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

[**IMFTranscodeProfile:: getcontainerattributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-getcontainerattributes)
</dt> <dt>

[**IMFTranscodeProfile:: setcontainerattributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes)
</dt> </dl>

 

 




