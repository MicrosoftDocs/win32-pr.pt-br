---
title: Propriedade baseURL IWMPSettings
description: A propriedade baseURL Obtém ou define a URL base usada para resolução de caminho relativo com comandos de script de URL inseridos no conteúdo de mídia digital.
ms.assetid: e136303f-ba08-434f-ad7e-9fffa66785c4
keywords:
- Propriedade baseURL Windows Media Player
- Propriedade baseURL Windows Media Player, interface IWMPSettings
- Interface IWMPSettings Windows Media Player, Propriedade baseURL
topic_type:
- apiref
api_name:
- IWMPSettings.baseURL
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 393575a93bf904f6fe312b13647ad5a7557b15bc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105791342"
---
# <a name="iwmpsettingsbaseurl-property"></a>Propriedade IWMPSettings:: baseURL

A propriedade **baseURL** Obtém ou define a URL base usada para resolução de caminho relativo com comandos de script de URL inseridos no conteúdo de mídia digital.

## <a name="syntax"></a>Sintaxe


```CSharp
public System.String baseURL {get; set;}
```


```VB

Public Property baseURL As System.String
```





## <a name="property-value"></a>Valor da propriedade

Um **System. String** que é a URL base.

## <a name="remarks"></a>Comentários

Essa propriedade especifica a URL HTTP base que é passada como o parâmetro de comando pelo evento **AxWindowsMediaPlayer \_ WMPOCXEvents \_ ScriptCommandEvent** . A URL base é concatenada com a URL relativa da seguinte maneira:

1.  Uma barra (/) à direita é adicionada ao valor recuperado pela propriedade **baseURL** .
2.  Um ponto à esquerda, uma barra invertida ou um caractere de barra invertida (., \\ e/) é excluído da URL relativa.
3.  A URL relativa é adicionada ao final da URL base.
4.  Todos os caracteres de barra na URL totalmente qualificada resultante são apontados na mesma direção (convertida para barras para frente ou para trás) com base na direção do caractere de primeira barra encontrado na nova URL.

**Observação**

O controle do Windows Media Player não oferece suporte ao uso de dois pontos (..) na URL relativa para indicar o pai do local atual.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versão<br/>   | Windows Media Player 9 Series ou posterior<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Evento AxWindowsMediaPlayer. ScriptCommand (VB e C#)**](axwmplib-axwindowsmediaplayer-scriptcommand.md)
</dt> <dt>

[**Interface IWMPSettings (VB e C#)**](iwmpsettings--vb-and-c.md)
</dt> </dl>

 

 





