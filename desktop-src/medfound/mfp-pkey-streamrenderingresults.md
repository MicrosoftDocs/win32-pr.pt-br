---
description: Especifica quais fluxos foram conectados com êxito a um coletor de mídia.
ms.assetid: b5e45bfc-d91d-41b8-aaa4-72b3a23d869e
title: Propriedade MFP_PKEY_StreamRenderingResults (Mfplay. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6acf04f751e8611f3add3a62fc7b4406d757999e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296434"
---
# <a name="mfp_pkey_streamrenderingresults-property"></a>\_Propriedade PKEY \_ STREAMRENDERINGRESULTS de MFP

> [!IMPORTANT]
> Preterido. Essa API pode ser removida de versões futuras do Windows. Os aplicativos devem usar a [sessão de mídia](media-session.md) para reprodução.

 

Especifica quais fluxos foram conectados com êxito a um coletor de mídia.



Tipo de dados

Tipo PROPVARIANT (VT)

Membro PROPVARIANT

Matriz de valores **DWORD** (**Caul**)

\_UI4 de vetor \| VT \_ VT

**caul**



## <a name="remarks"></a>Comentários

Essa propriedade pode ser enviada com o **\_ tipo de evento MFP \_ \_ MEDIAITEM \_ set** Event.

O valor da propriedade é uma matriz de **HRESULT** s. As entradas de matriz correspondem aos fluxos no item de mídia atual. Cada entrada na matriz indica se o fluxo correspondente foi conectado a um coletor de mídia, da seguinte maneira:

-   Se o fluxo estiver conectado a um coletor de mídia, o valor será **S \_ OK**.
-   Se o fluxo não estiver selecionado, o valor será **S \_ false**.
-   Se um erro ocorreu ao tentar conectar o fluxo, o valor é um código de erro.

Se pelo menos um fluxo foi conectado com êxito, a reprodução é possível. Por exemplo, o usuário pode ter o codec necessário para reproduzir o fluxo de áudio, mas não para reproduzir o fluxo de vídeo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]<br/>                             |
| parâmetro<br/>                   | <dl> <dt>Mfplay. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades de Media Foundation](media-foundation-properties.md)
</dt> <dt>

[**\_MEDIAITEM de \_ conjunto de \_ eventos da MFP**](/windows/desktop/api/mfplay/ns-mfplay-mfp_mediaitem_set_event)
</dt> </dl>

 

 




