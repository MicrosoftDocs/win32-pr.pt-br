---
description: Especifica o número de quadros de vídeo codificados pelo codec que realmente contêm dados.
ms.assetid: f96fd0b2-8c81-4318-b44c-4b794b3945a3
title: Propriedade MFPKEY_CODEDNONZEROFRAMES (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b1ca5fb26288e2ea9ff801ba13aa7bef570ca95
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105812237"
---
# <a name="mfpkey_codednonzeroframes-property"></a>\_Propriedade MFPKEY CODEDNONZEROFRAMES

Especifica o número de quadros de vídeo codificados pelo codec que realmente contêm dados.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Disponível apenas usando [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo de Dados

\_I4 VT

## <a name="remarks"></a>Comentários

Esse valor é igual a [MFPKEY \_ TOTALFRAMES](mfpkey-totalframesproperty.md) menos quaisquer quadros que foram descartados devido a restrições de taxa de bits, menos quaisquer quadros de zero byte. Você pode obter esse valor depois de terminar de passar amostras. Quadros de zero byte podem ser criados para quadros duplicados.

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

 

 
