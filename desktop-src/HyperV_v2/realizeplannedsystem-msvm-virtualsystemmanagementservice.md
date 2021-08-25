---
description: Valida a configuração de uma máquina virtual planejada e a converte em uma máquina virtual realizada.
ms.assetid: bddbdc35-4603-45c3-96b4-04f445dbb3a6
title: Método RealizePlannedSystem da Msvm_VirtualSystemManagementService classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.RealizePlannedSystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 7589c4c68a5375971c085abd0411c0e6e8c7813797ba2f5e5e6f72483a4894a0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119980206"
---
# <a name="realizeplannedsystem-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Método RealizePlannedSystem da classe Msvm \_ VirtualSystemManagementService

Valida a configuração de uma máquina virtual planejada e a converte em uma máquina virtual realizada. Qualquer runtime ou arquivos de estado salvos associados à máquina virtual serão copiados do diretório de importação para a raiz de dados da máquina virtual, se aplicável.

## <a name="syntax"></a>Sintaxe


```mof
uint32 RealizePlannedSystem(
  [in]  Msvm_PlannedComputerSystem REF PlannedSystem,
  [out] CIM_ComputerSystem         REF ResultingSystem,
  [out] CIM_ConcreteJob            REF Job
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*PlannedSystem* \[ Em\]
</dt> <dd>

Uma referência à [**instância Msvm \_ PlannedComputerSystem**](msvm-plannedcomputersystem.md) que deve ser convertida em uma máquina virtual realizada.

</dd> <dt>

*ResultingSystem* \[ out\]
</dt> <dd>

Se a operação for concluída de forma síncrona, uma referência a um objeto [**\_ ComputerSystem cim**](msvm-computersystem.md) que representa a máquina virtual resultante realizada.

Tipo de dados atualizado [**do Msvm \_ ComputerSystem**](msvm-computersystem.md) Windows 10, versão 1703.

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

## <a name="examples"></a>Exemplos

O exemplo de C# a seguir usa **o método RealizePlannedSystem** para realizar uma máquina virtual planejada. Esse código é retirado do exemplo de máquinas virtuais [planejadas do Hyper-V.](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Hyper-V/Pvm) Os utilitários referenciados podem ser encontrados em [Utilitários comuns para as amostras de virtualização (V2)](common-utilities-for-the-virtualization-samples-v2.md).

> [!IMPORTANT]
> Para funcionar corretamente, o código a seguir deve ser executado no servidor host da máquina virtual e deve ser executado com privilégios de Administrador.

 


```CSharp
/// <summary>
/// Finds the first Planned VM matching pvmName and realizes it.
/// </summary>
/// <param name="pvmName">The name of the PVM to be realized.</param>
/// <returns>The Realized Virtual Machine.</returns>
internal static ManagementObject
RealizePvm(
    string pvmName
    )
{
    ManagementObject vm = null;
    ManagementScope scope = new ManagementScope(@"root\virtualization\v2");

    using (ManagementObject pvm = WmiUtilities.GetPlannedVirtualMachine(pvmName, scope))
    using (ManagementObject managementService = WmiUtilities.GetVirtualMachineManagementService(scope))
    using (ManagementBaseObject inParams =
        managementService.GetMethodParameters("RealizePlannedSystem"))
    {
        inParams["PlannedSystem"] = pvm.Path;

        Console.WriteLine("Realizing Planned Virtual Machine \"{0}\" ({1})...",
                pvm["ElementName"], pvm["Name"]);

        using (ManagementBaseObject outParams =
            managementService.InvokeMethod("RealizePlannedSystem", inParams, null))
        {
            if (WmiUtilities.ValidateOutput(outParams, scope, true, true))
            {
                using (ManagementObject job =
                    new ManagementObject((string)outParams["Job"]))
                using (ManagementObjectCollection pvmCollection =
                    job.GetRelated("Msvm_ComputerSystem",
                        "Msvm_AffectedJobElement", null, null, null, null, false, null))
                {
                    vm = WmiUtilities.GetFirstObjectFromCollection(pvmCollection);
                }
            }
        }
    }

    return vm;
}
```



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

 

