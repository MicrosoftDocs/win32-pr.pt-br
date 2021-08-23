---
description: Especifica se o chamador vai alocar as texturas usadas para saída.
ms.assetid: CAB41B22-AD96-4932-9686-66474CB26C38
title: Atributo MF_XVP_CALLER_ALLOCATES_OUTPUT (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31da89bec9c9573d9d968077e51d413e1861bca28cb606667d402fab5a408f96
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119599966"
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
| Cliente mínimo com suporte<br/> | Windows 10 \[ somente aplicativos da área de trabalho\]<br/>                                          |
| Servidor mínimo com suporte<br/> | Windows Server 2016 \[ somente aplicativos da área de trabalho\]<br/>                                 |
| Cabeçalho<br/>                   | <dl> <dt>Mfidl. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>Mfidl. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




