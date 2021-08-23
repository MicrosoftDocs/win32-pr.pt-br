---
description: Desmonta o dispositivo PCI especificado para que ele possa ser atribuído.
ms.assetid: 8ea3bc27-93ba-4db8-a4aa-cdfea225eaa9
title: Método DismountAssignableDevice da classe Msvm_AssignableDeviceService classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_AssignableDeviceService.DismountAssignableDevice
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c9b602a26f789b0d7ccded487bafe8c0295133f6e4dd9457d51ce33ee24a8d0c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119693476"
---
# <a name="dismountassignabledevice-method-of-the-msvm_assignabledeviceservice-class"></a>Método DismountAssignableDevice da classe Msvm \_ AssignableDeviceService

Desmonta o dispositivo PCI especificado para que ele possa ser atribuído.

## <a name="syntax"></a>Sintaxe


```mof
uint32 DismountAssignableDevice(
  [in]  string              DismountSettingData,
  [out] string              DismountedDeviceInstancePath,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*DismountSettingData* \[ Em\]
</dt> <dd>

Instância inserida de um objeto de dados de configuração que especifica o dispositivo PCI a ser desmontado.

</dd> <dt>

*DismountedDeviceInstancePath* \[ out\]
</dt> <dd>

Cadeia de caracteres que contém o caminho da instância do dispositivo para o dispositivo desmontado.

</dd> <dt>

*Trabalho* \[ out\]
</dt> <dd>

Uma referência ao trabalho (pode ser nula se a tarefa for concluída).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Em caso de sucesso, retorna 0 ou 4096; caso contrário, retornará um erro.

<dl> <dt>

**Concluído sem erro** (0)
</dt> <dt>

**Parâmetros de método verificados – Trabalho iniciado** (4096)
</dt> <dt>

**Falha** (32768)
</dt> <dt>

**Acesso negado** (32769)
</dt> <dt>

**Sem suporte** (32770)
</dt> <dt>

**O status é desconhecido** (32771)
</dt> <dt>

**Tempoout** (32772)
</dt> <dt>

**Parâmetro inválido** (32773)
</dt> <dt>

**O sistema está em uso** (32774)
</dt> <dt>

**Estado inválido para esta operação** (32775)
</dt> <dt>

**Tipo de dados incorreto** (32776)
</dt> <dt>

**O sistema não está disponível** (32777)
</dt> <dt>

**Memória sem memória** (32778)
</dt> <dt>

**Arquivo não encontrado** (32779)
</dt> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10, versão 1703 somente \[ para aplicativos da área de trabalho\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | Virtualização \\ raiz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Msvm \_ AssignableDeviceService**](msvm-assignabledeviceservice.md)
</dt> </dl>

 

 




