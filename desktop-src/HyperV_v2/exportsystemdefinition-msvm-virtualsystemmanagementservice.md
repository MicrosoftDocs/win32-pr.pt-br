---
description: Exporta uma máquina virtual ou um instantâneo de uma máquina virtual para um arquivo.
ms.assetid: b88712e4-a1a6-4188-8082-f4973f89018d
title: Método ExportSystemDefinition da classe Msvm_VirtualSystemManagementService dados
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.ExportSystemDefinition
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 72198055a81ce13a6b38859ed5ba6370faf7de046bc9f2cc3a158548c2679685
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119254026"
---
# <a name="exportsystemdefinition-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Método ExportSystemDefinition da classe Msvm \_ VirtualSystemManagementService

Exporta uma máquina virtual ou um instantâneo de uma máquina virtual para um arquivo. A máquina virtual deve estar no estado "desligado" ou "salvo" a ser exportado. A máquina virtual, suas definições de configuração associadas e suas configurações de recurso associadas serão preservadas no arquivo resultante.

## <a name="syntax"></a>Sintaxe


```mof
uint32 ExportSystemDefinition(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 ExportDirectory,
  [in]  string                 ExportSettingData,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ComputerSystem* \[ Em\]
</dt> <dd>

Uma referência a um [**\_ ComputerSystem cim**](/windows/desktop/CIMWin32Prov/cim-computersystem) que representa a máquina virtual a ser exportada.

</dd> <dt>

*ExportDirectory* \[ Em\]
</dt> <dd>

O caminho totalmente qualificado do diretório para o qual a máquina virtual deve ser exportada. Se a propriedade **CreateVmExportSubdirectory** da classe [**Msvm \_ VirtualSystemExportSettingData**](msvm-virtualsystemexportsettingdata.md) no parâmetro *ExportSettingData* for definida como **True**, esse diretório poderá ser reutilizado para exportar várias máquinas virtuais e esse método colocará cada definição de máquina virtual em um subdiretório separado nesse caminho.

</dd> <dt>

*ExportSettingData* \[ Em\]
</dt> <dd>

Uma instância inserida da [**classe Msvm \_ VirtualSystemExportSettingData**](msvm-virtualsystemexportsettingdata.md) que representa as configurações para a operação de exportação.

</dd> <dt>

*Trabalho* \[ out\]
</dt> <dd>

Se a operação for executada de forma assíncrona, esse método retornará 4096 e esse parâmetro conterá uma referência a um objeto derivado de [**CIM \_ ConcreteJob.**](/previous-versions//cc136808(v=vs.85))

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método retorna um dos valores a seguir.

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
</dt> </dl>

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

[**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

