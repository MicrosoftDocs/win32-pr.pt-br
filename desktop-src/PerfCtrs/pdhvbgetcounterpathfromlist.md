---
description: A função PdhVbGetCounterPathFromList copia o caminho do contador referenciado pelo parâmetro Index de uma lista de caminhos de contador criada pelo usuário da chamada mais recente para a função PdhVbCreateCounterPathList.
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
ms.openlocfilehash: 85760bbcdcc81204340004304be1f0c14bf9bcbbbd7a5b59eebf47a25f7b15c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120033776"
---
# <a name="pdhvbgetcounterpathfromlist-function"></a>Função PdhVbGetCounterPathFromList

A **função PdhVbGetCounterPathFromList** copia o caminho do contador referenciado pelo parâmetro *Index* de uma lista de caminhos de contador criada pelo usuário da chamada mais recente para a função [**PdhVbCreateCounterPathList.**](pdhvbcreatecounterpathlist.md)

> [!IMPORTANT]
> A função que este tópico descreve pode ser alterada ou não disponível no futuro. Em vez disso, a Microsoft recomenda que você use as funções descritas em [Funções de Contadores de Desempenho](performance-counters-functions.md).

Função PdhVbGetCounterPathFromList( \_ ByVal Index as Long, \_ ByVal Buffer as String, \_ ByVal BufferLength as long \_ )

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Index* 
</dt> <dd>

Índice do caminho do contador a ser recuperado. Esse deve ser um valor maior ou igual a 1 e menor ou igual ao valor retornado pela [**função PdhVbCreateCounterPathList.**](pdhvbcreatecounterpathlist.md)

</dd> <dt>

*Buffer* 
</dt> <dd>

Cadeia de caracteres dimensionada e inicializada que receberá o caminho do contador que corresponde ao valor do parâmetro Index.

</dd> <dt>

*BufferLength* 
</dt> <dd>

Número máximo de caracteres que se ajustarão à cadeia de caracteres referenciada por Buffer.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

A função retorna o número de caracteres copiados para Buffer.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                               |
| Biblioteca<br/>                  | <dl> <dt>Pdh.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Pdh.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**PdhVbCreateCounterPathList**](pdhvbcreatecounterpathlist.md)
</dt> <dt>

[**PdhVbGetCounterPathElements**](pdhvbgetcounterpathelements.md)
</dt> <dt>

[**PdhVbGetOneCounterPath**](pdhvbgetonecounterpath.md)
</dt> </dl>

 

 




