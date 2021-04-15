---
description: Desabilita os recursos do.
ms.assetid: 2ea2dcfb-84e6-4f83-9afd-c3050b53f37c
title: função pSetupSetGlobalFlags
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pSetupSetGlobalFlags
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 6fcb56f26d5aea233156e0fe3dfab13099d29df7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747266"
---
# <a name="psetupsetglobalflags-function"></a>função pSetupSetGlobalFlags

\[Essa função não está disponível no Windows Vista ou no Windows Server 2008.\]

Desabilita os recursos do.

## <a name="syntax"></a>Sintaxe


```C++
VOID pSetupSetGlobalFlags(
  _In_ DWORD Value
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Valor* \[ do no\]
</dt> <dd>

Os sinalizadores usados para desabilitar a interface do usuário ou o backup automático.



| Valor                                                                                                                                                                                                                                         | Significado                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="PSPGF_NONINTERACTIVE"></span><span id="pspgf_noninteractive"></span><dl> <dt>**PSPGF \_**</dt> <dt>0X004</dt> não interativa </dl> | Defina para desabilitar a interface do usuário.<br/>   |
| <span id="PSPGF_NO_BACKUP"></span><span id="pspgf_no_backup"></span><dl> <dt>**PSPGF \_ NENHUM \_**</dt> <dt>0x002</dt> de backup </dl>               | Defina para desabilitar o backup automático.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Setupapi.dll</dt> </dl> |



 

 
