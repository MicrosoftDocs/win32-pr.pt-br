---
description: Modifica os dados de configuração para o serviço.
ms.assetid: E6133DA7-A137-42FA-A523-5B93E9C6DB79
title: Método ModifyServiceSettings da classe Msvm_MetricService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricService.ModifyServiceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: b680f5f46d99d46f99094e05db653083fd7ae952
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647330"
---
# <a name="modifyservicesettings-method-of-the-msvm_metricservice-class"></a>Método ModifyServiceSettings da \_ classe MetricService Msvm

Modifica os dados de configuração para o serviço.

## <a name="syntax"></a>Sintaxe


```mof
uint32 ModifyServiceSettings(
  [in]  string              SettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*SettingData* \[ no\]
</dt> <dd>

Contém uma instância inserida da classe [**Msvm \_ MetricServiceSettingData**](msvm-metricservicesettingdata.md) que contém os dados de configuração modificados para o serviço.

</dd> <dt>

*Trabalho* \[ do fora\]
</dt> <dd>

Se a operação for executada de forma assíncrona, esse método retornará 4096, e esse parâmetro conterá uma referência a um objeto derivado de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método retorna um dos valores a seguir.



| Código/valor de retorno                                                                                                                                                                | Descrição                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <dt>**Concluído sem erro**</dt> <dt>0</dt> </dl>                    | Sucesso.<br/>                                |
| <dl> <dt>**Parâmetros de método verificados-trabalho iniciado**</dt> <dt>4096</dt> </dl> | Parâmetros de método marcados, trabalho iniciado.<br/> |
| <dl> <dt>32768</dt> <dt>**com falha**</dt> </dl>                                 | Falhou.<br/>                                 |
| <dl> <dt>**Acesso negado**</dt> <dt>32769</dt> </dl>                          | Acesso negado.<br/>                          |
| <dl> <dt>**Sem suporte**</dt> <dt>32770</dt> </dl>                          | Não há suporte.<br/>                          |
| <dl> O <dt>**status é desconhecido**</dt> <dt>32771</dt> </dl>                      | O status é desconhecido.<br/>                      |
| <dl> <dt>**Tempo limite**</dt> <dt>32772</dt> </dl>                                | Tempo limite.<br/>                               |
| <dl> <dt>**Parâmetro inválido**</dt> <dt>32773</dt> </dl>                      | Parâmetro inválido.<br/>                      |
| <dl> O <dt>**sistema está em uso**</dt> <dt>32774</dt> </dl>                       | O sistema está em uso.<br/>                       |
| <dl> <dt>**Estado inválido para esta operação**</dt> <dt>32775</dt> </dl>       | Estado inválido para esta operação.<br/>       |
| <dl> <dt>**Tipo de dados incorreto**</dt> <dt>32776</dt> </dl>                    | Tipo de dados incorreto.<br/>                    |
| <dl> O <dt>**sistema não está disponível**</dt> <dt>32777</dt> </dl>                | O sistema não está disponível.<br/>                |
| <dl> <dt>**Memória insuficiente**</dt> <dt>32778</dt> </dl>                          | Sem memória.<br/>                          |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                                              |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                                    |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Msvm \_ MetricService**](msvm-metricservice.md)
</dt> </dl>

 

