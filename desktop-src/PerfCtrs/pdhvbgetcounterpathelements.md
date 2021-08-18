---
description: A função PdhVbGetCounterPathElements analisa uma cadeia de caracteres de caminho de contador de desempenho totalmente qualificado em seus elementos individuais.
ms.assetid: 5459c7dd-e8b6-48cd-a33f-cafdc64dd9ee
title: Função PdhVbGetCounterPathElements
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbGetCounterPathElements
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: fecd9ecac573ecc1a5afabcfc4a14bf6fd1ca5cee7b44387ea910b0cf1a5820d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011324"
---
# <a name="pdhvbgetcounterpathelements-function"></a>Função PdhVbGetCounterPathElements

A função **PdhVbGetCounterPathElements** analisa uma cadeia de caracteres de caminho de contador de desempenho totalmente qualificado em seus elementos individuais. Cada uma das variáveis de cadeia de caracteres deve ter o mesmo tamanho (*BufferSize*) e dimensionada e inicializada antes de ser usada nessa função.

> [!IMPORTANT]
> A função que este tópico descreve pode ser alterada ou indisponível no futuro. Em vez disso, a Microsoft recomenda que você use as funções descritas em [funções de contadores de desempenho](performance-counters-functions.md).

Função PdhVbGetCounterPathElements ( \_ ByVal pathstring como String, \_ ByVal MachineName as String, \_ ByVal ObjectName as String, \_ ByVal InstanceName as String, \_ ByVal ParentInstance as String, \_ ByVal CounterName as String, \_ ByVal BufferSize as Long \_ ) como Long

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Caminho da* 
</dt> <dd>

Cadeia de caracteres de caminho do contador que deve ser dividida em seus elementos individuais.

</dd> <dt>

*MachineName* 
</dt> <dd>

Cadeia de caracteres para receber o nome do computador.

</dd> <dt>

*ObjectName* 
</dt> <dd>

Cadeia de caracteres para receber o nome do objeto.

</dd> <dt>

*InstanceName* 
</dt> <dd>

Cadeia de caracteres para receber o nome da instância, se usado.

</dd> <dt>

*ParentInstance* 
</dt> <dd>

Cadeia de caracteres para receber a instância pai, se usada.

</dd> <dt>

*CounterName* 
</dt> <dd>

Cadeia de caracteres para receber o nome do contador.

</dd> <dt>

*BufferSize* 
</dt> <dd>

Tamanho máximo de cada variável de cadeia de caracteres usada como parâmetro para esta chamada de função.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, ela retornará um inteiro **longo** igual a erro de \_ êxito.

Se a função falhar, o valor de retorno será um [código de erro do sistema](/windows/desktop/Debug/system-error-codes) ou um código de [erro PDH](pdh-error-codes.md). Os valores a seguir são possíveis.



| Código de retorno                                                                                                     | Descrição                                                                                    |
|-----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_argumento inválido de PDH \_**</dt> </dl>           | Um ou mais dos buffers de cadeia de caracteres não tem o tamanho correto.<br/>                          |
| <dl> <dt>**\_mais \_ dados da PDH**</dt> </dl>                  | Um ou mais dos elementos do caminho do contador é muito grande para o comprimento do buffer de retorno.<br/> |
| <dl> <dt>**\_falha de \_ alocação de memória de PDH \_**</dt> </dl> | Não foi possível alocar um buffer de memória temporário.<br/>                                   |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho XP\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                               |
| Biblioteca<br/>                  | <dl> <dt>PDH. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Pdh.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**PdhVbCreateCounterPathList**](pdhvbcreatecounterpathlist.md)
</dt> <dt>

[**PdhVbGetCounterPathFromList**](pdhvbgetcounterpathfromlist.md)
</dt> <dt>

[**PdhVbGetOneCounterPath**](pdhvbgetonecounterpath.md)
</dt> </dl>

 

