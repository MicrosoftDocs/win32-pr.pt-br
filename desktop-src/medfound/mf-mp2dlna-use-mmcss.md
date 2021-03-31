---
description: Especifica se o coletor de mídia de rede de vida digital (DLNA) usa o serviço do Agendador de classes de multimídia (MMCSS).
ms.assetid: 4c27e2ec-624a-4b1f-bea9-3aaad1534c9b
title: Atributo MF_MP2DLNA_USE_MMCSS (Mfmp2dlna. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ccfdaf36ce51f1158e110dcb3682a5b072c060dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011100"
---
# <a name="mf_mp2dlna_use_mmcss-attribute"></a>MF \_ MP2DLNA \_ usar o \_ atributo MMCSS

Especifica se o coletor de mídia de rede de vida digital (DLNA) usa o serviço do Agendador de classes de multimídia (MMCSS).

## <a name="data-type"></a>Tipo de dados

**Bool** armazenado como **UINT32**

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para definir esse atributo, chame [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Comentários

Para definir esse atributo no coletor de mídia DLNA, consulte o coletor de mídia para a interface [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) . Defina o atributo antes de o streaming começar.

Se esse atributo for **true**, o coletor de mídia DLNA se registrará com o MMCSS.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                             |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]<br/>                                |
| parâmetro<br/>                   | <dl> <dt>Mfmp2dlna. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




