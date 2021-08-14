---
description: Retorna uma cadeia de caracteres de mensagem de erro formatada para a matriz especificada de instâncias de erro Msvm \_ inseridas.
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
ms.openlocfilehash: 31b7f2ba03c21c08af3b9249c0ee3099291fdd190d22516ed503c012dae63f4b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119253946"
---
# <a name="formaterror-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Método FormatError da classe Msvm \_ VirtualSystemManagementService

Retorna uma cadeia de caracteres de mensagem de erro formatada para a matriz especificada de [**instâncias de erro Msvm \_**](msvm-error.md) inseridas.

## <a name="syntax"></a>Sintaxe


```mof
uint32 FormatError(
  [in]  string Errors[],
  [out] string ErrorMessage
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Erros* \[ Em\]
</dt> <dd>

Tipo: cadeia **de caracteres \[ \]**

Uma matriz de cadeias de caracteres que contém [**instâncias de Erro Msvm \_**](msvm-error.md) usadas para gerar a mensagem de erro de saída.

</dd> <dt>

*ErrorMessage* \[ out\]
</dt> <dd>

Tipo: cadeia **de caracteres**

Na saída, uma cadeia de caracteres que contém as mensagens de erro concatenadas representadas pelas instâncias de [**Erro Msvm \_**](msvm-error.md) passadas no *parâmetro Errors.* Cada cadeia de caracteres de erro é separada por um par de caracteres de nova linha (' \\ n').

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **uint32**

Esse método retorna um dos valores a seguir.

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
</dt> </dl>

## <a name="remarks"></a>Comentários

O acesso à [**classe \_ VirtualSystemManagementService do Msvm**](msvm-virtualsystemmanagementservice.md) pode ser restrito pela Filtragem de UAC. Para obter mais informações, consulte [Controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

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

[**FormatError (V1)**](/previous-versions/windows/desktop/virtual/formaterror-msvm-virtualsystemmanagementservice)
</dt> <dt>

[**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

