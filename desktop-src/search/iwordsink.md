---
description: Manipula palavras identificadas por quebras de palavras durante tanto o tempo de índice quanto o tempo de consulta.
ms.assetid: 220FCAE5-D22D-45ED-9689-E78C0D8E0BB3
title: Interface IWordSink (Search. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWordSink
api_type:
- COM
api_location:
- search.h
ms.openlocfilehash: 2eab8eee4f7b07b0f712e68d7ad05b970506b00b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105807279"
---
# <a name="iwordsink-interface"></a>Interface IWordSink

Manipula palavras identificadas por quebras de palavras durante tanto o tempo de índice quanto o tempo de consulta.

## <a name="members"></a>Membros

A interface **IWordSink** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IWordSink** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IWordSink** tem esses métodos.



| Método                                             | Descrição                                                                                                                             |
|:---------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------|
| [**EndAltPhrase**](iwordsink-endaltphrase.md)     | Indica o fim da frase final em uma sequência de frases alternativas que um separador de palavras gera durante o tempo do índice.<br/>  |
| [**PutAltWord**](iwordsink-putaltword.md)         | Coloca uma palavra alternativa e sua posição no objeto **IWordSink** .<br/>                                                       |
| [**PutBreak**](iwordsink-putbreak.md)             | Coloca uma quebra após a palavra anterior.<br/>                                                                                       |
| [**PutWord**](iwordsink-putword.md)               | Coloca uma palavra e sua posição no objeto **IWordSink** .<br/>                                                                    |
| [**StartAltPhrase**](iwordsink-startaltphrase.md) | Indica o limite entre as frases em uma sequência de frases alternativas que um separador de palavras gera durante o tempo de indexação.<br/> |



 

## <a name="remarks"></a>Comentários

O Windows Search cria e inicializa instâncias do objeto **IWordSink** . O objeto **IWordSink** recebe o parâmetro *fQuery* durante a inicialização e usa esse parâmetro para determinar o contexto de quebra de palavras no qual o objeto é usado.

Implementações [**IWordBreaker**](/windows/win32/api/indexsrv/nn-indexsrv-iwordbreaker) recebem um ponteiro para o objeto **IWordSink** no método [**IWordBreaker:: BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Pesquisar. h</dt> </dl> |



 

 
