---
description: Dados de formato adicionais para um fluxo binário em um arquivo ASF (Advanced Systems Format).
ms.assetid: fc5b9890-1508-498e-b2ce-ed4fa2052f9c
title: Atributo MF_MT_ARBITRARY_FORMAT (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6cf98da23fbc4631ca67462dfc58f870abe73885
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105793889"
---
# <a name="mf_mt_arbitrary_format-attribute"></a>\_Atributo de \_ \_ formato arbitrário do MF MT

Dados de formato adicionais para um fluxo binário em um arquivo ASF (Advanced Systems Format).

## <a name="data-type"></a>Tipo de dados

**MINUCIOSA\[\]**

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [**IMFAttributes:: getBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).

Para definir esse atributo, chame [**IMFAttributes:: setBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).

## <a name="remarks"></a>Comentários

Os aplicativos podem usar fluxos binários para manter tipos de dados personalizados. A fonte de mídia do ASF trata o valor desse atributo como um blob opaco. O membro **formatType** da estrutura [**de \_ \_ cabeçalho arbitrário MT**](/windows/desktop/api/mfapi/ns-mfapi-mt_arbitrary_header) define o layout dos dados de formato.

Essa estrutura corresponde ao campo formatar dados dos dados específicos do tipo no objeto Propriedades do fluxo, em arquivos em que o tipo de fluxo é **\_ \_ mídia binária de ASF**. Para obter mais informações, consulte a especificação do ASF.

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
</dt> <dt>

[\_ \_ cabeçalho ARBITRÁRIO do MF MT \_](mf-mt-arbitrary-header.md)
</dt> </dl>

 

 




