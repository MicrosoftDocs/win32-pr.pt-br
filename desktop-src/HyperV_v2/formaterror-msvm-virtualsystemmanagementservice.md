---
description: Retorna uma cadeia de caracteres de mensagem de erro formatada para a matriz especificada de instâncias de erro Msvm inseridas \_ .
ms.assetid: 477EF4AE-00A8-4F2D-A335-E41A2EF620BB
title: Método FormatError da classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.FormatError
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: e768a6ea968d428d7809c7c322a80f3ad233aa2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105755110"
---
# <a name="formaterror-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Método FormatError da \_ classe VirtualSystemManagementService Msvm

Retorna uma cadeia de caracteres de mensagem de erro formatada para a matriz especificada de instâncias de [**\_ erro Msvm**](msvm-error.md) inseridas.

## <a name="syntax"></a>Sintaxe


```mof
uint32 FormatError(
  [in]  string Errors[],
  [out] string ErrorMessage
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Erros* \[ do no\]
</dt> <dd>

Tipo: **cadeia \[ \] de caracteres**

Uma matriz de cadeias de caracteres que contém instâncias de [**\_ erro Msvm**](msvm-error.md) usadas para gerar a mensagem de erro de saída.

</dd> <dt>

*ErrorMessage* \[ fora\]
</dt> <dd>

Tipo: **cadeia de caracteres**

Na saída, uma cadeia de caracteres que contém as mensagens de erro concatenadas representadas pelas instâncias de [**\_ erro Msvm**](msvm-error.md) passadas no parâmetro *erros* . Cada cadeia de caracteres de erro é separada por um par de caracteres de nova linha (' \\ n').

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

[**FormatError (v1)**](/previous-versions/windows/desktop/virtual/formaterror-msvm-virtualsystemmanagementservice)
</dt> <dt>

[**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

