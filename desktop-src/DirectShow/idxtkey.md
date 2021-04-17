---
description: A interface IDxtKey define propriedades na transição de chave. Essa interface é usada internamente pelos serviços de edição do DirectShow (DES) quando ele renderiza a transição de chave.
ms.assetid: b929bf0c-8aaf-456e-b692-e23d88e480dd
title: Interface IDxtKey (QEdit. h)
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
ms.openlocfilehash: f4f1bc6a5dd0e89789e098fc4180bfc826f10c93
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105779526"
---
# <a name="idxtkey-interface"></a>Interface IDxtKey

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

A `IDxtKey` interface define propriedades na transição de [chave](key-transition.md) .

Essa interface é usada internamente pelos serviços de edição do DirectShow (DES) quando ele renderiza a transição de chave. Os aplicativos DES não precisam usar essa interface. Para definir as propriedades em uma transição em DES, use a interface [**IPropertySetter**](ipropertysetter.md) .

## <a name="members"></a>Membros

A interface **IDxtKey** herda de **IDXEffect**. **IDxtKey** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IDxtKey** tem esses métodos.



| Método                                            | Descrição                                                                            |
|:--------------------------------------------------|:---------------------------------------------------------------------------------------|
| [**obter \_ matiz**](idxtkey-get-hue.md)               | Recupera o valor de matiz para o qual fazer a chave.<br/>                                    |
| [**obter \_ inverter**](idxtkey-get-invert.md)         | Recupera um valor booliano que indica se a operação de chave está invertida.<br/> |
| [**obter \_ KeyType**](idxtkey-get-keytype.md)       | Recupera o tipo de chave.<br/>                                                  |
| [**obter \_ luminância**](idxtkey-get-luminance.md)   | Recupera o valor de luminância no qual a chave deve ser Key.<br/>                              |
| [**obter \_ RGB**](idxtkey-get-rgb.md)               | Recupera a cor RGB para a chave.<br/>                                    |
| [**obter \_ similaridade**](idxtkey-get-similarity.md) | Recupera o intervalo de dados de cor que se torna transparente.<br/>                 |
| [**colocar \_ matiz**](idxtkey-put-hue.md)               | Especifica o valor de matiz a ser chaveada.<br/>                                    |
| [**colocar \_ inverter**](idxtkey-put-invert.md)         | Especifica se a operação de chave está invertida.<br/>                            |
| [**colocar \_ KeyType**](idxtkey-put-keytype.md)       | Especifica o tipo de chave.<br/>                                                  |
| [**colocar \_ luminância**](idxtkey-put-luminance.md)   | Especifica o valor de luminância para a chave.<br/>                              |
| [**colocar \_ RGB**](idxtkey-put-rgb.md)               | Especifica a cor RGB para a chave.<br/>                                    |
| [**colocar \_ similaridade**](idxtkey-put-similarity.md) | Especifica o intervalo de dados de cor que se torna transparente.<br/>                 |



 

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



 

 




