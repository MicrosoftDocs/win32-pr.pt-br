---
description: Especifica se o codificador produz grupos abertos de imagens (GOPS segundos) ou GOPS segundos fechado. Essa propriedade se aplica a codificadores de vídeo MPEG.
ms.assetid: 424751cd-65d2-4cab-9f7b-cad50c09c767
title: Propriedade AVEncMPVGOPOpen (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6dd971a6cc9926245b97794868f58758af814803
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103646006"
---
# <a name="avencmpvgopopen-property"></a>Propriedade AVEncMPVGOPOpen

Especifica se o codificador produz grupos abertos de imagens (GOPS segundos) ou GOPS segundos fechado. Essa propriedade se aplica a codificadores de vídeo MPEG.

Esta propriedade é de leitura/gravação.

## <a name="data-type"></a>Tipo de dados

**Variante \_ BOOL** (**VT \_ bool**)

## <a name="property-guid"></a>GUID da propriedade

**CODECAPI \_ AVEncMPVGOPOpen**

## <a name="property-value"></a>Valor da propriedade



| Valor          | Descrição |
|----------------|-------------|
| VARIANTE \_ falso | GOPS segundos fechado |
| VARIANTE \_ true  | Abrir GOPS segundos   |



 

## <a name="remarks"></a>Comentários

Um GOP aberto contém quadros Delta que fazem referência a quadros do GOP anterior. Um GOP fechado não contém nenhum quadro Delta que referencie o GOP anterior.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Aplicativos do Windows 2000 Professional \[ Desktop aplicativos \| UWP\]<br/>                     |
| Servidor mínimo com suporte<br/> | Aplicativos da área de trabalho do Windows 2000 Server aplicativos \[ \| UWP\]<br/>                           |
| parâmetro<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades da API do codec](codec-api-properties.md)
</dt> <dt>

[**Interface ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




