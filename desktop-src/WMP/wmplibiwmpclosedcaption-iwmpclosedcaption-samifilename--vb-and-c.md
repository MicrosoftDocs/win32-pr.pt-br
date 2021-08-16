---
title: Propriedade IWMPClosedCaption SAMIFileName
description: A propriedade SAMIFileName Obtém ou define o nome de um arquivo que contém as informações necessárias para Legendagem oculta.
ms.assetid: c3162c5f-9d66-41d4-920c-ed9840742d9d
keywords:
- Windows Media Player da propriedade SAMIFileName
- propriedade SAMIFileName Windows Media Player, interface IWMPClosedCaption
- Windows Media Player de interface IWMPClosedCaption, propriedade SAMIFileName
topic_type:
- apiref
api_name:
- IWMPClosedCaption.SAMIFileName
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 973b0757eca4251e74180d829205ee6c7080ca821db2eeada3abc825bb4b5073
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117930319"
---
# <a name="iwmpclosedcaptionsamifilename-property"></a>Propriedade IWMPClosedCaption:: SAMIFileName

A propriedade **SAMIFileName** Obtém ou define o nome de um arquivo que contém as informações necessárias para Legendagem oculta.

## <a name="syntax"></a>Syntax


```CSharp
public System.String SAMIFileName {get; set;}
```


```VB

Public Property SAMIFileName As System.String
```





## <a name="property-value"></a>Valor da propriedade

O **System. String** que é o nome do arquivo de intercâmbio de mídia acessível (Sami) sincronizado.

## <a name="remarks"></a>Comentários

O arquivo SAMI deve usar uma extensão de nome de arquivo. SMI ou. Sami.

Se você não definir um valor usando **SAMIFileName**, essa propriedade obterá uma **cadeia de caracteres** que contém o nome de arquivo padrão ou a URL associada ao item de mídia atual. Essa associação pode ocorrer quando um arquivo SAMI é especificado usando o parâmetro de URL *Sami* , ou automaticamente quando o arquivo Sami tem o mesmo nome que o arquivo de mídia digital (exceto para a extensão de nome de arquivo). Se não houver nenhum arquivo SAMI padrão associado à mídia atual, essa propriedade obterá uma cadeia de caracteres de comprimento zero ("").

Depois de definir um valor usando **SAMIFileName**, esse valor persiste até que você defina um novo valor (ou até que um novo item de mídia seja aberto usando o parâmetro de URL Sami). Portanto, você deve definir um novo valor para essa propriedade antes de reproduzir cada novo item de mídia. Dessa forma, o novo valor de **SAMIFileName** entrará em vigor quando o próximo item de mídia for aberto (ou quando **AxWindowsMediaPlayer. Close** for chamado). A especificação de um novo valor para **SAMIFileName** não tem nenhum efeito para a mídia atual.

para fazer com que Windows Media Player use o arquivo SAMI padrão associado a um item de mídia específico, defina **SAMIFileName** como uma cadeia de caracteres de comprimento zero ("") antes de reproduzir o próximo item de mídia.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versão<br/>   | Windows Media Player 9 Series ou posterior<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Adicionando legendas ocultas à mídia digital**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**AxWindowsMediaPlayer. Close**](axwmplib-axwindowsmediaplayer-close.md)
</dt> <dt>

[**Interface IWMPClosedCaption (VB e C#)**](iwmpclosedcaption--vb-and-c.md)
</dt> <dt>

[**Interface IWMPClosedCaption2 (VB e C#)**](iwmpclosedcaption2--vb-and-c.md)
</dt> </dl>

 

 





