---
description: Chama a biblioteca para validar se um CLSID específico é seguro para ser chamado.
ms.assetid: 94C8731B-88FD-4240-BF5D-2CD67C41B063
title: Função WldpIsClassInApprovedList (Wldp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WldpIsClassInApprovedList
api_type:
- DllExport
api_location:
- wldp.dll
ms.openlocfilehash: ef4f6a719a1fe5146badbe59239dc16f9031f553ee8bba189c838dddcb641d8b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119642036"
---
# <a name="wldpisclassinapprovedlist-function"></a>Função WldpIsClassInApprovedList

Chama a biblioteca para validar se um **CLSID específico** é seguro para ser chamado. A função não tem nenhuma biblioteca de importação associada. Você deve usar as funções LoadLibrary e GetProcAddress para vincular dinamicamente a wldp.dll.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT WINAPI WldpIsClassInApprovedList(
        REFCLSID               classID,
  _In_  PWLDP_HOST_INFORMATION hostInformation,
  _Out_ PBOOL                  isApproved,
        DWORD                  optionalFlags
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Classid* 
</dt> <dd>

A ID da classe COM a ser verificada quanto à aprovação.

</dd> <dt>

*hostInformation* \[ Em\]
</dt> <dd>

Uma [**estrutura WLDP \_ HOST \_ INFORMATION**](wldp-host-information.md) que identifica o host a ser avaliado.

</dd> <dt>

*isApproved* \[ out\]
</dt> <dd>

Após a conclusão bem-sucedida, **conterá TRUE** se a ID da classe for aprovada; caso contrário, **FALSE.**

</dd> <dt>

*optionalFlags* 
</dt> <dd>

Esse parâmetro é reservado e deve ser definido como zero.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método retornará **S \_ OK se** for bem-sucedido ou um código de falha, caso contrário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 10 somente aplicativos da área de trabalho\]<br/>                                         |
| Servidor mínimo com suporte<br/> | \[Windows Server 2016 somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Wldp.h</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Wldp.dll</dt> </dl> |



 

 




