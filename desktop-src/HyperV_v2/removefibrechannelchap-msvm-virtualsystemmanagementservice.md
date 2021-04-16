---
description: Remove os parâmetros DH-CHAP (Diffie Hellman-Challenge Handshake Authentication Protocol) de uma porta de Fibre Channel sintética em uma máquina virtual.
ms.assetid: f15673e2-287d-4e87-bee4-6c0f5f9178c8
title: Método RemoveFibreChannelChap da classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.RemoveFibreChannelChap
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 06e944c3c592b0b61ace8a72b5d42a801ab0f5df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105757404"
---
# <a name="removefibrechannelchap-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Método RemoveFibreChannelChap da \_ classe VirtualSystemManagementService Msvm

Remove os parâmetros DH-CHAP (Diffie Hellman-Challenge Handshake Authentication Protocol) de uma porta de Fibre Channel sintética em uma máquina virtual. Esse método falhará se a máquina virtual estiver em execução.

## <a name="syntax"></a>Sintaxe


```mof
uint32 RemoveFibreChannelChap(
  [in] string FcPortSettings[]
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*FcPortSettings* \[ no\]
</dt> <dd>

Uma matriz de cadeias de caracteres que contém uma instância inserida da classe [**Msvm \_ SyntheticFcPortSettingData**](msvm-syntheticfcportsettingdata.md) que define as portas de Fibre Channel sintéticas das quais os parâmetros DH-CHAP são removidos. A propriedade **InstanceId** de cada uma dessas instâncias identifica os elementos a serem modificados.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método retorna um dos valores a seguir.

<dl> <dt>

**Concluído sem erro** (0)
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
</dt> </dl>

 

 




