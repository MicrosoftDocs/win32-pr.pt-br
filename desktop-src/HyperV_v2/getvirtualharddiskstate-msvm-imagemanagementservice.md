---
description: Recupera informações de estado para um arquivo de disco rígido virtual.
ms.assetid: 398b098b-dc1a-45e0-abcb-37b4b0a32290
title: Método GetVirtualHardDiskState da classe Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.GetVirtualHardDiskState
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 73b4c696a04ef72075c520694e0983056c74e80e9257d220a9714351664aa841
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119532336"
---
# <a name="getvirtualharddiskstate-method-of-the-msvm_imagemanagementservice-class"></a>Método GetVirtualHardDiskState da \_ classe imagens Msvm

Recupera informações de estado para um arquivo de disco rígido virtual.

## <a name="syntax"></a>Sintaxe


```mof
uint32 GetVirtualHardDiskState(
  [in]  string              Path,
  [out] string              State,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Caminho* \[ do no\]
</dt> <dd>

O caminho totalmente qualificado do arquivo de imagem de disco.

</dd> <dt>

*Estado* \[ fora\]
</dt> <dd>

Se for bem-sucedido, o receberá uma instância inserida da classe [**Msvm \_ VirtualHardDiskState**](msvm-virtualharddiskstate.md) que contém as informações de estado do disco rígido virtual.

</dd> <dt>

*Trabalho* \[ do fora\]
</dt> <dd>

Se a operação for executada de forma assíncrona, esse método retornará 4096, e esse parâmetro conterá uma referência a um objeto derivado de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

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
</dt> <dt>

**Arquivo não encontrado** (32779)
</dt> </dl>

## <a name="remarks"></a>Comentários

O acesso à classe [**Msvm \_ imagens**](msvm-imagemanagementservice.md) pode ser restringido pela filtragem do UAC. Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="examples"></a>Exemplos

O exemplo de C# a seguir mostra como chamar o método **GetVirtualHardDiskState** . Os utilitários referenciados podem ser encontrados em [utilitários comuns para os exemplos de virtualização (v2)](common-utilities-for-the-virtualization-samples-v2.md).


```CSharp
public static void GetVirtualHardDiskState(string vhdPath)
{
    ManagementScope scope = new ManagementScope(@"root\virtualization\V2", null);
    ManagementObject imageService = Utility.GetServiceObject(scope, "Msvm_ImageManagementService");
    ManagementBaseObject inParams = imageService.GetMethodParameters("GetVirtualHardDiskState");

    inParams["Path"] = vhdPath;
    
    ManagementBaseObject outParams = imageService.InvokeMethod("GetVirtualHardDiskState", inParams, null);
    if ((UInt32)outParams["ReturnValue"] == ReturnCode.Started)
    {
        if (Utility.JobCompleted(outParams, scope))
        {
            Console.WriteLine("GetVirtualHardDiskState was successful.");
        }
        else
        {
            Console.WriteLine("GetVirtualHardDiskState was not successful.");
        }
    }
    else if ((UInt32)outParams["ReturnValue"] == ReturnCode.Completed)
    {
        string diskStateString = outParams["State"].ToString();
        Utility.PrintEmbeddedInstance(diskStateString);
    }

    outParams.Dispose();
    inParams.Dispose();
    imageService.Dispose();
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8 \[ somente aplicativos da área de trabalho\]<br/>                                                              |
| Servidor mínimo com suporte<br/> | Windows Server 2012 \[ somente aplicativos da área de trabalho\]<br/>                                                    |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Msvm \_ imagens**](msvm-imagemanagementservice.md)
</dt> </dl>

 

