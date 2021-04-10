---
description: Inicia uma operação de desligamento do sistema operacional na máquina virtual filho associada. Se zero (0) for retornado, o desligamento foi iniciado com êxito. Qualquer outro código de retorno indica uma condição de erro.
ms.assetid: 946BBC62-5479-4AE0-8870-D0A07827B902
title: Método InitiateShutdown da classe Msvm_ShutdownComponent (winreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ShutdownComponent.InitiateShutdown
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 266ab64bb058325ac165a2e12c2a91d442a90269
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170251"
---
# <a name="initiateshutdown-method-of-the-msvm_shutdowncomponent-class"></a>Método InitiateShutdown da \_ classe ShutdownComponent Msvm

Inicia uma operação de desligamento do sistema operacional na máquina virtual filho associada. Se zero (0) for retornado, o desligamento foi iniciado com êxito. Qualquer outro código de retorno indica uma condição de erro.

## <a name="syntax"></a>Sintaxe


```mof
uint32 InitiateShutdown(
  [in] boolean Force,
  [in] string  Reason
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Forçar* \[ no\]
</dt> <dd>

Tipo: **booliano**

Um sinalizador que, se **verdadeiro**, força os aplicativos a serem fechados, apesar de terem dados não salvos.

</dd> <dt>

*Motivo* \[ no\]
</dt> <dd>

Tipo: **cadeia de caracteres**

O motivo para a operação de desligamento. Esta é uma cadeia de caracteres definida pelo usuário.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **UInt32**

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
</dt> <dt>

**O sistema não está pronto** (32780)
</dt> <dt>

**A máquina está bloqueada e não pode ser desligada sem a opção Force** (32781)
</dt> <dt>

**Um desligamento do sistema está em andamento** (32782)
</dt> </dl>

## <a name="remarks"></a>Comentários

O acesso à classe [**Msvm \_ ShutdownComponent**](msvm-shutdowncomponent.md) pode ser restringido pela filtragem do UAC. Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                                              |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                                    |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| parâmetro<br/>                   | <dl> <dt>Winreg. h</dt> </dl>                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Msvm \_ ShutdownComponent**](msvm-shutdowncomponent.md)
</dt> </dl>

 

