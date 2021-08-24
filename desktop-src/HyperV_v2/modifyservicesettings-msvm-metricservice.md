---
description: Método ModifyServiceSettings da classe Msvm_MetricService - Modifica os dados de configuração para o serviço.
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
ms.openlocfilehash: 51af98d230433687d9a16cb3ab858fd746b7ff1ca4e17eaf0b36cce16e92c875
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119693906"
---
# <a name="modifyservicesettings-method-of-the-msvm_metricservice-class"></a>Método ModifyServiceSettings da classe Msvm \_ MetricService

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

*SettingData* \[ Em\]
</dt> <dd>

Contém uma instância inserida da [**classe Msvm \_ MetricServiceSettingData**](msvm-metricservicesettingdata.md) que contém os dados de configuração modificados para o serviço.

</dd> <dt>

*Trabalho* \[ out\]
</dt> <dd>

Se a operação for executada de forma assíncrona, esse método retornará 4096 e esse parâmetro conterá uma referência a um objeto derivado de [**CIM \_ ConcreteJob.**](/previous-versions//cc136808(v=vs.85))

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método retorna um dos valores a seguir.



| Valor/código de retorno                                                                                                                                                                | Descrição                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <dt>**Concluído sem erro**</dt> <dt>0</dt> </dl>                    | Êxito.<br/>                                |
| <dl> <dt>**Parâmetros de método verificados – Trabalho iniciado**</dt> <dt>4096</dt> </dl> | Parâmetros de método verificados, trabalho iniciado.<br/> |
| <dl> <dt>**Falha**</dt> <dt>32768</dt> </dl>                                 | Falhou.<br/>                                 |
| <dl> <dt>**Acesso negado**</dt> <dt>32769</dt> </dl>                          | Acesso negado<br/>                          |
| <dl> <dt>**Sem suporte**</dt> <dt>32770</dt> </dl>                          | Sem suporte.<br/>                          |
| <dl> <dt>**O status é desconhecido**</dt> <dt>32771</dt> </dl>                      | O status é desconhecido.<br/>                      |
| <dl> <dt>**Tempoout**</dt> <dt>32772</dt> </dl>                                | Tempo de vida.<br/>                               |
| <dl> <dt>**Parâmetro inválido**</dt> <dt>32773</dt> </dl>                      | Parâmetro inválido.<br/>                      |
| <dl> <dt>**O sistema está em uso**</dt> <dt>32774</dt> </dl>                       | O sistema está em uso.<br/>                       |
| <dl> <dt>**Estado inválido para esta operação**</dt> <dt>32775</dt> </dl>       | Estado inválido para esta operação.<br/>       |
| <dl> <dt>**Tipo de dados incorreto**</dt> <dt>32776</dt> </dl>                    | Tipo de dados incorreto.<br/>                    |
| <dl> <dt>**O sistema não está disponível**</dt> <dt>32777</dt> </dl>                | O sistema não está disponível.<br/>                |
| <dl> <dt>**Memória sem memória**</dt> <dt>32778</dt> </dl>                          | Sem memória.<br/>                          |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8 somente aplicativos da área de trabalho\]<br/>                                                              |
| Servidor mínimo com suporte<br/> | \[Windows Server 2012 somente aplicativos da área de trabalho\]<br/>                                                    |
| Namespace<br/>                | Virtualização \\ raiz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Msvm \_ MetricService**](msvm-metricservice.md)
</dt> </dl>

 

