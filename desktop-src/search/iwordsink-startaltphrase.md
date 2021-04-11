---
description: Indica o limite entre as frases em uma sequência de frases alternativas que um separador de palavras gera durante o tempo de indexação.
ms.assetid: 3F3B6761-887B-426E-A44F-E636397180C7
title: 'Método IWordSink:: StartAltPhrase (Search. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWordSink.StartAltPhrase
api_type:
- COM
api_location:
- search.h
ms.openlocfilehash: e4e35c5ed75016292dd420e7a832c6cfb780284a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164324"
---
# <a name="iwordsinkstartaltphrase-method"></a>Método IWordSink:: StartAltPhrase

Indica o limite entre as frases em uma sequência de frases alternativas que um separador de palavras gera durante o tempo de indexação.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT StartAltPhrase();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Esse método pode retornar um desses valores.



| Código de retorno                                                                                           | Descrição                                                                                |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| <dl> <dt>**\_ \_ somente consulta WBREAK \_ E**</dt> </dl> | [**StartAltPhrase**](iwordsink-startaltphrase.md) é chamado durante o tempo de consulta.<br/> |



 

## <a name="remarks"></a>Comentários

Cada frase alternativa começa com uma chamada **StartAltPhrase** . A frase é colocada no objeto [**IWordSink**](iwordsink.md) por meio de chamadas subsequentes para o método [**IWordSink::P utword**](iwordsink-putword.md) ou [**IWordSink::P utaltword**](iwordsink-putaltword.md) . A frase alternativa final em uma sequência de frases é encerrada com uma chamada para o método [**IWordSink:: EndAltPhrase**](iwordsink-endaltphrase.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Pesquisar. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IWordSink**](iwordsink.md)
</dt> </dl>

 

 




