---
description: Inicia uma operação de desligamento do sistema operacional na máquina virtual filho associada. Se zero (0) for retornado, o desligamento foi iniciado com êxito. Qualquer outro código de retorno indica uma condição de erro.
ms.assetid: 946BBC62-5479-4AE0-8870-D0A07827B902
title: Método InitiateShutdown da classe Msvm_ShutdownComponent (Winreg.h)
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
ms.openlocfilehash: f128eb2babfed0c70aca063832e579ad254ca1b02d6beaefb451c64598faa8d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118950395"
---
# <a name="initiateshutdown-method-of-the-msvm_shutdowncomponent-class"></a>Método InitiateShutdown da classe Msvm \_ ShutdownComponent

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

*Forçar* \[ Em\]
</dt> <dd>

Tipo: **booliana**

Um sinalizador que, se **True,** força os aplicativos a serem fechados, apesar de ter dados não savados.

</dd> <dt>

*Motivo* \[ Em\]
</dt> <dd>

Tipo: cadeia **de caracteres**

O motivo da operação de desligamento. Essa é uma cadeia de caracteres definida pelo usuário.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **uint32**

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

**O sistema está em usado** (32774)
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
</dt> <dt>

**O sistema não está pronto** (32780)
</dt> <dt>

**O computador está bloqueado e não pode ser desligado sem a opção force** (32781)
</dt> <dt>

**Um desligamento do sistema está em andamento** (32782)
</dt> </dl>

## <a name="remarks"></a>Comentários

O acesso à [**classe \_ ShutdownComponent do Msvm**](msvm-shutdowncomponent.md) pode ser restrito pela Filtragem de UAC. Para obter mais informações, consulte [Controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8 somente aplicativos da área de trabalho\]<br/>                                                              |
| Servidor mínimo com suporte<br/> | \[Windows Server 2012 somente aplicativos da área de trabalho\]<br/>                                                    |
| Namespace<br/>                | Virtualização \\ raiz \\ V2<br/>                                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Winreg.h</dt> </dl>                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Desligamento do \_ MsvmComponent**](msvm-shutdowncomponent.md)
</dt> </dl>

 

