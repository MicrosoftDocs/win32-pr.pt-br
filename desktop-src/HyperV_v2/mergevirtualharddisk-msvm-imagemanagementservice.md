---
description: Mescla um disco rígido virtual filho em uma cadeia diferencial com um ou mais discos rígidos virtuais pai na cadeia.
ms.assetid: 10633176-F0C3-4CA0-8E7B-2B11FF93B0EA
title: Método MergeVirtualHardDisk da classe Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.MergeVirtualHardDisk
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: fa9867222cf27e6ca23a4d96a04a6b94b558e7c043f182fdf8d8331ad73010c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118644868"
---
# <a name="mergevirtualharddisk-method-of-the-msvm_imagemanagementservice-class"></a>Método MergeVirtualHardDisk da classe Msvm \_ ImageManagementService

Mescla um disco rígido virtual filho em uma cadeia diferencial com um ou mais discos rígidos virtuais pai na cadeia. Consulte Comentários sobre restrições de uso para esse método.

Se o usuário que executa essa função não tiver permissão para atualizar as máquinas virtuais, essa função falhará.

## <a name="syntax"></a>Sintaxe


```mof
uint32 MergeVirtualHardDisk(
  [in]  string              SourcePath,
  [in]  string              DestinationPath,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*SourcePath* \[ Em\]
</dt> <dd>

Tipo: cadeia **de caracteres**

Um caminho totalmente qualificado que especifica o local do arquivo de disco rígido virtual a ser mesclado.

</dd> <dt>

*DestinationPath* \[ Em\]
</dt> <dd>

Tipo: cadeia **de caracteres**

Um caminho totalmente qualificado que especifica o local do arquivo de disco rígido virtual pai no qual os dados devem ser mesclados. Esse pode ser o disco rígido virtual pai imediato do arquivo mesclado ou a imagem de disco pai alguns níveis acima da cadeia diferencial.

</dd> <dt>

*Trabalho* \[ out\]
</dt> <dd>

Tipo: **[ **CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))**

Se a operação for executada de forma assíncrona, esse método retornará 4096 e esse parâmetro conterá uma referência a um objeto derivado de [**CIM \_ ConcreteJob.**](/previous-versions//cc136808(v=vs.85))

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **uint32**

Esse método pode retornar um dos valores a seguir.

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

## <a name="remarks"></a>Comentários

O disco rígido virtual filho deve estar offline.

Somente os seguintes tipos de discos rígidos virtuais podem ser usados com este método:

-   VHD diferencial
-   Diferenciando VHDX

O acesso à [**classe Msvm \_ ImageManagementService**](msvm-imagemanagementservice.md) pode ser restrito pela Filtragem de UAC. Para obter mais informações, consulte [Controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="examples"></a>Exemplos

O exemplo de C# a seguir expande um arquivo de disco rígido virtual. Os utilitários referenciados podem ser encontrados em [Utilitários comuns para as amostras de virtualização (V2)](common-utilities-for-the-virtualization-samples-v2.md).


```CSharp
// Merges a VHD into a parent VHD.
// ChildPath: The path to the VHD to merge.</param>
// ParentPath: The path to the parent into which to merge.</param>
public static void MergeVirtualHardDisk(string ChildPath, string ParentPath)
{
    ManagementScope scope = new ManagementScope(@"root\virtualization\v2", null);
    ManagementObject imageService = Utility.GetServiceObject(scope, "Msvm_ImageManagementService");

    ManagementBaseObject inParams = imageService.GetMethodParameters("MergeVirtualHardDisk");

    inParams["SourcePath"] = ChildPath;
    inParams["DestinationPath"] = ParentPath;

    ManagementBaseObject outParams = imageService.InvokeMethod("MergeVirtualHardDisk", inParams, null);

    if ((UInt32)outParams["ReturnValue"] == ReturnCode.Started)
    {
        if (Utility.JobCompleted(outParams, scope))
        {
            Console.WriteLine("MergeVirtualHardDisk succeeded.");
        }
        else
        {
            Console.WriteLine("MergeVirtualHardDisk failed.");
        }
    }

    outParams.Dispose();
    inParams.Dispose();
    imageService.Dispose();
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

[**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))
</dt> <dt>

[**Msvm \_ ImageManagementService**](msvm-imagemanagementservice.md)
</dt> </dl>

 

