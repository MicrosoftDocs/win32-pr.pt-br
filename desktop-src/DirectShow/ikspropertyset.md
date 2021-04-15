---
description: A interface IKsPropertySet foi originalmente projetada como uma maneira eficiente de definir e recuperar propriedades de dispositivo em drivers WDM, usando KSProxy para converter as chamadas de método COM de modo de usuário em conjuntos de propriedades de modo kernel usados por drivers de classe de streaming WDM. Essa interface agora também é usada para passar informações estritamente entre componentes de software. Em alguns casos, os componentes de software devem implementar essa interface ou também a interface IKsControl (documentada no DirectShow DDK). Por exemplo, se você estiver escrevendo um decodificador MPEG-2 de software para uso com o navegador de DVD, deverá implementar uma dessas interfaces e também oferecer suporte aos conjuntos de propriedades relacionados a DVD que o navegador enviará para o decodificador. Os Pins podem dar suporte a uma dessas interfaces para permitir que outros Pins ou filtros definam ou recuperem suas propriedades. Observe que outra interface por esse nome existe no arquivo de cabeçalho dsound. h. As duas interfaces não são compatíveis. A interface IKsControl, documentada no DirectShow DDK, agora é a interface recomendada para passar os conjuntos de propriedades entre os drivers WDM e os componentes do modo de usuário. .
ms.assetid: df26341d-f2d5-4a4e-954e-705e07415808
title: Interface IKsPropertySet (ksproxy. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IKsPropertySet
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
ms.openlocfilehash: 49a1f897d79a7514600f0c6553f931411aae8993
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104456387"
---
# <a name="ikspropertyset-interface"></a>Interface IKsPropertySet

A `IKsPropertySet` interface foi originalmente projetada como uma maneira eficiente de definir e recuperar propriedades de dispositivo em drivers WDM, usando ksproxy para converter as chamadas de método com de modo de usuário em conjuntos de propriedades de modo kernel usadas por drivers de classe de streaming WDM. Essa interface agora também é usada para passar informações estritamente entre componentes de software.

Em alguns casos, os componentes de software devem implementar essa interface ou também a interface **IKsControl** (documentada no DirectShow DDK). Por exemplo, se você estiver escrevendo um decodificador MPEG-2 de software para uso com o [navegador de DVD](dvd-navigator-filter.md), deverá implementar uma dessas interfaces e também oferecer suporte aos conjuntos de propriedades relacionados a DVD que o navegador enviará para o decodificador. Os Pins podem dar suporte a uma dessas interfaces para permitir que outros Pins ou filtros definam ou recuperem suas propriedades.

> [!Note]  
> Outra interface com esse nome existe no arquivo de cabeçalho dsound. h. As duas interfaces não são compatíveis. A interface **IKsControl** , documentada no DirectShow DDK, agora é a interface recomendada para passar os conjuntos de propriedades entre os drivers WDM e os componentes do modo de usuário.

 

## <a name="members"></a>Membros

A interface **IKsPropertySet** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IKsPropertySet** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IKsPropertySet** tem esses métodos.



| Método                                                  | Descrição                                                                          |
|:--------------------------------------------------------|:-------------------------------------------------------------------------------------|
| [**Obter**](ikspropertyset-get.md)                       | Recupera uma propriedade identificada por um GUID de conjunto de propriedades e uma ID de propriedade.<br/> |
| [**QuerySupported**](ikspropertyset-querysupported.md) | Determina se um objeto dá suporte a um conjunto de propriedades especificado.<br/>           |
| [**Definição**](ikspropertyset-set.md)                       | Define uma propriedade identificada por um GUID de conjunto de propriedades e uma ID de propriedade.<br/>      |



 

## <a name="remarks"></a>Comentários

Você deve incluir KS. h antes de ksproxy. h.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                              |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                    |
| Cabeçalho<br/>                   | <dl> <dt>Ksproxy. h</dt> </dl>    |
| Biblioteca<br/>                  | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Conjuntos de propriedades](property-sets.md)
</dt> </dl>

 

 
