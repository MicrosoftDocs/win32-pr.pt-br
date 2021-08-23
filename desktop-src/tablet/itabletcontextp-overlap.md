---
description: Move um contexto de tablet para a frente ou para trás da fila de entrada.
ms.assetid: ef4521b5-776b-46dc-864a-625bc221054a
title: Método ITabletContextP::Overlap
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletContextP.Overlap
api_type:
- COM
api_location:
- Wisptis.exe
- Wisptis.exe.dll
ms.openlocfilehash: ec8b462f2d06e1613c32b795af1793776cafddd6a3531ac6a0b5385f3d3e5128
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119712236"
---
# <a name="itabletcontextpoverlap-method"></a>Método ITabletContextP::Overlap

Move um contexto de tablet para a frente ou para trás da fila de entrada.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Overlap(
  [in]  BOOL  bTop,
  [out] DWORD *pdwtcid
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*bTop* \[ Em\]
</dt> <dd>

Indica se o contexto do tablet deve ser movido para a parte superior ou inferior da fila de entrada.

</dd> <dt>

*pdwtcid* \[ out\]
</dt> <dd>

O identificador de contexto do tablet.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método pode retornar um desses valores.



| Código de retorno                                                                            | Descrição                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | Êxito.<br/>                       |
| <dl> <dt>**E \_ FAIL**</dt> </dl> | Ocorreu um erro não especificado.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do XP Tablet PC \[ Edition\]<br/>                          |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                              |
| Biblioteca<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ITabletContextP Interface**](itabletcontextp.md)
</dt> </dl>

 

 




