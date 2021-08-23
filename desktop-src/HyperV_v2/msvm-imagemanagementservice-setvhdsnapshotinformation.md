---
description: Edita uma entrada de instantâneo VHD em um arquivo de conjunto VHD. Se a ID de instantâneo em questão já existir, a entrada de instantâneo existente será substituída pela nova entrada. Caso contrário, a nova entrada será adicionada ao arquivo do conjunto VHD.
ms.assetid: dd14960d-3fb8-4d47-986f-fbbbb08eb37d
title: Método SetVHDSnapshotInformation da classe Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.SetVHDSnapshotInformation
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: af4adddb2b59da303f558cfffac61003e70e5767c77e381b13ba6089228d6643
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119522446"
---
# <a name="setvhdsnapshotinformation-method-of-the-msvm_imagemanagementservice-class"></a>Método SetVHDSnapshotInformation da \_ classe imagens Msvm

Edita uma entrada de instantâneo VHD em um arquivo de conjunto VHD. Se a ID de instantâneo em questão já existir, a entrada de instantâneo existente será substituída pela nova entrada. Caso contrário, a nova entrada será adicionada ao arquivo do conjunto VHD.

## <a name="syntax"></a>Sintaxe


```mof
uint32 SetVHDSnapshotInformation(
  [in]  string              Information,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Informações* \[ do no\]
</dt> <dd>

Informações de instantâneo do VHD a serem alteradas ou adicionadas no arquivo do conjunto VHD. A cadeia de caracteres é uma instância incorporada de [**Msvm \_ VHDSnapshotInformation**](msvm-vhdsnapshotinformation.md).

</dd> <dt>

*Trabalho* \[ do fora\]
</dt> <dd>

Uma referência ao trabalho (pode ser NULL se a tarefa for concluída).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método retorna um dos seguintes valores:

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

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10 \[ somente aplicativos da área de trabalho\]<br/>                                                             |
| Servidor mínimo com suporte<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Msvm \_ imagens**](msvm-imagemanagementservice.md)
</dt> </dl>

 

 




