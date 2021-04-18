---
description: Representa o acesso a um retângulo.
ms.assetid: 78e6c29c-0f43-46a5-9d30-948de5f369c8
title: Classe InkRectangle (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkRectangle
- InkRectangle.IInkRectangle
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: d643696fe19523bac93ebca71cf885cd93b8570a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105814181"
---
# <a name="inkrectangle-class"></a>Classe InkRectangle

Representa o acesso a um retângulo.

**InkRectangle** tem estes tipos de membros:

-   [Interfaces](#interfaces)
-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="interfaces"></a>Interfaces

A classe **InkRectangle** define essas interfaces.



| Interface         | Descrição                                                            |
|:------------------|:-----------------------------------------------------------------------|
| **IInkRectangle** | Esse objeto implementa a interface com do **IInkRectangle** .<br/> |



 

### <a name="methods"></a>Métodos

A classe **InkRectangle** tem esses métodos.



| Método                                            | Descrição                                                                        |
|:--------------------------------------------------|:-----------------------------------------------------------------------------------|
| [**Getrectangle**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-getrectangle) | Recupera os elementos do objeto **InkRectangle** em uma única chamada.<br/> |
| [**Setrectangle**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-setrectangle) | Modifica os elementos do objeto **InkRectangle** em uma única chamada.<br/>  |



 

### <a name="properties"></a>Propriedades

A classe **InkRectangle** tem essas propriedades.



| Propriedade                                         | Tipo de acesso           | Descrição                                                        |
|:-------------------------------------------------|:----------------------|:-------------------------------------------------------------------|
| [**Inferior**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-get_bottom)<br/> | Leitura/gravação<br/> | Obtém ou define a posição inferior do retângulo.<br/>      |
| [**Dados**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-get_data)<br/>     | Leitura/gravação<br/> | Obtém ou define o acesso ao struct do retângulo (somente C++).<br/> |
| [**Mantida**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-get_left)<br/>     | Leitura/gravação<br/> | Obtém ou define a posição esquerda do retângulo.<br/>        |
| [**Certo**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-get_right)<br/>   | Leitura/gravação<br/> | Obtém ou define a posição correta do retângulo.<br/>       |
| [**Início**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-get_top)<br/>       | Leitura/gravação<br/> | Obtém ou define a posição superior do retângulo.<br/>         |



 

## <a name="remarks"></a>Comentários

> [!Note]  
> Um ponto está dentro de um **InkRectangle** se ele está no lado [**esquerdo**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-get_left) ou [**superior**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-get_top) ou está dentro de todos os quatro lados. Um ponto no lado [**direito**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-get_right) ou [**inferior**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrectangle-get_bottom) é considerado fora do retângulo.

 

Esse objeto pode ser instanciado chamando o método [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) .

> [!Note]  
> Um **InkRectangle** não poderá ser usado se for maior que o \_ máximo longo (2 ^ 31-1) em qualquer dimensão.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]<br/>                                                       |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                           |
| parâmetro<br/>                   | <dl> <dt>Msinkaut. h (também requer Msinkaut \_ i. c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



 

