---
title: Interface IWMPClosedCaption2 (VB e C) (WMP. h)
description: Fornece propriedades e métodos para legendas codificadas que complementam a interface IWMPClosedCaption. Além das propriedades herdadas de IWMPClosedCaption, a interface IWMPClosedCaption2 expõe as propriedades a seguir.
ms.assetid: e34ea819-dc1a-48f3-9e55-cf2217379ddb
keywords:
- IWMPClosedCaption2 (VB e C) interface do Windows Media Player
- IWMPClosedCaption2 (VB e C) interface do Windows Media Player, descrito
topic_type:
- apiref
api_name:
- IWMPClosedCaption2 (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3dbf81cef3734a6466b6fd177ccc87a38c5c7085
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105784192"
---
# <a name="iwmpclosedcaption2-vb-and-c-interface"></a>Interface IWMPClosedCaption2 (VB e C#)

Fornece propriedades e métodos para legendas codificadas que complementam a interface **IWMPClosedCaption** .

Além das propriedades herdadas de **IWMPClosedCaption**, a interface **IWMPClosedCaption2** expõe as propriedades a seguir.

## <a name="members"></a>Membros

A interface **IWMPClosedCaption2 (VB e C#)** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A interface **IWMPClosedCaption2 (VB e C#)** tem esses métodos.



| Método                                                                                             | Descrição                                                                                       |
|:---------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------|
| [**getSAMILangID**](wmplibiwmpclosedcaption2-iwmpclosedcaption2-getsamilangid--vb-and-c.md)       | Retorna o LCID (identificador de localidade) de um idioma com suporte do arquivo SAMI atual.<br/> |
| [**getSAMILangName**](wmplibiwmpclosedcaption2-iwmpclosedcaption2-getsamilangname--vb-and-c.md)   | Retorna o nome de um idioma com suporte do arquivo SAMI atual.<br/>                     |
| [**getSAMIStyleName**](wmplibiwmpclosedcaption2-iwmpclosedcaption2-getsamistylename--vb-and-c.md) | Retorna o nome de um estilo suportado pelo arquivo SAMI atual.<br/>                        |



 

### <a name="properties"></a>Propriedades

A interface **IWMPClosedCaption2 (VB e C#)** tem essas propriedades.



| Propriedade                                                                                                | Tipo de acesso           | Descrição                                                                         |
|:--------------------------------------------------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------|
| [**SAMILangCount**](wmplibiwmpclosedcaption2-iwmpclosedcaption2-samilangcount--vb-and-c.md)<br/> | Leitura/gravação<br/> | Obtém ou define o número de idiomas com suporte pelo arquivo SAMI atual.<br/> |
| [**SAMIStyleCount**](wmplibiwmpclosedcaption2-samistylecount.md)<br/>                            | Leitura/gravação<br/> | Obtém ou define o número de estilos com suporte pelo arquivo SAMI atual.<br/>    |



 

Obtenha uma interface **IWMPClosedCaption2** convertendo o valor retornado pela propriedade [**AxWindowsMediaPlayer. closedCaption**](axwmplib-axwindowsmediaplayer-closedcaption--vb-and-c.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>WMP. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Adicionando legendas ocultas à mídia digital**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**Interfaces para Visual Basic .NET e C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[**Interface IWMPClosedCaption (VB e C#)**](iwmpclosedcaption--vb-and-c.md)
</dt> </dl>

 

 





