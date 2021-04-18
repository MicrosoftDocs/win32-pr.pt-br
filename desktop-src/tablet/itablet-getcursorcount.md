---
description: Retorna o número de objetos de cursor associados ao Tablet.
ms.assetid: 7aa5802c-1255-41a4-b1fa-23e5f56c0b80
title: 'Método ITablet:: GetCursorCount'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet.GetCursorCount
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 2309384e4aa36383277ba72cc407cabef7ab4b27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105788784"
---
# <a name="itabletgetcursorcount-method"></a>Método ITablet:: GetCursorCount

Retorna o número de objetos de cursor associados ao Tablet.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetCursorCount(
  [out] ULONG *pcCurs
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pcCurs* \[ fora\]
</dt> <dd>

O número de objetos de cursor associados ao Tablet.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método pode retornar um desses valores.



| Código de retorno                                                                            | Descrição                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | Êxito.<br/>                       |
| <dl> <dt>**E \_ falha**</dt> </dl> | Ocorreu um erro não especificado.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]<br/>                          |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                              |
| Biblioteca<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface ITablet**](itablet.md)
</dt> </dl>

 

 




