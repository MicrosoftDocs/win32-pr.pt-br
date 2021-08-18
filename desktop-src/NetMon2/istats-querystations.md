---
description: O método QueryStations fornece uma lista de todos os computadores que estão capturando dados usando Monitor de Rede.
ms.assetid: feebcb28-914b-450e-95d4-10a60cbf1438
title: Método IStats::QueryStations (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.QueryStations
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: b2d4ead22b3e7308aee3c44b3ff6dff407591cbe675b09a3300f3e7a8720726c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119742636"
---
# <a name="istatsquerystations-method"></a>Método IStats::QueryStations

O **método QueryStations** fornece uma lista de todos os computadores que estão capturando dados usando Monitor de Rede.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT STDMETHODCALLTYPE QueryStations(
  [in, out] QUERYTABLE *lpQueryTable
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lpQueryTable* \[ in, out\]
</dt> <dd>

Ponteiro para uma [estrutura QUERYTABLE.](querytable.md) Na entrada, essa estrutura deve conter o número máximo de computadores que você Monitor de Rede retornar e uma matriz de [estruturas STATIONQUERY.](stationquery.md)

Na saída, essa estrutura retorna o número de computadores que estão capturando dados e uma [estrutura STATIONQUERY](stationquery.md) para cada computador encontrado. Observe que essas informações podem incluir computadores que usam versões Monitor de Rede anteriores à versão 2.0.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se o método for bem-sucedido, o valor de retorno será NMERR \_ SUCCESS.

Se o método não for bem-sucedido, o valor de retorno será o seguinte código de erro:



| Código de retorno                                                                                           | Descrição                                                           |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ \_ SEM \_ MEMÓRIA**</dt> </dl> | A memória necessária para processar essa consulta não estava disponível.<br/> |



 

## <a name="remarks"></a>Comentários

Esse método pode ser chamado a qualquer momento depois [que CreateNPPInterface](createnppinterface.md) é chamado. Uma chamada para esse método é uma chamada síncrona, que pode levar vários segundos para ser concluída conforme Monitor de Rede espera que os computadores remotos respondam à consulta. Somente computadores na sub-rede local podem ser consultados.

É sua responsabilidade alocar a memória para a estrutura [QUERYTABLE](querytable.md) e liberar essa memória depois que a tabela não for mais necessária. Esse requisito inclui a memória necessária para a matriz [STATIONQUERY](stationquery.md) usada em QUERYTABLE.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Netmon.h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[IStats](istats.md)
</dt> <dt>

[Querytable](querytable.md)
</dt> <dt>

[STATIONQUERY](stationquery.md)
</dt> </dl>

 

 




