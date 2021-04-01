---
description: Especifica a configuração padrão para o bit original no fluxo de áudio MPEG-1. Essa propriedade se aplica a codificadores de áudio MPEG.
ms.assetid: 62b56868-684f-4f28-90da-dac19cb07946
title: Propriedade AVEncMPAOriginalBitstream (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a1a49fda5bb605ac8735ebac4be758e7f73efb9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103825895"
---
# <a name="avencmpaoriginalbitstream-property"></a>Propriedade AVEncMPAOriginalBitstream

Especifica a configuração padrão para o bit original no fluxo de áudio MPEG-1. Essa propriedade se aplica a codificadores de áudio MPEG.

Esta propriedade é de leitura/gravação.

## <a name="data-type"></a>Tipo de dados

**Variante \_ BOOL** (**VT \_ bool**)

## <a name="property-guid"></a>GUID da propriedade

**CODECAPI \_ AVEncMPAOriginalBitstream**

## <a name="property-value"></a>Valor da propriedade

Essa propriedade pode ter os valores a seguir.



| Valor          | Descrição          |
|----------------|----------------------|
| VARIANTE \_ falso | O bit original está desativado. |
| VARIANTE \_ true  | O bit original está ativado.  |



 

## <a name="remarks"></a>Comentários

O codificador pode substituir essa configuração, com base no conteúdo do fluxo de entrada.

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

 

 




