---
description: Move um contexto do Tablet para a frente ou para trás da fila de entrada.
ms.assetid: ef4521b5-776b-46dc-864a-625bc221054a
title: 'Método ITabletContextP:: sobreposição'
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
ms.openlocfilehash: b009bc08dddb15bc7aa5b12c8846ea66c4a52e56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105798253"
---
# <a name="itabletcontextpoverlap-method"></a>Método ITabletContextP:: sobreposição

Move um contexto do Tablet para a frente ou para trás da fila de entrada.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Overlap(
  [in]  BOOL  bTop,
  [out] DWORD *pdwtcid
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*bTop* \[ no\]
</dt> <dd>

Indica se o contexto do Tablet deve ser movido para a parte superior ou inferior da fila de entrada.

</dd> <dt>

*pdwtcid* \[ fora\]
</dt> <dd>

O identificador de contexto do Tablet.

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

[**Interface ITabletContextP**](itabletcontextp.md)
</dt> </dl>

 

 




