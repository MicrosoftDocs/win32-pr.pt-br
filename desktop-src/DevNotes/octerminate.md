---
description: Fecha o gerenciador de OC.
ms.assetid: feba9954-03b2-4b57-b7ba-933e171751ff
title: Função OcTerminate
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OcTerminate
api_type:
- DllExport
api_location:
- OcManage.dll
ms.openlocfilehash: 399bdb936befb4f7ff45f9f5a3b132245b984bf2a5201ce054ee0fbeb50f5598
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119833346"
---
# <a name="octerminate-function"></a>Função OcTerminate

Fecha o gerenciador de OC.

## <a name="syntax"></a>Sintaxe


```C++
VOID OcTerminate(
  _Inout_ PVOID *OcManagerContext
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*OcManagerContext* \[ in, out\]
</dt> <dd>

Na entrada, contém o ponteiro de contexto do gerenciador de OC retornado por [**OcInitialize**](ocinitialize.md). Na saída, recebe **NULL.**

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

Essa função não tem nenhuma biblioteca de importação ou arquivo de header associado; você deve chamá-lo usando [**as funções LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**e GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>OcManage.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**OcInitialize**](ocinitialize.md)
</dt> </dl>

 

 
