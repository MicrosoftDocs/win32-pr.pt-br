---
description: Especifica se uma Media Foundation de transformação (MFT) é registrada somente no processo de aplicativos.
ms.assetid: e10d6378-8e85-4f73-9fa3-a2e954fc8249
title: Atributo MFT_PROCESS_LOCAL_Attribute (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d1d3595ef530008b8d09f27e3e76fad81a06039
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103661492"
---
# <a name="mft_process_local_attribute-attribute"></a>\_Atributo de \_ atributo local do processo de MFT \_

Especifica se uma Media Foundation de transformação (MFT) é registrada somente no processo do aplicativo.

## <a name="data-type"></a>Tipo de dados

**UINT32**

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para definir esse atributo, chame [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Comentários

Esse atributo é usado da seguinte maneira:

1.  O aplicativo registra um MFT local chamando a função [**MFTRegisterLocal**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocal) ou [**MFTRegisterLocalByCLSID**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocalbyclsid) . Essas funções registram o MFT no processo do aplicativo.
2.  A função [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) é chamada para enumerar MFTs que correspondem a um conjunto específico de critérios. O aplicativo pode chamar a função **MFTEnumEx** diretamente, mas, mais frequentemente, essa função é chamada pelo carregador de topologia.
3.  A função [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) recupera uma matriz de ponteiros [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) , cada um representando um objeto de ativação para um MFT. Se uma MFT for registrada localmente, o \_ atributo local do processo de MFT \_ \_ será definido como **true** no objeto de ativação correspondente.

O valor padrão para esse atributo é **false**.

A constante de GUID para esse atributo é exportada de mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Aplicativos de \[ aplicativos da área de trabalho do Windows 7 \| UWP\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2008 R2 \|\]<br/>                           |
| parâmetro<br/>                   | <dl> <dt>Mftransform. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de transformação](transform-attributes.md)
</dt> </dl>

 

 




