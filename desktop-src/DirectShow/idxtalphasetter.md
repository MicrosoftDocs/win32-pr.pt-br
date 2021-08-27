---
description: A interface IDxtAlphaSetter define propriedades no efeito Alfa Setter. Essa interface é usada internamente DirectShow DES (Serviços de Edição) quando renderiza o efeito Alfa Setter.
ms.assetid: 9f0439b9-55d2-4526-ae4c-64ab90e11a64
title: Interface IDxtAlphaSetter (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtAlphaSetter
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: f1cc4056733dbd0e46639a921da65e5cb2a81f3601fa1ae00624be7d92ddc0e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120051926"
---
# <a name="idxtalphasetter-interface"></a>Interface IDxtAlphaSetter

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

A `IDxtAlphaSetter` interface define propriedades no efeito Alfa [Setter.](alpha-setter-effect.md)

Essa interface é usada internamente DirectShow DES (Serviços de Edição) quando renderiza o efeito Alfa Setter. Os aplicativos DES não têm que usar essa interface. Para definir as propriedades em uma transição no DES, use a interface [**IPropertySetter.**](ipropertysetter.md)

## <a name="members"></a>Membros

A interface **IDxtAlphaSetter** herda de **IDXEffect.** **IDxtAlphaSetter** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IDxtAlphaSetter** tem esses métodos.



| Método                                                  | Descrição                                                |
|:--------------------------------------------------------|:-----------------------------------------------------------|
| [**obter \_ Alfa**](idxtalphasetter-get-alpha.md)         | Recupera o valor alfa para toda a imagem.<br/> |
| [**obter \_ AlphaRamp**](idxtalphasetter-get-alpharamp.md) | Recupera a propriedade de rampa alfa.<br/>              |
| [**colocar \_ Alfa**](idxtalphasetter-put-alpha.md)         | Especifica o valor alfa para toda a imagem.<br/> |
| [**colocar \_ AlphaRamp**](idxtalphasetter-put-alpharamp.md) | Especifica a propriedade de rampa alfa.<br/>              |



 

## <a name="remarks"></a>Comentários

> [!Note]  
> O arquivo de título Qedit.h não é compatível com os headers direct3D posteriores à versão 7.

 

> [!Note]  
> Para obter o Qedit.h, baixe [o Microsoft Windows SDK Update para Windows Vista e .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). O Qedit.h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



 

 




