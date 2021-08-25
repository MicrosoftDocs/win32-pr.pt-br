---
description: Especifica se o codificador deve verificar se há consistência de dados entre passagens ao executar a codificação VBR de duas passagens. Leitura/gravação.
ms.assetid: 68750820-e931-41c2-9d12-89ab83b4b97e
title: MFPKEY_CHECKDATACONSISTENCY2P propriedade (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a1cef9c8c2a8e4fcd536ce73653e80e62282b40734cc695493d6cba4187c8f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119954716"
---
# <a name="mfpkey_checkdataconsistency2p-property"></a>Propriedade MFPKEY \_ CHECKDATACONSISTENCY2P

Especifica se o codificador deve verificar se há consistência de dados entre passagens ao executar a codificação VBR de duas passagens. Leitura/gravação.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Disponível somente usando [**IPropertyStore.**](/windows/win32/api/propsys/nn-propsys-ipropertystore)

## <a name="data-type"></a>Tipo de Dados

**BOOL da VT \_**

## <a name="default-value"></a>Valor padrão

**VARIANT \_ TRUE**

## <a name="remarks"></a>Comentários

Se você deixar essa propriedade com seu valor padrão **de VARIANT \_ TRUE**, o codificador verificará se as amostras de entrada corresponderão entre as duas passagens e falhará se detectar uma discrepância. O cenário principal que leva a uma discrepância é quando a entrada vem de um dispositivo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-----------------------------------------------------------------------------------------|
| Cliente<br/> | Windows Vista ou Windows 7<br/>                                                   |
| Cabeçalho<br/> | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Media Foundation propriedades](media-foundation-properties.md)
</dt> </dl>

 

 
