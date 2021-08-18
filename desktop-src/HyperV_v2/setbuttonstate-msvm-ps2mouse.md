---
description: Método SetButtonState da classe Msvm_Ps2Mouse - Define o estado atual do botão de dispositivo especificado.
ms.assetid: 312A2B8B-D518-4797-9B50-F12493598CD6
title: Método SetButtonState da classe Msvm_Ps2Mouse classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Ps2Mouse.SetButtonState
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: b8ccc67590861a07b8a1d0181c43530a19d27e3f9426f3c6c363be44c0996f78
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119822886"
---
# <a name="setbuttonstate-method-of-the-msvm_ps2mouse-class"></a>Método SetButtonState da classe Msvm \_ Ps2Mouse

Define o estado atual do botão de dispositivo especificado.

## <a name="syntax"></a>Sintaxe


```mof
uint32 SetButtonState(
  [in] uint32  buttonIndex,
  [in] boolean buttonState
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*buttonIndex* \[ Em\]
</dt> <dd>

Tipo: **uint32**

O índice baseado em 1 do botão a ser modificado.

</dd> <dt>

*buttonState* \[ Em\]
</dt> <dd>

Tipo: **booliana**

O novo estado para baixo do botão. Um **valor True** significa que o botão está ino mouse.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **uint32**

Um valor de retorno de zero indica êxito. Um valor não zero indica uma falha ao modificar o estado do botão.

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
</dt> </dl>

## <a name="remarks"></a>Comentários

O acesso à [**classe Msvm \_ Ps2Mouse**](msvm-ps2mouse.md) pode ser restrito pela Filtragem de UAC. Para obter mais informações, consulte [Controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

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

[**Msvm \_ Ps2Mouse**](msvm-ps2mouse.md)
</dt> </dl>

 

