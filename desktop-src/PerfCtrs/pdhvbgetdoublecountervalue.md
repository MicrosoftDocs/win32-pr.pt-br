---
description: A função PdhVbGetDoubleCounterValue retorna o valor atual do contador especificado como um valor de ponto flutuante de precisão dupla.
ms.assetid: a2ee63dd-da39-4104-921d-371172bcb45c
title: Função PdhVbGetDoubleCounterValue
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbGetDoubleCounterValue
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: 67f0372a26649fbe781cf4d9bd25794b82d6346e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296751"
---
# <a name="pdhvbgetdoublecountervalue-function"></a>Função PdhVbGetDoubleCounterValue

A função **PdhVbGetDoubleCounterValue** retorna o valor atual do contador especificado como um valor de ponto flutuante de precisão dupla. Você deve verificar o *status do progresso* antes de usar o número retornado, pois o contador pode não ser válido quando for lido. Para verificar o status do contador, chame a função [**PdhVbIsGoodStatus**](pdhvbisgoodstatus.md) .

> [!IMPORTANT]
> A função que este tópico descreve pode ser alterada ou indisponível no futuro. Em vez disso, a Microsoft recomenda que você use as funções descritas em [funções de contadores de desempenho](performance-counters-functions.md).

Função PdhVbGetDoubleCounterValue ( \_ ByVal enhandle, como Long, \_ ByVal status por Long \_ ) como Double

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Manipulador* 
</dt> <dd>

ID do contador cujo valor atual deve ser lido.

</dd> <dt>

*Status do progresso* 
</dt> <dd>

Variável na qual o status atual do valor do contador é retornado para o chamador. O valor de dados retornados será válido se e somente se o valor retornado em mystatus for \_ PDH \_ CSTATUS \_ dados válidos ou PDH \_ CSTATUS \_ novos \_ dados (consulte códigos de erro da PDH). Se o valor retornado em mystatus for qualquer outro valor, não use os dados.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

A função retorna o valor de ponto flutuante de precisão dupla do contador atual, computado e formatado, conforme definido pelo tipo de contador.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                               |
| Biblioteca<br/>                  | <dl> <dt>PDH. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Pdh.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**PdhVbIsGoodStatus**](pdhvbisgoodstatus.md)
</dt> </dl>

 

 




