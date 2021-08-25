---
description: Especifica se uma CRC (verificação de redundância cíclica) deve ser acrescentada ao header do quadro. Essa propriedade se aplica a codificadores de áudio MPEG.
ms.assetid: 55f0de8b-26dd-4d48-b7ed-2ddcef630227
title: Propriedade AVEncMPAEnableRedundancyProtection (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b50e010b0b088e8817eca4dae1989cd6f623f55a9616c4449df62f115f98ff7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119824106"
---
# <a name="avencmpaenableredundancyprotection-property"></a>Propriedade AVEncMPAEnableRedundancyProtection

Especifica se uma CRC (verificação de redundância cíclica) deve ser acrescentada ao header do quadro. Essa propriedade se aplica a codificadores de áudio MPEG.

Essa propriedade é leitura/gravação.

## <a name="data-type"></a>Tipo de dados

**VARIANT \_ BOOL** (**VT \_ BOOL**)

## <a name="property-guid"></a>GUID da propriedade

**CODECAPI \_ AVEncMPAEnableRedundancyProtection**

## <a name="property-value"></a>Valor da propriedade

Essa propriedade pode ter os valores a seguir.



| Valor          | Descrição                |
|----------------|----------------------------|
| VARIANT \_ FALSE | Não adicione uma soma de verificação CRC. |
| VARIANT \_ TRUE  | Adicione uma soma de verificação de CRC.        |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[ aplicativos UWP da área de \| trabalho\]<br/>                     |
| Servidor mínimo com suporte<br/> | Windows aplicativos da área de trabalho do servidor 2000 \[ \| aplicativos UWP\]<br/>                           |
| Cabeçalho<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades da API do Codec](codec-api-properties.md)
</dt> <dt>

[**ICodecAPI Interface**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




