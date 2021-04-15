---
description: Especifica se o chamador vai alocar as texturas usadas para saída.
ms.assetid: CAB41B22-AD96-4932-9686-66474CB26C38
title: Atributo MF_XVP_CALLER_ALLOCATES_OUTPUT (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: def1b1d138c031393e1a1b1a3832c1ad6d066306
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502103"
---
# <a name="mf_xvp_caller_allocates_output-attribute"></a>O \_ chamador XVP do MF \_ aloca o atributo de \_ \_ saída

Especifica se o chamador vai alocar as texturas usadas para saída.

## <a name="data-type"></a>Tipo de dados

**Bool** armazenado como **UINT32**

## <a name="remarks"></a>Comentários

Se esse atributo for **true**, o processador de vídeo esperará que as texturas de saída sejam alocadas pelo chamador, mesmo quando estiverem operando no modo DXVA (aceleração de vídeo do DirectX). Se esse atributo for **false**, o processador de vídeo alocará as texturas de saída ao operar no modo de DXVA e falhará se as texturas de saída fornecidas pelo chamador forem fornecidas.

Para definir este atributo:

1.  Chame [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) no processador de vídeo.
2.  Chamar [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

Defina o atributo antes de o streaming começar.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10\]<br/>                                          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2016\]<br/>                                 |
| parâmetro<br/>                   | <dl> <dt>Mfidl. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>Mfidl. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




