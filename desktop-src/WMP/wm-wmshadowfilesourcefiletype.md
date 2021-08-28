---
title: WM/WMShadowFileSourceFileType (SDK do Windows Media Player)
description: O WM/WMShadowFileSourceFileType é o tipo de arquivo do arquivo contido no arquivo de sombra.
ms.assetid: 4c4b70b6-0e26-49f3-b7c1-f6e1fe791e48
keywords:
- Windows Media Player do WM/WMShadowFileSourceFileType
topic_type:
- apiref
api_name:
- WM/WMShadowFileSourceFileType
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fecddc4ddaf1d28b464a2d120c5d7fea11779784ed6ec496cdddcb1a09a9ded
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120000776"
---
# <a name="wmwmshadowfilesourcefiletype-windows-media-player-sdk"></a>WM/WMShadowFileSourceFileType (SDK do Windows Media Player)

O **WM/WMShadowFileSourceFileType** é o tipo de arquivo do arquivo contido no arquivo de sombra.

## <a name="remarks"></a>Comentários

Um arquivo de sombra pode ser um wrapper para um arquivo de origem. Esse atributo é uma cadeia de caracteres que contém a extensão de nome de arquivo (sem o delimitador de ponto) para o arquivo de origem. Por exemplo, se o arquivo de origem for um arquivo AAC, esse atributo conterá a cadeia de caracteres "AAC".

O arquivo de sombra é especificado usando o atributo [ShadowFilePath](shadowfilepath-attribute.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------|
| Versão<br/> | Windows Media Player 11<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Sobre plug-ins de conversão**](about-conversion-plug-ins.md)
</dt> <dt>

[**Referência de atributo**](attribute-reference.md)
</dt> </dl>

 

 





