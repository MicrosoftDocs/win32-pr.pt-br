---
description: Recupera um valor que descreve o status de imposição de política do Device Guard para código dinâmico do .NET.
ms.assetid: 11E6C631-0FF8-4DB2-931A-1012B3CA4357
title: Função WldpIsDynamicCodePolicyEnabled (Wldp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WldpIsDynamicCodePolicyEnabled
api_type:
- DllExport
api_location:
- wldp.dll
ms.openlocfilehash: 4df0555f89e9c575a7d97b69a5252c17936eb3d2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104088889"
---
# <a name="wldpisdynamiccodepolicyenabled-function"></a>Função WldpIsDynamicCodePolicyEnabled

Recupera um valor que descreve o status de imposição de política do Device Guard para código dinâmico do .NET.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT WINAPI WldpIsDynamicCodePolicyEnabled(
  _Out_ PBOOL  isEnabled
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*IsEnabled* \[ fora\]
</dt> <dd>

Em caso de sucesso, retornará **true** se a política de proteção do dispositivo impor a política de código dinâmico do .net; caso contrário, retornará **false**.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método retornará **S \_ OK** , se for bem-sucedido ou um código de falha.

## <a name="remarks"></a>Comentários

O código dinâmico refere-se à CRL do .NET código gerado dinamicamente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10, versão 1803\]<br/>                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2016\]<br/>                                |
| parâmetro<br/>                   | <dl> <dt>Wldp. h</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Wldp.dll</dt> </dl> |



 

 




