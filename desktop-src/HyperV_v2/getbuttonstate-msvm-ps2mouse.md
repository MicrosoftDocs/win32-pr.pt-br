---
description: Método GetButtonState da classe Msvm_Ps2Mouse - recupera o estado atual do botão de dispositivo especificado.
ms.assetid: 7772A3AC-1677-44A7-9E5E-D31E90988705
title: Método GetButtonState da classe Msvm_Ps2Mouse classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Ps2Mouse.GetButtonState
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: dbbd77b87c0df1d12b20958497d145b77ad62ed5b9691b443be2596fd58e4df6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119682516"
---
# <a name="getbuttonstate-method-of-the-msvm_ps2mouse-class"></a>Método GetButtonState da classe Msvm \_ Ps2Mouse

Recupera o estado atual do botão de dispositivo especificado.

## <a name="syntax"></a>Sintaxe


```mof
uint32 GetButtonState(
  [in]  uint32  buttonIndex,
  [out] boolean buttonState
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*buttonIndex* \[ Em\]
</dt> <dd>

Tipo: **uint32**

O índice baseado em 1 do botão a ser consultado.

</dd> <dt>

*buttonState* \[ out\]
</dt> <dd>

Tipo: **booliana**

O estado para baixo atual do botão. Um **valor True** significa que o botão está ino mouse.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **uint32**

Um valor de retorno de zero indica êxito. Um valor não zero indica uma falha de consulta.

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

 

