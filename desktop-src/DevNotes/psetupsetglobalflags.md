---
description: Desabilita os recursos.
ms.assetid: 2ea2dcfb-84e6-4f83-9afd-c3050b53f37c
title: Função pSetupSetGlobalFlags
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
ms.openlocfilehash: d28bb948d351b2b9ad54c7e2bdc8c8cbfde83f6f4ade42a0f90440eca28bfc05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955695"
---
# <a name="psetupsetglobalflags-function"></a>Função pSetupSetGlobalFlags

\[Essa função não está disponível no Windows Vista ou Windows Server 2008.\]

Desabilita os recursos.

## <a name="syntax"></a>Sintaxe


```C++
VOID pSetupSetGlobalFlags(
  _In_ DWORD Value
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Valor* \[ Em\]
</dt> <dd>

Os sinalizadores usados para desabilitar a interface do usuário ou o backup automático.



| Valor                                                                                                                                                                                                                                         | Significado                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="PSPGF_NONINTERACTIVE"></span><span id="pspgf_noninteractive"></span><dl> <dt>**PSPGF \_ Não 0X004**</dt> <dt></dt> </dl> | De definido para desabilitar a interface do usuário.<br/>   |
| <span id="PSPGF_NO_BACKUP"></span><span id="pspgf_no_backup"></span><dl> <dt>**PSPGF \_ NENHUMA \_ 0X002**</dt> <dt></dt> </dl>               | De definido para desabilitar o backup automático.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

Essa função não tem nenhuma biblioteca de importação ou arquivo de header associado; você deve chamá-lo usando [**as funções LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**e GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Setupapi.dll</dt> </dl> |



 

 
