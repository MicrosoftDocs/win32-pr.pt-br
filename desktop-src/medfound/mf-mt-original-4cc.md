---
description: Contém o codec original FOURCC para um fluxo de vídeo.
ms.assetid: 2e6ef198-5754-4ded-9fe3-61edd0742a17
title: Atributo MF_MT_ORIGINAL_4CC (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b374ba3ef74cb98925edcc5d809e1fd5e0b7fbcc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922393"
---
# <a name="mf_mt_original_4cc-attribute"></a>\_Atributo 4cc do MF MT \_ original \_

Contém o codec original FOURCC para um fluxo de vídeo.

## <a name="data-type"></a>Tipo de dados

**UINT32**

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para definir esse atributo, chame [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Aplica-se a

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a>Comentários

Dependendo do arquivo de origem, a origem da mídia AVI pode definir esse atributo nos tipos de mídia que ele oferece.

Um arquivo AVI contém um cabeçalho de fluxo para cada fluxo no arquivo. A fonte de mídia AVI converte o cabeçalho do fluxo em um tipo de mídia. Para fluxos de vídeo compactados, o cabeçalho de fluxo contém um FOURCC que identifica o codec de vídeo. Na maioria dos casos, a origem de mídia AVI converte esse FOURCC diretamente em um GUID de subtipo, conforme descrito no tópico [GUIDs de subtipo de vídeo](video-subtype-guids.md). Em alguns casos, no entanto, ele mapeia o FOURCC original para outro FOURCC que é equivalente. Nesse caso, a origem da mídia armazena o FOURCC original no tipo de mídia, usando o \_ atributo 4cc do MF MT \_ original \_ .

Os mapeamentos FOURCC são armazenados no registro sob a seguinte chave:

**HKEY \_ CLASSES \_ raiz** \\ **MediaFoundation** \\ **MapVideo4cc**

Cada entrada é um valor **DWORD** . O nome da entrada é a representação hexadecimal do FOURCC, sem um prefixo "0x", e com o primeiro caractere exibido primeiro na cadeia de caracteres. Por exemplo, o código FOURCC ' ABCD ' apareceria como "61626364". O valor da entrada é o código FOURCC equivalente.

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

 

 




