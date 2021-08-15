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
ms.openlocfilehash: 47ae90c966ac259791d0ffb9c60d736430ede610db3932dd08ff60cc9e3b7b21
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119390186"
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

## <a name="return-value"></a>Valor retornado

Esse método retornará S \_ OK, se for bem-sucedido ou um código de falha.

## <a name="remarks"></a>Comentários

Quando chamado com WLDP \_ host \_ Information. SZSOURCE = NULL, a política genérica para o host é retornada.

Quando chamado com WLDP \_ host \_ Information. DWHOSTID = WLDP \_ host \_ ID \_ global, WLDP \_ host \_ Information. szSource deve ser NULL e a função retornará a política global do sistema.

Os \_ sinalizadores SKIPSIGNATUREVALIDATION WLDP dwFlag \_ podem ser usados para ignorar a validação de SaferIdentifyLevel (), o que irá ignorar se um script está assinado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10 \[ somente aplicativos da área de trabalho\]<br/>                                         |
| Servidor mínimo com suporte<br/> | Windows Server 2016 \[ somente aplicativos da área de trabalho\]<br/>                                |
| parâmetro<br/>                   | <dl> <dt>Wldp. h</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Wldp.dll</dt> </dl> |



 

 




