---
description: Permite que a especificação do ponto no tempo coleta de métricas seja iniciada e especifique o tempo de intervalo de exemplo preferencial para a coleta de dados periódicas.
ms.assetid: 3dd6dc16-a618-49ff-bbaf-cfa25c249cf1
title: Método ControlSampleTimes da classe CIM_MetricService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MetricService.ControlSampleTimes
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 833e828a7622dfcd76a7b061e3890fbe111de10a6b8c3c2d3faf0801429678f3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119695066"
---
# <a name="controlsampletimes-method-of-the-cim_metricservice-class"></a>Método ControlSampleTimes da \_ classe METRICSERVICE CIM

Permite que a especificação do ponto no tempo coleta de métricas seja iniciada e especifique o tempo de intervalo de exemplo preferencial para a coleta de dados periódicas.

Sempre que a amostragem de métricas adicionais é iniciada, as configurações especificadas por esse método podem ser usadas.

## <a name="syntax"></a>Sintaxe


```mof
uint32 ControlSampleTimes(
  [in] datetime StartSampleTime,
  [in] datetime PreferredSampleInterval,
  [in] boolean  RestartGathering
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*StartSampleTime* \[ no\]
</dt> <dd>

Ponto no tempo em que a amostragem para as métricas deve ser iniciada.

Um valor de 99990101000000.000000 + 000 deverá indicar que a amostragem deve ser iniciada na próxima vez que for sincronizada com a hora completa. A amostragem será sincronizada com a hora completa se segundos desde o intervalo de amostragem de módulo de meia-noite em segundos for igual a 0.

</dd> <dt>

*PreferredSampleInterval* \[ no\]
</dt> <dd>

Tempo de intervalo de amostragem preferencial. Para obter métricas correlacionadas, é recomendável que o intervalo de exemplo seja escolhido de forma que o tempo de intervalo de amostragem de 3600 de módulo em segundos seja igual a 0.

É responsabilidade da implementação do serviço de métrica CIM decidir se o tempo de intervalo de amostragem solicitado é respeitado.

O cliente CIM pode verificar se os provedores de métrica estão respeitando o tempo de intervalo de amostragem solicitado, recuperando instâncias BaseMetricDefinition relacionadas e verificando o conteúdo [**do \_ BaseMetricDefinition CIM**](cim-basemetricdefinition.md).**Propriedade SampleInterval** .

</dd> <dt>

*RestartGathering* \[ no\]
</dt> <dd>

**True** para solicitar que a coleta de todas as métricas associadas ao serviço de métrica seja reiniciada com essa chamada de método.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um 0 em caso de êxito; caso contrário, retornará um erro.

<dl> <dt>

**Êxito** (0)
</dt> <dt>

**Sem suporte** (1)
</dt> <dt>

**Falha** (2)
</dt> <dt>

**Método reservado** (..)
</dt> <dt>

**Específico do fornecedor** (32768.. 65535)
</dt> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8.1<br/>                                                                                  |
| Servidor mínimo com suporte<br/> | Windows Server 2012 R2<br/>                                                                       |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_METRICSERVICE CIM**](cim-metricservice.md)
</dt> </dl>

 

 




