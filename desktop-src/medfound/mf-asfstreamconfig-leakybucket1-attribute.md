---
description: Define a média &\# 0034; o Bucket de vazamento&\# 0034; parâmetros (consulte comentários) para codificar um arquivo de mídia do Windows. Defina esse atributo usando a interface IMFASFStreamConfig.
ms.assetid: 5aa570eb-1004-4942-9a63-b8f6373d4e53
title: Atributo MF_ASFSTREAMCONFIG_LEAKYBUCKET1 (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4db383d19ff5009ccc9fc3203281e04000870474
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105759860"
---
# <a name="mf_asfstreamconfig_leakybucket1-attribute"></a>\_Atributo MF ASFSTREAMCONFIG \_ LEAKYBUCKET1

Define os parâmetros médios de "Bucket de vazamentos" (consulte comentários) para codificar um arquivo de mídia do Windows. Defina esse atributo usando a interface [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) .

## <a name="data-type"></a>Tipo de dados

Matriz de bytes

## <a name="remarks"></a>Comentários

O valor desse atributo é uma matriz de três **DWORD** s, na seguinte ordem:

-   Taxa de bits, em bits por segundo.
-   Janela buffer, em milissegundos.
-   Total do buffer inicial, em bytes.

Para obter mais informações sobre o conceito de Bucket de vazamento, consulte o tópico [o modelo de buffer de buckets de vazamento](the-leaky-bucket-buffer-model.md) na documentação do SDK do Windows Media Format.

A constante de GUID para esse atributo é exportada de mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                     |
| parâmetro<br/>                   | <dl> <dt>Wmcontainer. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos ASF](asf-attributes.md)
</dt> <dt>

[**IMFAttributes:: getBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**IMFAttributes:: setBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[**\_ASFSTREAMCONFIG MF \_ LEAKYBUCKET2**](mf-asfstreamconfig-leakybucket2-attribute.md)
</dt> </dl>

 

 




