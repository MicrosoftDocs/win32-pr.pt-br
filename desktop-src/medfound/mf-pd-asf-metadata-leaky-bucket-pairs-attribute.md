---
description: Especifica uma lista de taxas de bits e janelas de buffer correspondentes para um arquivo de formato ASF (taxa de bits variável).
ms.assetid: e45d055f-d404-47e9-b3c8-ac743b290138
title: Atributo MF_PD_ASF_METADATA_LEAKY_BUCKET_PAIRS (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9444292ad437551622e1f418a6f21198ecd8341f01e4e5bda0a2047f847cfd37
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118740744"
---
# <a name="mf_pd_asf_metadata_leaky_bucket_pairs-attribute"></a>\_Atributo de \_ \_ pares de \_ buckets de vazamento de metadados \_ do MF PD ASF \_

Especifica uma lista de taxas de bits e janelas de buffer correspondentes para um arquivo de formato ASF (taxa de bits variável).

## <a name="data-type"></a>Tipo de dados

Matriz de bytes

## <a name="remarks"></a>Comentários

Esse atributo se aplica a descritores de apresentação para conteúdo ASF.

O método [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) gera esse atributo que se aplica ao descritor de apresentação para conteúdo ASF.

O valor do atributo tem o seguinte formato:

``` syntax
struct {
    WORD wReserved;
    WM_LEAKY_BUCKET_PAIR bucket[2];
};
```

A estrutura do **\_ \_ \_ par de buckets de vazamento do WM** é definida da seguinte maneira:

``` syntax
typedef struct _WMLeakyBucketPair {
  DWORD  dwBitrate;
  DWORD  msBufferWindow;
} WM_LEAKY_BUCKET_PAIR;
```

Para cada taxa de bits, o membro **msBufferWindow** indica a quantidade de conteúdo armazenada em buffer antes do início da reprodução, em milissegundos. O tamanho do buffer em bytes é igual a **msBufferWinow** x **dwBitrate** /8000.

> [!Note]  
> esse atributo corresponde ao atributo **ASFLeakyBucketPairs** no SDK do formato de mídia Windows.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                     |
| parâmetro<br/>                   | <dl> <dt>Wmcontainer. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes:: getBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**IMFAttributes:: setBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[Atributos do descritor de apresentação](presentation-descriptor-attributes.md)
</dt> <dt>

[Objeto de cabeçalho ASF](asf-file-structure.md)
</dt> <dt>

[Descritores de apresentação](presentation-descriptors.md)
</dt> </dl>

 

 




