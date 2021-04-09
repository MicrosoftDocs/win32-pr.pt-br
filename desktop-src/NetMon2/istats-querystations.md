---
description: O método QueryStations fornece uma lista de todos os computadores que estão atualmente capturando dados usando Monitor de Rede.
ms.assetid: feebcb28-914b-450e-95d4-10a60cbf1438
title: 'Método IStats:: QueryStations (Netmon. h)'
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
ms.openlocfilehash: 99c3be3926191c27ad038034373e411b5c22d9fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011460"
---
# <a name="istatsquerystations-method"></a>Método IStats:: QueryStations

O método **QueryStations** fornece uma lista de todos os computadores que estão atualmente capturando dados usando monitor de rede.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT STDMETHODCALLTYPE QueryStations(
  [in, out] QUERYTABLE *lpQueryTable
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lpQueryTable* \[ entrada, saída\]
</dt> <dd>

Ponteiro para uma estrutura de [QUERYTABLE](querytable.md) . Na entrada, essa estrutura deve conter o número máximo de computadores que você deseja Monitor de Rede para retornar e uma matriz de estruturas [STATIONQUERY](stationquery.md) .

Na saída, essa estrutura retorna o número de computadores que estão capturando dados e uma estrutura [STATIONQUERY](stationquery.md) para cada computador encontrado. Observe que essas informações podem incluir computadores que usam versões do Monitor de Rede que são anteriores à versão 2,0.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se o método for bem-sucedido, o valor de retorno será NMERR com \_ êxito.

Se o método não for bem-sucedido, o valor de retorno será o seguinte código de erro:



| Código de retorno                                                                                           | Descrição                                                           |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ \_ de \_ memória insuficiente**</dt> </dl> | A memória necessária para processar esta consulta não estava disponível.<br/> |



 

## <a name="remarks"></a>Comentários

Esse método pode ser chamado a qualquer momento depois que [CreateNPPInterface](createnppinterface.md) for chamado. Uma chamada para esse método é uma chamada síncrona, que pode levar vários segundos para ser concluída, pois Monitor de Rede aguarda que os computadores remotos respondam à consulta. Somente os computadores na sub-rede local podem ser consultados.

É sua responsabilidade alocar a memória para a estrutura [QUERYTABLE](querytable.md) e liberar essa memória depois que a tabela não for mais necessária. Esse requisito inclui a memória necessária para a matriz [STATIONQUERY](stationquery.md) usada em QUERYTABLE.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[IStats](istats.md)
</dt> <dt>

[CONSULTA](querytable.md)
</dt> <dt>

[STATIONQUERY](stationquery.md)
</dt> </dl>

 

 




