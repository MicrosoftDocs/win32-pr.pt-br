---
description: Especifica a classe do serviço do Agendador de classes de multimídia (MMCSS) para o thread de decodificação.
ms.assetid: 77724879-62e4-439e-9dd0-3642cd7f75ca
title: Propriedade AVDecMmcss (UUIDs. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0092ac516f9600929a9772d044f51e7e375548d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105768412"
---
# <a name="avdecmmcss-property"></a>Propriedade AVDecMmcss

Especifica a classe do serviço do Agendador de classes de multimídia (MMCSS) para o thread de decodificação.

Esta propriedade é de leitura/gravação.

## <a name="data-type"></a>Tipo de dados

**BSTR** (**VT \_ BSTR**)

## <a name="property-guid"></a>GUID da propriedade

**CODECAPI \_ AVDecMmcssClass**

## <a name="property-value"></a>Valor da propriedade

O valor dessa propriedade é o nome da classe do MMCSS.

## <a name="remarks"></a>Comentários

O MMCSS permite que os aplicativos garantam que o processamento sensível ao tempo tem acesso prioritário aos recursos da CPU. Ele funciona elevando threads registrados para prioridades de thread mais altas enquanto reduz periodicamente suas prioridades para gerar tempo para outros processos.

O valor recomendado para decodificadores de áudio é "áudio", e o valor recomendado para decodificadores de vídeo é "reprodução".

Se o serviço do MMCSS não estiver disponível ou se a classe do MMCSS especificada não existir, a definição da propriedade não terá nenhum efeito.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>UUIDs. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades da API do codec](codec-api-properties.md)
</dt> <dt>

[**Interface ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




