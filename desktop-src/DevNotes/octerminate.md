---
description: Fecha o Gerenciador de OC.
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
ms.openlocfilehash: 2e747c19db5e5a79e2827dc3bcfb88b97fae2ba6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752767"
---
# <a name="octerminate-function"></a>Função OcTerminate

Fecha o Gerenciador de OC.

## <a name="syntax"></a>Sintaxe


```C++
VOID OcTerminate(
  _Inout_ PVOID *OcManagerContext
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*OcManagerContext* \[ entrada, saída\]
</dt> <dd>

Na entrada, contém o ponteiro de contexto do Gerenciador OC retornado por [**OcInitialize**](ocinitialize.md). Na saída, recebe **NULL**.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>OcManage.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**OcInitialize**](ocinitialize.md)
</dt> </dl>

 

 
