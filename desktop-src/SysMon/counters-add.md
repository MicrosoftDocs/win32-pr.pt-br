---
title: Método Counters. Add
description: Adiciona uma instância de monoitem à coleção.
ms.assetid: 9daecfe6-c2a9-48af-8b59-4f81f0325535
keywords:
- Adicionar método SysMon
- Adicionar método SysMon, classe de contadores
- Classe Counters SysMon, método Add
topic_type:
- apiref
api_name:
- Counters.Add
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a36d2b9bdc2edc9565b1eac5ebae335e5fbad80752f572c48c0f1b05c9668de1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118883394"
---
# <a name="countersadd-method"></a>Método Counters. Add

Adiciona uma instância de [**monoitem**](counteritem.md) à coleção.

## <a name="syntax"></a>Sintaxe


```VB
Counters.Add( _
  ByVal pathname As String _
) As CounterItem
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*nome do caminho* \[ no\]
</dt> <dd>

Caminho para o contador. O caminho pode incluir um nome de computador e deve incluir um nome de objeto de desempenho, um nome de instância de objeto se o objeto de desempenho especificado der suporte a várias instâncias e um nome de contador. Esta especificação de caminho não diferencia maiúsculas de minúsculas.

Para obter detalhes sobre como especificar um caminho de contador, consulte [especificando um caminho de contador](/windows/desktop/PerfCtrs/specifying-a-counter-path).

</dd> </dl>

## <a name="exceptions"></a>Exceções



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Tipo de exceção</th>
<th>Condição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>System. Runtime. InteropServices. COMException</strong></td>
<td>Você pode receber essa exceção por um dos seguintes motivos:
<ul>
<li>O objeto de desempenho especificado não foi encontrado no computador. O valor Err. Number é 0xC0000BB8.</li>
<li>O contador especificado não pôde ser encontrado. O valor Err. Number é 0xC0000BB9.</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Comentários

Se você especificar um contador curinga no parâmetro *PathName* , o método **Add** criará um objeto de Counter [**Item**](counteritem.md) para cada caminho expandido. Em seguida, o método **Add** retorna um ponteiro para o primeiro **Item** a ser adicionado.

Se o caractere curinga resultar em um contador duplicado, o erro não será relatado e nenhuma duplicata será criada. Se ocorrer uma condição de erro antes que todos os contadores sejam criados, o erro será relatado e os contadores restantes não serão criados.

Não há nenhum limite para o número de contadores que você pode adicionar; no entanto, o SYSMON irá grafar apenas os primeiros 1.024 contadores na coleção. Não há nenhum limite para o número de contadores que o SYSMON exibirá em um relatório.

Para receber uma notificação quando um contador é adicionado, implemente o evento [OnCounterAdded](systemmonitor-oncounteradded.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                            |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Item**](counteritem.md)
</dt> <dt>

[**Contadores**](counters.md)
</dt> <dt>

[**SystemMonitor.BrowseCounters**](systemmonitor-browsecounters.md)
</dt> </dl>

 

