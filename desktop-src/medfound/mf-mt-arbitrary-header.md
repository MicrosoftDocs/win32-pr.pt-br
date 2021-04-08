---
description: Dados específicos de tipo para um fluxo binário em um arquivo ASF (Advanced Systems Format).
ms.assetid: 45608dde-894b-4204-80dc-505f068fb158
title: Atributo MF_MT_ARBITRARY_HEADER (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abd559ede3506335378ae1d56bf5b886e1407946
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010715"
---
# <a name="mf_mt_arbitrary_header-attribute"></a>\_Atributo de \_ cabeçalho arbitrário MF MT \_

Dados específicos de tipo para um fluxo binário em um arquivo ASF (Advanced Systems Format).

## <a name="data-type"></a>Tipo de dados

**[**MT \_ \_Cabeçalho arbitrário**](/windows/desktop/api/mfapi/ns-mfapi-mt_arbitrary_header)** armazenado como **byte \[ \]**

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [**IMFAttributes:: getBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).

Para definir esse atributo, chame [**IMFAttributes:: setBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).

## <a name="remarks"></a>Comentários

Os arquivos ASF podem conter fluxos com dados binários. O \_ atributo de \_ cabeçalho arbitrário MF MT \_ no tipo de mídia contém uma estrutura de [**\_ \_ cabeçalho arbitrário MT**](/windows/desktop/api/mfapi/ns-mfapi-mt_arbitrary_header) que descreve o fluxo.

Além do \_ \_ atributo de cabeçalho arbitrário MF MT \_ , o tipo de mídia para um fluxo binário ASF contém os seguintes atributos:



| Atributo                                                 | Descrição                                            |
|-----------------------------------------------------------|--------------------------------------------------------|
| [**\_ \_ tipo principal MF \_ MT**](mf-mt-major-type-attribute.md) | O valor do atributo é **\_ binário MFMediaType**. |
| [\_ \_ formato ARBITRÁRIO do MF MT \_](mf-mt-arbitrary-format.md)   | Contém dados de formato adicionais.                       |



 

> [!Note]  
> No SDK do Windows Media Format, os fluxos binários são chamados de *fluxos arbitrários* ou *fluxos de dados arbitrários*.

 

A constante de GUID para esse atributo é exportada de mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                         |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]<br/>                            |
| parâmetro<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de tipo de mídia](media-type-attributes.md)
</dt> </dl>

 

 




