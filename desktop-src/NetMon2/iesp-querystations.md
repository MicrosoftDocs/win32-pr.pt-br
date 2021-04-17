---
description: O método QueryStations fornece uma lista de todos os computadores que atualmente usam Monitor de Rede para capturar dados de rede.
ms.assetid: 5ad99810-e463-4477-a542-cf4dfa6967a4
title: 'Método IESP:: QueryStations (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IESP.QueryStations
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 5287f472b2a0641eb29e4f1b37b6fe4e089dfa86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105779974"
---
# <a name="iespquerystations-method"></a>Método IESP:: QueryStations

O método **QueryStations** fornece uma lista de todos os computadores que atualmente usam Monitor de rede para capturar dados de rede.

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

Na saída, essa estrutura retorna o número de computadores que estão capturando dados e uma estrutura [STATIONQUERY](stationquery.md) para cada computador encontrado. Observe que esse total pode incluir computadores que usam versões do Monitor de Rede que são anteriores à versão 2,0.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se o método for bem-sucedido, o valor de retorno será NMERR com \_ êxito.

Se o método não for bem-sucedido, o valor de retorno será o seguinte código de erro:



| Código de retorno                                                                                           | Descrição                                                         |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ \_ de \_ memória insuficiente**</dt> </dl> | A memória necessária para processar esta consulta não estava disponível.<br/> |



 

## <a name="remarks"></a>Comentários

Esse método pode ser chamado a qualquer momento depois que o método [CreateNPPInterface](createnppinterface.md) é chamado. Uma chamada para esse método é uma chamada síncrona, que pode levar vários segundos para ser concluída, pois Monitor de Rede aguarda que os computadores remotos respondam à consulta. Somente os computadores na sub-rede local podem ser consultados.

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

[IESP](iesp.md)
</dt> <dt>

[CONSULTA](querytable.md)
</dt> <dt>

[STATIONQUERY](stationquery.md)
</dt> </dl>

 

 




