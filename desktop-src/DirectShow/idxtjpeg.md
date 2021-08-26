---
description: A interface IDxtJpeg define propriedades na transição de apagaamento SMPTE. Essa interface é usada internamente DirectShow DES (Serviços de Edição) quando renderiza a transição de apagamento SMPTE.
ms.assetid: ce1920d4-ebe5-42d1-a2eb-d71ddeaf14fe
title: Interface IDxtJpeg (Qedit.h)
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
ms.openlocfilehash: b1f48ff04c087c0c0c391eaf1a64ae8e7768505a5ba8d108ab49c54ffc7b17f3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119997496"
---
# <a name="idxtjpeg-interface"></a>Interface IDxtJpeg

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

A `IDxtJpeg` interface define propriedades na transição de [Apagando SMPTE.](smpte-wipe-transition.md)

Essa interface é usada internamente DirectShow DES (Serviços de Edição) quando renderiza a transição de apagamento SMPTE. Os aplicativos DES não precisam usar essa interface. Para definir as propriedades em uma transição no DES, use a interface [**IPropertySetter.**](ipropertysetter.md)

## <a name="members"></a>Membros

A interface **IDxtJpeg** herda de **IDXEffect.** **IDxtJpeg** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A **interface IDxtJpeg** tem esses métodos.



| Método                                                     | Descrição                                                                               |
|:-----------------------------------------------------------|:------------------------------------------------------------------------------------------|
| [**Applychanges**](idxtjpeg-applychanges.md)              | Aplica todas as propriedades que foram alteradas.<br/>                                      |
| [**obter \_ BorderColor**](idxtjpeg-get-bordercolor.md)       | Recupera a cor da borda em torno das bordas do padrão de apagando.<br/>        |
| [**obter \_ BorderSoftness**](idxtjpeg-get-bordersoftness.md) | Recupera a largura da região desfocado em torno das bordas do padrão de apagando.<br/> |
| [**obter \_ BorderWidth**](idxtjpeg-get-borderwidth.md)       | Recupera a largura da borda sólida ao longo das bordas do padrão de apagando.<br/>   |
| [**get \_ MaskName**](idxtjpeg-get-maskname.md)             | Recupera o nome de um arquivo JPEG a ser usado como a máscara de apagando.<br/>                 |
| [**get \_ MaskNum**](idxtjpeg-get-masknum.md)               | Recupera o código de apagando SMPTE do apagando.<br/>                                     |
| [**get \_ OffsetX**](idxtjpeg-get-offsetx.md)               | Recupera o deslocamento horizontal da origem do apagando.<br/>                            |
| [**obter \_ OffsetY**](idxtjpeg-get-offsety.md)               | Recupera o deslocamento vertical da origem do apagando.<br/>                              |
| [**get \_ ReplicateX**](idxtjpeg-get-replicatex.md)         | Recupera o número de vezes que o padrão de apagando é replicado horizontalmente.<br/>     |
| [**get \_ Replicatey**](idxtjpeg-get-replicatey.md)         | Recupera o número de vezes que o padrão de apagando é replicado verticalmente.<br/>       |
| [**obter \_ ScaleX**](idxtjpeg-get-scalex.md)                 | Recupera a quantidade pela qual o apagaamento é estendido horizontalmente.<br/>              |
| [**obter \_ ScaleY**](idxtjpeg-get-scaley.md)                 | Recupera a quantidade pela qual o apagaamento é estendido verticalmente.<br/>                |
| [**LoadDefSettings**](idxtjpeg-loaddefsettings.md)        | Restaura as configurações padrão da transição apagar.<br/>                          |
| [**put \_ BorderColor**](idxtjpeg-put-bordercolor.md)       | Especifica a cor da borda em torno das bordas do padrão de apagando.<br/>        |
| [**put \_ BorderSoftness**](idxtjpeg-put-bordersoftness.md) | Especifica a largura da região desfocado em torno das bordas do padrão de apagando.<br/> |
| [**put \_ BorderWidth**](idxtjpeg-put-borderwidth.md)       | Especifica a largura da borda sólida ao longo das bordas do padrão de apagando.<br/>   |
| [**put \_ MaskName**](idxtjpeg-put-maskname.md)             | Especifica o nome de um arquivo JPEG a ser usado como a máscara de apagando.<br/>                     |
| [**put \_ MaskNum**](idxtjpeg-put-masknum.md)               | Especifica o código de apagando SMPTE do apagando.<br/>                                     |
| [**put \_ OffsetX**](idxtjpeg-put-offsetx.md)               | Especifica o deslocamento horizontal da origem do apagando.<br/>                            |
| [**put \_ OffsetY**](idxtjpeg-put-offsety.md)               | Especifica o deslocamento vertical da origem do apagando.<br/>                              |
| [**put \_ ReplicateX**](idxtjpeg-put-replicatex.md)         | Especifica o número de vezes que o padrão de apagando é replicado horizontalmente.<br/>     |
| [**put \_ Replicatey**](idxtjpeg-put-replicatey.md)         | Especifica o número de vezes que o padrão de apagando é replicado verticalmente.<br/>       |
| [**put \_ ScaleX**](idxtjpeg-put-scalex.md)                 | Especifica a quantidade pela qual o apagaamento é estendido horizontalmente.<br/>              |
| [**put \_ ScaleY**](idxtjpeg-put-scaley.md)                 | Especifica a quantidade pela qual o apagaamento é estendido verticalmente.<br/>                |



 

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



 

 




