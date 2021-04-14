---
description: Define um código dinâmico de CRL do .NET em disco confiável para .NET.
ms.assetid: 4C8C3EF5-5C3C-4710-8223-D7B5BA86EF47
title: Função WldpSetDynamicCodeTrust (Wldp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WldpSetDynamicCodeTrust
api_type:
- DllExport
api_location:
- wldp.dll
ms.openlocfilehash: a266563b40d255fe9e904f02e4e4593d4c4d3f33
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370402"
---
# <a name="wldpsetdynamiccodetrust-function"></a>Função WldpSetDynamicCodeTrust

Define um código dinâmico de CRL do .NET em disco confiável para .NET.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT WINAPI WldpSetDynamicCodeTrust(
   HANDLE FileHandle
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*FileHandle* 
</dt> <dd>

Identificador para um arquivo de código dinâmico em disco.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método retornará **S \_ OK** , se for bem-sucedido ou um código de falha.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10, versão 1803\]<br/>                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2016\]<br/>                                |
| parâmetro<br/>                   | <dl> <dt>Wldp. h</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Wldp.dll</dt> </dl> |



 

 




