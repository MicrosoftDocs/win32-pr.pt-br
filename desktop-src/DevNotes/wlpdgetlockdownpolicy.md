---
description: Chama a biblioteca para obter o estado de segurança relativo ao host, e script ou msi a ser usado.
ms.assetid: 4CCDA3B7-7661-47F6-A015-720BDEAEDBB1
title: Função WldpGetLockdownPolicy (Wldp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WldpGetLockdownPolicy
api_type:
- DllExport
api_location:
- wldp.dll
ms.openlocfilehash: a8f5e4da11e8ce7443d9a9bab323742cfc1b3a9d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104500903"
---
# <a name="wldpgetlockdownpolicy-function"></a>Função WldpGetLockdownPolicy

Chama a biblioteca para obter o estado de segurança relativo ao host, e script ou msi a ser usado. A função não tem biblioteca de importação associada. Você deve usar as funções LoadLibrary e GetProcAddress para vincular dinamicamente a wldp.dll.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT WINAPI WldpGetLockdownPolicy(
  _In_opt_ PWLDP_HOST_INFORMATION hostInformation,
  _Out_    PDWORD                 lockdownState,
  _In_     DWORD                  lockdownFlags
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hostInformation* \[ em, opcional\]
</dt> <dd>

Uma estrutura de [**\_ \_ informações de host WLDP**](wldp-host-information.md) que identifica o host e o arquivo de origem a serem avaliados.

</dd> <dt>

*lockdownstate* \[ fora\]
</dt> <dd>

Fornece o valor seguro da política resultante. Que! WLDP_LOCKDOWN_IS_OFF, então UMCI está habilitado. Você também pode verificar WLDP_LOCKDOWN_IS_AUDIT e WLDP_LOCKDOWN_IS_ENFORCE para determinar se uma política está no modo auditar ou impor.
</dd> <dt>

*lockdownFlags* \[ no\]
</dt> <dd>

Os seguintes valores de sinalizador são definidos WLDP \_ flags \_ SKIPSIGNATUREVALIDATION 0x00000100 – quando definido, ignore a validação de SaferIdentifyLevel, o que irá ignorar se um script está assinado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método retornará S \_ OK, se for bem-sucedido ou um código de falha.

## <a name="remarks"></a>Comentários

Quando chamado com WLDP \_ host \_ Information. SZSOURCE = NULL, a política genérica para o host é retornada.

Quando chamado com WLDP \_ host \_ Information. DWHOSTID = WLDP \_ host \_ ID \_ global, WLDP \_ host \_ Information. szSource deve ser NULL e a função retornará a política global do sistema.

Os \_ sinalizadores SKIPSIGNATUREVALIDATION WLDP dwFlag \_ podem ser usados para ignorar a validação de SaferIdentifyLevel (), o que irá ignorar se um script está assinado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10\]<br/>                                         |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2016\]<br/>                                |
| parâmetro<br/>                   | <dl> <dt>Wldp. h</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Wldp.dll</dt> </dl> |



 

 




