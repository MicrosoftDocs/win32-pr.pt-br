---
description: Indica o fim da frase final em uma sequência de frases alternativas que um separador de palavras gera durante o tempo do índice.
ms.assetid: 50E4E208-A290-42B7-9152-9472C01B20D5
title: 'Método IWordSink:: EndAltPhrase (Search. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWordSink.EndAltPhrase
api_type:
- COM
api_location:
- search.h
ms.openlocfilehash: d7e26a0cde3defe987c05ba2066b6643e74239494cbb9d674577905217a63f76
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117862740"
---
# <a name="iwordsinkendaltphrase-method"></a>Método IWordSink:: EndAltPhrase

Indica o fim da frase final em uma sequência de frases alternativas que um separador de palavras gera durante o tempo do índice.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT EndAltPhrase();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Esse método pode retornar um desses valores.



| Código de retorno                                                                                           | Descrição                                                                            |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <dt>**\_ \_ somente consulta WBREAK \_ E**</dt> </dl> | [**EndAltPhrase**](iwordsink-endaltphrase.md) é chamado durante o tempo de consulta.<br/> |



 

## <a name="remarks"></a>Comentários

Implementações de [**IWordBreaker**](/windows/win32/api/indexsrv/nn-indexsrv-iwordbreaker) chamam **IWordSink:: EndAltPhrase** do método [**IWordBreaker:: BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext) para encerrar uma sequência de frases alternativas. O método [**IWordSink:: StartAltPhrase**](iwordsink-startaltphrase.md) é chamado para indicar o final de uma frase e o início de outra em uma sequência de frases. Somente a última frase em uma sequência é encerrada com uma chamada para **EndAltPhrase**.

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

 

 
