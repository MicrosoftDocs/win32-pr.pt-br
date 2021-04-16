---
description: A interface IDxtAlphaSetter define propriedades no efeito de setter alfa. Essa interface é usada internamente pelos serviços de edição do DirectShow (DES) quando ele renderiza o efeito de setter alfa.
ms.assetid: 9f0439b9-55d2-4526-ae4c-64ab90e11a64
title: Interface IDxtAlphaSetter (QEdit. h)
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
ms.openlocfilehash: 0f4ad88d10f4a2538cddbdc31fa90bc5496bc7f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759292"
---
# <a name="idxtalphasetter-interface"></a>Interface IDxtAlphaSetter

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

A `IDxtAlphaSetter` interface define propriedades no efeito de [setter alfa](alpha-setter-effect.md) .

Essa interface é usada internamente pelos serviços de edição do DirectShow (DES) quando ele renderiza o efeito de setter alfa. Os aplicativos DES não precisam usar essa interface. Para definir as propriedades em uma transição em DES, use a interface [**IPropertySetter**](ipropertysetter.md) .

## <a name="members"></a>Membros

A interface **IDxtAlphaSetter** herda de **IDXEffect**. **IDxtAlphaSetter** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IDxtAlphaSetter** tem esses métodos.



| Método                                                  | Descrição                                                |
|:--------------------------------------------------------|:-----------------------------------------------------------|
| [**obter \_ alfa**](idxtalphasetter-get-alpha.md)         | Recupera o valor alfa de toda a imagem.<br/> |
| [**obter \_ AlphaRamp**](idxtalphasetter-get-alpharamp.md) | Recupera a propriedade de rampa alfa.<br/>              |
| [**colocar \_ alfa**](idxtalphasetter-put-alpha.md)         | Especifica o valor alfa para a imagem inteira.<br/> |
| [**colocar \_ AlphaRamp**](idxtalphasetter-put-alpharamp.md) | Especifica a propriedade de rampa alfa.<br/>              |



 

## <a name="remarks"></a>Comentários

> [!Note]  
> O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.

 

> [!Note]  
> Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>QEdit. h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



 

 




