---
description: A interface IDxtJpeg define propriedades na transição de apagamento SMPTE. Essa interface é usada internamente pelos serviços de edição do DirectShow (DES) quando ele renderiza a transição de apagamento SMPTE.
ms.assetid: ce1920d4-ebe5-42d1-a2eb-d71ddeaf14fe
title: Interface IDxtJpeg (QEdit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e9c32bee3f4041abaa9529036b7bc78250ac2487
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760743"
---
# <a name="idxtjpeg-interface"></a>Interface IDxtJpeg

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

A `IDxtJpeg` interface define propriedades na transição de [apagamento SMPTE](smpte-wipe-transition.md) .

Essa interface é usada internamente pelos serviços de edição do DirectShow (DES) quando ele renderiza a transição de apagamento SMPTE. Os aplicativos DES não precisam usar essa interface. Para definir as propriedades em uma transição em DES, use a interface [**IPropertySetter**](ipropertysetter.md) .

## <a name="members"></a>Membros

A interface **IDxtJpeg** herda de **IDXEffect**. **IDxtJpeg** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IDxtJpeg** tem esses métodos.



| Método                                                     | Descrição                                                                               |
|:-----------------------------------------------------------|:------------------------------------------------------------------------------------------|
| [**ApplyChanges**](idxtjpeg-applychanges.md)              | Aplica todas as propriedades que foram alteradas.<br/>                                      |
| [**obter \_ BorderColor**](idxtjpeg-get-bordercolor.md)       | Recupera a cor da borda ao torno das bordas do padrão de apagamento.<br/>        |
| [**obter \_ BorderSoftness**](idxtjpeg-get-bordersoftness.md) | Recupera a largura da região borrada em volta das bordas do padrão de apagamento.<br/> |
| [**obter \_ BorderWidth**](idxtjpeg-get-borderwidth.md)       | Recupera a largura da borda sólida ao longo das bordas do padrão de apagamento.<br/>   |
| [**obter \_ máscaraname**](idxtjpeg-get-maskname.md)             | Recupera o nome de um arquivo JPEG a ser usado como a máscara de apagamento.<br/>                 |
| [**obter \_ MaskNum**](idxtjpeg-get-masknum.md)               | Recupera o código de apagamento SMPTE do apagamento.<br/>                                     |
| [**obter \_ OffsetX**](idxtjpeg-get-offsetx.md)               | Recupera o deslocamento horizontal da origem do apagamento.<br/>                            |
| [**obter \_ OffsetY**](idxtjpeg-get-offsety.md)               | Recupera o deslocamento vertical da origem do apagamento.<br/>                              |
| [**obter \_ ReplicateX**](idxtjpeg-get-replicatex.md)         | Recupera o número de vezes que o padrão de apagamento é replicado horizontalmente.<br/>     |
| [**obter \_ complicação**](idxtjpeg-get-replicatey.md)         | Recupera o número de vezes que o padrão de apagamento é replicado verticalmente.<br/>       |
| [**obter \_ ScaleX**](idxtjpeg-get-scalex.md)                 | Recupera o valor pelo qual o apagamento é alongado horizontalmente.<br/>              |
| [**obter \_ ScaleY**](idxtjpeg-get-scaley.md)                 | Recupera o valor pelo qual o apagamento é alongado verticalmente.<br/>                |
| [**LoadDefSettings**](idxtjpeg-loaddefsettings.md)        | Restaura as configurações padrão da transição de apagamento.<br/>                          |
| [**colocar \_ BorderColor**](idxtjpeg-put-bordercolor.md)       | Especifica a cor da borda ao torno das bordas do padrão de apagamento.<br/>        |
| [**colocar \_ BorderSoftness**](idxtjpeg-put-bordersoftness.md) | Especifica a largura da região borrada ao contrário das bordas do padrão de apagamento.<br/> |
| [**colocar \_ BorderWidth**](idxtjpeg-put-borderwidth.md)       | Especifica a largura da borda sólida ao longo das bordas do padrão de apagamento.<br/>   |
| [**colocar \_ maskname**](idxtjpeg-put-maskname.md)             | Especifica o nome de um arquivo JPEG a ser usado como a máscara de apagamento.<br/>                     |
| [**colocar \_ MaskNum**](idxtjpeg-put-masknum.md)               | Especifica o código de apagamento SMPTE do apagamento.<br/>                                     |
| [**colocar \_ OffsetX**](idxtjpeg-put-offsetx.md)               | Especifica o deslocamento horizontal da origem do apagamento.<br/>                            |
| [**colocar \_ OffsetY**](idxtjpeg-put-offsety.md)               | Especifica o deslocamento vertical da origem do apagamento.<br/>                              |
| [**colocar \_ ReplicateX**](idxtjpeg-put-replicatex.md)         | Especifica o número de vezes que o padrão de apagamento é replicado horizontalmente.<br/>     |
| [**colocar \_ complicação**](idxtjpeg-put-replicatey.md)         | Especifica o número de vezes que o padrão de apagamento é replicado verticalmente.<br/>       |
| [**colocar \_ ScaleX**](idxtjpeg-put-scalex.md)                 | Especifica o valor pelo qual o apagamento é alongado horizontalmente.<br/>              |
| [**colocar \_ ScaleY**](idxtjpeg-put-scaley.md)                 | Especifica o valor pelo qual o apagamento é alongado verticalmente.<br/>                |



 

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



 

 




