---
description: Especifica se o codificador deve verificar a consistência dos dados entre as passagens ao executar a codificação de VBR de duas passagens. Leitura/gravação.
ms.assetid: 68750820-e931-41c2-9d12-89ab83b4b97e
title: Propriedade MFPKEY_CHECKDATACONSISTENCY2P (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abc706712ef1e8bff36a118031fde155bb9bda31
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105781231"
---
# <a name="mfpkey_checkdataconsistency2p-property"></a>\_Propriedade MFPKEY CHECKDATACONSISTENCY2P

Especifica se o codificador deve verificar a consistência dos dados entre as passagens ao executar a codificação de VBR de duas passagens. Leitura/gravação.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Disponível apenas usando [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo de Dados

**BOOL do VT \_**

## <a name="default-value"></a>Valor padrão

**VARIANTE \_ true**

## <a name="remarks"></a>Comentários

Se você deixar essa propriedade com seu valor padrão de **Variant \_ true**, o codificador verificará se as amostras de entrada correspondem entre as duas passagens e falhará se detectar uma discrepância. O cenário principal que leva a uma discrepância é quando a entrada vem de um dispositivo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-----------------------------------------------------------------------------------------|
| Cliente<br/> | Windows Vista ou Windows 7<br/>                                                   |
| parâmetro<br/> | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
