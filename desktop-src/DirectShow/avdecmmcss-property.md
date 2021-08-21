---
description: Especifica a classe MMCSS (Serviço de Agendador de Classe Multimídia) para o thread de decodificação.
ms.assetid: 77724879-62e4-439e-9dd0-3642cd7f75ca
title: Propriedade AVDecMmcss (Uuids.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b9084db3cce8d555afa44097271a6b08f58cfea2f2edcb7acb5845730afc86b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118159940"
---
# <a name="avdecmmcss-property"></a>Propriedade AVDecMmcss

Especifica a classe MMCSS (Serviço de Agendador de Classe Multimídia) para o thread de decodificação.

Essa propriedade é leitura/gravação.

## <a name="data-type"></a>Tipo de dados

**BSTR** (**VT \_ BSTR**)

## <a name="property-guid"></a>GUID da propriedade

**CODECAPI \_ AVDecMmcssClass**

## <a name="property-value"></a>Valor da propriedade

O valor dessa propriedade é o nome da classe MMCSS.

## <a name="remarks"></a>Comentários

O MMCSS permite que os aplicativos assegurem que o processamento sensível ao tempo tenha priorizado o acesso aos recursos da CPU. Ele funciona elevando threads registrados para prioridades de thread mais altas enquanto diminui periodicamente suas prioridades para gerar tempo para outros processos.

O valor recomendado para decodificadores de áudio é "Áudio" e o valor recomendado para decodificadores de vídeo é "Reprodução".

Se o serviço MMCSS não estiver disponível ou se a classe MMCSS especificada não existir, definir a propriedade não terá nenhum efeito.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Uuids.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades da API do Codec](codec-api-properties.md)
</dt> <dt>

[**ICodecAPI Interface**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




