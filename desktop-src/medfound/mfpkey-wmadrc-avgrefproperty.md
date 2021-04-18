---
description: Especifica o nível médio de volume de conteúdo de áudio.
ms.assetid: eabb36ff-300f-4ed1-aca3-9415627ac1a7
title: Propriedade MFPKEY_WMADRC_AVGREF (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf18c37b00f84cc3ae3fdf1f44b2fbefcc56d9f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105756330"
---
# <a name="mfpkey_wmadrc_avgref-property"></a>\_Propriedade MFPKEY WMADRC \_ AVGREF

Especifica o nível médio de volume de conteúdo de áudio.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMADRCAverageReference

## <a name="data-type"></a>Tipo de Dados

\_I4 VT

## <a name="remarks"></a>Comentários

Você pode obter esse valor do codificador depois que o conteúdo é processado. Esse valor também pode ser definido no decodificador para a finalidade do controle de intervalo dinâmico, mas terá efeito somente se a propriedade [MFPKEY \_ WMADEC \_ DRCMODE](mfpkey-wmadec-drcmodeproperty.md) for definida.

Para obter mais informações sobre o controle de intervalo dinâmico, consulte o artigo da Web [recursos de codec do Windows Media Audio Professional](/previous-versions/ms867218(v=msdn.10)).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                             |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                    |
| parâmetro<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
