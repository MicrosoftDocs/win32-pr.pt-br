---
description: define o pico &\# 0034; o bucket de vazamento&\# 0034; parâmetros (consulte comentários) para codificar um arquivo de mídia Windows. Esses parâmetros são usados para a taxa de bits de pico. Defina esse atributo usando a interface IMFASFStreamConfig.
ms.assetid: 422d6d1b-4d29-4156-877b-8dc3bcb7580f
title: Atributo MF_ASFSTREAMCONFIG_LEAKYBUCKET2 (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a540cab766cbd6a6a7246139d0e19e12c89e5ed837d40cdc3e10d9589f72ebe5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060836"
---
# <a name="mf_asfstreamconfig_leakybucket2-attribute"></a>\_Atributo MF ASFSTREAMCONFIG \_ LEAKYBUCKET2

define o pico dos parâmetros de "bucket de vazamentos" (consulte comentários) para codificar um arquivo de mídia Windows. Esses parâmetros são usados para a taxa de bits de pico. Defina esse atributo usando a interface [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) .

## <a name="data-type"></a>Tipo de dados

Matriz de bytes

## <a name="remarks"></a>Comentários

O valor desse atributo é uma matriz de três **DWORD** s, na seguinte ordem:

-   Taxa de bits, em bits por segundo.
-   Janela buffer, em milissegundos.
-   Total do buffer inicial, em bytes.

para obter mais informações sobre o conceito de bucket de vazamento, consulte o tópico [o modelo de Buffer de buckets de vazamento](the-leaky-bucket-buffer-model.md) na documentação do SDK do formato de mídia do Windows.

A constante de GUID para esse atributo é exportada de mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                     |
| Cabeçalho<br/>                   | <dl> <dt>Wmcontainer. h</dt> </dl> |



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

[**\_ASFSTREAMCONFIG MF \_ LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md)
</dt> </dl>

 

 




