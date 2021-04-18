---
description: A função PdhVbGetCounterPathFromList copia o caminho do contador referenciado pelo parâmetro de índice de uma lista de caminhos de contador criada pelo usuário a partir da chamada mais recente para a função PdhVbCreateCounterPathList.
ms.assetid: e77a022d-42f2-4c48-acb7-36cb013730dd
title: Função PdhVbGetCounterPathFromList
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbGetCounterPathFromList
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: 4c5ae4632ede898b7cd323723037ea68d53455b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105756700"
---
# <a name="pdhvbgetcounterpathfromlist-function"></a>Função PdhVbGetCounterPathFromList

A função **PdhVbGetCounterPathFromList** copia o caminho do contador referenciado pelo parâmetro de *índice* de uma lista de caminhos de contador criada pelo usuário a partir da chamada mais recente para a função [**PdhVbCreateCounterPathList**](pdhvbcreatecounterpathlist.md) .

> [!IMPORTANT]
> A função que este tópico descreve pode ser alterada ou indisponível no futuro. Em vez disso, a Microsoft recomenda que você use as funções descritas em [funções de contadores de desempenho](performance-counters-functions.md).

Função PdhVbGetCounterPathFromList ( \_ o índice ByVal como longo, \_ ByVal buffer como cadeia de caracteres, \_ ByVal BufferLength como longo \_ ) enquanto longo

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Index* 
</dt> <dd>

Índice do caminho do contador a ser recuperado. Deve ser um valor que seja maior ou igual a 1 e menor ou igual ao valor retornado pela função [**PdhVbCreateCounterPathList**](pdhvbcreatecounterpathlist.md) .

</dd> <dt>

*Buffer* 
</dt> <dd>

Cadeia de caracteres dimensioned e Initialized que receberá o caminho do contador que corresponde ao valor do parâmetro de índice.

</dd> <dt>

*BufferLength* 
</dt> <dd>

Número máximo de caracteres que se ajustarão à cadeia de caracteres referenciada pelo buffer.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

A função retorna o número de caracteres copiados para o buffer.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                               |
| Biblioteca<br/>                  | <dl> <dt>PDH. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Pdh.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**PdhVbCreateCounterPathList**](pdhvbcreatecounterpathlist.md)
</dt> <dt>

[**PdhVbGetCounterPathElements**](pdhvbgetcounterpathelements.md)
</dt> <dt>

[**PdhVbGetOneCounterPath**](pdhvbgetonecounterpath.md)
</dt> </dl>

 

 




