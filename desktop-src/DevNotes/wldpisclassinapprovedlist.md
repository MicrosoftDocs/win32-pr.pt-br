---
description: Chama a biblioteca para validar se um CLSID específico é seguro para ser chamado.
ms.assetid: 94C8731B-88FD-4240-BF5D-2CD67C41B063
title: Função WldpIsClassInApprovedList (Wldp. h)
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
ms.openlocfilehash: 01762c60a3f1aef1574cc218ace9988669175efe
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104088890"
---
# <a name="wldpisclassinapprovedlist-function"></a>Função WldpIsClassInApprovedList

Chama a biblioteca para validar se um **CLSID** específico é seguro para ser chamado. A função não tem biblioteca de importação associada. Você deve usar as funções LoadLibrary e GetProcAddress para vincular dinamicamente a wldp.dll.

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

*classID* 
</dt> <dd>

A ID da classe COM para verificar a aprovação.

</dd> <dt>

*hostInformation* \[ no\]
</dt> <dd>

Uma estrutura de [**\_ \_ informações de host WLDP**](wldp-host-information.md) que identifica o host a ser avaliado.

</dd> <dt>

*IsApproved* \[ fora\]
</dt> <dd>

Após a conclusão bem-sucedida, conterá **true** se a ID da classe for aprovada; caso contrário, **false**.

</dd> <dt>

*optionalFlags* 
</dt> <dd>

Esse parâmetro é reservado e deve ser definido como zero.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método retornará **S \_ OK** , se for bem-sucedido ou um código de falha.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10\]<br/>                                         |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2016\]<br/>                                |
| parâmetro<br/>                   | <dl> <dt>Wldp. h</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Wldp.dll</dt> </dl> |



 

 




