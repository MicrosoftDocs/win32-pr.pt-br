---
description: O método GetMaximumCursors recupera o número máximo de cursores que um dispositivo de Tablet dá suporte.
ms.assetid: 5a43d792-e64c-4506-9792-31efe0885959
title: 'Método ITablet3:: GetMaximumCursors'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet3.GetMaximumCursors
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 7c40184d35ac1d42cb5f5e845396b40efc2d928e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105788783"
---
# <a name="itablet3getmaximumcursors-method"></a>Método ITablet3:: GetMaximumCursors

O método **GetMaximumCursors** recupera o número máximo de cursores que um dispositivo de Tablet dá suporte.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetMaximumCursors(
   ULONG *pMaximumCursors
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pMaximumCursors* 
</dt> <dd>

O número máximo de entradas que o dispositivo dá suporte.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna S \_ OK em caso de êxito; caso contrário, retorna um código de erro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                             |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]<br/>                                |
| Biblioteca<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ITablet3**](itablet3.md)
</dt> </dl>

 

 




