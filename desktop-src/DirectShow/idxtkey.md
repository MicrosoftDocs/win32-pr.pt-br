---
description: A interface IDxtKey define propriedades na transição de chave. Essa interface é usada internamente DirectShow DES (Serviços de Edição) ao renderizar a transição de chave.
ms.assetid: b929bf0c-8aaf-456e-b692-e23d88e480dd
title: Interface IDxtKey (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: d967d15dededf879ffd08671aac00e7892aa8ad2f2c1a39ce478f7f9f3e4db90
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119792356"
---
# <a name="idxtkey-interface"></a>Interface IDxtKey

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

A `IDxtKey` interface define propriedades na transição [de](key-transition.md) chave.

Essa interface é usada internamente DirectShow DES (Serviços de Edição) ao renderizar a transição de chave. Os aplicativos DES não precisam usar essa interface. Para definir as propriedades em uma transição no DES, use a interface [**IPropertySetter.**](ipropertysetter.md)

## <a name="members"></a>Membros

A **interface IDxtKey** herda de **IDXEffect.** **IDxtKey** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A **interface IDxtKey** tem esses métodos.



| Método                                            | Descrição                                                                            |
|:--------------------------------------------------|:---------------------------------------------------------------------------------------|
| [**obter \_ Hue**](idxtkey-get-hue.md)               | Recupera o valor de matiz no qual a tecla deve ser chave.<br/>                                    |
| [**get \_ Invert**](idxtkey-get-invert.md)         | Recupera um valor booliana que indica se a operação de chave é invertida.<br/> |
| [**obter \_ KeyType**](idxtkey-get-keytype.md)       | Recupera o tipo de chave.<br/>                                                  |
| [**obter \_ Luminance**](idxtkey-get-luminance.md)   | Recupera o valor de luminância no qual a chave deve ser obtida.<br/>                              |
| [**obter \_ RGB**](idxtkey-get-rgb.md)               | Recupera a cor RGB na qual a tecla deve ser chave.<br/>                                    |
| [**obter \_ similaridade**](idxtkey-get-similarity.md) | Recupera o intervalo de dados de cores que se torna transparente.<br/>                 |
| [**put \_ Hue**](idxtkey-put-hue.md)               | Especifica o valor de matiz no qual a tecla deve ser chave.<br/>                                    |
| [**put \_ Invert**](idxtkey-put-invert.md)         | Especifica se a operação de chave é invertida.<br/>                            |
| [**put \_ KeyType**](idxtkey-put-keytype.md)       | Especifica o tipo de chave.<br/>                                                  |
| [**put \_ Luminance**](idxtkey-put-luminance.md)   | Especifica o valor de luminância no qual a chave deve ser chave.<br/>                              |
| [**put \_ RGB**](idxtkey-put-rgb.md)               | Especifica a cor RGB na qual a tecla deve ser chave.<br/>                                    |
| [**put \_ Similarity**](idxtkey-put-similarity.md) | Especifica o intervalo de dados de cores que se torna transparente.<br/>                 |



 

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



 

 




