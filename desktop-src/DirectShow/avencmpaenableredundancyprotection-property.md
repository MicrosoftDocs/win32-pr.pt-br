---
description: Especifica se uma CRC (verificação de redundância cíclica) deve ser adicionada ao cabeçalho do quadro. Essa propriedade se aplica a codificadores de áudio MPEG.
ms.assetid: 55f0de8b-26dd-4d48-b7ed-2ddcef630227
title: Propriedade AVEncMPAEnableRedundancyProtection (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2028b5adaad55d46cc53c61f9d65a73819cc899
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105749274"
---
# <a name="avencmpaenableredundancyprotection-property"></a>Propriedade AVEncMPAEnableRedundancyProtection

Especifica se uma CRC (verificação de redundância cíclica) deve ser adicionada ao cabeçalho do quadro. Essa propriedade se aplica a codificadores de áudio MPEG.

Esta propriedade é de leitura/gravação.

## <a name="data-type"></a>Tipo de dados

**Variante \_ BOOL** (**VT \_ bool**)

## <a name="property-guid"></a>GUID da propriedade

**CODECAPI \_ AVEncMPAEnableRedundancyProtection**

## <a name="property-value"></a>Valor da propriedade

Essa propriedade pode ter os valores a seguir.



| Valor          | Descrição                |
|----------------|----------------------------|
| VARIANTE \_ falso | Não adicione uma soma de verificação de CRC. |
| VARIANTE \_ true  | Adicione uma soma de verificação de CRC.        |



 

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

 

 




