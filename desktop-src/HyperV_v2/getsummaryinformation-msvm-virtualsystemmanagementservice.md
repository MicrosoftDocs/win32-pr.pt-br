---
description: Retorna informações de resumo da máquina virtual.
ms.assetid: CDDC2B5A-8172-4E6D-A206-CEAB9E54C69A
title: Método GetSummaryInformation da classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.GetSummaryInformation
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 1399acd40f768fdb857d6a4a26e80a52d29111b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296209"
---
# <a name="getsummaryinformation-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Método GetSummaryInformation da \_ classe VirtualSystemManagementService Msvm

Retorna informações de resumo da máquina virtual.

## <a name="syntax"></a>Sintaxe


```mof
uint32 GetSummaryInformation(
  [in]  CIM_VirtualSystemSettingData REF SettingData[],
  [in]  uint32                           RequestedInformation[],
  [out] Msvm_SummaryInformationBase      SummaryInformation[]
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*SettingData* \[ no\]
</dt> <dd>

Tipo: **CIM \_ VirtualSystemSettingData \[ \]**

Uma matriz de [**instâncias \_ VirtualSystemSettingData do CIM**](/previous-versions//cc136954(v=vs.85)) que especificam as máquinas virtuais ou instantâneos para os quais as informações serão recuperadas. Se esse parâmetro for **nulo**, as informações para todas as máquinas virtuais serão recuperadas.

</dd> <dt>

*RequestedInformation* \[ no\]
</dt> <dd>

Tipo: **UInt32 \[ \]**

Uma matriz de valores de enumeração que correspondem às propriedades na classe [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md) , que especificam os dados a serem recuperados para as máquinas virtuais e os instantâneos especificados na matriz *SettingData* .

<dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>**Nome** (0)


</dt> <dd>

Isso corresponde à propriedade **Name** da classe [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md) .

</dd> <dt>

<span id="Element_Name"></span><span id="element_name"></span><span id="ELEMENT_NAME"></span>

<span id="Element_Name"></span><span id="element_name"></span><span id="ELEMENT_NAME"></span>**Nome do elemento** (1)


</dt> <dd>

Isso corresponde à propriedade **ElementName** da classe [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md) .

</dd> <dt>

<span id="Creation_Time"></span><span id="creation_time"></span><span id="CREATION_TIME"></span>

<span id="Creation_Time"></span><span id="creation_time"></span><span id="CREATION_TIME"></span>**Hora de criação** (2)


</dt> <dd>

Isso corresponde à propriedade **CreationTime** da classe [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md) .

</dd> <dt>

<span id="Notes"></span><span id="notes"></span><span id="NOTES"></span>

<span id="Notes"></span><span id="notes"></span><span id="NOTES"></span>**Observações** (3)


</dt> <dd>

Isso corresponde à propriedade **Notes** da classe [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md) .

</dd> <dt>

<span id="Number_of_Processors"></span><span id="number_of_processors"></span><span id="NUMBER_OF_PROCESSORS"></span>

<span id="Number_of_Processors"></span><span id="number_of_processors"></span><span id="NUMBER_OF_PROCESSORS"></span>**Número de processadores** (4)


</dt> <dd>

Isso corresponde à propriedade **NumberOfProcessors** da classe [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md) .

</dd> <dt>

<span id="Small_Thumbnail_Image__80x60_"></span><span id="small_thumbnail_image__80x60_"></span><span id="SMALL_THUMBNAIL_IMAGE__80X60_"></span>

<span id="Small_Thumbnail_Image__80x60_"></span><span id="small_thumbnail_image__80x60_"></span><span id="SMALL_THUMBNAIL_IMAGE__80X60_"></span>**Pequena imagem em miniatura (80x60)** (5)


</dt> <dd>

Isso corresponde à propriedade **ThumbnailImage** da classe [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md) . Uma imagem em miniatura com as dimensões de 80 60 será recuperada.

</dd> <dt>

<span id="Medium_Thumbnail_Image__160x120_"></span><span id="medium_thumbnail_image__160x120_"></span><span id="MEDIUM_THUMBNAIL_IMAGE__160X120_"></span>

<span id="Medium_Thumbnail_Image__160x120_"></span><span id="medium_thumbnail_image__160x120_"></span><span id="MEDIUM_THUMBNAIL_IMAGE__160X120_"></span>**Imagem de miniatura média (160x120)** (6)


</dt> <dd>

Isso corresponde à propriedade **ThumbnailImage** da classe [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md) . Uma imagem em miniatura com as dimensões de 160 120 será recuperada.

</dd> <dt>

<span id="Large_Thumbnail_Image__320x240_"></span><span id="large_thumbnail_image__320x240_"></span><span id="LARGE_THUMBNAIL_IMAGE__320X240_"></span>

<span id="Large_Thumbnail_Image__320x240_"></span><span id="large_thumbnail_image__320x240_"></span><span id="LARGE_THUMBNAIL_IMAGE__320X240_"></span>**Imagem em miniatura grande (320 x 240)** (7)


</dt> <dd>

Isso corresponde à propriedade **ThumbnailImage** da classe [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md) . Uma imagem em miniatura com as dimensões de 320 240 será recuperada.

</dd> <dt>

<span id="AllocatedGPU"></span><span id="allocatedgpu"></span><span id="ALLOCATEDGPU"></span>

<span id="AllocatedGPU"></span><span id="allocatedgpu"></span><span id="ALLOCATEDGPU"></span>**AllocatedGPU** (8)


</dt> <dd>

Isso corresponde à propriedade **AllocatedGPU** da classe [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md) .

</dd> <dt>

<span id="VirtualSwitchNames"></span><span id="virtualswitchnames"></span><span id="VIRTUALSWITCHNAMES"></span>

<span id="VirtualSwitchNames"></span><span id="virtualswitchnames"></span><span id="VIRTUALSWITCHNAMES"></span>**VirtualSwitchNames** (9)


</dt> <dd></dd> <dt>

<span id="Version"></span><span id="version"></span><span id="VERSION"></span>

<span id="Version"></span><span id="version"></span><span id="VERSION"></span>**Versão** (10)


</dt> <dd>

> [!Note]  
> Adicionado ao Windows 10 e ao Windows Server 2016.

 

</dd> <dt>

<span id="Shielded"></span><span id="shielded"></span><span id="SHIELDED"></span>

<span id="Shielded"></span><span id="shielded"></span><span id="SHIELDED"></span>**Blindado** (11)


</dt> <dd>

> [!Note]  
> Adicionado no Windows 10, versão 1703 e Windows Server 2016.

 

</dd> <dt>

<span id="EnabledState"></span><span id="enabledstate"></span><span id="ENABLEDSTATE"></span>

<span id="EnabledState"></span><span id="enabledstate"></span><span id="ENABLEDSTATE"></span>**Enabledstate** (100)


</dt> <dd>

Isso corresponde à propriedade **enabledstate** da classe [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md) .

</dd> <dt>

<span id="ProcessorLoad"></span><span id="processorload"></span><span id="PROCESSORLOAD"></span>

<span id="ProcessorLoad"></span><span id="processorload"></span><span id="PROCESSORLOAD"></span>**ProcessorLoad** (101)


</dt> <dd>

Isso corresponde à propriedade **ProcessorLoad** da classe [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md) .

</dd> <dt>

<span id="ProcessorLoadHistory"></span><span id="processorloadhistory"></span><span id="PROCESSORLOADHISTORY"></span>

<span id="ProcessorLoadHistory"></span><span id="processorloadhistory"></span><span id="PROCESSORLOADHISTORY"></span>**ProcessorLoadHistory** (102)


</dt> <dd>

Isso corresponde à propriedade **ProcessorLoadHistory** da classe [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md) .

</dd> <dt>

<span id="MemoryUsage"></span><span id="memoryusage"></span><span id="MEMORYUSAGE"></span>

<span id="MemoryUsage"></span><span id="memoryusage"></span><span id="MEMORYUSAGE"></span>**MemoryUsage** (103)


</dt> <dd>

Isso corresponde à propriedade **MemoryUsage** da classe [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md) .

</dd> <dt>

<span id="Heartbeat"></span><span id="heartbeat"></span><span id="HEARTBEAT"></span>

<span id="Heartbeat"></span><span id="heartbeat"></span><span id="HEARTBEAT"></span>**Pulsação** (104)


</dt> <dd>

Isso corresponde à propriedade **Heartbeat** da classe [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md) .

</dd> <dt>

<span id="Uptime"></span><span id="uptime"></span><span id="UPTIME"></span>

<span id="Uptime"></span><span id="uptime"></span><span id="UPTIME"></span>**Tempo de atividade** (105)


</dt> <dd>

Isso corresponde à propriedade de **tempo de atividade** da classe [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md) .

</dd> <dt>

<span id="GuestOperatingSystem"></span><span id="guestoperatingsystem"></span><span id="GUESTOPERATINGSYSTEM"></span>

<span id="GuestOperatingSystem"></span><span id="guestoperatingsystem"></span><span id="GUESTOPERATINGSYSTEM"></span>**GuestOperatingSystem** (106)


</dt> <dd>

Isso corresponde à propriedade **GuestOperatingSystem** da classe [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md) .

</dd> <dt>

<span id="Snapshots"></span><span id="snapshots"></span><span id="SNAPSHOTS"></span>

<span id="Snapshots"></span><span id="snapshots"></span><span id="SNAPSHOTS"></span>**Instantâneos** (107)


</dt> <dd>

Isso corresponde à propriedade **Snapshots** da classe [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md) .

</dd> <dt>

<span id="AsynchronousTasks"></span><span id="asynchronoustasks"></span><span id="ASYNCHRONOUSTASKS"></span>

<span id="AsynchronousTasks"></span><span id="asynchronoustasks"></span><span id="ASYNCHRONOUSTASKS"></span>**AsynchronousTasks** (108)


</dt> <dd>

Isso corresponde à propriedade **AsynchronousTasks** da classe [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md) .

</dd> <dt>

<span id="HealthState"></span><span id="healthstate"></span><span id="HEALTHSTATE"></span>

<span id="HealthState"></span><span id="healthstate"></span><span id="HEALTHSTATE"></span>**HealthState** (109)


</dt> <dd>

Isso corresponde à propriedade **HealthState** da classe [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md) .

</dd> <dt>

<span id="OperationalStatus"></span><span id="operationalstatus"></span><span id="OPERATIONALSTATUS"></span>

<span id="OperationalStatus"></span><span id="operationalstatus"></span><span id="OPERATIONALSTATUS"></span>**OperationalStatus** (110)


</dt> <dd>

Isso corresponde à propriedade **OperationalStatus** da classe [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md) .

</dd> <dt>

<span id="StatusDescriptions"></span><span id="statusdescriptions"></span><span id="STATUSDESCRIPTIONS"></span>

<span id="StatusDescriptions"></span><span id="statusdescriptions"></span><span id="STATUSDESCRIPTIONS"></span>**StatusDescriptions** (111)


</dt> <dd>

Isso corresponde à propriedade **StatusDescriptions** da classe [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md) .

</dd> <dt>

<span id="MemoryAvailable"></span><span id="memoryavailable"></span><span id="MEMORYAVAILABLE"></span>

<span id="MemoryAvailable"></span><span id="memoryavailable"></span><span id="MEMORYAVAILABLE"></span>**MemoryAvailable** (112)


</dt> <dd>

Isso corresponde à propriedade **MemoryAvailable** da classe [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md) .

</dd> <dt>

<span id="AvailableMemoryBuffer"></span><span id="availablememorybuffer"></span><span id="AVAILABLEMEMORYBUFFER"></span>

<span id="AvailableMemoryBuffer"></span><span id="availablememorybuffer"></span><span id="AVAILABLEMEMORYBUFFER"></span>**AvailableMemoryBuffer** (113)


</dt> <dd>

Isso corresponde à propriedade **AvailableMemoryBuffer** da classe [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md) .

</dd> <dt>

<span id="Replication_Mode"></span><span id="replication_mode"></span><span id="REPLICATION_MODE"></span>

<span id="Replication_Mode"></span><span id="replication_mode"></span><span id="REPLICATION_MODE"></span>**Modo de replicação** (114)


</dt> <dd>

Isso corresponde à propriedade **replicationmode** da classe [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md) .

</dd> <dt>

<span id="Replication_State"></span><span id="replication_state"></span><span id="REPLICATION_STATE"></span>

<span id="Replication_State"></span><span id="replication_state"></span><span id="REPLICATION_STATE"></span>**Estado de replicação** (115)


</dt> <dd>

Isso corresponde à propriedade **replicationstate** da classe [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md) .

</dd> <dt>

<span id="Replication_HealthTest_Replica_System"></span><span id="replication_healthtest_replica_system"></span><span id="REPLICATION_HEALTHTEST_REPLICA_SYSTEM"></span>

<span id="Replication_HealthTest_Replica_System"></span><span id="replication_healthtest_replica_system"></span><span id="REPLICATION_HEALTHTEST_REPLICA_SYSTEM"></span>**Sistema de réplica HealthTest de replicação** (116)


</dt> <dd>

Isso corresponde à propriedade **ReplicationHealth** da classe [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md) .

</dd> <dt>

<span id="Application_Health"></span><span id="application_health"></span><span id="APPLICATION_HEALTH"></span>

<span id="Application_Health"></span><span id="application_health"></span><span id="APPLICATION_HEALTH"></span>**Integridade do aplicativo** (117)


</dt> <dd></dd> <dt>

<span id="ReplicationStateEx"></span><span id="replicationstateex"></span><span id="REPLICATIONSTATEEX"></span>

<span id="ReplicationStateEx"></span><span id="replicationstateex"></span><span id="REPLICATIONSTATEEX"></span>**ReplicationStateEx** (118)


</dt> <dd>

Isso corresponde à propriedade **replicationstate** da classe [**Msvm \_ ReplicationRelationship**](msvm-replicationrelationship.md) . Essa é a matriz para todos os valores de estado de replicação entre as relações primária e estendida. 0 o valor de índice é sempre para a relação primária e, se a replicação estendida estiver habilitada, ela será retornada no índice 1.

</dd> <dt>

<span id="ReplicationHealthEx"></span><span id="replicationhealthex"></span><span id="REPLICATIONHEALTHEX"></span>

<span id="ReplicationHealthEx"></span><span id="replicationhealthex"></span><span id="REPLICATIONHEALTHEX"></span>**ReplicationHealthEx** (119)


</dt> <dd>

Isso corresponde à propriedade **ReplicationHealth** da classe [**Msvm \_ ReplicationRelationship**](msvm-replicationrelationship.md) . Essa é uma matriz para todos os valores de integridade de replicação entre as relações primária e estendida. 0 o valor de índice é sempre para a relação primária e, se a replicação estendida estiver habilitada, ela será retornada no índice 1.

</dd> <dt>

<span id="SwapFilesInUse"></span><span id="swapfilesinuse"></span><span id="SWAPFILESINUSE"></span>

<span id="SwapFilesInUse"></span><span id="swapfilesinuse"></span><span id="SWAPFILESINUSE"></span>**SwapFilesInUse** (120)


</dt> <dd>

Isso corresponde à propriedade **SwapFilesInUse** da classe [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md) .

</dd> <dt>

<span id="IntegrationServicesVersionState"></span><span id="integrationservicesversionstate"></span><span id="INTEGRATIONSERVICESVERSIONSTATE"></span>

<span id="IntegrationServicesVersionState"></span><span id="integrationservicesversionstate"></span><span id="INTEGRATIONSERVICESVERSIONSTATE"></span>**IntegrationServicesVersionState** (121)


</dt> <dd></dd> <dt>

<span id="ReplicationProviderId"></span><span id="replicationproviderid"></span><span id="REPLICATIONPROVIDERID"></span>

<span id="ReplicationProviderId"></span><span id="replicationproviderid"></span><span id="REPLICATIONPROVIDERID"></span>**ReplicationProviderId** (122)


</dt> <dd>

Isso corresponde à propriedade **Name** da classe [**Msvm \_ replicationprovider**](msvm-replicationprovider.md) .

</dd> <dt>

<span id="MemorySpansPhysicalNumaNodes"></span><span id="memoryspansphysicalnumanodes"></span><span id="MEMORYSPANSPHYSICALNUMANODES"></span>

<span id="MemorySpansPhysicalNumaNodes"></span><span id="memoryspansphysicalnumanodes"></span><span id="MEMORYSPANSPHYSICALNUMANODES"></span>**MemorySpansPhysicalNumaNodes** (123)


</dt> <dd></dd> <dt>

<span id="IntegrationServicesVersionState"></span><span id="integrationservicesversionstate"></span><span id="INTEGRATIONSERVICESVERSIONSTATE"></span>

<span id="IntegrationServicesVersionState"></span><span id="integrationservicesversionstate"></span><span id="INTEGRATIONSERVICESVERSIONSTATE"></span>**IntegrationServicesVersionState** (132)


</dt> <dd>

Isso corresponde à propriedade **IntegrationServicesVersionState** da classe [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md) .

</dd> <dt>

<span id="OtherEnabledState"></span><span id="otherenabledstate"></span><span id="OTHERENABLEDSTATE"></span>

<span id="OtherEnabledState"></span><span id="otherenabledstate"></span><span id="OTHERENABLEDSTATE"></span>**OtherEnabledState** (132)


</dt> <dd>

Isso corresponde à propriedade **OtherEnabledState** da classe [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md) .

</dd> <dt>



 (133)


</dt> <dd></dd> </dl> </dd> <dt>

*SummaryInformation* \[ fora\]
</dt> <dd>

Tipo: **[ **Msvm \_ SummaryInformationBase**](msvm-summaryinformationbase.md)\[\]**

Uma matriz de instâncias do [**Msvm \_ SummaryInformationBase**](msvm-summaryinformationbase.md) que contém as informações solicitadas para as máquinas virtuais e/ou os instantâneos especificados na matriz *SettingData* . Essa matriz terá o mesmo número de elementos que a matriz *SettingData* . Cada uma dessas entradas conterá a propriedade **Name** , mesmo que essa propriedade não tenha sido solicitada. Se a máquina virtual ou o instantâneo não puder ser encontrado ou estiver indisponível, a propriedade **Name** da entrada de informações de resumo correspondente estará vazia.

As propriedades não especificadas no parâmetro *RequestedInformation* terão um valor **nulo** .

> [!Note]  
> Tipo de dados atualizado do no Windows 10, versão 1703 de [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md).

 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **UInt32**

Esse método retorna um dos valores a seguir.

<dl> <dt>

**Concluído sem erro** (0)
</dt> <dt>

**Parâmetros de método marcados-trabalho iniciado** (4096)
</dt> <dt>

**Falha** (32768)
</dt> <dt>

**Acesso negado** (32769)
</dt> <dt>

**Sem suporte** (32770)
</dt> <dt>

O **status é desconhecido** (32771)
</dt> <dt>

**Tempo limite** (32772)
</dt> <dt>

**Parâmetro inválido** (32773)
</dt> <dt>

O **sistema está em uso** (32774)
</dt> <dt>

**Estado inválido para esta operação** (32775)
</dt> <dt>

**Tipo de dados incorreto** (32776)
</dt> <dt>

O **sistema não está disponível** (32777)
</dt> <dt>

**Memória insuficiente** (32778)
</dt> </dl>

## <a name="remarks"></a>Comentários

O acesso à classe [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) pode ser restringido pela filtragem do UAC. Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="examples"></a>Exemplos

O exemplo de C# a seguir exibe informações de resumo. Os utilitários referenciados podem ser encontrados em [utilitários comuns para os exemplos de virtualização (v2)](common-utilities-for-the-virtualization-samples-v2.md).

> [!IMPORTANT]
> Para funcionar corretamente, o código a seguir deve ser executado no servidor de host da máquina virtual e deve ser executado com privilégios de administrador.

 


```CSharp
public class GetSummaryInformationClassV2
{
    public static void GetSummaryInformation(string[] vmNames)
    {
        ManagementScope scope = new ManagementScope(@"root\virtualization\v2", null);
        ManagementObject virtualSystemService = Utility.GetServiceObject(scope, "Msvm_VirtualSystemManagementService");
        ManagementBaseObject inParams = virtualSystemService.GetMethodParameters("GetSummaryInformation");

        ManagementObject[] virtualSystemSettings = new ManagementObject[vmNames.Length];

        for (int i = 0; i < vmNames.Length; i++)
        {
            virtualSystemSettings[i] = GetVirtualSystemSetting(vmNames[i], scope);
        }

        UInt32[] requestedInformation = new UInt32[4];
        requestedInformation[0] = 1;    // ElementName
        requestedInformation[2] = 103;  // MemoryUsage
        requestedInformation[3] = 112;  // MemoryAvailable

        inParams["SettingData"] = virtualSystemSettings;
        inParams["RequestedInformation"] = requestedInformation;

        ManagementBaseObject outParams = virtualSystemService.InvokeMethod("GetSummaryInformation", inParams, null);

        if ((UInt32)outParams["ReturnValue"] == ReturnCode.Completed)
        {
            Console.WriteLine("Summary information was retrieved successfully.");

            ManagementBaseObject[] summaryInformationArray = 
                (ManagementBaseObject[])outParams["SummaryInformation"];

            foreach (ManagementBaseObject summaryInformation in summaryInformationArray)
            {
                Console.WriteLine("\nVirtual System Summary Information:");
                if ((null == summaryInformation["Name"]) || 
                    (summaryInformation["Name"].ToString().Length == 0))
                {
                    Console.WriteLine("\tThe VM or snapshot could not be found.");
                }
                else
                {
                    Console.WriteLine("\tName: {0}", summaryInformation["Name"].ToString());
                    foreach (UInt32 requested in requestedInformation)
                    {
                        switch (requested)
                        {
                            case 1:
                                Console.WriteLine("\tElementName: {0}", summaryInformation["ElementName"].ToString());
                                break;

                            case 103:
                                Console.WriteLine("\tMemoryUsage: {0}", summaryInformation["MemoryUsage"].ToString());
                                break;

                            case 112:
                                Console.WriteLine("\tMemoryAvailable: {0}", summaryInformation["MemoryAvailable"].ToString());
                                break;
                        }
                    }
                }
            }
        }
        else
        {
            Console.WriteLine("Failed to retrieve virtual system summary information");
        }

        inParams.Dispose();
        outParams.Dispose();
        virtualSystemService.Dispose();
    }

    public static ManagementObject GetVirtualSystemSetting(string vmName, ManagementScope scope)
    {
        ManagementObject virtualSystem = Utility.GetTargetComputer(vmName, scope);

        ManagementObjectCollection virtualSystemSettings = virtualSystem.GetRelated
         (
             "Msvm_VirtualSystemSettingData",
             "Msvm_SettingsDefineState",
             null,
             null,
             "SettingData",
             "ManagedElement",
             false,
             null
         );

        ManagementObject virtualSystemSetting = null;

        foreach (ManagementObject instance in virtualSystemSettings)
        {
            virtualSystemSetting = instance;
            break;
        }

        return virtualSystemSetting;

    }
}
```



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

[**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)
</dt> <dt>

[**\_VIRTUALSYSTEMSETTINGDATA CIM**](/previous-versions//cc136954(v=vs.85))
</dt> <dt>

[**Msvm \_ SummaryInformation**](msvm-summaryinformation.md)
</dt> </dl>

 

