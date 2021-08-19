---
description: Armazena uma matriz de bytes que representa a licença DRM associada ao fluxo de bytes.
ms.assetid: 866a9706-0b0a-4675-af61-5f55a5a69014
title: Propriedade MFNETSOURCE_DRMNET_LICENSE_REPRESENTATION (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2718ba8a13d8d0c00114449f1141be77db0d3f83930d3b3de2171719c3bdf2d0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113546"
---
# <a name="mfnetsource_drmnet_license_representation-property"></a>\_Propriedade de \_ representação de licença MFNETSOURCE DRMNET \_

Armazena uma matriz de bytes que representa a licença DRM associada ao fluxo de bytes.



Tipo de dados

Tipo PROPVARIANT (VT)

Membro PROPVARIANT

Matriz de bytes (**blob**)

\_blob VT

**blob**



## <a name="remarks"></a>Comentários

A **representação de \_ \_ licença DRMNET \_ constante MFNETSOURCE** define o GUID para essa chave de propriedade. O identificador de propriedade (PID) é zero.

Esta propriedade é somente para leitura. Para obter o valor da Propriedade do fluxo de bytes de rede, chame **IPropertyStore:: GetValue** e passe a estrutura **PROPERTYKEY** no parâmetro de *chave* . O membro **fmtid** de **PROPERTYKEY** deve ser definido como a propriedade GUID.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                               |
| Cabeçalho<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades de Media Foundation](media-foundation-properties.md)
</dt> <dt>

[Rede em Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




